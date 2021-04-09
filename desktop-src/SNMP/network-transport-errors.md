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
# <a name="network-transport-errors"></a><span data-ttu-id="b2d65-103">網路傳輸錯誤</span><span class="sxs-lookup"><span data-stu-id="b2d65-103">Network Transport Errors</span></span>

<span data-ttu-id="b2d65-104">\[SNMP 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="b2d65-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b2d65-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="b2d65-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b2d65-106">相反地，請使用 [Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 MICROSOFT 對 ws-atomictransaction 的實。\]</span><span class="sxs-lookup"><span data-stu-id="b2d65-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="b2d65-107">Microsoft WinSNMP 的執行可以在傳輸 SNMP 訊息之後偵測到網路傳輸錯誤。</span><span class="sxs-lookup"><span data-stu-id="b2d65-107">The Microsoft WinSNMP implementation can detect a network transport error after it transmits an SNMP message.</span></span> <span data-ttu-id="b2d65-108">發生這種情況時，執行會將資料回條通知傳送至起始通訊要求的 WinSNMP 會話。</span><span class="sxs-lookup"><span data-stu-id="b2d65-108">When this occurs, the implementation sends a data receipt notification to the WinSNMP session that initiated the communication request.</span></span> <span data-ttu-id="b2d65-109">此執行也會 \_ 在下一次呼叫會話的 [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) 函式時，傳回 SNMPAPI 失敗。</span><span class="sxs-lookup"><span data-stu-id="b2d65-109">The implementation also returns SNMPAPI\_FAILURE on the next call to the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function for the session.</span></span> <span data-ttu-id="b2d65-110">**SnmpRecvMsg** 函式失敗，並出現擴充的錯誤碼，指出網路傳輸層錯誤。</span><span class="sxs-lookup"><span data-stu-id="b2d65-110">The **SnmpRecvMsg** function fails with an extended error code that indicates a network transport layer error.</span></span>

<span data-ttu-id="b2d65-111">如需特定傳輸層錯誤的清單，請參閱 [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister)、 [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)和 [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) 函數的參考頁面。</span><span class="sxs-lookup"><span data-stu-id="b2d65-111">For a list of specific transport layer errors, see the reference pages for the [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister), [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg), and [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) functions.</span></span>

 

 