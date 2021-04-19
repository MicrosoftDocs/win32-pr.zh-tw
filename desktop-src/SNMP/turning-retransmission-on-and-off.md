---
title: 開啟和關閉重新傳輸
description: 應用程式可以使用 SnmpSetRetransmitMode 函式的呼叫來設定重新傳輸模式。 新的重新傳輸模式會套用至後續呼叫 SnmpSendMsg 函式。
ms.assetid: 0e167014-2703-4942-91f0-c60a5c0d8e12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24936bcc90ed0debf66eb9040334fff3bceee2ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106996552"
---
# <a name="turning-retransmission-on-and-off"></a><span data-ttu-id="2569f-104">開啟和關閉重新傳輸</span><span class="sxs-lookup"><span data-stu-id="2569f-104">Turning Retransmission On and Off</span></span>

<span data-ttu-id="2569f-105">應用程式可以使用 [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) 函式的呼叫來設定重新傳輸模式。</span><span class="sxs-lookup"><span data-stu-id="2569f-105">An application can set the retransmission mode with a call to the [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) function.</span></span> <span data-ttu-id="2569f-106">新的重新傳輸模式會套用至後續呼叫 [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) 函式。</span><span class="sxs-lookup"><span data-stu-id="2569f-106">The new retransmission mode applies to subsequent calls to the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function.</span></span>

<span data-ttu-id="2569f-107">當應用程式呼叫 **SnmpSetRetransmitMode** 時，SNMPAPI 的重新傳輸模式值為 \_ ON 時，Microsoft WinSNMP 執行會開始執行應用程式的重新傳輸原則。</span><span class="sxs-lookup"><span data-stu-id="2569f-107">When the application calls **SnmpSetRetransmitMode** with the retransmission mode value SNMPAPI\_ON, the Microsoft WinSNMP implementation begins execution of the application's retransmission policy.</span></span> <span data-ttu-id="2569f-108">新的重新傳輸模式不會影響未處理的 SNMP 訊息。</span><span class="sxs-lookup"><span data-stu-id="2569f-108">The new retransmission mode does not affect outstanding SNMP messages.</span></span> <span data-ttu-id="2569f-109">未處理的訊息是指在應用程式變更重新傳輸模式時沒有回應的訊息。</span><span class="sxs-lookup"><span data-stu-id="2569f-109">An outstanding message is one that has no response at the time the application changes the retransmission mode.</span></span>

<span data-ttu-id="2569f-110">當 WinSNMP 應用程式呼叫 [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) 函式，並將重新傳輸模式值 SNMPAPI \_ 關閉時，該執行會停止執行重新傳輸原則。</span><span class="sxs-lookup"><span data-stu-id="2569f-110">When the WinSNMP application calls the [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) function with the retransmission mode value SNMPAPI\_OFF, the implementation stops executing the retransmission policy.</span></span> <span data-ttu-id="2569f-111">此執行會取消對未完成 SNMP 訊息的重新傳輸嘗試。</span><span class="sxs-lookup"><span data-stu-id="2569f-111">The implementation cancels retransmission attempts for outstanding SNMP messages.</span></span> <span data-ttu-id="2569f-112">這是因為在應用程式超時或重試計數器處理事件之前，執行可能無法處理所有未處理的 SNMP 要求和作業加上新的要求。</span><span class="sxs-lookup"><span data-stu-id="2569f-112">This is because it may not be possible for the implementation to handle all outstanding SNMP requests and operations plus new requests, before an application time-out or retry counter signals an event.</span></span>

 

 




