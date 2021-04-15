---
title: WinSNMP 錯誤碼
description: WinSNMP 錯誤碼
ms.assetid: 03b13b82-a31c-47e2-8b4d-17dcc4d19e56
keywords:
- WinSNMP 錯誤碼 SNMP
- 錯誤碼 SNMP、WinSNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d3cff7bd1e534f5f9c1fb0ae2ea2687d2ba99a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463569"
---
# <a name="winsnmp-error-codes"></a>WinSNMP 錯誤碼

\[SNMP 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，請使用 [Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 MICROSOFT 對 ws-atomictransaction 的實。\]

> [!Note]  
> 本主題所述的錯誤與相關 Rfc 所定義的 SNMP 錯誤碼不同。

 

如果函式失敗，所有的 WinSNMP 函數都會傳回值 **SNMPAPI \_ 失敗** 。 當 WinSNMP 函式失敗時，WinSNMP 應用程式必須立即呼叫 [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) 函式，以取得擴充的錯誤資訊。 下表列出的主題會討論由 WinSNMP 函數傳回的擴充錯誤碼。



| 主題                                                        | 描述                                             |
|--------------------------------------------------------------|---------------------------------------------------------|
| [WinSNMP 一般錯誤碼](winsnmp-common-error-codes.md) | 描述適用于 WinSNMP API 的常見錯誤碼。       |
| [網路傳輸錯誤](network-transport-errors.md)     | 說明 WinSNMP API 的網路傳輸錯誤。 |



 

傳遞內容特定資訊的 WinSNMP 錯誤會包含在 [函數參考] 頁面中。

 

 