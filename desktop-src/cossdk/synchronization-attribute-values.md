---
description: 同步處理屬性是一種宣告式屬性，可指定您想要元件在啟動時的同步處理類型。
ms.assetid: 7f044ee5-b99e-4f0c-a680-b1e2672949fc
title: 同步處理屬性值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4606726d5202a1453e98d5bf609084982f8f824e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385916"
---
# <a name="synchronization-attribute-values"></a><span data-ttu-id="89296-103">同步處理屬性值</span><span class="sxs-lookup"><span data-stu-id="89296-103">Synchronization Attribute Values</span></span>

<span data-ttu-id="89296-104">同步處理屬性是一種宣告式屬性，可指定您想要元件在啟動時的同步處理類型。</span><span class="sxs-lookup"><span data-stu-id="89296-104">The synchronization attribute is a declarative property that specifies what type of synchronization you want your components to have when they are activated.</span></span> <span data-ttu-id="89296-105">當您加入同步處理屬性時，COM + 會代表您處理同步處理的詳細資料;您不需要進行任何其他呼叫。</span><span class="sxs-lookup"><span data-stu-id="89296-105">When you include the synchronization attribute, COM+ handles the details of synchronization on your behalf; you do not have to make any other calls.</span></span>

<span data-ttu-id="89296-106">根據其需求，物件可以共用其呼叫端的同步處理、需要新的同步處理，或在不同步處理的情況下運作。</span><span class="sxs-lookup"><span data-stu-id="89296-106">Depending on its requirements, an object can share its caller's synchronization, require a new synchronization, or operate without synchronization.</span></span>

<span data-ttu-id="89296-107">COM + 提供下列同步處理屬性值：</span><span class="sxs-lookup"><span data-stu-id="89296-107">COM+ provides the following synchronization attribute values:</span></span>

-   <span data-ttu-id="89296-108">**已停用。**</span><span class="sxs-lookup"><span data-stu-id="89296-108">**Disabled.**</span></span> <span data-ttu-id="89296-109">當您停用同步處理屬性時，COM + 會忽略元件在判斷物件內容時的同步處理需求。</span><span class="sxs-lookup"><span data-stu-id="89296-109">When you disable the synchronization attribute, COM+ ignores the synchronization requirements of the component in determining context for the object.</span></span> <span data-ttu-id="89296-110">因此，此物件不一定會共用其呼叫端的內容 (和同步處理) 。</span><span class="sxs-lookup"><span data-stu-id="89296-110">As a result, the object may or may not share its caller's context (and synchronization).</span></span>

    <span data-ttu-id="89296-111">一般情況下，當您知道元件永遠不會存取 resource manager 時，您應該使用此屬性值。</span><span class="sxs-lookup"><span data-stu-id="89296-111">In general, you should use this attribute value when you know the component never accesses a resource manager.</span></span> <span data-ttu-id="89296-112">將 COM 元件遷移至 COM + 時，您必須停用同步處理屬性，才能維持與未設定的 COM 元件相同的行為。</span><span class="sxs-lookup"><span data-stu-id="89296-112">When migrating COM components to COM+, you must disable the synchronization attribute to maintain the same behavior as the unconfigured COM component.</span></span> <span data-ttu-id="89296-113">未設定的元件是未安裝在 COM + 應用程式中的 COM 元件。</span><span class="sxs-lookup"><span data-stu-id="89296-113">An unconfigured component is a COM component that has not been installed in a COM+ application.</span></span>

-   <span data-ttu-id="89296-114">**不支援。**</span><span class="sxs-lookup"><span data-stu-id="89296-114">**Not Supported.**</span></span> <span data-ttu-id="89296-115">具有這個值的物件從不參與同步處理，不論其呼叫端的狀態如何。</span><span class="sxs-lookup"><span data-stu-id="89296-115">An object with this value never participates in synchronization, regardless of the status of its caller.</span></span> <span data-ttu-id="89296-116">這項設定僅適用于非交易式的元件，而且不會使用 [Com + 及時 (JIT) 啟用](com--just-in-time-activation.md) 服務。</span><span class="sxs-lookup"><span data-stu-id="89296-116">This setting is available only for components that are non-transactional and do not use the [COM+ just-in-time (JIT) activation](com--just-in-time-activation.md) service.</span></span>

-   <span data-ttu-id="89296-117">**支援。**</span><span class="sxs-lookup"><span data-stu-id="89296-117">**Supported.**</span></span> <span data-ttu-id="89296-118">具有此值的物件會參與同步處理（如果存在的話）。</span><span class="sxs-lookup"><span data-stu-id="89296-118">An object with this value participates in synchronization if it exists.</span></span> <span data-ttu-id="89296-119">當您想要讓物件在其呼叫者的同步處理中共用，但不需要自己的同步處理時，您可以宣告此值。</span><span class="sxs-lookup"><span data-stu-id="89296-119">You declare this value when you want an object to share in its caller's synchronization but not require synchronization of its own.</span></span>

    <span data-ttu-id="89296-120">將同步處理屬性設定為 [支援] 的好理由，是此設定在系統資源方面可能較便宜。</span><span class="sxs-lookup"><span data-stu-id="89296-120">A good reason to set your synchronization attribute to Supported is that this setting can be less expensive in terms of system resources.</span></span> <span data-ttu-id="89296-121">不過，由於需要從並行呼叫加以保護，因此更難以撰寫您的元件。</span><span class="sxs-lookup"><span data-stu-id="89296-121">However, it is more difficult to write your component because of the need to protect it from concurrent calls.</span></span> <span data-ttu-id="89296-122">將同步處理屬性設定為 [支援] 的含意是，在某些情況下，可能會以不同步處理的方式建立物件的實例。</span><span class="sxs-lookup"><span data-stu-id="89296-122">The implication of setting the synchronization attribute to Supported is that, under certain circumstances, an instance of your object may be created in such a way that it's not synchronized.</span></span> <span data-ttu-id="89296-123">如果元件的執行緒模型為 Free 或 Both，您將必須使用某種類型的鎖定機制來保護您的實例資料。</span><span class="sxs-lookup"><span data-stu-id="89296-123">If the component's threading model is Free or Both, you will have to protect your instance data with some type of locking mechanism.</span></span> <span data-ttu-id="89296-124">如果執行緒模型是 (STA) ，您就不需要保護您的實例資料。</span><span class="sxs-lookup"><span data-stu-id="89296-124">If the Threading Model is Apartment (STA), you won't need to protect your instance data.</span></span>

-   <span data-ttu-id="89296-125">**必要。**</span><span class="sxs-lookup"><span data-stu-id="89296-125">**Required.**</span></span> <span data-ttu-id="89296-126">當您設定這個屬性時，COM + 會確保從元件建立的所有物件都會進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="89296-126">When you set this attribute, COM+ ensures that all objects created from the component will be synchronized.</span></span> <span data-ttu-id="89296-127">實際上，只要 COM + 建立元件的實例，就能確保一次只有一個執行緒會通過這個實例。</span><span class="sxs-lookup"><span data-stu-id="89296-127">In effect, whenever COM+ creates an instance of your component, it makes sure there's only one thread going through this instance at a time.</span></span>

    <span data-ttu-id="89296-128">當 COM + 啟始物件時，它會查看其呼叫端的同步處理狀態。</span><span class="sxs-lookup"><span data-stu-id="89296-128">As COM+ activates an object, it looks at the synchronization status of its caller.</span></span> <span data-ttu-id="89296-129">如果呼叫端已同步處理，COM + 就會將呼叫端的同步處理界限傳送至，以包含新的物件。</span><span class="sxs-lookup"><span data-stu-id="89296-129">If the caller is synchronized, COM+ flows the caller's synchronization boundary to include the new object.</span></span> <span data-ttu-id="89296-130">否則，COM + 會開始同步處理。</span><span class="sxs-lookup"><span data-stu-id="89296-130">Otherwise, COM+ begins the synchronization.</span></span>

-   <span data-ttu-id="89296-131">**需要新的。**</span><span class="sxs-lookup"><span data-stu-id="89296-131">**Requires New.**</span></span> <span data-ttu-id="89296-132">具有此值的物件必須參與新的同步處理，其中 COM + 會代表呼叫中牽涉到的所有元件來管理內容和單元。</span><span class="sxs-lookup"><span data-stu-id="89296-132">An object with this value must participate in a new synchronization, where COM+ manages contexts and apartments on behalf of all components involved in the call.</span></span> <span data-ttu-id="89296-133">COM + 會自動起始新的同步處理，這與呼叫者的同步處理不同。</span><span class="sxs-lookup"><span data-stu-id="89296-133">COM+ automatically initiates a new synchronization, which is distinct from the caller's synchronization.</span></span>

    <span data-ttu-id="89296-134">將同步處理屬性設定為需要 New 的好理由是，此設定可讓您更有效率地對元件的實例進行外部呼叫。</span><span class="sxs-lookup"><span data-stu-id="89296-134">A good reason to set your synchronization attribute to Requires New is that this setting allows you to make outside calls to an instance of your component more efficiently.</span></span> <span data-ttu-id="89296-135">不過，它也會在您的物件和建立它的物件之間進行呼叫，而使系統資源的成本更高。</span><span class="sxs-lookup"><span data-stu-id="89296-135">However, it also makes calls between your object and the object that created it more expensive in terms of system resources.</span></span>

    <span data-ttu-id="89296-136">例如，假設您的物件及其 creator 物件共用相同的同步處理界限的情況。</span><span class="sxs-lookup"><span data-stu-id="89296-136">For example, assume a case where your object and its creator object share the same synchronization boundary.</span></span> <span data-ttu-id="89296-137">如果用戶端 A 呼叫 creator 物件，而用戶端 B 呼叫您的物件，則第二次呼叫必須等到第一次呼叫完成之後，才會呼叫。</span><span class="sxs-lookup"><span data-stu-id="89296-137">If client A calls the creator object and client B calls your object, the second call will have to wait until the first call is completed.</span></span> <span data-ttu-id="89296-138">如果您設定 [需要新的]，則會在不同的同步處理界限內建立物件。</span><span class="sxs-lookup"><span data-stu-id="89296-138">If you set Requires New, your object is created in a separate synchronization boundary.</span></span> <span data-ttu-id="89296-139">在此情況下，可以同時處理來自其他物件的呼叫。</span><span class="sxs-lookup"><span data-stu-id="89296-139">In this case, calls from other objects can be processed at the same time.</span></span> <span data-ttu-id="89296-140">不過，從 creator 物件對您物件的呼叫需要更多系統資源，因為它們必須跨越同步處理界限。</span><span class="sxs-lookup"><span data-stu-id="89296-140">However, calls from the creator object to your object require more system resources because they must cross synchronization boundaries.</span></span>

## <a name="related-topics"></a><span data-ttu-id="89296-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="89296-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89296-142">設定同步處理屬性</span><span class="sxs-lookup"><span data-stu-id="89296-142">Setting the Synchronization Attribute</span></span>](setting-the-synchronization-attribute.md)
</dt> <dt>

[<span data-ttu-id="89296-143">同步處理相依性</span><span class="sxs-lookup"><span data-stu-id="89296-143">Synchronization Dependencies</span></span>](synchronization-dependencies.md)
</dt> </dl>

 

 



