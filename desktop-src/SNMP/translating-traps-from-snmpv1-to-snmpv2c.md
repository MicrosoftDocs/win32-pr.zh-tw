---
title: 將 SNMPv1 的陷阱翻譯為 SNMPv2C
description: 當 Microsoft WinSNMP 的執行從 SNMPv1 架構下的實體接收到陷阱時，會將陷阱轉譯為 SNMPv2C 格式。
ms.assetid: 472f67ba-05d5-46f7-a2f1-1cef6182574e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d36870bda9b434bcc19f42332f2751020689591
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839631"
---
# <a name="translating-traps-from-snmpv1-to-snmpv2c"></a><span data-ttu-id="2830d-103">將 SNMPv1 的陷阱翻譯為 SNMPv2C</span><span class="sxs-lookup"><span data-stu-id="2830d-103">Translating Traps from SNMPv1 to SNMPv2C</span></span>

<span data-ttu-id="2830d-104">當 Microsoft WinSNMP 的執行從 SNMPv1 架構下的實體接收到陷阱時，會將陷阱轉譯為 SNMPv2C 格式。</span><span class="sxs-lookup"><span data-stu-id="2830d-104">When the Microsoft WinSNMP implementation receives traps from an entity operating under the SNMPv1 framework, it translates the traps to the SNMPv2C format.</span></span> <span data-ttu-id="2830d-105">因此，當 [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) 傳遞時，它一律會採用 SNMPv2C 格式。</span><span class="sxs-lookup"><span data-stu-id="2830d-105">Therefore, when [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) delivers a trap it is always in the SNMPv2C format.</span></span> <span data-ttu-id="2830d-106">RFC 1908：「在第1版與第2版的網際網路標準網路管理架構之間共存」中，指定從 SNMPv1 轉譯為 SNMPv2C 陷阱格式的規則。</span><span class="sxs-lookup"><span data-stu-id="2830d-106">RFC 1908, "Coexistence between Version 1 and Version 2 of the Internet-standard Network Management Framework," specifies the rules for translating from the SNMPv1 to the SNMPv2C trap format.</span></span>

<span data-ttu-id="2830d-107">WinSNMP 應用程式可以檢查變數系結清單中的最後一個變數系結專案，以判斷專案是否為從 SNMPv1 轉譯為 SNMPv2C 格式的設陷。</span><span class="sxs-lookup"><span data-stu-id="2830d-107">A WinSNMP application can check the last variable binding entry in a variable binding list to determine if the entry is a trap translated from the SNMPv1 to the SNMPv2C format.</span></span> <span data-ttu-id="2830d-108">如果是的話，最後一個變數系結永遠等於值 "snmpTrapEnterpriseOID. 0"。</span><span class="sxs-lookup"><span data-stu-id="2830d-108">If so, the last variable binding will always be equal to the value "snmpTrapEnterpriseOID.0".</span></span>

<span data-ttu-id="2830d-109">如需詳細資訊，請參閱 [管理陷阱和通知](managing-traps-and-notifications.md)。</span><span class="sxs-lookup"><span data-stu-id="2830d-109">For more information, see [Managing Traps and Notifications](managing-traps-and-notifications.md).</span></span>

 

 




