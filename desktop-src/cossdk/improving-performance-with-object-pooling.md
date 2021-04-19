---
description: 使用物件共用改善效能
ms.assetid: 7a8a38d8-6549-4686-a298-f3b427b380e3
title: 使用物件共用改善效能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 398b9140080d3a439293b5152b4da7251978e800
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973584"
---
# <a name="improving-performance-with-object-pooling"></a><span data-ttu-id="95533-103">使用物件共用改善效能</span><span class="sxs-lookup"><span data-stu-id="95533-103">Improving Performance with Object Pooling</span></span>

<span data-ttu-id="95533-104">在特定情況下，物件共用可能會非常有效，並大幅提升效能。</span><span class="sxs-lookup"><span data-stu-id="95533-104">Object pooling can be extremely effective in certain circumstances, yielding substantial increases in performance.</span></span> <span data-ttu-id="95533-105">重複使用物件以發揮最大效益的一般概念，是盡可能將最多的資源集區、從實際執行的工作中分解出來，然後在部署時將集區特性自訂為實際硬體。</span><span class="sxs-lookup"><span data-stu-id="95533-105">The general idea for reusing objects to best advantage is to pool as many resources as possible, factoring out initialization from actual work performed, and then to administratively tailor the pool characteristics to actual hardware at deployment time.</span></span> <span data-ttu-id="95533-106">也就是說，您應該依照下列步驟進行：</span><span class="sxs-lookup"><span data-stu-id="95533-106">That is, you should proceed according to the following steps:</span></span>

1.  <span data-ttu-id="95533-107">撰寫物件，以便將針對任何用戶端所執行的昂貴初始化和資源取得納入考慮，以代表用戶端執行實際工作的先決條件。</span><span class="sxs-lookup"><span data-stu-id="95533-107">Write the object so as to factor out expensive initialization and resource acquisition that is performed for any client as a prerequisite to doing actual work on the client's behalf.</span></span> <span data-ttu-id="95533-108">寫入大量物件的函式，盡可能將這些資源集區化，以供物件保存，並在用戶端從集區取得物件時立即可用。</span><span class="sxs-lookup"><span data-stu-id="95533-108">Write heavy object constructors to pool as many resources as possible so that these are held by the object and immediately available when clients get an object from the pool.</span></span>
2.  <span data-ttu-id="95533-109">系統管理員設定集區以達到可用硬體資源的最佳平衡，通常會在 exchange 中交易維護特定大小集區的記憶體，以加快用戶端存取及使用物件的速度。</span><span class="sxs-lookup"><span data-stu-id="95533-109">Administratively configure the pool to achieve the best balance in available hardware resources, usually trading the memory dedicated to maintaining a pool of a certain size in exchange for faster client access and use of objects.</span></span> <span data-ttu-id="95533-110">在某個時間點，共用將會達到較低的報酬率，而且您可以獲得足夠的效能，同時限制特定元件可能的資源使用量。</span><span class="sxs-lookup"><span data-stu-id="95533-110">At a certain point, pooling will achieve diminishing returns and you can get good enough performance while limiting possible resource usage by a particular component.</span></span>

## <a name="doing-actual-work-or-acquiring-resources"></a><span data-ttu-id="95533-111">執行實際工作或取得資源</span><span class="sxs-lookup"><span data-stu-id="95533-111">Doing Actual Work or Acquiring Resources</span></span>

<span data-ttu-id="95533-112">如果您有一個元件，讓用戶端在執行用戶端的特定工作之前，很快就會使用部分的物件使用時間來取得資源或初始化，則撰寫您的元件以使用物件共用會是很大的好處。</span><span class="sxs-lookup"><span data-stu-id="95533-112">If you have a component that clients will use briefly and in rapid succession, where a significant portion of object use time is spent in acquiring resources or initializing prior to doing specific work for the client, chances are that writing your component to use object pooling will be a big win for you.</span></span>

<span data-ttu-id="95533-113">您可以撰寫元件，讓在物件的函式中執行的工作，就像是所有用戶端都可以一致的耗時工作一樣-取得一或多個連線、執行腳本、從檔案或透過網路提取初始化資料等等。</span><span class="sxs-lookup"><span data-stu-id="95533-113">You can write the component so that in the object's constructor you perform as much of the time-consuming work that is uniform for all clients as possible—acquiring one or several connections, running scripts, fetching initialization data from files or across a network, and so forth.</span></span> <span data-ttu-id="95533-114">這具有共用每個這類資源的效果。</span><span class="sxs-lookup"><span data-stu-id="95533-114">This has the effect of pooling every such resource.</span></span> <span data-ttu-id="95533-115">您會將資源的組合和執行某些工作所需的一般狀態集中在一起。</span><span class="sxs-lookup"><span data-stu-id="95533-115">You are pooling the combination of resources and generic state necessary to perform some work.</span></span>

<span data-ttu-id="95533-116">在此情況下，當用戶端從集區取得物件時，這些資源會立即可用。</span><span class="sxs-lookup"><span data-stu-id="95533-116">In this circumstance, when clients get an object from the pool, they have those resources immediately available.</span></span> <span data-ttu-id="95533-117">通常，它們會使用物件來執行一些小型工作單位，推送或提取資料，然後物件將呼叫 [**IObjectCoNtext：： SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) 或 [**IObjectCoNtext：： SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) 並傳回。</span><span class="sxs-lookup"><span data-stu-id="95533-117">Typically, they will use the object to do some small unit of work, pushing or pulling data, and then the object will call [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) or [**IObjectContext::SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) and return.</span></span> <span data-ttu-id="95533-118">使用像這樣的快速火災使用模式，就會產生絕佳的效能優勢。</span><span class="sxs-lookup"><span data-stu-id="95533-118">With rapid-fire use patterns such as this, pooling yields excellent performance benefits.</span></span> <span data-ttu-id="95533-119">您可以充分運用無狀態自動交易程式設計模型的簡易性，但可達成與傳統具狀態元件相同的效能。</span><span class="sxs-lookup"><span data-stu-id="95533-119">You can fully leverage the simplicity of the stateless automatic transaction programming model yet achieve performance on par with traditional stateful components.</span></span>

<span data-ttu-id="95533-120">但是，如果用戶端在每次呼叫時都使用物件一段很長的時間，共用就比較不合理。</span><span class="sxs-lookup"><span data-stu-id="95533-120">However, if clients use an object for a long time each time they call it, pooling will make less sense.</span></span> <span data-ttu-id="95533-121">您所獲得的速度優勢，會因為相對於初始化時間的使用時間增加而變得很低。</span><span class="sxs-lookup"><span data-stu-id="95533-121">The speed advantage that you gain is marginal as use time increases relative to initialization time.</span></span> <span data-ttu-id="95533-122">您會取得降低的傳回，這可能不會證明保留使用中物件集區所需的記憶體成本。</span><span class="sxs-lookup"><span data-stu-id="95533-122">You get diminishing returns that may not justify the cost of the memory necessary to hold a pool of active objects.</span></span>

## <a name="sharing-cost-across-multiple-clients"></a><span data-ttu-id="95533-123">跨多個用戶端共用成本</span><span class="sxs-lookup"><span data-stu-id="95533-123">Sharing Cost Across Multiple Clients</span></span>

<span data-ttu-id="95533-124">分解初始化的變化是，您可以使用共用以統計方式分攤取得昂貴資源的成本。</span><span class="sxs-lookup"><span data-stu-id="95533-124">A variation on factoring out initialization is that you can use pooling to statistically amortize the cost of acquiring expensive resources.</span></span> <span data-ttu-id="95533-125">如果您取得取得或初始化一次，然後重複使用物件，則會在其存留期內，于使用物件的所有用戶端之間共用該成本。</span><span class="sxs-lookup"><span data-stu-id="95533-125">If you take the hit of acquisition or initialization once and then reuse the object, you share that cost across all clients that use the object during its lifetime.</span></span> <span data-ttu-id="95533-126">每個物件只會產生一次繁重的結構時間。</span><span class="sxs-lookup"><span data-stu-id="95533-126">Heavy construction time is incurred only once per object.</span></span>

## <a name="preallocating-objects"></a><span data-ttu-id="95533-127">預先設定物件</span><span class="sxs-lookup"><span data-stu-id="95533-127">Preallocating Objects</span></span>

<span data-ttu-id="95533-128">如果您指定非零的最小集區大小，則會在應用程式啟動時建立並共用物件的最小數目，並準備好供任何呼叫應用程式的用戶端使用。</span><span class="sxs-lookup"><span data-stu-id="95533-128">If you specify a nonzero minimum pool size, that minimum number of objects will be created and pooled when the application starts, ready for any clients that call in to the application.</span></span>

## <a name="governing-resource-use-with-pool-management"></a><span data-ttu-id="95533-129">使用集區管理管理資源使用</span><span class="sxs-lookup"><span data-stu-id="95533-129">Governing Resource Use with Pool Management</span></span>

<span data-ttu-id="95533-130">您可以使用最大集區大小，以精確地管理資源的使用方式。</span><span class="sxs-lookup"><span data-stu-id="95533-130">You can use the maximum pool size to govern very precisely how you use resources.</span></span> <span data-ttu-id="95533-131">例如，如果您已授權特定數目的資料庫連接，您可以控制隨時開啟的連接數目。</span><span class="sxs-lookup"><span data-stu-id="95533-131">For example, if you have licensed a certain number of database connections, you can control how many connections you have open at any time.</span></span>

<span data-ttu-id="95533-132">當您將用戶端使用模式、物件使用特性以及實體資源（例如記憶體和連接）納入考慮時，您可能會在進行效能調整時找到一些最佳的平衡點。</span><span class="sxs-lookup"><span data-stu-id="95533-132">When you take into consideration client use patterns, object use characteristics, and physical resources such as memory and connections, you are likely to find some optimal balance point when you do performance tuning.</span></span> <span data-ttu-id="95533-133">在某個時間點之後，共用物件將會產生較低的傳回。</span><span class="sxs-lookup"><span data-stu-id="95533-133">Pooling objects will yield diminishing returns after a certain point.</span></span> <span data-ttu-id="95533-134">您可以判斷所需的效能層級，並根據所需的資源進行平衡。</span><span class="sxs-lookup"><span data-stu-id="95533-134">You can determine what level of performance you require and balance that against what resources are necessary to achieve it.</span></span>

<span data-ttu-id="95533-135">若要在設定物件共用時簡化效能調整，您可以監視應用程式中元件的物件統計資料。</span><span class="sxs-lookup"><span data-stu-id="95533-135">To facilitate performance tuning when you configure object pooling, you can monitor object statistics for the components in an application.</span></span> <span data-ttu-id="95533-136">如需詳細資訊，請參閱 [監視物件統計資料](monitoring-object-statistics.md)。</span><span class="sxs-lookup"><span data-stu-id="95533-136">For details, see [Monitoring Object Statistics](monitoring-object-statistics.md).</span></span>

## <a name="improve-performance-of-jit-activated-components"></a><span data-ttu-id="95533-137">改善 JIT-Activated 元件的效能</span><span class="sxs-lookup"><span data-stu-id="95533-137">Improve Performance of JIT-Activated Components</span></span>

<span data-ttu-id="95533-138">物件共用與 [Com + 即時啟用](com--just-in-time-activation.md) 服務非常適合。</span><span class="sxs-lookup"><span data-stu-id="95533-138">Object pooling works very well with the [COM+ just-in-time activation](com--just-in-time-activation.md) service.</span></span> <span data-ttu-id="95533-139">藉由共用正在 JIT 啟動的物件，您可以加快物件重新啟用的速度。</span><span class="sxs-lookup"><span data-stu-id="95533-139">By pooling objects that are being JIT-activated, you can speed object reactivation.</span></span> <span data-ttu-id="95533-140">您可以透過 JIT 啟用將通道保持開啟狀態的優點，同時減輕重新開機的成本。</span><span class="sxs-lookup"><span data-stu-id="95533-140">You get the benefits of holding the channel open by JIT activation while mitigating the cost of reactivation.</span></span> <span data-ttu-id="95533-141">在此情況下，您可以使用共用來管理要配置給有作用中之物件的記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="95533-141">You can use pooling in this case to govern how much memory you wish to allocate to objects that have references active.</span></span>

<span data-ttu-id="95533-142">當 JIT 啟動的元件為交易式時，您很可能會將其共用。</span><span class="sxs-lookup"><span data-stu-id="95533-142">You are most likely to be pooling JIT-activated components when they are transactional.</span></span> <span data-ttu-id="95533-143">物件共用已經過優化，可處理交易元件。</span><span class="sxs-lookup"><span data-stu-id="95533-143">Object pooling is optimized to handle transactional components.</span></span> <span data-ttu-id="95533-144">如需詳細資訊，請參閱共用 [交易對象](pooling-transactional-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="95533-144">For more information, see [Pooling Transactional Objects](pooling-transactional-objects.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="95533-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="95533-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95533-146">COM + 物件的函式字串</span><span class="sxs-lookup"><span data-stu-id="95533-146">COM+ Object Constructor Strings</span></span>](com--object-constructor-strings.md)
</dt> <dt>

[<span data-ttu-id="95533-147">控制物件存留期和狀態</span><span class="sxs-lookup"><span data-stu-id="95533-147">Controlling Object Lifetime and State</span></span>](controlling-object-lifetime-and-state.md)
</dt> <dt>

[<span data-ttu-id="95533-148">物件共用的運作方式</span><span class="sxs-lookup"><span data-stu-id="95533-148">How Object Pooling Works</span></span>](how-object-pooling-works.md)
</dt> <dt>

[<span data-ttu-id="95533-149">共用交易對象</span><span class="sxs-lookup"><span data-stu-id="95533-149">Pooling Transactional Objects</span></span>](pooling-transactional-objects.md)
</dt> <dt>

[<span data-ttu-id="95533-150">共用物件的需求</span><span class="sxs-lookup"><span data-stu-id="95533-150">Requirements for Poolable Objects</span></span>](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



