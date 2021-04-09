---
title: 網路傳輸錯誤
description: Microsoft WinSNMP 的執行可以在傳輸 SNMP 訊息之後偵測到網路傳輸錯誤。
ms.assetid: 2ff535b1-76cb-42aa-baeb-14c1a1bc41ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cf6b7610fbfe8d19a375bd3e3146263b9e9f0b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842607"
---
# <a name="network-transport-errors"></a>網路傳輸錯誤

\[SNMP 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，請使用 [Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 MICROSOFT 對 ws-atomictransaction 的實。\]

Microsoft WinSNMP 的執行可以在傳輸 SNMP 訊息之後偵測到網路傳輸錯誤。 發生這種情況時，執行會將資料回條通知傳送至起始通訊要求的 WinSNMP 會話。 此執行也會 \_ 在下一次呼叫會話的 [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) 函式時，傳回 SNMPAPI 失敗。 **SnmpRecvMsg** 函式失敗，並出現擴充的錯誤碼，指出網路傳輸層錯誤。

如需特定傳輸層錯誤的清單，請參閱 [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister)、 [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)和 [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) 函數的參考頁面。

 

 