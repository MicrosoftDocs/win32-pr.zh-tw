---
description: 對等基礎結構是一組功能強大且有彈性的 Api。
ms.assetid: aed7585a-88e5-4ca3-a8c3-e2ccfe13d35d
title: 什麼是對等基礎結構？
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 873717b3f90497fe9ab9f50bb9c18e6f0692a4e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988797"
---
# <a name="what-is-the-peer-infrastructure"></a><span data-ttu-id="d32c8-103">什麼是對等基礎結構？</span><span class="sxs-lookup"><span data-stu-id="d32c8-103">What is the Peer Infrastructure?</span></span>

<span data-ttu-id="d32c8-104">對等基礎結構是一組功能強大且有彈性的 Api。</span><span class="sxs-lookup"><span data-stu-id="d32c8-104">The Peer Infrastructure is a set of several APIs that are powerful and flexible.</span></span> <span data-ttu-id="d32c8-105">主要的元件包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="d32c8-105">The major components include the following:</span></span>

-   [<span data-ttu-id="d32c8-106">對等圖形 API</span><span class="sxs-lookup"><span data-stu-id="d32c8-106">Peer Graphing API</span></span>](#peer-graphing-api)
-   [<span data-ttu-id="d32c8-107">對等群組 API</span><span class="sxs-lookup"><span data-stu-id="d32c8-107">Peer Grouping API</span></span>](#peer-grouping-api)
-   [<span data-ttu-id="d32c8-108">對等身分識別管理員 API</span><span class="sxs-lookup"><span data-stu-id="d32c8-108">Peer Identity Manager API</span></span>](#peer-identity-manager-api)
-   [<span data-ttu-id="d32c8-109">PNRP 命名空間提供者 API</span><span class="sxs-lookup"><span data-stu-id="d32c8-109">PNRP Namespace Provider API</span></span>](#pnrp-namespace-provider-api)

## <a name="peer-graphing-api"></a><span data-ttu-id="d32c8-110">對等圖形 API</span><span class="sxs-lookup"><span data-stu-id="d32c8-110">Peer Graphing API</span></span>

<span data-ttu-id="d32c8-111">對等基礎結構提供圖形技術，可在對等圖形中的對等之間有效率且可靠地傳遞資訊。</span><span class="sxs-lookup"><span data-stu-id="d32c8-111">The Peer Infrastructure provides a graphing technology that can pass information efficiently and reliably between peers in a peer graph.</span></span> <span data-ttu-id="d32c8-112">[對等圖形 API](graphing-api.md)可確保每個節點在圖形中都具有一致的資料檢視。</span><span class="sxs-lookup"><span data-stu-id="d32c8-112">The [Peer Graphing API](graphing-api.md) ensures that each node has a consistent view of the data in a graph.</span></span>

<span data-ttu-id="d32c8-113">您可以使用 [對等圖形 API](graphing-api.md) 來執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="d32c8-113">You can use the [Peer Graphing API](graphing-api.md) to do the following:</span></span>

-   <span data-ttu-id="d32c8-114">建立和管理對等圖形</span><span class="sxs-lookup"><span data-stu-id="d32c8-114">Create and manage peer graphs</span></span>
-   <span data-ttu-id="d32c8-115">列舉對等圖形中的其他對等，並與之互動</span><span class="sxs-lookup"><span data-stu-id="d32c8-115">Enumerate and interact with other peers in a peer graph</span></span>
-   <span data-ttu-id="d32c8-116">以 a [記錄](records.md) 的形式將資料傳送至對等圖形中的每個節點</span><span class="sxs-lookup"><span data-stu-id="d32c8-116">Send data in the form of a [record](records.md) to each node in a peer graph</span></span>

## <a name="peer-grouping-api"></a><span data-ttu-id="d32c8-117">對等群組 API</span><span class="sxs-lookup"><span data-stu-id="d32c8-117">Peer Grouping API</span></span>

<span data-ttu-id="d32c8-118">[對等群組 API](grouping-api.md)結合和增強對等[PNRP](#pnrp-namespace-provider-api)和[圖形](#peer-graphing-api)api，並新增下列兩個元件：</span><span class="sxs-lookup"><span data-stu-id="d32c8-118">The [Peer Grouping API](grouping-api.md) combines and enhances the Peer [PNRP](#pnrp-namespace-provider-api) and [Graphing](#peer-graphing-api) APIs, and adds the following two components:</span></span>

-   <span data-ttu-id="d32c8-119">多工層，可讓一個對等實體上執行的多個應用程式連接到群組</span><span class="sxs-lookup"><span data-stu-id="d32c8-119">A multiplexing layer that allows multiple applications running on one peer entity to connect to a group</span></span>
-   <span data-ttu-id="d32c8-120">一種特定的安全性模型，可確保只有受邀加入群組的對等，才能在群組的存留期內連接到群組</span><span class="sxs-lookup"><span data-stu-id="d32c8-120">A specific security model that ensures only peers invited to a group can connect to the group through the lifetime of the group</span></span>

<span data-ttu-id="d32c8-121">您可以使用對等群組 API 來執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="d32c8-121">You can use the Peer Grouping API to do the following:</span></span>

-   <span data-ttu-id="d32c8-122">建立和管理安全對等群組</span><span class="sxs-lookup"><span data-stu-id="d32c8-122">Create and manage secure peer groups</span></span>
-   <span data-ttu-id="d32c8-123">列舉群組中的其他對等，並與之互動</span><span class="sxs-lookup"><span data-stu-id="d32c8-123">Enumerate and interact with other peers in a group</span></span>
-   <span data-ttu-id="d32c8-124">以 a [記錄](records.md) 的形式將資料傳送至對等群組中的每個節點</span><span class="sxs-lookup"><span data-stu-id="d32c8-124">Send data in the form of a [record](records.md) to each node in a peer group</span></span>

## <a name="peer-identity-manager-api"></a><span data-ttu-id="d32c8-125">對等身分識別管理員 API</span><span class="sxs-lookup"><span data-stu-id="d32c8-125">Peer Identity Manager API</span></span>

<span data-ttu-id="d32c8-126">您可以使用 [對等身分識別管理員 API](identity-manager-api.md) 建立安全的 [對等名稱](peer-names.md) ，以供 PNRP 用來確保發佈名稱的使用者正式擁有名稱。</span><span class="sxs-lookup"><span data-stu-id="d32c8-126">By using the [Peer Identity Manager API](identity-manager-api.md) you can create secure [peer names](peer-names.md) that PNRP can use to ensure that a person publishing a name officially owns the name.</span></span> <span data-ttu-id="d32c8-127">對等名稱也稱為身分識別，並會在對等群組 API 中用來識別群組中的個人。</span><span class="sxs-lookup"><span data-stu-id="d32c8-127">Peer names are also called identities, and they are used in the Peer Grouping API to identify the individuals in a group.</span></span>

<span data-ttu-id="d32c8-128">您可以使用 [對等身分識別管理員 API](identity-manager-api.md) 來執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="d32c8-128">You can use the [Peer Identity Manager API](identity-manager-api.md) to do the following:</span></span>

-   <span data-ttu-id="d32c8-129">建立、列舉和管理對等身分識別。</span><span class="sxs-lookup"><span data-stu-id="d32c8-129">Create, enumerate, and manage peer identities.</span></span>

## <a name="pnrp-namespace-provider-api"></a><span data-ttu-id="d32c8-130">PNRP 命名空間提供者 API</span><span class="sxs-lookup"><span data-stu-id="d32c8-130">PNRP Namespace Provider API</span></span>

<span data-ttu-id="d32c8-131">對等基礎結構提供無伺服器名稱解析技術，稱為 [PNRP 命名空間提供者 API](pnrp-namespace-provider-api.md)。</span><span class="sxs-lookup"><span data-stu-id="d32c8-131">The Peer Infrastructure provides a serverless name resolution technology called the [PNRP Namespace Provider API](pnrp-namespace-provider-api.md).</span></span> <span data-ttu-id="d32c8-132">藉由使用 Winsock 2 PNRP 命名空間提供者 API，對等、服務、計算裝置和對等群組端點可以管理、註冊、取消註冊和解析 PNRP [雲端](clouds.md)中的另一個端點。</span><span class="sxs-lookup"><span data-stu-id="d32c8-132">By using the Winsock 2 PNRP Namespace Provider API, a peer, service, computing device, and peer group endpoint can manage, register, unregister, and resolve another endpoint in a PNRP [cloud](clouds.md).</span></span>

> [!Note]  
> <span data-ttu-id="d32c8-133">PNRP 是 **對等名稱解析通訊協定** 的縮寫。</span><span class="sxs-lookup"><span data-stu-id="d32c8-133">PNRP is an acronym for **peer name resolution protocol**.</span></span>

 

 

 



