---
description: 對等網路是一種無伺服器的網路技術，可讓數個網路裝置共用資源，並直接彼此通訊。
ms.assetid: d2a43d3b-2782-4777-8c65-05e2c52930d0
title: 什麼是對等網路？
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c456fac9b7695a2846765ee0ccd38c1e5df646e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944272"
---
# <a name="what-is-peer-networking"></a><span data-ttu-id="bea55-103">什麼是對等網路？</span><span class="sxs-lookup"><span data-stu-id="bea55-103">What is Peer Networking?</span></span>

<span data-ttu-id="bea55-104">對等網路是一種無伺服器的網路技術，可讓數個網路裝置共用資源，並直接彼此通訊。</span><span class="sxs-lookup"><span data-stu-id="bea55-104">Peer-to-peer networking is a serverless networking technology that allows several network devices to share resources and communicate directly with each other.</span></span> <span data-ttu-id="bea55-105">這項技術適用于 Windows XP Service Pack 1 (SP1) 和更新版本的用戶端，這些用戶端會執行適用于對等基礎結構的 Advanced 網路套件。</span><span class="sxs-lookup"><span data-stu-id="bea55-105">This technology is available for Windows XP with Service Pack 1 (SP1) and later clients that run the Advanced Networking Pack for the Peer-to-Peer Infrastructure.</span></span>

<span data-ttu-id="bea55-106">對等基礎結構是一組網路 Api，可協助您開發使用網路上電腦之共同功能的非集中式網路應用程式。</span><span class="sxs-lookup"><span data-stu-id="bea55-106">The Peer-to-Peer Infrastructure is a set of networking APIs to help you develop decentralized networking applications that use the collective power of computers on a network.</span></span> <span data-ttu-id="bea55-107">例如，對等應用程式可以是共同作業通訊、內容發佈技術等等。</span><span class="sxs-lookup"><span data-stu-id="bea55-107">For example, peer-to-peer applications can be collaborative communications, content distribution technologies, and so on.</span></span>

<span data-ttu-id="bea55-108">對等基礎結構提供穩固的網路基礎結構，讓您可以專注于開發應用程式，因為基礎結構是為您而開發。</span><span class="sxs-lookup"><span data-stu-id="bea55-108">The Peer-to-Peer Infrastructure provides a solid networking infrastructure so that you can concentrate on developing applications, because the infrastructure is developed for you.</span></span>

<span data-ttu-id="bea55-109">對等基礎結構包含下列主要元件：</span><span class="sxs-lookup"><span data-stu-id="bea55-109">The Peer-to-Peer Infrastructure includes the following major components:</span></span>

-   [<span data-ttu-id="bea55-110">可擴充且安全的對等名稱解析</span><span class="sxs-lookup"><span data-stu-id="bea55-110">Scalable and secure peer name resolution</span></span>](#scalable-and-secure-peer-name-resolution)
-   [<span data-ttu-id="bea55-111">有效的 multipoint 通訊</span><span class="sxs-lookup"><span data-stu-id="bea55-111">Efficient multipoint communication</span></span>](#efficient-multipoint-communication)
-   [<span data-ttu-id="bea55-112">分散式資料管理</span><span class="sxs-lookup"><span data-stu-id="bea55-112">Distributed data management</span></span>](#distributed-data-management)
-   [<span data-ttu-id="bea55-113">安全對等身分識別</span><span class="sxs-lookup"><span data-stu-id="bea55-113">Secure peer identities</span></span>](#secure-peer-identities)
-   [<span data-ttu-id="bea55-114">安全對等群組</span><span class="sxs-lookup"><span data-stu-id="bea55-114">Secure Peer-to-Peer groups</span></span>](#secure-peer-to-peer-groups)

## <a name="scalable-and-secure-peer-name-resolution"></a><span data-ttu-id="bea55-115">可擴充且安全的對等名稱解析</span><span class="sxs-lookup"><span data-stu-id="bea55-115">Scalable and Secure Peer Name Resolution</span></span>

<span data-ttu-id="bea55-116">[對等名稱解析通訊協定 (PNRP) 命名空間提供者 API](pnrp-namespace-provider-api.md)是一種名稱對 IP 解析通訊協定。</span><span class="sxs-lookup"><span data-stu-id="bea55-116">The [Peer Name Resolution Protocol (PNRP) Namespace Provider API](pnrp-namespace-provider-api.md) is a name-to-IP resolution protocol.</span></span> <span data-ttu-id="bea55-117">包含所有參與對等的 IPv6 範圍或內容稱為 [雲端](clouds.md)。</span><span class="sxs-lookup"><span data-stu-id="bea55-117">The IPv6 scope or context that includes all participating peers is called a [cloud](clouds.md).</span></span> <span data-ttu-id="bea55-118">PNRP 可讓對等在雲端內彼此互動。</span><span class="sxs-lookup"><span data-stu-id="bea55-118">PNRP allows peers to interact with each other within a cloud.</span></span>

## <a name="efficient-multipoint-communication"></a><span data-ttu-id="bea55-119">有效的 Multipoint 通訊</span><span class="sxs-lookup"><span data-stu-id="bea55-119">Efficient Multipoint Communication</span></span>

<span data-ttu-id="bea55-120">對等基礎結構包含可提供有效 multipoint 通訊的 [圖形 API](graphing-api.md) 。</span><span class="sxs-lookup"><span data-stu-id="bea55-120">The Peer-to-Peer Infrastructure includes the [Graphing API](graphing-api.md) that provides efficient multipoint communication.</span></span> <span data-ttu-id="bea55-121">如同 PNRP，點對點圖形可讓一組節點進行互動，並以 [記錄](records.md)的形式互相傳遞資料。</span><span class="sxs-lookup"><span data-stu-id="bea55-121">Like PNRP, peer-to-peer graphing allows a set of nodes to interact, and pass data to and from each other in the form of a [record](records.md).</span></span> <span data-ttu-id="bea55-122">對等產生或更新的每一筆記錄都會傳送到圖形中的所有節點。</span><span class="sxs-lookup"><span data-stu-id="bea55-122">Each record that a peer generates or updates is sent to all nodes in a graph.</span></span>

## <a name="distributed-data-management"></a><span data-ttu-id="bea55-123">分散式資料管理</span><span class="sxs-lookup"><span data-stu-id="bea55-123">Distributed Data Management</span></span>

<span data-ttu-id="bea55-124">分散式資料管理會自動儲存所有傳送至對等圖形的記錄，直到每筆記錄的指定到期時間為止。</span><span class="sxs-lookup"><span data-stu-id="bea55-124">Distributed data management automatically stores all records sent to a peer-to-peer graph until the specified expiration time for each record.</span></span> <span data-ttu-id="bea55-125">對等網路可確保點對點圖形中的每個節點都具有記錄資料庫的類似觀點。</span><span class="sxs-lookup"><span data-stu-id="bea55-125">Peer-to-peer networking ensures that each node in a peer-to-peer graph has a similar view of the record database.</span></span> <span data-ttu-id="bea55-126">如果對等圖形具有與其相關聯的安全性模型，則圖形會包含下列資訊：</span><span class="sxs-lookup"><span data-stu-id="bea55-126">If a peer-to-peer graph has a security model associated with it, the graph contains the following information:</span></span>

-   <span data-ttu-id="bea55-127">誰可以和無法連接至圖形</span><span class="sxs-lookup"><span data-stu-id="bea55-127">Who can and cannot connect to a graph</span></span>
-   <span data-ttu-id="bea55-128">誰可以根據外部定義的準則來保護和驗證記錄</span><span class="sxs-lookup"><span data-stu-id="bea55-128">Who can secure and validate records based on externally defined criteria</span></span>

## <a name="secure-peer-identities"></a><span data-ttu-id="bea55-129">安全對等身分識別</span><span class="sxs-lookup"><span data-stu-id="bea55-129">Secure Peer Identities</span></span>

<span data-ttu-id="bea55-130">對等的基礎結構提供對等身分 [識別管理員 API](identity-manager-api.md) ，可讓您建立、管理和操作對等身分識別。</span><span class="sxs-lookup"><span data-stu-id="bea55-130">The Peer-to-Peer Infrastructure provides a Peer-to-Peer [Identity Manager API](identity-manager-api.md) that allows you to create, manage, and manipulate the peer identities.</span></span> <span data-ttu-id="bea55-131">對等身分識別是用來定義 PNRP 中安全端點的名稱，而且可以代表任何參與對等網路的資源，包括安全的對等群組和服務。</span><span class="sxs-lookup"><span data-stu-id="bea55-131">Peer identities are used to define names for secure endpoints in PNRP, and can represent any resource that participates in a peer-to-peer network, including secure peer-to-peer groups and services.</span></span>

## <a name="secure-peer-to-peer-groups"></a><span data-ttu-id="bea55-132">安全對等群組</span><span class="sxs-lookup"><span data-stu-id="bea55-132">Secure Peer-to-Peer Groups</span></span>

<span data-ttu-id="bea55-133">對等 [群組 API](grouping-api.md) 結合了對等圖形、Identity MANAGER 和 PNRP api，形成對等網路應用程式開發的一致且方便的解決方案。</span><span class="sxs-lookup"><span data-stu-id="bea55-133">The Peer-to-Peer [Grouping API](grouping-api.md) combines the Peer-to-Peer Graphing, Identity Manager, and PNRP APIs to form a cohesive and convenient solution for peer-to-peer networking application development.</span></span> <span data-ttu-id="bea55-134">點對點群組 API 會使用對等身分識別管理員 API 和自我簽署憑證配置，以確保圖形基礎結構內的安全性。</span><span class="sxs-lookup"><span data-stu-id="bea55-134">The Peer-to-Peer Grouping API uses the Peer-to-Peer Identity Manager API and a self-signed certificate scheme to ensure security within the graphing infrastructure.</span></span> <span data-ttu-id="bea55-135">您可以透過 PNRP 解析和註冊每個群組，以允許在註冊的點對點群組內進行隨機對等的名稱解析。</span><span class="sxs-lookup"><span data-stu-id="bea55-135">Each group can be resolved and registered through PNRP, which allows for the name resolution of random peers within a registered peer-to-peer group.</span></span> <span data-ttu-id="bea55-136">群組可以是 PNRP 中的端點，就像對等一樣。</span><span class="sxs-lookup"><span data-stu-id="bea55-136">A group can be an endpoint in PNRP, just like a peer.</span></span>

<span data-ttu-id="bea55-137">如需對等基礎結構的總覽，請參閱「[WINDOWS XP 對等網路簡介](https://www.microsoft.com/windowsxp/pro/techinfo/administration/p2p/introduction.asp)」一文。</span><span class="sxs-lookup"><span data-stu-id="bea55-137">For an overview of the Peer-to-Peer Infrastructure, see the article "[Introduction to Windows XP Peer-to-Peer Networking](https://www.microsoft.com/windowsxp/pro/techinfo/administration/p2p/introduction.asp)".</span></span>

<span data-ttu-id="bea55-138">如需對等基礎結構中的 Api 總覽，請參閱「 [什麼是對等基礎結構？](what-is-the-peer-infrastructure-.md)」主題。</span><span class="sxs-lookup"><span data-stu-id="bea55-138">For an overview of the APIs in the Peer-to-Peer Infrastructure, see the topic [What is the Peer Infrastructure?](what-is-the-peer-infrastructure-.md).</span></span>

 

 



