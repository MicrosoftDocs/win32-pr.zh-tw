---
title: 符合回應和要求 Pdu
description: WinSNMP 應用程式接收 SNMP 回應的順序可能不符合應用程式提交 SNMP 作業要求的順序。
ms.assetid: cd09cc4b-2ef6-4d2f-8f0f-b83d8df8599a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75a05f4a450ac1712d7cdd01a3c0e79dfddeb2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932391"
---
# <a name="matching-response-and-request-pdus"></a><span data-ttu-id="d08b1-103">符合回應和要求 Pdu</span><span class="sxs-lookup"><span data-stu-id="d08b1-103">Matching Response and Request PDUs</span></span>

<span data-ttu-id="d08b1-104">WinSNMP 應用程式接收 SNMP 回應的順序可能不符合應用程式提交 SNMP 作業要求的順序。</span><span class="sxs-lookup"><span data-stu-id="d08b1-104">The order in which the WinSNMP application receives SNMP responses may not match the order in which the application submits SNMP operation requests.</span></span> <span data-ttu-id="d08b1-105">為了符合要求的回應，應用程式必須使用要求識別碼欄位 (回應的要求識別碼 **) \_** 。</span><span class="sxs-lookup"><span data-stu-id="d08b1-105">To match the response with the request, the application must use the request identifier field (the **request\_id**) of the response.</span></span>

<span data-ttu-id="d08b1-106">[ **要求 \_ 識別碼** ] 欄位是識別 PDU 的唯一數位值。</span><span class="sxs-lookup"><span data-stu-id="d08b1-106">The **request\_id** field is a unique numeric value that identifies the PDU.</span></span> <span data-ttu-id="d08b1-107">應用程式可以藉由呼叫 [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) 函數或 [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) 函數來指派要求識別碼。</span><span class="sxs-lookup"><span data-stu-id="d08b1-107">Applications can assign request identifiers by calling the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function or the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) function.</span></span> <span data-ttu-id="d08b1-108">呼叫 [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) 函式來取出 PDU 的 **要求 \_ 識別碼**。</span><span class="sxs-lookup"><span data-stu-id="d08b1-108">Call the [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) function to retrieve a PDU's **request\_id**.</span></span>

 

 




