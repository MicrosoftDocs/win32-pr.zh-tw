---
title: 篩選仲裁
description: 篩選仲裁是內建在 Windows 篩選平台 (WFP) 的邏輯，用來決定篩選器在進行網路流量篩選決策時如何彼此互動。
ms.assetid: d097f307-113e-4dc3-ad59-ddfb85061583
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fd7df778d1c24b7480de3321e7a1ec126d8e642
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682284"
---
# <a name="filter-arbitration"></a><span data-ttu-id="c5978-103">篩選仲裁</span><span class="sxs-lookup"><span data-stu-id="c5978-103">Filter Arbitration</span></span>

<span data-ttu-id="c5978-104">篩選仲裁是內建在 Windows 篩選平台 (WFP) 的邏輯，用來決定篩選器在進行網路流量篩選決策時如何彼此互動。</span><span class="sxs-lookup"><span data-stu-id="c5978-104">Filter arbitration is the logic built into the Windows Filtering Platform (WFP) that is used to determine how filters interact with each other when making network traffic filtering decisions.</span></span>

## <a name="filter-arbitration-behaviors"></a><span data-ttu-id="c5978-105">篩選仲裁行為</span><span class="sxs-lookup"><span data-stu-id="c5978-105">Filter Arbitration Behaviors</span></span>

<span data-ttu-id="c5978-106">下列行為會描述篩選仲裁系統的特性：</span><span class="sxs-lookup"><span data-stu-id="c5978-106">The following behaviors characterize the filter arbitration system:</span></span>

-   <span data-ttu-id="c5978-107">所有流量都可以檢查。</span><span class="sxs-lookup"><span data-stu-id="c5978-107">All traffic can be inspected.</span></span> <span data-ttu-id="c5978-108">沒有任何流量可以略過指定層的篩選。</span><span class="sxs-lookup"><span data-stu-id="c5978-108">No traffic can bypass filters at a given layer.</span></span>
-   <span data-ttu-id="c5978-109">即使較高優先順序的篩選準則已允許， **也可以** 透過遮罩來封鎖流量。</span><span class="sxs-lookup"><span data-stu-id="c5978-109">Traffic can be blocked by a callout filter via a **Veto** even if a higher priority filter has permitted it.</span></span>
-   <span data-ttu-id="c5978-110">多個提供者可以檢查相同層級的流量。</span><span class="sxs-lookup"><span data-stu-id="c5978-110">Multiple providers can inspect traffic at the same layer.</span></span> <span data-ttu-id="c5978-111">例如，防火牆後面接著入侵偵測系統 (識別碼) 篩選器，或 IPsec 後面接著服務品質 (QoS) 篩選器可能全都檢查相同層級的流量。</span><span class="sxs-lookup"><span data-stu-id="c5978-111">For example, firewall followed by intrusion-detection system (IDS) filters, or IPsec followed by Quality of Service (QoS) filters may all examine the traffic at the same layer.</span></span>

## <a name="filtering-model"></a><span data-ttu-id="c5978-112">篩選模型</span><span class="sxs-lookup"><span data-stu-id="c5978-112">Filtering Model</span></span>

<span data-ttu-id="c5978-113">每個篩選層都分成依優先順序排序的子層 (也稱為權數) 。</span><span class="sxs-lookup"><span data-stu-id="c5978-113">Each filter layer is divided into sub-layers ordered by priority (also called weight).</span></span> <span data-ttu-id="c5978-114">網路流量會從最高優先順序到最低優先順序的子層。</span><span class="sxs-lookup"><span data-stu-id="c5978-114">Network traffic traverses sub-layers from the highest priority to the lowest priority.</span></span> <span data-ttu-id="c5978-115">子層是由使用 WFP API 的開發人員所建立和管理。</span><span class="sxs-lookup"><span data-stu-id="c5978-115">Sub-layers are created and managed by the developers using the WFP API.</span></span>

<span data-ttu-id="c5978-116">在每個子層內，篩選準則會依權數進行排序。</span><span class="sxs-lookup"><span data-stu-id="c5978-116">Within each sub-layer, filters are ordered by weight.</span></span> <span data-ttu-id="c5978-117">指出將篩選從最高權數降至最低權數的網路流量。</span><span class="sxs-lookup"><span data-stu-id="c5978-117">Network traffic is indicated to matching filters from highest weight to lowest weight.</span></span>

<span data-ttu-id="c5978-118">篩選準則仲裁演算法會套用至圖層內的所有子層，並在所有子層都經過評估之後進行最後的篩選決策。</span><span class="sxs-lookup"><span data-stu-id="c5978-118">The filter arbitration algorithm is applied to all sub-layers within a layer and the final filtering decision is made after all sub-layers have been evaluated.</span></span> <span data-ttu-id="c5978-119">這可提供多個相符功能。</span><span class="sxs-lookup"><span data-stu-id="c5978-119">This provides for multiple matching capability.</span></span>

<span data-ttu-id="c5978-120">在子層內，篩選準則仲裁的執行方式如下：</span><span class="sxs-lookup"><span data-stu-id="c5978-120">Within a sub-layer, filter arbitration is performed as follows:</span></span>

-   <span data-ttu-id="c5978-121">計算依加權排序的相符篩選清單（從最高到最低）。</span><span class="sxs-lookup"><span data-stu-id="c5978-121">Compute the list of matching filters ordered by weight from highest to lowest.</span></span>
-   <span data-ttu-id="c5978-122">依序評估符合的篩選準則，直到傳回「允許」或「封鎖」 (篩選準則也會傳回「繼續」 ) 或直到清單耗盡為止。</span><span class="sxs-lookup"><span data-stu-id="c5978-122">Evaluate matching filters in order until a "Permit" or a "Block" is returned (filters can also return "Continue") or until the list is exhausted.</span></span>
-   <span data-ttu-id="c5978-123">略過其餘的篩選準則，然後從上一個評估的篩選傳回動作。</span><span class="sxs-lookup"><span data-stu-id="c5978-123">Skip the remaining filters and return the action from the last evaluated filter.</span></span>

<span data-ttu-id="c5978-124">在圖層中，會以下列方式執行篩選仲裁：</span><span class="sxs-lookup"><span data-stu-id="c5978-124">Within a layer, filter arbitration is performed as follows:</span></span>

-   <span data-ttu-id="c5978-125">依序從最高優先順序到最低優先順序，在每個子層執行篩選仲裁。</span><span class="sxs-lookup"><span data-stu-id="c5978-125">Perform filter arbitration at every sub-layer in order from highest priority to lowest priority.</span></span>
-   <span data-ttu-id="c5978-126">即使較高優先順序的子層決定封鎖流量，也請評估所有子層。</span><span class="sxs-lookup"><span data-stu-id="c5978-126">Evaluate all sub-layers even if a higher priority sub-layer has decided to block the traffic.</span></span>
-   <span data-ttu-id="c5978-127">根據下一節所述的原則規則，傳回產生的動作。</span><span class="sxs-lookup"><span data-stu-id="c5978-127">Return the resulting action based on the policy rules described in the following section.</span></span>

<span data-ttu-id="c5978-128">下圖說明子層設定的範例。</span><span class="sxs-lookup"><span data-stu-id="c5978-128">The diagram below illustrates a sample sub-layer configuration.</span></span> <span data-ttu-id="c5978-129">外部方塊代表圖層。</span><span class="sxs-lookup"><span data-stu-id="c5978-129">The outer boxes represent layers.</span></span> <span data-ttu-id="c5978-130">內部方塊代表包含篩選準則的子層。</span><span class="sxs-lookup"><span data-stu-id="c5978-130">The inner boxes represent sub-layers that contain filters.</span></span> <span data-ttu-id="c5978-131">\*篩選準則中的萬用字元 () 表示所有流量都符合篩選準則。</span><span class="sxs-lookup"><span data-stu-id="c5978-131">The wildcard (\*) in a filter means all traffic matches the filter.</span></span>

![範例子層設定](images/fwp-sub-config2.png)

<span data-ttu-id="c5978-133">要略過篩選準則的唯一方法是，如果有較高的權數篩選準則允許或封鎖相同子層內的流量。</span><span class="sxs-lookup"><span data-stu-id="c5978-133">The only way for a filter to be bypassed is if a higher weight filter has permitted or blocked the traffic within the same sub-layer.</span></span> <span data-ttu-id="c5978-134">相反地，若要確保篩選準則一律會看到某個階層內的所有流量，其中一種方法是新增子層，其中包含符合所有流量的單一篩選。</span><span class="sxs-lookup"><span data-stu-id="c5978-134">Conversely, one way of ensuring that a filter always sees all traffic within a layer is to add a sub-layer that contains a single filter that matches all traffic.</span></span>

## <a name="configurable-override-policy"></a><span data-ttu-id="c5978-135">可設定的覆寫原則</span><span class="sxs-lookup"><span data-stu-id="c5978-135">Configurable Override Policy</span></span>

<span data-ttu-id="c5978-136">以下所述的規則會管理層內的仲裁決策。</span><span class="sxs-lookup"><span data-stu-id="c5978-136">The rules described below govern the arbitration decisions within a layer.</span></span> <span data-ttu-id="c5978-137">篩選引擎會使用這些規則來決定要將哪一個子層動作套用到網路流量。</span><span class="sxs-lookup"><span data-stu-id="c5978-137">These rules are used by the filter engine to decide which one of the sub-layer actions is applied to the network traffic.</span></span>

<span data-ttu-id="c5978-138">基本原則如下所示。</span><span class="sxs-lookup"><span data-stu-id="c5978-138">The basic policy is as follows.</span></span>

-   <span data-ttu-id="c5978-139">動作會依子層的優先權順序（從最高優先順序到最低優先順序）進行評估。</span><span class="sxs-lookup"><span data-stu-id="c5978-139">Actions are evaluated in priority order of sub-layers from highest priority to lowest priority.</span></span>
-   <span data-ttu-id="c5978-140">「封鎖」會覆寫「允許」。</span><span class="sxs-lookup"><span data-stu-id="c5978-140">"Block" overrides "Permit".</span></span>
-   <span data-ttu-id="c5978-141">"Block" 是最後的 (無法覆寫) 並停止評估。</span><span class="sxs-lookup"><span data-stu-id="c5978-141">"Block" is final (cannot be overridden) and stops the evaluation.</span></span> <span data-ttu-id="c5978-142">封包會被捨棄。</span><span class="sxs-lookup"><span data-stu-id="c5978-142">The packet is discarded.</span></span>

<span data-ttu-id="c5978-143">基本原則不支援防火牆未覆寫例外狀況的案例。</span><span class="sxs-lookup"><span data-stu-id="c5978-143">The basic policy does not support the scenario of an exception not overridden by a firewall.</span></span> <span data-ttu-id="c5978-144">這類案例的一般範例包括：</span><span class="sxs-lookup"><span data-stu-id="c5978-144">Typical examples of this type of scenario are:</span></span>

-   <span data-ttu-id="c5978-145">即使有協力廠商防火牆，也需要開啟遠端系統管理埠。</span><span class="sxs-lookup"><span data-stu-id="c5978-145">Remote administration port required to be opened even in the presence of a third-party firewall.</span></span>
-   <span data-ttu-id="c5978-146">需要開啟埠才能運作 (的元件，例如通用隨插即用 UPnP) 。</span><span class="sxs-lookup"><span data-stu-id="c5978-146">Components that require ports to be opened in order to function (for example, Universal Plug and Play UPnP).</span></span> <span data-ttu-id="c5978-147">如果系統管理員已明確啟用元件，則防火牆不應以無訊息方式封鎖流量。</span><span class="sxs-lookup"><span data-stu-id="c5978-147">If the administrator has explicitly enabled the component, the firewall should not silently block the traffic.</span></span>

<span data-ttu-id="c5978-148">為了支援上述案例，您必須藉由管理動作覆寫許可權，使篩選決策更難以覆寫為另一個篩選決策。</span><span class="sxs-lookup"><span data-stu-id="c5978-148">In order to support the above scenarios, a filtering decision must be made more difficult to override than another filtering decision by managing the action override permission.</span></span> <span data-ttu-id="c5978-149">此許可權會實作為 **FWPS \_ 右 \_ 動作 \_ 寫入** 旗標，並以每個篩選為基礎進行設定。</span><span class="sxs-lookup"><span data-stu-id="c5978-149">This permission is implemented as the **FWPS\_RIGHT\_ACTION\_WRITE** flag and it is set on a per-filter basis.</span></span>

<span data-ttu-id="c5978-150">評估演算法會維護目前的動作 ( 「允許」或「封鎖」 ) 以及 **FWPS \_ 右 \_ 動作 \_ 寫入** 旗標。</span><span class="sxs-lookup"><span data-stu-id="c5978-150">The evaluation algorithm maintains the current action ("Permit" or "Block") along with the **FWPS\_RIGHT\_ACTION\_WRITE** flag.</span></span> <span data-ttu-id="c5978-151">旗標會控制是否允許較低優先順序的子層覆寫動作。</span><span class="sxs-lookup"><span data-stu-id="c5978-151">The flag controls whether a lower priority sub-layer is allowed to override the action.</span></span> <span data-ttu-id="c5978-152">藉由在 [FWPS \_ 分類 \_ OUT0](/windows/win32/api/fwpstypes/ns-fwpstypes-fwps_classify_out0)結構中設定或重設 **FWPS \_ RIGHT \_ ACTION \_ WRITE** 旗標，提供者會控制動作可以或無法覆寫的方式。</span><span class="sxs-lookup"><span data-stu-id="c5978-152">By setting or resetting the **FWPS\_RIGHT\_ACTION\_WRITE** flag in the [FWPS\_CLASSIFY\_OUT0](/windows/win32/api/fwpstypes/ns-fwpstypes-fwps_classify_out0) structure, a provider governs how actions can or cannot be overridden.</span></span> <span data-ttu-id="c5978-153">如果已設定旗標，則表示可以覆寫該動作。</span><span class="sxs-lookup"><span data-stu-id="c5978-153">If the flag is set, it indicates that the action can be overridden.</span></span> <span data-ttu-id="c5978-154">如果旗標不存在，就無法覆寫動作。</span><span class="sxs-lookup"><span data-stu-id="c5978-154">If the flag is absent, the action cannot be overridden.</span></span>



| <span data-ttu-id="c5978-155">動作</span><span class="sxs-lookup"><span data-stu-id="c5978-155">Action</span></span> | <span data-ttu-id="c5978-156">允許覆寫 (\_ FWPS \_ \_ 已設定正確的動作寫入) </span><span class="sxs-lookup"><span data-stu-id="c5978-156">Allow override (FWPS\_RIGHT\_ACTION\_WRITE is set)</span></span> | <span data-ttu-id="c5978-157">Description</span><span class="sxs-lookup"><span data-stu-id="c5978-157">Description</span></span>                                                                                                          |
|--------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5978-158">允許</span><span class="sxs-lookup"><span data-stu-id="c5978-158">Permit</span></span> | <span data-ttu-id="c5978-159">Yes</span><span class="sxs-lookup"><span data-stu-id="c5978-159">Yes</span></span>                                                | <span data-ttu-id="c5978-160">您可以在另一個子層封鎖流量。</span><span class="sxs-lookup"><span data-stu-id="c5978-160">The traffic can be blocked at another sub-layer.</span></span> <span data-ttu-id="c5978-161">這稱為「軟許可」。</span><span class="sxs-lookup"><span data-stu-id="c5978-161">This is called a soft permit.</span></span><br/>                            |
| <span data-ttu-id="c5978-162">允許</span><span class="sxs-lookup"><span data-stu-id="c5978-162">Permit</span></span> | <span data-ttu-id="c5978-163">No</span><span class="sxs-lookup"><span data-stu-id="c5978-163">No</span></span>                                                 | <span data-ttu-id="c5978-164">只有注標拒絕才能在另一個子層封鎖 **流量。**</span><span class="sxs-lookup"><span data-stu-id="c5978-164">The traffic can be blocked at another sub-layer only by a callout **Veto**.</span></span> <span data-ttu-id="c5978-165">這稱為「硬許可」。</span><span class="sxs-lookup"><span data-stu-id="c5978-165">This is called a hard permit.</span></span><br/> |
| <span data-ttu-id="c5978-166">封鎖</span><span class="sxs-lookup"><span data-stu-id="c5978-166">Block</span></span>  | <span data-ttu-id="c5978-167">Yes</span><span class="sxs-lookup"><span data-stu-id="c5978-167">Yes</span></span>                                                | <span data-ttu-id="c5978-168">可以在另一個子層允許流量。</span><span class="sxs-lookup"><span data-stu-id="c5978-168">The traffic can be permitted at another sub-layer.</span></span> <span data-ttu-id="c5978-169">這稱為「軟區塊」。</span><span class="sxs-lookup"><span data-stu-id="c5978-169">This is called a soft block.</span></span><br/>                           |
| <span data-ttu-id="c5978-170">封鎖</span><span class="sxs-lookup"><span data-stu-id="c5978-170">Block</span></span>  | <span data-ttu-id="c5978-171">No</span><span class="sxs-lookup"><span data-stu-id="c5978-171">No</span></span>                                                 | <span data-ttu-id="c5978-172">無法在另一個子層允許流量。</span><span class="sxs-lookup"><span data-stu-id="c5978-172">The traffic cannot be permitted at another sub-layer.</span></span> <span data-ttu-id="c5978-173">這稱為「硬封鎖」。</span><span class="sxs-lookup"><span data-stu-id="c5978-173">This is called a hard block.</span></span><br/>                        |



 

<span data-ttu-id="c5978-174">您可以設定篩選動作，方法是將結構 [**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)中的 **型** 別成員設定為 [已建立] 或 [.fwp]**動作 [ \_ \_ 允許**]。 **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="c5978-174">The filter action can be set by setting the **type** member in the structure [**FWPM\_ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0) to either **FWP\_ACTION\_BLOCK** or **FWP\_ACTION\_PERMIT**.</span></span> <span data-ttu-id="c5978-175">除了動作類型之外，篩選也會公開旗標 **FWPM \_ 篩選旗 \_ 標 \_ CLEAR \_ 動作 \_ 許可權**。</span><span class="sxs-lookup"><span data-stu-id="c5978-175">Along with the action type, a filter also exposes the flag **FWPM\_FILTER\_FLAG\_CLEAR\_ACTION\_RIGHT**.</span></span> <span data-ttu-id="c5978-176">如果清除此旗標，則動作類型為「固定」且無法覆寫，除非由拒絕所覆寫的硬許可 **（如稍後** 所述），否則它會以高優先順序動作來覆寫。</span><span class="sxs-lookup"><span data-stu-id="c5978-176">If this flag is cleared, then the action type is hard and cannot be overridden except when a hard permit is overridden by a **Veto** as explained later on, else it is soft which can be overridden by high priority action.</span></span>

<span data-ttu-id="c5978-177">下表列出篩選和標注動作的預設行為。</span><span class="sxs-lookup"><span data-stu-id="c5978-177">The following table lists the default behavior for filter and callout actions.</span></span>

| <span data-ttu-id="c5978-178">動作</span><span class="sxs-lookup"><span data-stu-id="c5978-178">Action</span></span>         | <span data-ttu-id="c5978-179">預設行為</span><span class="sxs-lookup"><span data-stu-id="c5978-179">Default Behavior</span></span> |
|----------------|------------------|
| <span data-ttu-id="c5978-180">篩選準則允許</span><span class="sxs-lookup"><span data-stu-id="c5978-180">Filter permit</span></span>  | <span data-ttu-id="c5978-181">軟許可</span><span class="sxs-lookup"><span data-stu-id="c5978-181">Soft permit</span></span>      |
| <span data-ttu-id="c5978-182">標注允許</span><span class="sxs-lookup"><span data-stu-id="c5978-182">Callout permit</span></span> | <span data-ttu-id="c5978-183">軟許可</span><span class="sxs-lookup"><span data-stu-id="c5978-183">Soft permit</span></span>      |
| <span data-ttu-id="c5978-184">篩選準則區塊</span><span class="sxs-lookup"><span data-stu-id="c5978-184">Filter block</span></span>   | <span data-ttu-id="c5978-185">硬封鎖</span><span class="sxs-lookup"><span data-stu-id="c5978-185">Hard block</span></span>       |
| <span data-ttu-id="c5978-186">標注區塊</span><span class="sxs-lookup"><span data-stu-id="c5978-186">Callout block</span></span>  | <span data-ttu-id="c5978-187">軟區塊</span><span class="sxs-lookup"><span data-stu-id="c5978-187">Soft block</span></span>       |



 

<span data-ttu-id="c5978-188">在呼叫篩選器之前重設 **FWPS \_ 右 \_ 動作 \_ 寫入** 旗標時，**拒絕是篩選所傳回** 的「封鎖」動作。</span><span class="sxs-lookup"><span data-stu-id="c5978-188">A **Veto** is a "Block" action returned by the filter when the **FWPS\_RIGHT\_ACTION\_WRITE** flag was reset prior to calling the filter.</span></span> <span data-ttu-id="c5978-189">拒絕 **會封鎖** 由硬許可允許的流量。</span><span class="sxs-lookup"><span data-stu-id="c5978-189">A **Veto** will block traffic that was permitted with a hard permit.</span></span>

<span data-ttu-id="c5978-190">發出拒絕 **時，** 即表示設定中發生衝突。</span><span class="sxs-lookup"><span data-stu-id="c5978-190">When a **Veto** is issued, it is an indication of conflict in the configuration.</span></span> <span data-ttu-id="c5978-191">採取下列動作來減輕衝突。</span><span class="sxs-lookup"><span data-stu-id="c5978-191">The following actions are taken to mitigate the conflict.</span></span>

-   <span data-ttu-id="c5978-192">流量被封鎖。</span><span class="sxs-lookup"><span data-stu-id="c5978-192">The traffic is blocked.</span></span>
-   <span data-ttu-id="c5978-193">產生 audit 事件。</span><span class="sxs-lookup"><span data-stu-id="c5978-193">An audit event is generated.</span></span>
-   <span data-ttu-id="c5978-194">會產生通知。</span><span class="sxs-lookup"><span data-stu-id="c5978-194">A notification is generated.</span></span>
    > [!Note]  
    > <span data-ttu-id="c5978-195">所有已訂閱的實體都會收到通知。</span><span class="sxs-lookup"><span data-stu-id="c5978-195">The notification is received by all entities that have subscribed to it.</span></span> <span data-ttu-id="c5978-196">這通常會包含防火牆 (，以偵測) 或應用程式 (的錯誤，以偵測是否) 覆寫其特定篩選。</span><span class="sxs-lookup"><span data-stu-id="c5978-196">This will typically include the firewall (in order to detect mis-configurations), or applications (in order to detect if their particular filter is overridden).</span></span>

     

    > [!Note]  
    > <span data-ttu-id="c5978-197">在覆寫「硬許可」篩選準則時，不會 (UI) 具現化強制使用者介面。</span><span class="sxs-lookup"><span data-stu-id="c5978-197">There is no mandatory user interface (UI) instantiated when a "Hard Permit" filter is overridden.</span></span> <span data-ttu-id="c5978-198">覆寫的通知會傳送給任何註冊接收這些通知的提供者，以允許防火牆或建立「允許」篩選準則的應用程式顯示 UI，以要求使用者執行動作。</span><span class="sxs-lookup"><span data-stu-id="c5978-198">The notifications of the override are sent to any provider that registered to receive them, which allows firewalls, or the applications that created the "Permit" filters, to show UI asking for user action.</span></span> <span data-ttu-id="c5978-199">因為不想要以無訊息方式封鎖的防火牆 Isv 可以藉由在 WFP 的不同位置註冊來執行此動作)  (，所以沒有任何值可針對這些覆寫事件提供平臺 UI 通知</span><span class="sxs-lookup"><span data-stu-id="c5978-199">There is no value in having a platform UI notification for these override events since firewall ISVs that do not want to silently block can do so by registering at a different place in WFP, or (less preferred) handle all their logic in a call-out driver.</span></span> <span data-ttu-id="c5978-200">想要提示使用者的 Isv，最好是想要擁有使用者體驗，並建立自己的 UI。</span><span class="sxs-lookup"><span data-stu-id="c5978-200">ISVs that do think prompting users is a good idea will want to own the user experience and create their own UI.</span></span>

     

<span data-ttu-id="c5978-201">上述的緩和行為可確保「硬許可」篩選器不會以無訊息方式覆寫「封鎖」篩選，並涵蓋不允許防火牆封鎖遠端系統管理埠的案例。</span><span class="sxs-lookup"><span data-stu-id="c5978-201">The mitigation behavior described above ensures that a "Hard Permit" filter is not silently overridden by a "Block" filter, and covers the scenario where a remote administration port is not allowed to be blocked by the firewall.</span></span> <span data-ttu-id="c5978-202">為了以無訊息方式覆寫「硬許可」篩選準則，防火牆必須在較高優先順序的子層內新增其篩選。</span><span class="sxs-lookup"><span data-stu-id="c5978-202">In order to silently override "Hard Permit" filters a firewall has to add its filters within a higher priority sub-layer.</span></span>

> [!Note]  
> <span data-ttu-id="c5978-203">因為沒有跨層仲裁，所以允許「硬許可」的流量可能仍會封鎖在另一層。</span><span class="sxs-lookup"><span data-stu-id="c5978-203">Since there is no cross-layer arbitration, traffic permitted with "Hard Permit" may still be blocked at another layer.</span></span> <span data-ttu-id="c5978-204">原則作者必須負責確保每個層級的流量都能在必要時允許。</span><span class="sxs-lookup"><span data-stu-id="c5978-204">It is the responsibility of the policy author to ensure that traffic is permitted at each layer if necessary.</span></span>

 

<span data-ttu-id="c5978-205">要求開啟埠的使用者應用程式會將可覆寫的篩選準則新增至低優先順序子層。</span><span class="sxs-lookup"><span data-stu-id="c5978-205">User applications requesting ports to be opened add overridable filters to a low priority sub-layer.</span></span> <span data-ttu-id="c5978-206">防火牆可以訂閱篩選準則新增通知事件，以及在使用者 (或原則) 驗證之後新增相符的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="c5978-206">The firewall can subscribe to the filter add notification events and add a matching filter after user (or policy) validation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5978-207">相關主題</span><span class="sxs-lookup"><span data-stu-id="c5978-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5978-208">篩選器加權指派</span><span class="sxs-lookup"><span data-stu-id="c5978-208">Filter Weight Assignment</span></span>](filter-weight-assignment.md)
</dt> </dl>

 

