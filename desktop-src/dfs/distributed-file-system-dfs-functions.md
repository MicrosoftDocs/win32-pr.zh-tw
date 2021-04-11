---
title: 分散式檔案系統 (DFS) 函式
description: 分散式檔案系統 (DFS) 函式可讓您以邏輯方式將多部伺服器上的共用群組在一起，並以透明方式將共用連結至單一階層命名空間。 DFS 會在樹狀結構中組織網路上的共用資源。
ms.assetid: a29cde3e-483a-4658-94d4-27398f66abfb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73738d4f503d10e7668f0f323583f49604e3a90d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191002"
---
# <a name="distributed-file-system-dfs-functions"></a><span data-ttu-id="864cb-104">分散式檔案系統 (DFS) 函式</span><span class="sxs-lookup"><span data-stu-id="864cb-104">Distributed File System (DFS) Functions</span></span>

<span data-ttu-id="864cb-105">分散式檔案系統 (DFS) 函式可讓您以邏輯方式將多部伺服器上的共用群組在一起，並以透明方式將共用連結至單一階層命名空間。</span><span class="sxs-lookup"><span data-stu-id="864cb-105">The Distributed File System (DFS) functions provide the ability to logically group shares on multiple servers and to transparently link shares into a single hierarchical namespace.</span></span> <span data-ttu-id="864cb-106">DFS 會在樹狀結構中組織網路上的共用資源。</span><span class="sxs-lookup"><span data-stu-id="864cb-106">DFS organizes shared resources on a network in a treelike structure.</span></span>

<span data-ttu-id="864cb-107">DFS 支援 *獨立* DFS 命名空間、具有一部主機伺服器的網域，以及具有多部主機伺服器和高可用性的 *網域型* 命名空間。</span><span class="sxs-lookup"><span data-stu-id="864cb-107">DFS supports *stand-alone* DFS namespaces, those with one host server, and *domain-based* namespaces that have multiple host servers and high availability.</span></span> <span data-ttu-id="864cb-108">以網域為基礎的命名空間的 DFS *拓撲資料* 會儲存在 Active Directory 中。</span><span class="sxs-lookup"><span data-stu-id="864cb-108">The DFS *topology data* for domain-based namespaces is stored in Active Directory.</span></span> <span data-ttu-id="864cb-109">資料包含 DFS 根目錄、DFS 連結和 DFS 目標。</span><span class="sxs-lookup"><span data-stu-id="864cb-109">The data includes the DFS root, DFS links, and DFS targets.</span></span>

<span data-ttu-id="864cb-110">每個 DFS 樹狀結構都有一或多個 *根目標*。</span><span class="sxs-lookup"><span data-stu-id="864cb-110">Each DFS tree structure has one or more *root targets*.</span></span> <span data-ttu-id="864cb-111">根目標是執行 DFS 服務的主機伺服器。</span><span class="sxs-lookup"><span data-stu-id="864cb-111">The root target is a host server that runs the DFS service.</span></span> <span data-ttu-id="864cb-112">DFS 樹狀結構可以包含一或多個 *dfs 連結*。</span><span class="sxs-lookup"><span data-stu-id="864cb-112">A DFS tree structure can contain one or more *DFS links*.</span></span> <span data-ttu-id="864cb-113">每個 DFS 連結都會指向網路上的一個或多個共用資料夾。</span><span class="sxs-lookup"><span data-stu-id="864cb-113">Each DFS link points to one or more shared folders on the network.</span></span> <span data-ttu-id="864cb-114">您可以新增、修改和刪除 DFS 命名空間的 DFS 連結。</span><span class="sxs-lookup"><span data-stu-id="864cb-114">You can add, modify and delete DFS links from a DFS namespace.</span></span> <span data-ttu-id="864cb-115">當您移除與 DFS 連結相關聯的最後一個目標時，DFS 會刪除 DFS 命名空間中的 DFS 連結。</span><span class="sxs-lookup"><span data-stu-id="864cb-115">When you remove the last target associated with a DFS link, DFS deletes the DFS link in the DFS namespace.</span></span> <span data-ttu-id="864cb-116"> (在先前的檔中，DFS 連結稱為連接點。 ) </span><span class="sxs-lookup"><span data-stu-id="864cb-116">(In earlier documentation, DFS links were called junction points.)</span></span>

<span data-ttu-id="864cb-117">DFS 連結可以指向一或多個共用資料夾;這些資料夾稱為 *目標*。</span><span class="sxs-lookup"><span data-stu-id="864cb-117">A DFS link can point to one or more shared folders; the folders are called *targets*.</span></span> <span data-ttu-id="864cb-118">當使用者存取 DFS 連結時，DFS 伺服器會根據用戶端的網站資訊來選取一組目標。</span><span class="sxs-lookup"><span data-stu-id="864cb-118">When users access a DFS link, the DFS server selects a set of targets based on a client's site information.</span></span> <span data-ttu-id="864cb-119">用戶端會存取集合中第一個可用的目標。</span><span class="sxs-lookup"><span data-stu-id="864cb-119">The client accesses the first available target in the set.</span></span> <span data-ttu-id="864cb-120">這有助於將用戶端要求分散到可能的目標，並可為使用者提供持續的可存取性，即使某些伺服器失敗亦同。</span><span class="sxs-lookup"><span data-stu-id="864cb-120">This helps to distribute client requests across the possible targets and can provide continued accessibility for users even when some servers fail.</span></span>

<span data-ttu-id="864cb-121">應用程式可以使用 DFS 功能來：</span><span class="sxs-lookup"><span data-stu-id="864cb-121">An application can use the DFS functions to:</span></span>

- <span data-ttu-id="864cb-122">新增 dfs 根目錄的 DFS 連結。</span><span class="sxs-lookup"><span data-stu-id="864cb-122">Add a DFS link to a DFS root.</span></span>
- <span data-ttu-id="864cb-123">建立或移除獨立和網域型 DFS 命名空間。</span><span class="sxs-lookup"><span data-stu-id="864cb-123">Create or remove stand-alone and domain-based DFS namespaces.</span></span>
- <span data-ttu-id="864cb-124">將目標新增至現有的 DFS 連結。</span><span class="sxs-lookup"><span data-stu-id="864cb-124">Add targets to an existing DFS link.</span></span>
- <span data-ttu-id="864cb-125">從 DFS 根目錄移除 DFS 連結。</span><span class="sxs-lookup"><span data-stu-id="864cb-125">Remove a DFS link from a DFS root.</span></span>
- <span data-ttu-id="864cb-126">從 DFS 連結移除目標。</span><span class="sxs-lookup"><span data-stu-id="864cb-126">Remove a target from a DFS link.</span></span>
- <span data-ttu-id="864cb-127">查看及設定 DFS 根目錄和連結的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="864cb-127">View and configure information about DFS roots and links.</span></span>

<span data-ttu-id="864cb-128">如需 DFS 函式的清單，請參閱 [分散式檔案系統](distributed-file-system-functions.md)函式。</span><span class="sxs-lookup"><span data-stu-id="864cb-128">For a list of the DFS functions, see [Distributed File System Functions](distributed-file-system-functions.md).</span></span>

<span data-ttu-id="864cb-129">如需 DFS 結構的清單，請參閱 [分散式檔案系統結構](distributed-file-system-structures.md)。</span><span class="sxs-lookup"><span data-stu-id="864cb-129">For a list of the DFS structures, see [Distributed File System Structures](distributed-file-system-structures.md).</span></span>

<span data-ttu-id="864cb-130">在執行 Microsoft Windows 的電腦上，您可以在 DFS 命名空間中發佈目標。</span><span class="sxs-lookup"><span data-stu-id="864cb-130">Targets on computers that are running Microsoft Windows can be published in a DFS namespace.</span></span> <span data-ttu-id="864cb-131">您也可以發佈任何可在 DFS 命名空間中使用用戶端重新導向程式的非 Microsoft 共用。</span><span class="sxs-lookup"><span data-stu-id="864cb-131">You can also publish any non-Microsoft shares for which client redirectors are available in a DFS namespace.</span></span> <span data-ttu-id="864cb-132">但是，不同于在執行 Windows Server 的伺服器上發佈的共用，它們無法裝載 DFS 根目錄或提供其他 DFS 目標的參考。</span><span class="sxs-lookup"><span data-stu-id="864cb-132">However, unlike a share that is published on a server that is running Windows Server, they cannot host a DFS root or provide referrals to other DFS targets.</span></span>

<span data-ttu-id="864cb-133">DFS 使用 Windows Server 檔案複寫服務複製複寫目標之間的變更。</span><span class="sxs-lookup"><span data-stu-id="864cb-133">DFS uses the Windows Server file replication service to copy changes between replicated targets.</span></span> <span data-ttu-id="864cb-134">使用者可以修改儲存在某個目標上的檔案，而且檔案複寫服務會將變更傳播到其他指定的目標。</span><span class="sxs-lookup"><span data-stu-id="864cb-134">Users can modify files stored on one target, and the file replication service propagates the changes to the other designated targets.</span></span> <span data-ttu-id="864cb-135">服務會保留檔或檔案的最新變更。</span><span class="sxs-lookup"><span data-stu-id="864cb-135">The service preserves the most recent change to a document or files.</span></span>
