---
title: 路由
description: 路由 Api 可以建立應用程式來管理作業系統的路由功能。
ms.assetid: 66e1bbb4-73c8-40fc-9575-ffe76d4b697b
keywords:
- 路由 RAS
- 路由 RAS，起始頁
- RRAS RAS
- RRAS RAS，請參閱路由
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40e3b2a92a6c54f47693d657315ec0a48e660061
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842668"
---
# <a name="routing"></a><span data-ttu-id="e26e2-107">路由</span><span class="sxs-lookup"><span data-stu-id="e26e2-107">Routing</span></span>

## <a name="purpose"></a><span data-ttu-id="e26e2-108">目的</span><span class="sxs-lookup"><span data-stu-id="e26e2-108">Purpose</span></span>

<span data-ttu-id="e26e2-109">路由 Api 可以建立應用程式來管理作業系統的路由功能。</span><span class="sxs-lookup"><span data-stu-id="e26e2-109">The Routing APIs make it possible to create applications to administer the routing capabilities of the operating system.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="e26e2-110">適用時</span><span class="sxs-lookup"><span data-stu-id="e26e2-110">Where applicable</span></span>

<span data-ttu-id="e26e2-111">路由讓電腦能夠以網路路由器的形式運作。</span><span class="sxs-lookup"><span data-stu-id="e26e2-111">Routing makes it possible for a computer to function as a network router.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="e26e2-112">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="e26e2-112">Developer audience</span></span>

<span data-ttu-id="e26e2-113">路由 Api 是設計來供 C/c + + 程式設計人員使用。</span><span class="sxs-lookup"><span data-stu-id="e26e2-113">The Routing APIs are designed for use by C/C++ programmers.</span></span> <span data-ttu-id="e26e2-114">程式設計人員也應該熟悉網路概念。</span><span class="sxs-lookup"><span data-stu-id="e26e2-114">Programmers should also be familiar with networking concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="e26e2-115">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="e26e2-115">Run-time requirements</span></span>

<span data-ttu-id="e26e2-116">路由是以伺服器為基礎的技術。</span><span class="sxs-lookup"><span data-stu-id="e26e2-116">Routing is a server-based technology.</span></span> <span data-ttu-id="e26e2-117">路由的所有功能都整合到 Windows 2000 Server 和 Windows Server 2003 中。</span><span class="sxs-lookup"><span data-stu-id="e26e2-117">All the functionality of Routing is incorporated into Windows 2000 Server and the Windows Server 2003.</span></span> <span data-ttu-id="e26e2-118">路由應用程式無法在 Windows NT 工作站4.0 或用戶端作業系統（例如 Windows 95）上執行。</span><span class="sxs-lookup"><span data-stu-id="e26e2-118">Routing applications cannot run on Windows NT Workstation 4.0 or on client operating systems, such as Windows 95.</span></span> <span data-ttu-id="e26e2-119">如需有關哪些作業系統支援特定功能的詳細資訊，請參閱檔中的需求一節。</span><span class="sxs-lookup"><span data-stu-id="e26e2-119">For more specific information about which operating systems support a particular function, refer to the Requirements sections in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e26e2-120">本節內容</span><span class="sxs-lookup"><span data-stu-id="e26e2-120">In this section</span></span>



| <span data-ttu-id="e26e2-121">主題</span><span class="sxs-lookup"><span data-stu-id="e26e2-121">Topic</span></span>                                                                                               | <span data-ttu-id="e26e2-122">描述</span><span class="sxs-lookup"><span data-stu-id="e26e2-122">Description</span></span>                                                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e26e2-123">路由器管理</span><span class="sxs-lookup"><span data-stu-id="e26e2-123">Router Management</span></span>](about-router-management.md)<br/>                                         | <span data-ttu-id="e26e2-124">路由器管理 API 可讓開發人員建立應用程式，以在執行 Windows 2000 伺服器和更新版本作業系統的電腦上管理路由器服務。</span><span class="sxs-lookup"><span data-stu-id="e26e2-124">The router administration API allows developers to create applications to manage the router service on a computer running Windows 2000 Server and later operating systems.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="e26e2-125">路由器管理員和管理資訊基礎</span><span class="sxs-lookup"><span data-stu-id="e26e2-125">Router Managers and Management Information Base</span></span>](/windows/desktop/RRAS/about-router-management-with-mib)<br/> | <span data-ttu-id="e26e2-126">適用于路由器管理的管理資訊基礎 (MIB) Api，可讓您查詢和設定由其中一個路由器管理員或路由器管理員服務之任何路由通訊協定所匯出的 MIB 變數值。</span><span class="sxs-lookup"><span data-stu-id="e26e2-126">The Management Information Base (MIB) APIs for router management makes it possible to query and set the values of MIB variables exported by one of the router managers or any of the routing protocols that the router managers service.</span></span> <span data-ttu-id="e26e2-127">藉由使用此 API，路由器可支援 (SNMP) 的簡易網路管理通訊協定。</span><span class="sxs-lookup"><span data-stu-id="e26e2-127">By using this API, the router supports the Simple Network Management Protocol (SNMP).</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="e26e2-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="e26e2-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e26e2-129">IP 協助程式函式</span><span class="sxs-lookup"><span data-stu-id="e26e2-129">IP Helper Functions</span></span>](../iphlp/ip-helper-start-page.md)
</dt> <dt>

[<span data-ttu-id="e26e2-130">遠端存取</span><span class="sxs-lookup"><span data-stu-id="e26e2-130">Remote Access</span></span>](remote-access-start-page.md)
</dt> <dt>

[<span data-ttu-id="e26e2-131">路由通訊協定</span><span class="sxs-lookup"><span data-stu-id="e26e2-131">Routing Protocols</span></span>](routing-protocols-start-page.md)
</dt> </dl>

 

