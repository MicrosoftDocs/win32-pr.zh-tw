---
title: WinSNMP API
description: Microsoft Windows SNMP 應用程式開發介面 () 1.1 a 和2.0 版的 WinSNMP API，可讓您開發以 SNMP 為基礎的網路管理應用程式，在 Windows 環境中執行。
ms.assetid: 54d9b61a-815a-41c3-9365-ec4478acc3f2
keywords:
- WinSNMP API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12d502060daa2931ca67c4476448347602159c98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023811"
---
# <a name="winsnmp-api"></a><span data-ttu-id="d55b7-104">WinSNMP API</span><span class="sxs-lookup"><span data-stu-id="d55b7-104">WinSNMP API</span></span>

<span data-ttu-id="d55b7-105">\[SNMP 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="d55b7-105">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d55b7-106">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="d55b7-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="d55b7-107">相反地，請使用 [Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 MICROSOFT 對 ws-atomictransaction 的實。\]</span><span class="sxs-lookup"><span data-stu-id="d55b7-107">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="d55b7-108">Microsoft Windows SNMP 應用程式開發介面 () 1.1 a 和2.0 版的 WinSNMP API，可讓您開發以 SNMP 為基礎的網路管理應用程式，在 Windows 環境中執行。</span><span class="sxs-lookup"><span data-stu-id="d55b7-108">The Microsoft Windows SNMP Application Programming Interface (the WinSNMP API) versions 1.1a and 2.0 allow you to develop SNMP-based network management applications that execute in the Windows environment.</span></span> <span data-ttu-id="d55b7-109">簡易網路管理通訊協定 (SNMP) 是一種要求-回應通訊協定，可在通訊協定實體之間傳輸管理資訊。</span><span class="sxs-lookup"><span data-stu-id="d55b7-109">The Simple Network Management Protocol (SNMP) is a request-response protocol that transfers management information between protocol entities.</span></span>

<span data-ttu-id="d55b7-110">已透過數個公司、關聯和個人的合作、輸入和支援，共同開發了 WinSNMP。</span><span class="sxs-lookup"><span data-stu-id="d55b7-110">WinSNMP has been jointly developed with the cooperation, input, and support from several companies, associations and individuals.</span></span>

<span data-ttu-id="d55b7-111">本總覽的第一個部分提供有關 WinSNMP 2.0 增補、SNMP 版本的資訊，以及 (Rfc) 的相關要求清單。</span><span class="sxs-lookup"><span data-stu-id="d55b7-111">The first part of this overview provides information about the WinSNMP 2.0 Addendum, SNMP versions, and a list of the relevant Requests for Comments (RFCs).</span></span> <span data-ttu-id="d55b7-112">它也會說明 WinSNMP 模型，以及 Microsoft WinSNMP 的元件和功能。</span><span class="sxs-lookup"><span data-stu-id="d55b7-112">It also describes the WinSNMP model, and the components and features of the Microsoft WinSNMP implementation.</span></span> <span data-ttu-id="d55b7-113">此外也提供您在 WinSNMP 環境中進行程式設計所需的資料管理和通訊概念的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d55b7-113">It also provides information about data management and communications concepts you need to program in the WinSNMP environment.</span></span>

<span data-ttu-id="d55b7-114">第二節討論的是 WinSNMP 函數以及下列相關的 WinSNMP 程式設計工作：</span><span class="sxs-lookup"><span data-stu-id="d55b7-114">The second section discusses the WinSNMP functions and the following related WinSNMP programming tasks:</span></span>

-   [<span data-ttu-id="d55b7-115">開啟和關閉 WinSNMP 應用程式</span><span class="sxs-lookup"><span data-stu-id="d55b7-115">Opening and closing a WinSNMP application</span></span>](opening-and-closing-a-winsnmp-application.md)
-   [<span data-ttu-id="d55b7-116">開啟和關閉 WinSNMP 會話</span><span class="sxs-lookup"><span data-stu-id="d55b7-116">Opening and closing a WinSNMP session</span></span>](opening-and-closing-a-winsnmp-session.md)
-   [<span data-ttu-id="d55b7-117">管理陷阱和通知</span><span class="sxs-lookup"><span data-stu-id="d55b7-117">Managing traps and notifications</span></span>](managing-traps-and-notifications.md)
-   [<span data-ttu-id="d55b7-118">使用變數系結清單</span><span class="sxs-lookup"><span data-stu-id="d55b7-118">Working with variable binding lists</span></span>](working-with-variable-binding-lists.md)
-   [<span data-ttu-id="d55b7-119">使用通訊協定資料單位</span><span class="sxs-lookup"><span data-stu-id="d55b7-119">Working with protocol data units</span></span>](working-with-protocol-data-units.md)
-   [<span data-ttu-id="d55b7-120">傳送 SNMP 訊息</span><span class="sxs-lookup"><span data-stu-id="d55b7-120">Sending SNMP messages</span></span>](sending-snmp-messages.md)
-   [<span data-ttu-id="d55b7-121">接收 SNMP 訊息</span><span class="sxs-lookup"><span data-stu-id="d55b7-121">Receiving SNMP messages</span></span>](receiving-snmp-messages.md)
-   [<span data-ttu-id="d55b7-122">管理物件識別碼</span><span class="sxs-lookup"><span data-stu-id="d55b7-122">Managing object identifiers</span></span>](managing-object-identifiers.md)
-   [<span data-ttu-id="d55b7-123">釋放 WinSNMP 描述項</span><span class="sxs-lookup"><span data-stu-id="d55b7-123">Freeing WinSNMP descriptors</span></span>](freeing-winsnmp-descriptors.md)
-   [<span data-ttu-id="d55b7-124">設定實體和內容轉譯模式</span><span class="sxs-lookup"><span data-stu-id="d55b7-124">Setting the entity and context translation mode</span></span>](setting-the-entity-and-context-translation-mode.md)
-   [<span data-ttu-id="d55b7-125">管理重新傳輸原則</span><span class="sxs-lookup"><span data-stu-id="d55b7-125">Managing the retransmission policy</span></span>](managing-the-retransmission-policy.md)
-   [<span data-ttu-id="d55b7-126">使用多個執行緒撰寫的 WinSNMP 應用程式</span><span class="sxs-lookup"><span data-stu-id="d55b7-126">Writing WinSNMP applications with multiple threads</span></span>](writing-winsnmp-applications-with-multiple-threads.md)
-   [<span data-ttu-id="d55b7-127">註冊 SNMP 代理程式應用程式</span><span class="sxs-lookup"><span data-stu-id="d55b7-127">Registering an SNMP agent application</span></span>](registering-an-snmp-agent-application.md)

<span data-ttu-id="d55b7-128">閱讀此總覽之前，您應該先熟悉 SNMP 和 Windows 程式設計的基本概念。</span><span class="sxs-lookup"><span data-stu-id="d55b7-128">You should be familiar with the basic concepts of SNMP and Windows programming before reading this overview.</span></span> <span data-ttu-id="d55b7-129">如需 SNMP 的詳細資訊，請參閱「 [簡易網路管理通訊協定](simple-network-management-protocol-snmp-.md) 」和批註的相關要求 (rfc) 這些要求是由「網際網路工程任務推動力 (IETF) 所發行。</span><span class="sxs-lookup"><span data-stu-id="d55b7-129">For more information about SNMP, see [Simple Network Management Protocol](simple-network-management-protocol-snmp-.md) and the relevant Requests for Comments (RFCs) which are published by the Internet Engineering Task Force (IETF).</span></span>

 

 