---
title: 關於陷阱和通知
description: SNMP 代理程式應用程式可以傳送至 WinSNMP 應用程式的一種訊息，就是通知應用程式有重大事件的非同步訊息。
ms.assetid: 5249c5a5-9260-4a67-b00f-a12214012bb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2bacc6a92de2cb5a12aaf09f5caa629f28338f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840076"
---
# <a name="about-traps-and-notifications"></a><span data-ttu-id="de438-103">關於陷阱和通知</span><span class="sxs-lookup"><span data-stu-id="de438-103">About Traps and Notifications</span></span>

<span data-ttu-id="de438-104">SNMP 代理程式應用程式可以傳送至 WinSNMP 應用程式的一種訊息，就是通知應用程式有重大事件的非同步訊息。</span><span class="sxs-lookup"><span data-stu-id="de438-104">One type of message an SNMP agent application can send to a WinSNMP application is an asynchronous message that informs the application of a significant event.</span></span> <span data-ttu-id="de438-105">重大事件的一個範例是當網路連結關機或發生驗證失敗時。</span><span class="sxs-lookup"><span data-stu-id="de438-105">An example of a significant event is when a network link shuts down or when an authentication failure occurs.</span></span>

<span data-ttu-id="de438-106">這些類型的訊息在 SNMPv1 和 SNMPv2C 底下的通知下稱為「陷阱」。</span><span class="sxs-lookup"><span data-stu-id="de438-106">These types of messages are called traps under SNMPv1 and notifications under SNMPv2C.</span></span> <span data-ttu-id="de438-107">Microsoft 的 WinSNMP 實行一律會將 SNMPv1 陷阱轉譯為 SNMPv2C 格式，如 RFC 1908 所定義。</span><span class="sxs-lookup"><span data-stu-id="de438-107">The Microsoft WinSNMP implementation always translates SNMPv1 traps to the SNMPv2C format, as defined by RFC 1908.</span></span>

<span data-ttu-id="de438-108">當您呼叫 [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) 函式來建立陷印 pdu 時，您只能建立 SNMPV2C 陷阱 pdu。</span><span class="sxs-lookup"><span data-stu-id="de438-108">When you call the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function to create a trap PDU, you can create only an SNMPv2C trap PDU.</span></span> <span data-ttu-id="de438-109">您可以使用 [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) 函式的呼叫來更新的唯一類型的陷阱 Pdu 是 SNMPv2C 的陷阱 pdu。</span><span class="sxs-lookup"><span data-stu-id="de438-109">The only type of trap PDU you can update with a call to the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) function is an SNMPv2C trap PDU.</span></span>

<span data-ttu-id="de438-110">如需詳細資訊，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="de438-110">For more information, see the following topics.</span></span>



| <span data-ttu-id="de438-111">主題</span><span class="sxs-lookup"><span data-stu-id="de438-111">Topic</span></span>                                                                                    | <span data-ttu-id="de438-112">描述</span><span class="sxs-lookup"><span data-stu-id="de438-112">Description</span></span> |
|------------------------------------------------------------------------------------------|-------------|
| [<span data-ttu-id="de438-113">將 SNMPv1 的陷阱翻譯為 SNMPv2C</span><span class="sxs-lookup"><span data-stu-id="de438-113">Translating Traps from SNMPv1 to SNMPv2C</span></span>](translating-traps-from-snmpv1-to-snmpv2c.md) |             |
| [<span data-ttu-id="de438-114">補漏設格式</span><span class="sxs-lookup"><span data-stu-id="de438-114">Trap Formats</span></span>](trap-formats.md)                                                         |             |



 

 

 




