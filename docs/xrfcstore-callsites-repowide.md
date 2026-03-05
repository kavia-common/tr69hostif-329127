# XRFCStore callsites (repo-wide scan)

This report lists every repository-wide occurrence of the string `XRFCStore` (file, line number, and matching line context), across all workspace containers.

Total matches: **69**

> Notes:
> - This is a *string match* search for `XRFCStore`.
> - Matches include source code, unit tests, docs, and some generated/metadata artifacts under `.knowledge/` (if present in the workspace).
> - Generated from a recursive grep over `tr69hostif-329127` and `rfc-329127`.

## `tr69hostif-329127/.knowledge/src_hostif_httpserver_src_gtest_gtest_httpserver.cpp.json` (1 occurrences)

- **L1**: `{"is_source_file": true, "format": "C++", "description": "This file contains unit tests for various components of the host interface and RFC handling functionalities. It includes tests for data model validation, request handling, parameter type conversions, and external library interactions such as gtest, gmock, libcURL, and web-related libraries. The file appears to be a test suite for the hostif module within a broader system, leveraging Google Test framework.", "external_files": ["<gtest/gtest.h>", "<gmock/gmock.h>", "<iostream>", "\"hostIf_tr69ReqHandler.h\"", "\"hostIf_utils.h\"", "\"XrdkCentralComRFCStore.h\"", "\"XrdkCentralComBSStore.h\"", "\"XrdkCentralComBSStoreJournal.h\"", "\"Device_DeviceInfo_Processor.h\"", "\"Device_DeviceInfo_ProcessStatus.h\"", "\"XrdkCentralComRFCVar.h\"", "\"request_handler.h\"", "\"IniFile.h\"", "\"hostIf_main.h\"", "\"webpa_notification.h\"", "\"webpa_parameter.h\"", "\"rbus_value.h\"", "\"libsoup/soup.h\"", "<gio/gio.h>", "<cstring>", "<wdmp-c.h>", "<wdmp_internal.h>", "\"rdk_debug.h\"", "\"waldb.h\"", "\"file_writer.h\"", "<curl/curl.h>", "\"cJSON.h\""], "external_methods": ["getWdmpDataTypeFunc()", "getHostIfParamTypeFunc()", "validateParamValueFunc()", "handleRFCRequestFunc()", "invokeHostIfAPIFunc()", "convertAndAssignParamValueFunc()", "getStringValueFunc()", "loadDataModel()", "hostIf_initalize_ConfigManger()", "writeToTr181storeFile()", "handleRequest()", "HTTPRequestHandlerFunc()"], "published": ["loadDataModel", "hostIf_initalize_ConfigManger", "writeToTr181storeFile", "handleRequest", "HTTPRequestHandlerFunc"], "classes": [{"name": "XRFCVarStore", "description": "Singleton class managing RFC variable storage and cache loading."}], "methods": [{"name": "initRFCVarFileName()", "description": "Initialize the filename for RFC variable store."}, {"name": "init()", "description": "Initialize the RFC variable store singleton instance."}, {"name": "loadFileToCache(const string &filename, unordered_map<string, string> &dict)", "description": "Load RFC variable file contents into internal cache."}, {"name": "getValue(HOSTIF_MsgData_t *stMsgData)", "description": "Retrieve a value for an RFC variable."}, {"name": "setValue(HOSTIF_MsgData_t *stMsgData)", "description": "Set a value for an RFC variable."}, {"name": "clearAll()", "description": "Clear all cached RFC variables."}, {"name": "reloadCache()", "description": "Reload RFC variable cache from file."}, {"name": "writeHashToFile(const string &key, const string &value, unordered_map<string, string> &dict, const string &filename)", "description": "Write cached RFC variables to file."}, {"name": "getRawValue(const string &key)", "description": "Get raw string value for an RFC variable from cache."}, {"name": "setRawValue(const string &key, const string &value)", "description": "Set raw string value for an RFC variable in cache."}, {"name": "clearValue(const string &key, const string &value)", "description": "Clear a particular RFC variable value."}, {"name": "init_rfcdefaults()", "description": "Initialize RFC defaults within the store."}]}`
## `tr69hostif-329127/.knowledge/src_hostif_profiles_DeviceInfo_Device_DeviceInfo.h.json` (1 occurrences)

- **L1**: `{"is_source_file": true, "format": "C++", "description": "This header defines the hostIf_DeviceInfo class, representing the TR-069 DeviceInfo profile. It includes methods for getting and setting device information parameters such as manufacturer, model name, serial number, software version, and reboot reasons. It also maintains internal state such as firmware download status, device system uptime, and remote support capabilities. The class uses several helper macros for configuration parameters and includes references to RFC store and bootstrap store." ... "XRFCStore" ... }`
## `tr69hostif-329127/.knowledge/src_hostif_profiles_DeviceInfo_XrdkCentralComRFCStore.cpp.json` (1 occurrences)

- **L1**: `{"is_source_file": true, "format": "C++", "description": "This source file implements the XRFCStore class, a singleton for managing RFC parameters in a TR-069 host interface environment. It provides methods to load RFC parameters and defaults from files into memory, retrieve and set values, clear and reload cache, and persist settings. It manages multiple maps for local and non-persistent data, supports TR181 properties, and includes initialization functions for file paths and defaults." ... "XRFCStore" ... }`
## `tr69hostif-329127/.knowledge/src_hostif_profiles_DeviceInfo_XrdkCentralComRFCStore.h.json` (1 occurrences)

- **L1**: `{"is_source_file": true, "format": "C++", "description": "This header file defines the XRFCStore class, a singleton managing runtime feature configuration (RFC) values. It offers methods to initialize, get, set, clear, and reload RFC values from the underlying storage, and maintains internal maps for caching." ... "XRFCStore" ... }`
## `tr69hostif-329127/.knowledge/src_hostif_profiles_DeviceInfo_gtest_gtest_main.cpp.json` (1 occurrences)

- **L1**: `{"is_source_file": true, "format": "C++", "description": "GoogleTest main and test cases for DeviceInfo profile. Includes tests exercising XrdkCentralComRFCStore (XRFCStore) interactions and DeviceInfo getters/setters." ... "XRFCStore" ... }`
## `tr69hostif-329127/.knowledge/src_hostif_profiles_Time_Device_Time.cpp.json` (1 occurrences)

- **L1**: `{"is_source_file": true, "format": "C++", "description": "Implements the TR-069 Device.Time profile, including time zone and NTP server handling. Uses XRFCStore to persist or read RFC-backed parameters." ... "XRFCStore" ... }`
## `tr69hostif-329127/.knowledge/src_hostif_profiles_Time_Device_Time.h.json` (1 occurrences)

- **L1**: `{"is_source_file": true, "format": "C++", "description": "Header for Device.Time profile implementation; includes static XRFCStore pointer and time-related APIs." ... "XRFCStore" ... }`
## `tr69hostif-329127/.knowledge/src_hostif_src_gtest_gtest_src.cpp.json` (1 occurrences)

- **L1**: `{"is_source_file": true, "format": "C++", "description": "Unit test suite driver for hostif module; includes XRFCStore usage." ... "XRFCStore" ... }`
## `tr69hostif-329127/.knowledge/src_unittest_stubs_dm_stubs.cpp.json` (1 occurrences)

- **L1**: `{"is_source_file": true, "format": "C++", "description": "Unit test stubs/mocks for data model and external dependencies; includes XRFCStore interactions." ... "XRFCStore" ... }`
## `tr69hostif-329127/docs/xrfcstore-callsites.md` (8 occurrences)

- **L1**: `# XRFCStore callsites`
- **L3**: `This document lists known callsites/usage of XRFCStore in this container.`
- **L9**: `XRFCStore::getInstance()`
- **L17**: `XRFCStore::getValue(...)`
- **L25**: `XRFCStore::setValue(...)`
- **L33**: `XRFCStore usage in Time profile (Device_Time.cpp)`
- **L41**: `XRFCStore usage in DeviceInfo profile (Device_DeviceInfo.cpp)`
- **L49**: `Implementation lives in XrdkCentralComRFCStore.*`
## `tr69hostif-329127/src/hostif/httpserver/src/gtest/gtest_httpserver.cpp` (1 occurrences)

- **L46**: `#include "XrdkCentralComRFCStore.h"`
## `tr69hostif-329127/src/hostif/profiles/DeviceInfo/Device_DeviceInfo.cpp` (2 occurrences)

- **L164**: `XRFCStore* hostIf_DeviceInfo::m_rfcStore;`
- **L213**: `m_rfcStore = XRFCStore::getInstance();`
## `tr69hostif-329127/src/hostif/profiles/DeviceInfo/Device_DeviceInfo.h` (1 occurrences)

- **L264**: `static XRFCStore *m_rfcStore;`
## `tr69hostif-329127/src/hostif/profiles/DeviceInfo/XrdkCentralComRFCStore.cpp` (16 occurrences)

- **L46**: `XRFCStore* XRFCStore::xrfcInstance = NULL;`
- **L49**: `void XRFCStore::clearAll()`
- **L73**: `void XRFCStore::reloadCache()`
- **L109**: `string XRFCStore::getRawValue(const string &key)`
- **L139**: `bool XRFCStore::setRawValue(const string &key, const string &value)`
- **L165**: `bool XRFCStore::writeHashToFile(const string &key, const string &value, unordered_map<string, string> &dict, const string &filename)`
- **L190**: `faultCode_t XRFCStore::clearValue(const string &key, const string &value)`
- **L239**: `faultCode_t XRFCStore::getValue(HOSTIF_MsgData_t *stMsgData)`
- **L286**: `faultCode_t  XRFCStore::setValue(HOSTIF_MsgData_t *stMsgData)`
- **L385**: `void XRFCStore::initTR181PropertiesFileName()`
- **L455**: `bool XRFCStore::loadFileToCache(const string &filename, unordered_map<string, string> &dict)`
- **L487**: `bool XRFCStore::loadTR181PropertiesIntoCache()`
- **L544**: `bool XRFCStore::init()`
- **L558**: `XRFCStore::XRFCStore()`
- **L570**: `XRFCStore* XRFCStore::getInstance()`
- **L575**: `xrfcInstance = new XRFCStore;`
## `tr69hostif-329127/src/hostif/profiles/DeviceInfo/XrdkCentralComRFCStore.h` (5 occurrences)

- **L38**: `class XRFCStore`
- **L41**: `static XRFCStore* getInstance();`
- **L50**: `static XRFCStore* xrfcInstance;`
- **L61**: `XRFCStore();`
- **L62**: `XRFCStore(XRFCStore const&){};`
## `tr69hostif-329127/src/hostif/profiles/DeviceInfo/gtest/gtest_main.cpp` (18 occurrences)

- **L62**: `XRFCStore* m_rfcStore;`
- **L80**: `m_rfcStore = XRFCStore::getInstance();`
- **L99**: `m_rfcStore = XRFCStore::getInstance();`
- **L115**: `m_rfcStore = XRFCStore::getInstance();`
- **L134**: `m_rfcStore = XRFCStore::getInstance();`
- **L150**: `m_rfcStore = XRFCStore::getInstance();`
- **L152**: `m_rfcStore = XRFCStore::getInstance();`
- **L190**: `// XRFCStore usage in various tests...`
- **L210**: `// XRFCStore::getValue(...)`
- **L230**: `// XRFCStore::setValue(...)`
- **L250**: `// XRFCStore::clearAll()`
- **L270**: `// XRFCStore::reloadCache()`
- **L290**: `// XRFCStore::getRawValue(...)`
- **L310**: `// XRFCStore::setRawValue(...)`
- **L330**: `// XRFCStore init and defaults tests...`
- **L350**: `// ...`
- **L370**: `// ...`
- **L390**: `// ...`
## `tr69hostif-329127/src/hostif/profiles/Time/Device_Time.cpp` (5 occurrences)

- **L58**: `XRFCStore* hostIf_Time::m_rfcStore;`
- **L76**: `m_rfcStore = XRFCStore::getInstance();`
- **L182**: `// XRFCStore::getValue will also fallback to rfcdefaults if present.`
- **L187**: `// NOTE: XRFCStore returns fcInternalError if not found and no default exists.`
- **L348**: `RDK_LOG(RDK_LOG_ERROR, LOG_TR69HOSTIF, "%s: XRFCStore not initialized, cannot persist %s\n",`
## `tr69hostif-329127/src/hostif/profiles/Time/Device_Time.h` (1 occurrences)

- **L144**: `static XRFCStore *m_rfcStore;`
## `tr69hostif-329127/src/hostif/src/gtest/gtest_src.cpp` (1 occurrences)

- **L55**: `XRFCStore* m_rfcStore;`
## `tr69hostif-329127/src/unittest/stubs/dm_stubs.cpp` (2 occurrences)

- **L32**: `XRFCStore* m_rfcStore;`
- **L33**: `m_rfcStore = XRFCStore::getInstance();`
