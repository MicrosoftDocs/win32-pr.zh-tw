---
title: 註冊 SNMP 代理程式應用程式
description: 除了 SNMP 管理員作業之外，WinSNMP API 版本2.0 也支援 SNMP 代理程式作業。
ms.assetid: 473560b5-4611-410e-aeae-764c9c76e765
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40922469c52e33e4b5c2f408c1c107b6784529f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932389"
---
# <a name="registering-an-snmp-agent-application"></a><span data-ttu-id="9552b-103">註冊 SNMP 代理程式應用程式</span><span class="sxs-lookup"><span data-stu-id="9552b-103">Registering an SNMP Agent Application</span></span>

<span data-ttu-id="9552b-104">除了 SNMP 管理員作業之外，WinSNMP API 版本2.0 也支援 SNMP 代理程式作業。</span><span class="sxs-lookup"><span data-stu-id="9552b-104">In addition to SNMP manager operations, the WinSNMP API version 2.0 also supports SNMP agent operations.</span></span>

<span data-ttu-id="9552b-105">若要將 WinSNMP 應用程式註冊為 SNMP 代理程式，應用程式可以呼叫 [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) 函數。</span><span class="sxs-lookup"><span data-stu-id="9552b-105">To register a WinSNMP application as an SNMP agent, the application can call the [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) function.</span></span> <span data-ttu-id="9552b-106">此函式會通知 Microsoft WinSNMP 執行，SNMP 實體將會扮演 SNMP 代理程式的角色。</span><span class="sxs-lookup"><span data-stu-id="9552b-106">This function informs the Microsoft WinSNMP implementation that an SNMP entity will be acting in the role of an SNMP agent.</span></span> <span data-ttu-id="9552b-107">當應用程式不再作為代理程式時，應用程式也可以呼叫 **SnmpListen** 來通知執行。</span><span class="sxs-lookup"><span data-stu-id="9552b-107">The application can also call **SnmpListen** to inform the implementation when it will no longer be acting as an agent.</span></span>

<span data-ttu-id="9552b-108">如果應用程式呼叫 [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) 函式，並 \_ 在 *LSTATUS* 參數中傳遞 SNMPAPI 的值，則會發生下列動作：</span><span class="sxs-lookup"><span data-stu-id="9552b-108">If an application calls the [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) function and passes the value SNMPAPI\_ON in the *lStatus* parameter, the following actions occur:</span></span>

1.  <span data-ttu-id="9552b-109">將在 SNMP 代理程式角色中運作的實體會系結至其指派的埠，並針對傳入的 SNMP 訊息要求進行「接聽」。</span><span class="sxs-lookup"><span data-stu-id="9552b-109">The entity that will be functioning in an SNMP agent role binds to its assigned port, and "listens" for incoming SNMP message requests.</span></span>
2.  <span data-ttu-id="9552b-110">代理程式會使用應用程式特定邏輯來處理每個 SNMP 要求。</span><span class="sxs-lookup"><span data-stu-id="9552b-110">The agent uses application-specific logic to process each SNMP request.</span></span>
3.  <span data-ttu-id="9552b-111">代理程式會針對每個要求形成適當的回應。</span><span class="sxs-lookup"><span data-stu-id="9552b-111">The agent forms appropriate responses to each request.</span></span>
4.  <span data-ttu-id="9552b-112">代理程式藉由呼叫 [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) 函式，將回應傳送給要求的實體。</span><span class="sxs-lookup"><span data-stu-id="9552b-112">The agent transmits the response to the requesting entity by calling the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function.</span></span> <span data-ttu-id="9552b-113">當代理程式呼叫 **SnmpSendMsg** 時，它會在 *srcEntity* 參數中指定代理程式的位址，並在 *dstEntity* 參數中指定遠端系統管理員實體的位址。</span><span class="sxs-lookup"><span data-stu-id="9552b-113">When the agent calls **SnmpSendMsg**, it specifies the address of the agent in the *srcEntity* parameter, and the address of the remote manager entity in the *dstEntity* parameter.</span></span> <span data-ttu-id="9552b-114"> (這些值是 agent 實體在呼叫 [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) 函式以抓取 SNMP 要求時，在這些參數中收到的值的相反值。 ) </span><span class="sxs-lookup"><span data-stu-id="9552b-114">(These values are the reverse of the values the agent entity received in these parameters when it called the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function to retrieve an SNMP request.)</span></span>

<span data-ttu-id="9552b-115">如需 SNMP 管理應用程式和代理程式應用程式的詳細資訊，請參閱 [關於 snmp](about-snmp.md)。</span><span class="sxs-lookup"><span data-stu-id="9552b-115">For more information about SNMP management applications and agent applications, see [About SNMP](about-snmp.md).</span></span>

 

 




