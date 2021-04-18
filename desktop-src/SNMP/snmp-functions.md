---
title: SNMP 函數
description: 本主題說明三組 SNMP 功能，並列出每個群組中包含的函式
ms.assetid: 8913caa9-6b2c-424c-a778-bd54d6584dac
keywords:
- SNMP 函數 SNMP
- 函數 SNMP，SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f4cc98ce84fbb66f8beb59a6bf995dc4315159
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463573"
---
# <a name="snmp-functions"></a>SNMP 函數

\[SNMP 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，請使用 [Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 MICROSOFT 對 ws-atomictransaction 的實。\]

本主題說明三組 SNMP 功能，並列出每個群組中包含的函式：

-   [SNMP 擴充功能代理程式 API 函式](#snmp-extension-agent-api-functions)
-   [SNMP 管理 API 函式](#snmp-management-api-functions)
-   [SNMP 公用程式 API 函式](#snmp-utility-api-functions)

## <a name="snmp-extension-agent-api-functions"></a>SNMP 擴充功能代理程式 API 函式

SNMP 擴充代理程式功能會定義 SNMP 服務與協力廠商 SNMP 延伸模組代理程式 Dll 之間的介面。 下表列出的函式可讓應用程式用來解析傳入 SNMP 通訊協定資料單位所指定的變數系結， (Pdu) 。

| SNMP 擴充功能代理程式 API 函式                    | Description                                                                                                              |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**SnmpExtensionClose**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionclose)     | 要求 SNMP 擴充代理程式解除配置資源和終止作業。                                    |
| [**SnmpExtensionInit**](/windows/desktop/api/Snmp/nf-snmp-snmpextensioninit)       | 初始化 SNMP 延伸模組代理程式 DLL。                                                                                |
| [**SnmpExtensionInitEx**](/windows/desktop/api/Snmp/nf-snmp-snmpextensioninitex)   | 識別 SNMP 延伸模組代理程式所支援的任何其他管理資訊基底 (MIB) 子樹。             |
| [**SnmpExtensionMonitor**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionmonitor) | 提供 SNMP 延伸模組代理程式與服務內部計數器和參數的相關資訊。            |
| [**SnmpExtensionQuery**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionquery)     | 解析 SNMP 要求，其中包含 SNMP 擴充代理程式的一或多個已註冊 MIB 子樹中的變數。 |
| [**SnmpExtensionQueryEx**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex) | 處理 SNMP 要求，這些要求會指定由 SNMP 延伸模組代理程式註冊的一或多個 MIB 子樹中的變數。 |
| [**SnmpExtensionTrap**](/windows/desktop/api/Snmp/nf-snmp-snmpextensiontrap)       | 抓取服務為 SNMP 擴充代理程式產生陷阱所需的資訊。                          |



 

## <a name="snmp-management-api-functions"></a>SNMP 管理 API 函式

SNMP 管理功能會定義協力廠商 SNMP 管理員應用程式與管理函式動態連結程式庫之間的介面 (DLL) Mgmtapi.dll。 此 DLL 可搭配 SNMP 陷阱服務 (Snmptrap.exe) ，並可與一或多個協力廠商 SNMP 管理員應用程式互動。 下表列出協力廠商管理員應用程式用來執行 SNMP 管理員操作的管理功能。

| SNMP 管理 API 函式                   | Description                                                                                                                                                                                            |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SnmpMgrClose**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrclose)           | 關閉與指定會話相關聯的通訊通訊端和資料結構。                                                                                                  |
| [**SnmpMgrCtl**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrctl)               | 設定與 SNMP 會話相關聯的指令引數。                                                                                                                                   |
| [**SnmpMgrGetTrap**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrgettrap)       | 如果啟用了設陷接收，則會傳回呼叫端未收到的未完成陷阱資料。                                                                                                           |
| [**SnmpMgrGetTrapEx**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrgettrapex)   | 如果啟用了設陷接收，則會傳回呼叫端未收到的未完成陷阱資料。 也會傳回傳輸來源的位址，以及與該陷阱相關聯的社區陷阱。 |
| [**SnmpMgrOidToStr**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgroidtostr)     | 將內部物件識別碼結構轉換為其字串表示。                                                                                                                         |
| [**SnmpMgrOpen**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgropen)             | 初始化與 SNMP 代理程式建立通訊時所需的通訊通訊端和資料結構。                                                                               |
| [**SnmpMgrRequest**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrrequest)       | 要求指定的代理程式執行指定的作業。                                                                                                                             |
| [**SnmpMgrStrToOid**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrstrtooid)     | 將物件識別碼的字串格式轉換為其內部物件識別碼結構。                                                                                                        |
| [**SnmpMgrTrapListen**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrtraplisten) | 註冊 SNMP 管理員應用程式從 SNMP 陷阱服務接收 SNMP 陷阱的能力。                                                                                                 |



 

## <a name="snmp-utility-api-functions"></a>SNMP 公用程式 API 函式

SNMP 公用程式函式提供在開發 SNMP 應用程式時很有用的功能，包括簡化 SNMP 資料結構的操作。 下表列出 SNMP 公用程式函式。

| SNMP 公用程式 API 函式                                  | Description                                                                                                                                                        |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SnmpSvcGetUptime**](/windows/desktop/api/Snmp/nf-snmp-snmpsvcgetuptime)               | 取得 SNMP 服務執行所在的 centiseconds 時間。                                                                                  |
| [**SnmpSvcSetLogLevel**](/windows/desktop/api/Snmp/nf-snmp-snmpsvcsetloglevel)           | 調整來自 SNMP 服務和 SNMP 擴充代理程式之偵錯工具輸出的詳細層級。                                                              |
| [**SnmpSvcSetLogType**](/windows/desktop/api/Snmp/nf-snmp-snmpsvcsetlogtype)             | 調整來自 SNMP 服務和 SNMP 擴充代理程式之偵錯工具輸出的目的地。                                                                 |
| [**SnmpUtilAsnAnyCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputilasnanycpy)             | 將來源 [**AsnAny**](/windows/desktop/api/Snmp/ns-snmp-asnany) 結構複製到目的地 **AsnAny** 結構。                                                                      |
| [**SnmpUtilAsnAnyFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilasnanyfree)           | 釋出配置給指定 [**AsnAny**](/windows/desktop/api/Snmp/ns-snmp-asnany) 結構的記憶體。                                                                        |
| [**SnmpUtilDbgPrint**](/windows/desktop/api/Snmp/nf-snmp-snmputildbgprint)               | 設定要從 SNMP 服務或從呼叫 [**SnmpUtilDbgPrint**](/windows/desktop/api/Snmp/nf-snmp-snmputildbgprint)接收的偵錯工具資訊層級。                       |
| [**SnmpUtilIdsToA**](/windows/desktop/api/Snmp/nf-snmp-snmputilidstoa)                   | 將物件識別碼 (OID) 轉換為以 null 結束的字串。                                                                                                   |
| [**SnmpUtilMemAlloc**](/windows/desktop/api/Snmp/nf-snmp-snmputilmemalloc)               | 從進程堆積配置動態記憶體。                                                                                                                    |
| [**SnmpUtilMemFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilmemfree)                 | 釋出指定的記憶體物件。                                                                                                                                 |
| [**SnmpUtilMemReAlloc**](/windows/desktop/api/Snmp/nf-snmp-snmputilmemrealloc)           | 變更指定之記憶體物件的大小。                                                                                                                   |
| [**SnmpUtilOctetsCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetscmp)             | 比較兩個八位字串。                                                                                                                                        |
| [**SnmpUtilOctetsCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetscpy)             | 將來源 [**AsnOctetString**](/windows/desktop/api/Snmp/ns-snmp-asnoctetstring) 結構複製到目的地 **AsnOctetString** 結構。                                              |
| [**SnmpUtilOctetsFree**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetsfree)           | 釋出配置給指定之八位字串的記憶體。                                                                                                |
| [**SnmpUtilOctetsNCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetsncmp)           | 執行兩個八位字串與指定 subidentifiers 數目的比較。                                                                              |
| [**SnmpUtilOidAppend**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidappend)             | 將包含在 [**AsnObjectIdentifier**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) 結構中的來源物件識別碼附加至目的地物件識別碼。          |
| [**SnmpUtilOidCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidcmp)                   | 比較 [**AsnObjectIdentifier**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) 結構中所包含的兩個物件識別碼。                                           |
| [**SnmpUtilOidCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidcpy)                   | 將來源 [**AsnObjectIdentifier**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) 結構複製到目的地 **AsnObjectIdentifier** 結構。                               |
| [**SnmpUtilOidFree**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidfree)                 | 釋出配置給指定之物件識別碼的記憶體。                                                                                           |
| [**SnmpUtilOidNCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidncmp)                 | 將 [**AsnObjectIdentifier**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) 結構中所包含的兩個物件識別碼，與指定的 subidentifiers 數目進行比較。 |
| [**SnmpUtilOidToA**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidtoa)                   | 將物件識別碼 (OID) 轉換為以 null 結束的字串。                                                                                                   |
| [**SnmpUtilPrintAsnAny**](/windows/desktop/api/Snmp/nf-snmp-snmputilprintasnany)         | 列印包含在 [**AsnAny**](/windows/desktop/api/Snmp/ns-snmp-asnany) 結構中的值，以供進行偵錯工具和開發之用。                                              |
| [**SnmpUtilPrintOid**](/windows/desktop/api/Snmp/nf-snmp-snmputilprintoid)               | 將指定的物件識別碼格式化 (OID) ，並將結果列印至標準輸出裝置。                                                                 |
| [**SnmpUtilVarBindCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindcpy)           | 將來源 [**SnmpVarBind**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbind) 結構複製到目的地 **SnmpVarBind** 結構。                                                       |
| [**SnmpUtilVarBindListCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindlistcpy)   | 將來源 [**SnmpVarBindList**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbindlist) 結構複製到目的地 **SnmpVarBindList** 結構。                                           |
| [**SnmpUtilVarBindFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindfree)         | 釋出配置給指定 [**SnmpVarBind**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbind) 結構的記憶體。                                                            |
| [**SnmpUtilVarBindListFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindlistfree) | 釋出配置給指定 [**SnmpVarBindList**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbindlist) 結構的記憶體。                                                    |



 

 

 