---
title: 傳送 SNMP 訊息
description: WinSNMP 應用程式會藉由傳送 SNMP 訊息來起始傳輸要求。 SNMP 訊息包含 SNMP 通訊協定資料單位。 如需詳細資訊，請參閱使用通訊協定資料單位。
ms.assetid: a7439cd2-af13-4e2b-a0a6-5cc271a011e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613ac7079f7dc206280b8d8077d2d5ea8db7151c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301552"
---
# <a name="sending-snmp-messages"></a><span data-ttu-id="30384-105">傳送 SNMP 訊息</span><span class="sxs-lookup"><span data-stu-id="30384-105">Sending SNMP Messages</span></span>

<span data-ttu-id="30384-106">WinSNMP 應用程式會藉由傳送 SNMP 訊息來起始傳輸要求。</span><span class="sxs-lookup"><span data-stu-id="30384-106">A WinSNMP application initiates a transmission request by sending an SNMP message.</span></span> <span data-ttu-id="30384-107">SNMP 訊息包含 SNMP 通訊協定資料單位。</span><span class="sxs-lookup"><span data-stu-id="30384-107">SNMP messages include an SNMP protocol data unit.</span></span> <span data-ttu-id="30384-108">如需詳細資訊，請參閱 [使用通訊協定資料單位](working-with-protocol-data-units.md)。</span><span class="sxs-lookup"><span data-stu-id="30384-108">For more information, see [Working with Protocol Data Units](working-with-protocol-data-units.md).</span></span>

<span data-ttu-id="30384-109">WinSNMP 應用程式必須呼叫 [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) 函式，以要求 Microsoft WinSNMP 執行傳輸 PDU，以及相關 RFC 所定義的其他必要訊息元素。</span><span class="sxs-lookup"><span data-stu-id="30384-109">A WinSNMP application must call the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function to request that the Microsoft WinSNMP implementation transmit the PDU, with the other required message elements defined by the relevant RFC.</span></span> <span data-ttu-id="30384-110">除了目的地實體之外，應用程式還必須指定來源實體和要求的內容。</span><span class="sxs-lookup"><span data-stu-id="30384-110">In addition to the destination entity, the application must specify the source entity and a context for the request.</span></span> <span data-ttu-id="30384-111">[**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)函式會以非同步方式執行。</span><span class="sxs-lookup"><span data-stu-id="30384-111">The [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function executes asynchronously.</span></span>

<span data-ttu-id="30384-112">WinSNMP 應用程式必須呼叫 [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) 函式，才能取得 **SnmpSendMsg** 要求的回應。</span><span class="sxs-lookup"><span data-stu-id="30384-112">The WinSNMP application must call the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function to retrieve the response to an **SnmpSendMsg** request.</span></span>

<span data-ttu-id="30384-113">當應用程式呼叫 [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)時，此實作為驗證 PDU 和其他訊息元素的有效性。</span><span class="sxs-lookup"><span data-stu-id="30384-113">The implementation verifies the validity of the PDU and the other message elements when an application calls [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg).</span></span>

 

 




