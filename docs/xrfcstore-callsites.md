# XRFCStore (TR-181 persistent store) callsites

This file documents all known usages of `XRFCStore` in the `tr69hostif-329127` repository, focusing on handler/profile get/set logic that uses the TR-181 persistent store API (`getValue`/`setValue`), along with key test/stub references.

## Production handler/profile callsites

### `src/hostif/profiles/Time/Device_Time.cpp`
- **Line 76**: store init
  ```cpp
  m_rfcStore = XRFCStore::getInstance();
  ```

- **Line 188**: persisted GET
  ```cpp
  faultCode_t fc = m_rfcStore->getValue(&storeMsg);
  ```

- **Line 353**: persisted SET
  ```cpp
  faultCode_t fc = m_rfcStore->setValue(stMsgData);
  ```

### `src/hostif/profiles/DeviceInfo/Device_DeviceInfo.cpp`
- **Line 3968**: RFC SET routed to XRFCStore when `!legacyRFCEnabled()`
  ```cpp
  ret = m_rfcStore->setValue(stMsgData);
  ```

- **Line 4179**: RFC GET routed to XRFCStore when `!legacyRFCEnabled()`
  ```cpp
  ret = m_rfcStore->getValue(stMsgData);
  ```

- **Line 4922**: RetrieveNow SET stored via XRFCStore
  ```cpp
  ret = m_rfcStore->setValue(stMsgData);
  ```

## Tests / stubs (non-production logic)
- `src/unittest/stubs/dm_stubs.cpp:33`
  ```cpp
  m_rfcStore = XRFCStore::getInstance();
  ```

- `src/hostif/src/gtest/gtest_src.cpp:55` (decl/fixture)
- `src/hostif/profiles/DeviceInfo/gtest/gtest_main.cpp` (multiple: `getValue`, `setValue`, `getRawValue`, `setRawValue`)
- `src/hostif/httpserver/src/gtest/gtest_httpserver.cpp:51` (decl/fixture)

## XRFCStore implementation files (for reference)
- `src/hostif/profiles/DeviceInfo/XrdkCentralComRFCStore.cpp`
- `src/hostif/profiles/DeviceInfo/XrdkCentralComRFCStore.h`
