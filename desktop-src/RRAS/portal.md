---
title: 路由及遠端存取服務
description: .
ms.assetid: fa0a183a-0254-401e-8b78-441cb3f83e8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdaae9e54cd37bef1b45a3336eb389027ebf01ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969071"
---
# <a name="routing-and-remote-access-service"></a><span data-ttu-id="6f7d1-103">路由及遠端存取服務</span><span class="sxs-lookup"><span data-stu-id="6f7d1-103">Routing and Remote Access Service</span></span>

## <a name="purpose"></a><span data-ttu-id="6f7d1-104">目的</span><span class="sxs-lookup"><span data-stu-id="6f7d1-104">Purpose</span></span>

<span data-ttu-id="6f7d1-105">遠端存取服務 (RAS) 可以用來建立用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="6f7d1-105">Remote Access Service (RAS) can be used to create client applications.</span></span> <span data-ttu-id="6f7d1-106">這些應用程式會顯示 RAS 通用對話方塊、管理遠端存取連線和裝置，以及操作電話簿專案。</span><span class="sxs-lookup"><span data-stu-id="6f7d1-106">These applications display RAS common dialog boxes, manage remote access connections and devices, and manipulate phone-book entries.</span></span>

<span data-ttu-id="6f7d1-107">路由 Api 可以建立應用程式來管理作業系統的路由功能。</span><span class="sxs-lookup"><span data-stu-id="6f7d1-107">The Routing APIs make it possible to create applications to administer the routing capabilities of the operating system.</span></span>

<span data-ttu-id="6f7d1-108">開發人員可以使用路由通訊協定 Api 來執行路由通訊協定。</span><span class="sxs-lookup"><span data-stu-id="6f7d1-108">Developers can use the Routing Protocol APIs to implement routing protocols.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="6f7d1-109">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="6f7d1-109">Developer audience</span></span>

<span data-ttu-id="6f7d1-110">「路由及遠端存取」服務 Api 是設計來供 C/c + + 程式設計人員使用。</span><span class="sxs-lookup"><span data-stu-id="6f7d1-110">The Routing and Remote Access Service APIs are designed for use by C/C++ programmers.</span></span> <span data-ttu-id="6f7d1-111">程式設計人員也應該熟悉網路概念。</span><span class="sxs-lookup"><span data-stu-id="6f7d1-111">Programmers should also be familiar with networking concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="6f7d1-112">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="6f7d1-112">Run-time requirements</span></span>

<span data-ttu-id="6f7d1-113">如需有關哪些作業系統支援特定功能的詳細資訊，請參閱檔中的需求一節。</span><span class="sxs-lookup"><span data-stu-id="6f7d1-113">For more specific information about which operating systems support a particular function, refer to the Requirements sections in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6f7d1-114">本節內容</span><span class="sxs-lookup"><span data-stu-id="6f7d1-114">In this section</span></span>



| <span data-ttu-id="6f7d1-115">主題</span><span class="sxs-lookup"><span data-stu-id="6f7d1-115">Topic</span></span>                                                                                                             | <span data-ttu-id="6f7d1-116">描述</span><span class="sxs-lookup"><span data-stu-id="6f7d1-116">Description</span></span>                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f7d1-117">路由及遠端存取服務架構</span><span class="sxs-lookup"><span data-stu-id="6f7d1-117">Routing and Remote Access Services Architecture</span></span>](routing-and-remote-access-services-architecture.md)<br/> | <span data-ttu-id="6f7d1-118">路由和遠端存取服務架構的總覽。</span><span class="sxs-lookup"><span data-stu-id="6f7d1-118">Overview of the Routing and Remote Access Services architecture.</span></span><br/>                                           |
| [<span data-ttu-id="6f7d1-119">路由及遠端存取登錄版面配置</span><span class="sxs-lookup"><span data-stu-id="6f7d1-119">Routing and Remote Access Registry Layout</span></span>](routing-and-remote-access-registry-layout.md)<br/>             | <span data-ttu-id="6f7d1-120">路由器服務的登錄版面配置範例</span><span class="sxs-lookup"><span data-stu-id="6f7d1-120">An example registry layout for the router service</span></span><br/>                                                          |
| [<span data-ttu-id="6f7d1-121">路由和遠端存取錯誤代碼</span><span class="sxs-lookup"><span data-stu-id="6f7d1-121">Routing and Remote Access Error Codes</span></span>](routing-and-remote-access-error-codes.md)<br/>                     | <span data-ttu-id="6f7d1-122">所有路由和遠端存取錯誤代碼的清單。</span><span class="sxs-lookup"><span data-stu-id="6f7d1-122">List of all routing and remote access error codes.</span></span><br/>                                                         |
| [<span data-ttu-id="6f7d1-123">遠端存取</span><span class="sxs-lookup"><span data-stu-id="6f7d1-123">Remote Access</span></span>](remote-access-start-page.md)<br/>                                                          | <span data-ttu-id="6f7d1-124">RAS 和 RAS 管理 Api 的檔。</span><span class="sxs-lookup"><span data-stu-id="6f7d1-124">Documentation for RAS and RAS Administration APIs.</span></span><br/>                                                         |
| [<span data-ttu-id="6f7d1-125">路由</span><span class="sxs-lookup"><span data-stu-id="6f7d1-125">Routing</span></span>](routing-start-page.md)<br/>                                                                      | <span data-ttu-id="6f7d1-126">路由器管理和管理資訊基礎 (MIB) Api 的檔。</span><span class="sxs-lookup"><span data-stu-id="6f7d1-126">Documentation for the Router Management and Management Information Base (MIB) APIs.</span></span><br/>                        |
| [<span data-ttu-id="6f7d1-127">路由通訊協定</span><span class="sxs-lookup"><span data-stu-id="6f7d1-127">Routing Protocols</span></span>](routing-protocols-start-page.md)<br/>                                                  | <span data-ttu-id="6f7d1-128">多播群組管理員、路由通訊協定介面和路由表管理員 Api 的檔。</span><span class="sxs-lookup"><span data-stu-id="6f7d1-128">Documentation for the Multicast Group Manager, Routing Protocol Interface, and Routing Table Manager APIs.</span></span><br/> |
| [<span data-ttu-id="6f7d1-129">詞彙</span><span class="sxs-lookup"><span data-stu-id="6f7d1-129">Glossary</span></span>](glossary.md)<br/>                                                                               | <span data-ttu-id="6f7d1-130">「路由及遠端存取」服務檔中使用的詞彙定義。</span><span class="sxs-lookup"><span data-stu-id="6f7d1-130">Definitions for terms used in the Routing and Remote Access Service documentation.</span></span><br/>                         |



 

 

 





