---
title: WinSNMP 一般錯誤碼
description: 當 WinSNMP 函式失敗之後，SnmpGetLastError 函式可能會傳回一般錯誤碼。 下表列出的是 WinSNMP 一般錯誤碼。
ms.assetid: c286750f-a542-4f61-a22c-d77debd45775
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beee49aef651784b0b8dc05c0114b7bf906be113
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023810"
---
# <a name="winsnmp-common-error-codes"></a>WinSNMP 一般錯誤碼

\[SNMP 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，請使用 [Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 MICROSOFT 對 ws-atomictransaction 的實。\]

當 WinSNMP 函式失敗之後， [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) 函式可能會傳回一般錯誤碼。 下表列出的是 WinSNMP 一般錯誤碼。



| 錯誤碼                | 意義                                                                                                                                                                                                        | 建議的動作                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SNMPAPI \_ 未 \_ 初始化 | [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup)函式未順利完成，因為程式執行開始，或因為 [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup)函式的呼叫已成功完成。 | 應用程式在 [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup)失敗時，應該先呼叫 [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) ，然後再呼叫任何其他的 WinSNMP API 函數。 [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror)函數會傳回有關 [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup)失敗的延伸錯誤資訊。                                                          |
| SNMPAPI \_ 分配 \_ 錯誤     | 應用程式指定了不正確指標，或記憶體配置期間發生錯誤。 Microsoft WinSNMP 實行無法取得足夠的資源來執行要求。                | 應用程式應該提供所有輸出參數的有效記憶體指標。 它應該釋出資源、降低資源需求，或協助正常關機。 正常關機包括多個對 [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) 函式的呼叫，每個開啟的 WinSNMP 會話各有一個呼叫。 它也包含對 [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) 函數的呼叫。 |
| SNMPAPI \_ NOOP             | 因為所有輸出參數都是 **Null**，所以函數未順利完成。                                                                                                                         | 呼叫會將資訊傳回給應用程式的函式時，應用程式必須指定至少一個非 **Null** 的輸出參數。                                                                                                                                                                                                                                  |
| SNMPAPI \_ 其他 \_ 錯誤     | 發生未知或未定義的錯誤。                                                                                                                                                                        | 應用程式通常應該會以正常關機的方式回應。 正常關機包括多個對 [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) 函式的呼叫，每個開啟的 WinSNMP 會話各有一個呼叫。 它也包含對 [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) 函數的呼叫。                                                                                                           |



 

傳遞內容特定資訊的 WinSNMP 錯誤會在每個函式的參考頁面中注明。

 

 