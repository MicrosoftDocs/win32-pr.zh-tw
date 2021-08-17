---
title: WinSNMP 函數
description: 用於 WinSNMP 的函式可分為下列功能群組。 字母清單如下。
ms.assetid: ae95ac47-81ff-4715-b3e9-e19c07223712
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29169e8cf86b7f21ebbc40ced2ac37a46668c727183a9b2970eb368c7e81d85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142801"
---
# <a name="winsnmp-functions"></a>WinSNMP 函數

\[SNMP 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，請使用[Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 Microsoft 對 ws-atomictransaction 的實。\]

用於 WinSNMP 的函式可分為下列功能群組。 字母清單如下。

-   [通訊功能](#winsnmp-communications-functions)
-   [Entity 和 CoNtext 函數](#winsnmp-entity-and-context-functions)
-   [資料庫函數](#winsnmp-database-functions)
-   [PDU 函式](#winsnmp-pdu-functions)
-   [公用程式函數](#winsnmp-utility-functions)
-   [變數系結函式](#winsnmp-variable-binding-functions)
-   [WinSNMP 函數位母清單](/windows)

## <a name="winsnmp-communications-functions"></a>WinSNMP 通訊功能

WinSNMP 通訊函式提供呼叫的 WinSNMP 應用程式與 Microsoft WinSNMP 執行之間的介面。 此執行會處理應用程式與其他管理實體之間的通訊。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>函式</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg"><strong>SnmpCancelMsg</strong></a></td>
<td>要求 Microsoft WinSNMP 執行會取消重新傳輸嘗試，以及輸入 SNMP 要求訊息的超時通知。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>SnmpCleanup</strong></a></td>
<td>通知執行應用程式已中斷連線，不再需要配置的資源。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanupex"><strong>SnmpCleanupEx</strong></a></td>
<td>當在 WinSNMP 應用程式內沒有任何未處理的 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a> 或 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartupex"><strong>SnmpStartupEx</strong></a> 呼叫成功時，執行清除。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>SnmpClose</strong></a></td>
<td>啟用執行以解除配置與會話相關聯的資源，以及關閉通訊機制。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a></td>
<td>要求執行以開啟 WinSNMP 會話，並配置資源和通訊機制。 開發新的 WinSNMP 應用程式時，建議您呼叫 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a> 函式來開啟 WinSNMP 會話，而不是呼叫 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpopen"><strong>SnmpOpen</strong></a> 函數。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten"><strong>SnmpListen</strong></a></td>
<td>將 WinSNMP 應用程式註冊或取消註冊為 SNMP 代理程式。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpopen"><strong>SnmpOpen</strong></a></td>
<td>要求執行以開啟 WinSNMP 會話，並配置資源和通訊機制。 開發新的 WinSNMP 應用程式時，建議您呼叫 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a> 函式來開啟 WinSNMP 會話，而不是呼叫 <strong>SnmpOpen</strong> 函數。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>SnmpRecvMsg</strong></a></td>
<td>傳回 SNMP 訊息和未完成的陷阱資料和通知。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>SnmpRegister</strong></a></td>
<td>通知執行應用程式必須註冊或取消註冊陷阱和通知。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>SnmpSendMsg</strong></a></td>
<td>要求執行會傳輸通訊協定資料單位。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a></td>
<td>通知執行執行應用程式的初始化程式。 應用程式必須先成功呼叫 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a> 函式，才能呼叫任何其他的 WinSNMP 函數。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartupex"><strong>SnmpStartupEx</strong></a></td>
<td>通知 Microsoft WinSNMP 可執行檔 WinSNMP 應用程式需要執行的服務。 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartupex"><strong>SnmpStartupEx</strong></a> 可支援在相同應用程式中使用 WinSNMP 的多個獨立軟體模組。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nc-winsnmp-snmpapi_callback"><strong>SNMPAPI_CALLBACK</strong></a></td>
<td>通知可使用 SNMP 訊息或非同步事件的 WinSNMP 會話。
<blockquote>
[!Note]<br />
這個回呼函式只適用于因為呼叫 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a> 函式而開啟的會話。
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="winsnmp-entity-and-context-functions"></a>WinSNMP 實體和內容函式

WinSNMP 實體和內容函數可讓 WinSNMP 應用程式為 SNMP 實體和內容指定易記的名稱。 Microsoft WinSNMP 實行會使用實作為資料庫，將名稱轉譯為其 SNMPv1 或 SNMPv2C 元件。



| 函式                                     | 描述                                                                                                            |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**SnmpCoNtextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) | 傳回字串，這個字串會識別一組受管理物件資源)  (的 SNMP 內容。                                  |
| [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr)   | 傳回識別 SNMP 管理實體的字串。                                                            |
| [**SnmpFreeCoNtext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)   | 釋放 [**SnmpStrToCoNtext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) 函數針對 SNMP 內容所配置的資源。         |
| [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)     | 釋放 [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) 函式針對 SNMP 管理實體所配置的資源。 |
| [**SnmpSetPort**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetport)           | 變更指派給 SNMP 目的地實體的埠。                                                               |
| [**SnmpStrToCoNtext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) | 傳回特定于執行之 SNMP 內容資訊的控制碼。                                   |
| [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity)   | 傳回特定于執行之 SNMP 管理實體資訊的控制碼。                         |



 

## <a name="winsnmp-database-functions"></a>WinSNMP 資料庫函式

WinSNMP 資料庫函式會提供一個可存取 Microsoft WinSNMP 實行系統管理資訊存放區中目前設定的 WinSNMP 應用程式。 這些函數允許變更重新傳輸模式以及實體和內容轉譯模式。 資料庫函式也會提供應用程式操作超時和重試計數值的能力。



| 函式                                               | 描述                                                                                           |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**SnmpGetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode) | 傳回重新傳輸模式的目前設定。                                               |
| [**SnmpGetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry)                   | 傳回重新傳輸 SNMP 訊息要求的重試計數值（單位為單位）。             |
| [**SnmpGetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout)               | 傳回 SNMP 訊息要求的傳輸超時值（以百分之一秒為限）。 |
| [**SnmpGetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettranslatemode)   | 傳回實體和內容轉譯模式的目前設定。                               |
| [**SnmpGetVendorInfo**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvendorinfo)         | 抓取可識別 WinSNMP 供應商的資訊。                                             |
| [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) | 變更重新傳輸模式。                                                                      |
| [**SnmpSetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry)                   | 變更 SNMP 訊息要求重新傳輸的重試計數值。                        |
| [**SnmpSetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout)               | 變更 SNMP 訊息要求的傳輸超時值。                             |
| [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode)   | 變更實體和內容轉譯模式。                                                      |



 

## <a name="winsnmp-pdu-functions"></a>WinSNMP PDU 函式

WinSNMP PDU 函式可讓 WinSNMP 應用程式解壓縮和更新 PDU (或欄位) 的資料元素。 這包括呼叫 [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) 函式或 [**SnmpDecodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdecodemsg) 函數所傳回的 pdu。 PDU 函式也會建立要在 [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) 和 [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) 函式中使用的 pdu。



| 函式                                     | 描述                                                                                                                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu)       | 建立並初始化 SNMP 通訊協定資料單位。                                                                                                                               |
| [**SnmpDuplicatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu) | 複製 SNMP 通訊協定資料單位。                                                                                                                                            |
| [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu)           | 釋放與 [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) 或 [**SnmpDuplicatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu) 函數所建立的 SNMP 通訊協定資料單位相關聯的資源。 |
| [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata)     | 從指定的 SNMP 通訊協定資料單位傳回選取的資料元素。                                                                                                          |
| [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata)     | 更新指定 SNMP 通訊協定資料單位中選取的資料元素。                                                                                                            |



 

## <a name="winsnmp-utility-functions"></a>WinSNMP 公用程式函式

WinSNMP 公用程式函式可讓 WinSNMP 應用程式跨 WinSNMP 介面管理物件和 SNMP 訊息。



| 函式                                         | 描述                                                                                                         |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**SnmpDecodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdecodemsg)           | 將已編碼或已序列化的 SNMP 訊息解碼成其構成元件。                                      |
| [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg)           | 建立編碼的 SNMP 訊息。                                                                                    |
| [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) | 發出 Microsoft WinSNMP 的信號，指出它應該釋放配置給特定描述項的記憶體。 |
| [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror)     | 傳回最後一次 SNMP 操作的最後錯誤碼值。                                                      |
| [**SnmpOidCompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare)         | 比較兩個 SNMP 物件識別碼。                                                                               |
| [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy)               | 複製 SNMP 物件識別碼。                                                                                   |
| [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr)             | 將 SNMP 物件識別碼的內部二進位標記法轉換為其點數位字串格式。       |
| [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)             | 將 SNMP 物件識別碼的點數位字串格式轉換為其內部二進位標記法。       |



 

## <a name="winsnmp-variable-binding-functions"></a>WinSNMP 變數系結函式

WinSNMP 變數系結函式可讓 WinSNMP 應用程式建立和操作變數系結清單，並將它們包含在 Pdu 中。



| 函式                                     | 描述                                                                                                                                                                     |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SnmpCountVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcountvbl)         | 列舉指定變數系結清單中的變數系結專案。                                                                                                   |
| [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl)       | 建立新的變數系結清單。                                                                                                                                            |
| [**SnmpDeleteVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb)         | 從變數系結清單中移除變數系結專案。                                                                                                                  |
| [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) | 複製變數繫結欄位表。                                                                                                                                                 |
| [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl)           | 釋放 [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) 或 [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) 函數先前配置的變數系結清單資源。 |
| [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb)               | 從指定的變數繫結項目抓取資訊。                                                                                                                  |
| [**SnmpSetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb)               | 變更變數系結清單中的變數繫結項目;將新的變數繫結項目附加至現有的變數系結清單。                                         |



 

## <a name="winsnmp-functions---alphabetic-list"></a>WinSNMP 函數位母清單

-   [**SNMPAPI \_ 回呼**](/windows/desktop/api/Winsnmp/nc-winsnmp-snmpapi_callback)
-   [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg)
-   [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup)
-   [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose)
-   [**SnmpCoNtextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr)
-   [**SnmpCountVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcountvbl)
-   [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu)
-   [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession)
-   [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl)
-   [**SnmpDecodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdecodemsg)
-   [**SnmpDeleteVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb)
-   [**SnmpDuplicatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu)
-   [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl)
-   [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg)
-   [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr)
-   [**SnmpFreeCoNtext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)
-   [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor)
-   [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)
-   [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu)
-   [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl)
-   [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror)
-   [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata)
-   [**SnmpGetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode)
-   [**SnmpGetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry)
-   [**SnmpGetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout)
-   [**SnmpGetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettranslatemode)
-   [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb)
-   [**SnmpGetVendorInfo**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvendorinfo)
-   [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten)
-   [**SnmpOidCompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare)
-   [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy)
-   [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr)
-   [**SnmpOpen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpopen)
-   [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg)
-   [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister)
-   [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)
-   [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata)
-   [**SnmpSetPort**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetport)
-   [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode)
-   [**SnmpSetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry)
-   [**SnmpSetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout)
-   [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode)
-   [**SnmpSetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb)
-   [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup)
-   [**SnmpStrToCoNtext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext)
-   [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity)
-   [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)

 

