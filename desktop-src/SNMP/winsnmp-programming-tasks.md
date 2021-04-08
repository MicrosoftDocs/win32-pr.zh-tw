---
title: WinSNMP 程式設計工作
description: 下表摘要說明您必須執行以編寫 WinSNMP 應用程式程式碼的基本程式設計程式，以及提供這些工作相關資訊的主題。
ms.assetid: 70c24042-bf44-4484-8e5e-d117e2ba28d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d75fa8d2ad223fbd8f71eff78c7cd232ddc492a9
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/11/2020
ms.locfileid: "103841867"
---
# <a name="winsnmp-programming-tasks"></a><span data-ttu-id="d2e01-103">WinSNMP 程式設計工作</span><span class="sxs-lookup"><span data-stu-id="d2e01-103">WinSNMP Programming Tasks</span></span>

<span data-ttu-id="d2e01-104">下表摘要說明您必須執行以編寫 WinSNMP 應用程式程式碼的基本程式設計程式，以及提供這些工作相關資訊的主題。</span><span class="sxs-lookup"><span data-stu-id="d2e01-104">The following table summarizes the basic programming procedures that you must perform to code a WinSNMP application, and the topics that provide information about these tasks.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d2e01-105">程式設計工作</span><span class="sxs-lookup"><span data-stu-id="d2e01-105">Programming task</span></span></th>
<th><span data-ttu-id="d2e01-106">工作相關的函式和主題</span><span class="sxs-lookup"><span data-stu-id="d2e01-106">Task-related function and topics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d2e01-107">開啟 WinSNMP 應用程式。</span><span class="sxs-lookup"><span data-stu-id="d2e01-107">Open the WinSNMP application.</span></span></td>
<td><span data-ttu-id="d2e01-108">使用 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="d2e01-108">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a>.</span></span> <span data-ttu-id="d2e01-109">請參閱 <a href="opening-and-closing-a-winsnmp-application.md">開啟和關閉 WinSNMP 應用程式</a>。</span><span class="sxs-lookup"><span data-stu-id="d2e01-109">See <a href="opening-and-closing-a-winsnmp-application.md">Opening and Closing a WinSNMP Application</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2e01-110">開啟一或多個 WinSNMP 會話。</span><span class="sxs-lookup"><span data-stu-id="d2e01-110">Open one or more WinSNMP sessions.</span></span></td>
<td><span data-ttu-id="d2e01-111">使用 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="d2e01-111">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a>.</span></span> <span data-ttu-id="d2e01-112">請參閱 <a href="opening-and-closing-a-winsnmp-session.md">開啟和關閉 WinSNMP 會話</a>。</span><span class="sxs-lookup"><span data-stu-id="d2e01-112">See <a href="opening-and-closing-a-winsnmp-session.md">Opening and Closing a WinSNMP Session</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2e01-113">註冊以接收陷阱或通知。</span><span class="sxs-lookup"><span data-stu-id="d2e01-113">Register to receive traps or notifications.</span></span></td>
<td><span data-ttu-id="d2e01-114">使用 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>SnmpRegister</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="d2e01-114">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>SnmpRegister</strong></a>.</span></span> <span data-ttu-id="d2e01-115">請參閱 <a href="managing-traps-and-notifications.md">管理陷阱和通知</a>。</span><span class="sxs-lookup"><span data-stu-id="d2e01-115">See <a href="managing-traps-and-notifications.md">Managing Traps and Notifications</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2e01-116">建立一或多個變數系結清單，以合併在 PDU 中。</span><span class="sxs-lookup"><span data-stu-id="d2e01-116">Create one or more variable binding lists for incorporation in a PDU.</span></span></td>
<td><span data-ttu-id="d2e01-117">使用 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl"><strong>SnmpCreateVbl</strong></a>、 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl"><strong>SnmpDuplicateVbl</strong></a>、 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb"><strong>SnmpSetVb</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="d2e01-117">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl"><strong>SnmpCreateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl"><strong>SnmpDuplicateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb"><strong>SnmpSetVb</strong></a>.</span></span> <span data-ttu-id="d2e01-118">請參閱 <a href="working-with-variable-binding-lists.md">使用變數繫結欄位表</a>。</span><span class="sxs-lookup"><span data-stu-id="d2e01-118">See <a href="working-with-variable-binding-lists.md">Working with Variable Binding Lists</a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d2e01-119">應用程式可能需要呼叫其他變數系結 <a href="winsnmp-functions.md">函數</a> ，以建立變數系結清單。</span><span class="sxs-lookup"><span data-stu-id="d2e01-119">The application may need to call other <a href="winsnmp-functions.md">variable binding functions</a> to create the variable binding list.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2e01-120">建立一或多個用於傳輸和處理的 Pdu。</span><span class="sxs-lookup"><span data-stu-id="d2e01-120">Create one or more PDUs for transmission and processing.</span></span></td>
<td><span data-ttu-id="d2e01-121">使用 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu"><strong>SnmpCreatePDU</strong></a>、 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata"><strong>SnmpSetPduData</strong></a>、 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu"><strong>SnmpDuplicatePDU</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="d2e01-121">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu"><strong>SnmpCreatePDU</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata"><strong>SnmpSetPduData</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu"><strong>SnmpDuplicatePDU</strong></a>.</span></span> <span data-ttu-id="d2e01-122">請參閱 <a href="working-with-protocol-data-units.md">使用通訊協定資料單位</a>。</span><span class="sxs-lookup"><span data-stu-id="d2e01-122">See <a href="working-with-protocol-data-units.md">Working with Protocol Data Units</a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d2e01-123">應用程式可能需要呼叫其他的 <a href="winsnmp-functions.md">pdu 功能</a> 和 WinSNMP <a href="winsnmp-functions.md">公用程式</a> 函式來建立 PDU。</span><span class="sxs-lookup"><span data-stu-id="d2e01-123">The application may need to call other <a href="winsnmp-functions.md">PDU functions</a> and WinSNMP <a href="winsnmp-functions.md">utility functions</a> to create the PDU.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2e01-124">提交一或多個 SNMP 操作要求。</span><span class="sxs-lookup"><span data-stu-id="d2e01-124">Submit one or more SNMP operation requests.</span></span></td>
<td><span data-ttu-id="d2e01-125">使用 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>SnmpSendMsg</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="d2e01-125">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>SnmpSendMsg</strong></a>.</span></span> <span data-ttu-id="d2e01-126">請參閱傳送 <a href="sending-snmp-messages.md">SNMP 訊息</a>。</span><span class="sxs-lookup"><span data-stu-id="d2e01-126">See <a href="sending-snmp-messages.md">Sending SNMP Messages</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2e01-127">取得 SNMP 作業要求的回應。</span><span class="sxs-lookup"><span data-stu-id="d2e01-127">Retrieve the response to the SNMP operation request.</span></span></td>
<td><span data-ttu-id="d2e01-128">使用 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>SnmpRecvMsg</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="d2e01-128">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>SnmpRecvMsg</strong></a>.</span></span> <span data-ttu-id="d2e01-129">請參閱 <a href="receiving-snmp-messages.md">接收 SNMP 訊息</a>。</span><span class="sxs-lookup"><span data-stu-id="d2e01-129">See <a href="receiving-snmp-messages.md">Receiving SNMP Messages</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2e01-130">處理要求回應。</span><span class="sxs-lookup"><span data-stu-id="d2e01-130">Process the request response.</span></span></td>
<td><span data-ttu-id="d2e01-131">使用應用程式特定邏輯。</span><span class="sxs-lookup"><span data-stu-id="d2e01-131">Use application-specific logic.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2e01-132">關閉每個 WinSNMP 會話。</span><span class="sxs-lookup"><span data-stu-id="d2e01-132">Close each WinSNMP session.</span></span></td>
<td><span data-ttu-id="d2e01-133">使用 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>SnmpClose</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="d2e01-133">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>SnmpClose</strong></a>.</span></span> <span data-ttu-id="d2e01-134">請參閱 <a href="opening-and-closing-a-winsnmp-session.md">開啟和關閉 WinSNMP 會話</a>。</span><span class="sxs-lookup"><span data-stu-id="d2e01-134">See <a href="opening-and-closing-a-winsnmp-session.md">Opening and Closing a WinSNMP Session</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2e01-135">關閉 WinSNMP 應用程式。</span><span class="sxs-lookup"><span data-stu-id="d2e01-135">Close the WinSNMP application.</span></span></td>
<td><span data-ttu-id="d2e01-136">使用 <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>SnmpCleanup</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="d2e01-136">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>SnmpCleanup</strong></a>.</span></span> <span data-ttu-id="d2e01-137">請參閱 <a href="opening-and-closing-a-winsnmp-application.md">開啟和關閉 WinSNMP 應用程式</a>。</span><span class="sxs-lookup"><span data-stu-id="d2e01-137">See <a href="opening-and-closing-a-winsnmp-application.md">Opening and Closing a WinSNMP Application</a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d2e01-138">下列主題包含有關 WinSNMP 環境特定的其他一般程式設計概念的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="d2e01-138">The following topics contain additional information about other general programming concepts specific to the WinSNMP environment.</span></span>



|                                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2e01-139">一般程式設計工作</span><span class="sxs-lookup"><span data-stu-id="d2e01-139">General programming tasks</span></span>](general-winsnmp-programming-tasks.md) | <span data-ttu-id="d2e01-140">[管理物件識別碼](managing-object-identifiers.md)[釋放 WinSNMP 描述](freeing-winsnmp-descriptors.md)項</span><span class="sxs-lookup"><span data-stu-id="d2e01-140">[Managing Object Identifiers](managing-object-identifiers.md)[Freeing WinSNMP Descriptors](freeing-winsnmp-descriptors.md)</span></span><br/> [<span data-ttu-id="d2e01-141">設定實體和內容轉譯模式</span><span class="sxs-lookup"><span data-stu-id="d2e01-141">Setting the Entity and Context Translation Mode</span></span>](setting-the-entity-and-context-translation-mode.md)<br/> [<span data-ttu-id="d2e01-142">管理重新傳輸原則</span><span class="sxs-lookup"><span data-stu-id="d2e01-142">Managing the Retransmission Policy</span></span>](managing-the-retransmission-policy.md)<br/> [<span data-ttu-id="d2e01-143">使用多個執行緒撰寫的 WinSNMP 應用程式</span><span class="sxs-lookup"><span data-stu-id="d2e01-143">Writing WinSNMP Applications with Multiple Threads</span></span>](writing-winsnmp-applications-with-multiple-threads.md)<br/> [<span data-ttu-id="d2e01-144">註冊 SNMP 代理程式應用程式</span><span class="sxs-lookup"><span data-stu-id="d2e01-144">Registering an SNMP Agent Application</span></span>](registering-an-snmp-agent-application.md)<br/> |



 

<span data-ttu-id="d2e01-145">此外，WinSNMP 應用程式可能需要將呼叫併入下列的 WinSNMP 函數： [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl)、 [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)、 [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor)、 [**SnmpFreeCoNtext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)和 [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu)。</span><span class="sxs-lookup"><span data-stu-id="d2e01-145">In addition, the WinSNMP application may need to incorporate calls to the following WinSNMP functions: [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext), and [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu).</span></span> <span data-ttu-id="d2e01-146">這可讓 Microsoft WinSNMP 實行釋出 WinSNMP 記憶體物件。</span><span class="sxs-lookup"><span data-stu-id="d2e01-146">This enables the Microsoft WinSNMP implementation to free WinSNMP memory objects.</span></span> <span data-ttu-id="d2e01-147">一般來說，當您呼叫 WinSNMP 函式時，必須釋放所有配置的資源。</span><span class="sxs-lookup"><span data-stu-id="d2e01-147">As a general rule, the WinSNMP application should free all resources allocated as the result of a call to a WinSNMP function.</span></span> <span data-ttu-id="d2e01-148">如需解除配置資源的詳細資訊，請參閱配置 [WinSNMP 記憶體物件](allocating-winsnmp-memory-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="d2e01-148">For additional information about deallocating resources, see [Allocating WinSNMP Memory Objects](allocating-winsnmp-memory-objects.md).</span></span>

 

 





