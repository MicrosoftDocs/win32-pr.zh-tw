---
title: DFS 伺服器目標優先順序
description: DFS 伺服器目標優先順序是 Microsoft Windows Server 2003 Service Pack 1 (SP1) 和更新版本作業系統中提供的功能。
ms.assetid: 0aacebf7-49cc-4287-a5c4-0d25a416d227
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e784a540a67f624ca5b8075009cd862c6063427
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191022"
---
# <a name="dfs-server-target-prioritization"></a><span data-ttu-id="7fba5-103">DFS 伺服器目標優先順序</span><span class="sxs-lookup"><span data-stu-id="7fba5-103">DFS Server Target Prioritization</span></span>

<span data-ttu-id="7fba5-104">DFS 伺服器目標優先順序是 Microsoft Windows Server 2003 Service Pack 1 (SP1) 和更新版本作業系統中提供的功能。</span><span class="sxs-lookup"><span data-stu-id="7fba5-104">DFS Server Target Prioritization is a feature available in Microsoft Windows Server 2003 with Service Pack 1 (SP1) and later operating systems.</span></span> <span data-ttu-id="7fba5-105">這項功能可讓 DFS 伺服器充分利用可用的 Active Directory 網站成本資訊，以優先處理用戶端參考中的目標。</span><span class="sxs-lookup"><span data-stu-id="7fba5-105">This feature enables DFS servers to take advantage of available Active Directory site-cost information to prioritize the targets in client referrals.</span></span>

<span data-ttu-id="7fba5-106">在 Windows Server 2003 SP1 之前，目標已分為兩個集合：一個群組，其中包含與用戶端位於相同網站中的所有目標;另一個群組用於所有其他目標。</span><span class="sxs-lookup"><span data-stu-id="7fba5-106">Before Windows Server 2003 with SP1, targets were grouped into two sets: one group for containing all targets in the same site as the client; and another group for all other targets.</span></span> <span data-ttu-id="7fba5-107">與用戶端共用相同網站的目標稱為「現場」，如果已啟用網站成本，則會為其指派相對於整個網站的特定成本值，而較高的網站成本則優先。</span><span class="sxs-lookup"><span data-stu-id="7fba5-107">Those targets sharing the same site as the client are called "in-site", and if site-costing is enabled, they are assigned a specific cost value relative to the site overall, with lower site costs preferred over higher ones.</span></span>

<span data-ttu-id="7fba5-108">有了此網站成本資料的可用性，就能優先使用伺服器目標，以取得更有效率的 DFS 伺服器容錯移轉策略。</span><span class="sxs-lookup"><span data-stu-id="7fba5-108">With the availability of this site-costing data, server targets can be prioritized for more effective DFS server failover strategies.</span></span> <span data-ttu-id="7fba5-109">在過去，您無法使用此細微層級的詳細資料，而且系統管理員必須將 (例如 AD) 中的虛擬網站，以支援像是在「主要」 DFS 伺服器失敗時，將特定伺服器指定為「備份」或「次要」伺服器的簡單需求。</span><span class="sxs-lookup"><span data-stu-id="7fba5-109">In the past, this granular level of detail was not available, and administrators had to resort to artificial means (such as dummy sites in AD) to support even simple requirements like the designation of specific servers as a "backup" or "secondary" server in the case where a "primary" DFS server fails.</span></span> <span data-ttu-id="7fba5-110">現在，透過網站成本提供的額外詳細資料，可能會有多層級的容錯移轉策略。</span><span class="sxs-lookup"><span data-stu-id="7fba5-110">Now, with the additional detail provided by site-costing, multi-level failover strategies are possible.</span></span>

<span data-ttu-id="7fba5-111">下列討論假設已啟用網站成本。</span><span class="sxs-lookup"><span data-stu-id="7fba5-111">The following discussion assumes that site-costing is enabled.</span></span>

## <a name="target-prioritization"></a><span data-ttu-id="7fba5-112">目標優先順序</span><span class="sxs-lookup"><span data-stu-id="7fba5-112">Target Prioritization</span></span>

<span data-ttu-id="7fba5-113">目標優先順序是從系統管理的觀點來看，根據其在 DFS 用戶端的網站成本來明確喜好設定，來分類及排名站內伺服器。</span><span class="sxs-lookup"><span data-stu-id="7fba5-113">Target priority is a specific ordering from an administrative perspective, classifying and ranking in-site servers in terms of explicit preference based on their site cost from a DFS client.</span></span> <span data-ttu-id="7fba5-114">全域優先順序與網站成本無關。</span><span class="sxs-lookup"><span data-stu-id="7fba5-114">Global priority is independent of the site-cost.</span></span> <span data-ttu-id="7fba5-115">請注意，全域優先順序類別並不一定會從 DFS 用戶端的觀點來指出最適合的目標，而是從網站管理員的觀點來反映特定目標的重要性（或缺乏重要性）。</span><span class="sxs-lookup"><span data-stu-id="7fba5-115">Note that global priority classes do not necessarily indicate the most optimal targets from a DFS client's perspective, but instead reflect the importance, or lack of importance, of specific targets from a site administrator's perspective.</span></span>

<span data-ttu-id="7fba5-116">伺服器目標優先順序分為兩個值類別：優先順序類別和優先權等級。</span><span class="sxs-lookup"><span data-stu-id="7fba5-116">Server target priority is divided into two value categories: priority class and priority rank.</span></span> <span data-ttu-id="7fba5-117">優先順序類別分為兩個層級：本機和全域。</span><span class="sxs-lookup"><span data-stu-id="7fba5-117">Priority classes are divided into two levels: local and global.</span></span> <span data-ttu-id="7fba5-118">在這些類別中，會根據網站成本（群組為高、標準和低優先順序）來建立目標的粗略排序。</span><span class="sxs-lookup"><span data-stu-id="7fba5-118">Within these classes there is a rough ordering of targets based on site cost, grouped as high, normal, and low priority.</span></span> <span data-ttu-id="7fba5-119">結果是五個優先權類別，從最高到最低優先順序，如下所示：</span><span class="sxs-lookup"><span data-stu-id="7fba5-119">The result is five priority classes, in order from highest to lowest priority as follows:</span></span>

- <span data-ttu-id="7fba5-120">全域高優先順序</span><span class="sxs-lookup"><span data-stu-id="7fba5-120">Global high priority</span></span>
- <span data-ttu-id="7fba5-121">網站-成本高優先順序</span><span class="sxs-lookup"><span data-stu-id="7fba5-121">Site-cost high priority</span></span>
- <span data-ttu-id="7fba5-122">網站-成本正常優先順序</span><span class="sxs-lookup"><span data-stu-id="7fba5-122">Site-cost normal priority</span></span>
- <span data-ttu-id="7fba5-123">網站-成本低優先順序</span><span class="sxs-lookup"><span data-stu-id="7fba5-123">Site-cost low priority</span></span>
- <span data-ttu-id="7fba5-124">全域低優先順序</span><span class="sxs-lookup"><span data-stu-id="7fba5-124">Global low priority</span></span>

<span data-ttu-id="7fba5-125">網站成本類別可以視為「全域一般優先順序」的細分。</span><span class="sxs-lookup"><span data-stu-id="7fba5-125">The site-cost classes can be considered as subdivisions of "global normal priority".</span></span> <span data-ttu-id="7fba5-126">優先權排名是根據序數值的簡單整數排名：0、1、2和之後，0是最大值，而所有後續值則表示遞減排名。</span><span class="sxs-lookup"><span data-stu-id="7fba5-126">Priority rank is a simple integer ranking based on ordinal values: 0, 1, 2, and onward, with 0 being the highest value and all subsequent values indicating decreasing rank.</span></span>

<span data-ttu-id="7fba5-127">全域高和低優先順序不會考慮網站成本值。</span><span class="sxs-lookup"><span data-stu-id="7fba5-127">The global high and low priorities do not consider site-cost values.</span></span> <span data-ttu-id="7fba5-128">在所有其他目標上具有全域高優先順序接收喜好設定的目標，而具有全域低優先順序的目標則會收到最少的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="7fba5-128">Targets with a global high priority receive preference over all other targets, and targets with a global low priority receive the least preference.</span></span>

<span data-ttu-id="7fba5-129">在訂購參考時，完整的程式有下列步驟：</span><span class="sxs-lookup"><span data-stu-id="7fba5-129">In ordering a referral, the complete process has the following steps:</span></span>

1. <span data-ttu-id="7fba5-130">系統會識別全域高和低目標的集合，以及剩餘的「全域一般」目標。</span><span class="sxs-lookup"><span data-stu-id="7fba5-130">The sets of global high and low targets are identified, along with the remaining "global normal" targets.</span></span>
2. <span data-ttu-id="7fba5-131">如果設定了 "INSITE" 選項，就會移除用戶端網站以外的所有目標。</span><span class="sxs-lookup"><span data-stu-id="7fba5-131">If the "INSITE" option is set, all targets outside of the client's site are removed.</span></span> <span data-ttu-id="7fba5-132">"INSITE" 選項不會套用至全域高和低優先順序的集合。</span><span class="sxs-lookup"><span data-stu-id="7fba5-132">The "INSITE" option is not applied to the global high and low priority sets.</span></span>
3. <span data-ttu-id="7fba5-133">在這三個集合中，系統會使用本機或完整網站成本，以 AD 網站成本機制來排序目標。</span><span class="sxs-lookup"><span data-stu-id="7fba5-133">Within each of these three sets, the targets are ordered using the AD site-cost mechanism, using either local or full site costing.</span></span> <span data-ttu-id="7fba5-134">結果是相等網站成本的設定目標。</span><span class="sxs-lookup"><span data-stu-id="7fba5-134">The result is sets of targets of equal site cost.</span></span>
4. <span data-ttu-id="7fba5-135">在相等網站成本的「全域標準」目標集內，目標是從「網站成本高」、「一般」和「低優先順序」排名指派優先順序類別。</span><span class="sxs-lookup"><span data-stu-id="7fba5-135">Within the sets of "global normal" targets of equal site cost, targets are assigned a priority class from the site-cost high, normal, and low priority rankings.</span></span>
5. <span data-ttu-id="7fba5-136">在相等的網站成本和優先順序類別的目標集合中，目標現在依優先順序排名排序，0是最高等級。</span><span class="sxs-lookup"><span data-stu-id="7fba5-136">Within the sets of targets of equal site cost and priority class, targets are now ordered by priority rank, with 0 being the highest rank.</span></span>
6. <span data-ttu-id="7fba5-137">在相等網站成本、優先順序類別和優先順序等級的目標集合中，目標會隨機隨機隨機設定以進行負載平衡。</span><span class="sxs-lookup"><span data-stu-id="7fba5-137">Within the sets of targets of equal site cost, priority class, and priority rank, targets are randomly shuffled for load balancing.</span></span>

<span data-ttu-id="7fba5-138">以圖形方式，一組目標的排序方式如下所示：</span><span class="sxs-lookup"><span data-stu-id="7fba5-138">Graphically, a set of targets are ordered as seen below:</span></span>

- <span data-ttu-id="7fba5-139">全域高優先順序類別目標</span><span class="sxs-lookup"><span data-stu-id="7fba5-139">global high priority class targets</span></span> 
- <span data-ttu-id="7fba5-140">site cost 高優先順序類別目標，網站成本 = 0</span><span class="sxs-lookup"><span data-stu-id="7fba5-140">site-cost high priority class targets with site cost = 0</span></span>
- <span data-ttu-id="7fba5-141">具有 site cost 的一般 = 0</span><span class="sxs-lookup"><span data-stu-id="7fba5-141">normal with site cost = 0</span></span>
- <span data-ttu-id="7fba5-142">低（含網站成本 = 0）</span><span class="sxs-lookup"><span data-stu-id="7fba5-142">low with site cost = 0</span></span>
- <span data-ttu-id="7fba5-143">site cost 高優先順序類別目標，網站成本 = 1</span><span class="sxs-lookup"><span data-stu-id="7fba5-143">site-cost high priority class targets with site cost = 1</span></span>
- <span data-ttu-id="7fba5-144">具有 site cost 的一般 = 1</span><span class="sxs-lookup"><span data-stu-id="7fba5-144">normal with site cost = 1</span></span>
- <span data-ttu-id="7fba5-145">低和網站成本 = 1</span><span class="sxs-lookup"><span data-stu-id="7fba5-145">low with site cost = 1</span></span>
- <span data-ttu-id="7fba5-146">依此類推</span><span class="sxs-lookup"><span data-stu-id="7fba5-146">and so on</span></span>
- <span data-ttu-id="7fba5-147">全域低優先順序類別目標</span><span class="sxs-lookup"><span data-stu-id="7fba5-147">global low priority class targets</span></span>

<span data-ttu-id="7fba5-148">在上述每個集合中，目標會根據優先順序排名來排序。</span><span class="sxs-lookup"><span data-stu-id="7fba5-148">Within each of these sets, targets are sorted according to priority rank.</span></span> <span data-ttu-id="7fba5-149">最高等級為零，每個後續的整數值 (1，2，依此類推，) 指出逐漸降低的等級。</span><span class="sxs-lookup"><span data-stu-id="7fba5-149">The highest rank is zero, with each subsequent integer value (1, 2, and so on) indicating an increasingly lower rank.</span></span>

<span data-ttu-id="7fba5-150">目標優先順序是在 (的連結或 DFS 命名空間中的根) 的特定目標上設定的。</span><span class="sxs-lookup"><span data-stu-id="7fba5-150">Target priority is set on a specific target of a link (or root) in a DFS namespace.</span></span> <span data-ttu-id="7fba5-151">如果使用相同的目標路徑多次，則某個連結的目標優先順序不會影響其他連結的順序。</span><span class="sxs-lookup"><span data-stu-id="7fba5-151">A target's priority for one link does not influence the ordering of other links if that same target path is used multiple times.</span></span> <span data-ttu-id="7fba5-152">例如，如果有兩個連結的 \\ \\ 伺服器 \\ >\fileserver1\share1\ 做為目標，則 \\ \\ 會為 \\ 這兩個連結分別設定伺服器 >\fileserver1\share1\ 的優先順序。</span><span class="sxs-lookup"><span data-stu-id="7fba5-152">For example, if two links have \\\\server\\share1 as a target, the priority of \\\\server\\share1 is set separately for both links.</span></span>

<span data-ttu-id="7fba5-153">所有連結的預設優先順序是網站成本的一般優先權，其排名為0。</span><span class="sxs-lookup"><span data-stu-id="7fba5-153">The default priority for all links is the site-cost normal priority with a rank of 0.</span></span> <span data-ttu-id="7fba5-154">目標優先順序不會影響參考的順序，除非使用它，而且所有現有的連結都會依收到的順序排序。</span><span class="sxs-lookup"><span data-stu-id="7fba5-154">Target priority does not affect the ordering of referrals unless it is used, and all existing links are ordered as they are received.</span></span>

<span data-ttu-id="7fba5-155">來自 DFS 伺服器的推薦回應包含依上述順序排序的目標集，其中每個非全域目標集都包含相同網站成本、優先順序類別和優先順序等級的目標。</span><span class="sxs-lookup"><span data-stu-id="7fba5-155">The referral response from a DFS server consists of target sets ordered as indicated above, with each non-global target set containing targets of the same site cost, priority class, and priority rank.</span></span> <span data-ttu-id="7fba5-156">每個集合內的目標會隨機排序。</span><span class="sxs-lookup"><span data-stu-id="7fba5-156">Targets within each set are ordered randomly.</span></span> <span data-ttu-id="7fba5-157">接收參照的 DFS 用戶端會從第一個集合的第一個目標開始，並繼續執行清單，直到找到指定 DFS 根目錄或連結的可用目標為止。</span><span class="sxs-lookup"><span data-stu-id="7fba5-157">DFS clients that receive the referral start with the first target of the first set, and continue through the list until an available target for a given DFS root or link is found.</span></span>

<span data-ttu-id="7fba5-158">如需此功能的特定 API 執行，請參閱下列參考主題：</span><span class="sxs-lookup"><span data-stu-id="7fba5-158">For the specific API implementation of this feature, please see the following reference topics:</span></span>

<span data-ttu-id="7fba5-159">[**DFS_INFO_6**](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_6) 
[**DFS_INFO_104**](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_104) 
[**DFS_INFO_106**](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_106) 
[**DFS_TARGET_PRIORITY**](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_target_priority) 
[**DFS_TARGET_PRIORITY_CLASS**](/windows/win32/api/lmdfs/ne-lmdfs-dfs_target_priority_class~r1)</span><span class="sxs-lookup"><span data-stu-id="7fba5-159">[**DFS_INFO_6**](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_6)
[**DFS_INFO_104**](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_104)
[**DFS_INFO_106**](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_106)
[**DFS_TARGET_PRIORITY**](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_target_priority)
[**DFS_TARGET_PRIORITY_CLASS**](/windows/win32/api/lmdfs/ne-lmdfs-dfs_target_priority_class~r1)</span></span>
