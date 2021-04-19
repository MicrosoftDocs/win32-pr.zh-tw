---
title: WFP 操作
description: Windows 篩選平台 (WFP) 透過整合下列基底實體層、篩選器、填充碼和標注來執行其工作。
ms.assetid: bf88ace7-1160-434b-9be0-3f9db6aa2e87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e7a7d38bd0de5b1f549e2187c414644bf68442
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106966455"
---
# <a name="wfp-operation"></a><span data-ttu-id="c7be4-103">WFP 操作</span><span class="sxs-lookup"><span data-stu-id="c7be4-103">WFP Operation</span></span>

<span data-ttu-id="c7be4-104">Windows 篩選平台 (WFP) 透過整合下列基底實體來執行其工作： *圖層*、 *篩選*、 *填充* 碼和 *標注*。</span><span class="sxs-lookup"><span data-stu-id="c7be4-104">Windows Filtering Platform (WFP) performs its tasks by integrating the following basic entities: *Layers*, *Filters*, *Shims*, and *Callouts*.</span></span>

## <a name="layers"></a><span data-ttu-id="c7be4-105">圖層</span><span class="sxs-lookup"><span data-stu-id="c7be4-105">Layers</span></span>

<span data-ttu-id="c7be4-106">*圖層* 是篩選引擎所管理的容器，其函式是用來將篩選組織成集合。</span><span class="sxs-lookup"><span data-stu-id="c7be4-106">A *layer* is a container managed by the filter engine whose function is to organize filters into sets.</span></span> <span data-ttu-id="c7be4-107">圖層不是網路堆疊中的模組。</span><span class="sxs-lookup"><span data-stu-id="c7be4-107">A layer is not a module in the network stack.</span></span> <span data-ttu-id="c7be4-108">每一層都有一個架構，可定義可以加入的篩選器類型。</span><span class="sxs-lookup"><span data-stu-id="c7be4-108">Each layer has a schema that defines the type of filters that can be added to it.</span></span> <span data-ttu-id="c7be4-109">如需詳細資訊，請參閱 [每個篩選層級可用的篩選準則](filtering-conditions-available-at-each-filtering-layer.md) 。</span><span class="sxs-lookup"><span data-stu-id="c7be4-109">See [Filtering Conditions Available at Each Filtering Layer](filtering-conditions-available-at-each-filtering-layer.md) for more information.</span></span>

<span data-ttu-id="c7be4-110">圖層可能會包含子層以管理衝突的篩選準則需求，例如「封鎖超過1024的 TCP 埠」和「開啟埠1080」。</span><span class="sxs-lookup"><span data-stu-id="c7be4-110">Layers may contain sub-layers to manage conflicting filter requirements such as "Block TCP ports above 1024" and "Open port 1080".</span></span> <span data-ttu-id="c7be4-111">用於管理篩選衝突的規則是由 [篩選仲裁](filter-arbitration.md)所決定。</span><span class="sxs-lookup"><span data-stu-id="c7be4-111">The rules for managing filtering conflicts are determined by [Filter Arbitration](filter-arbitration.md).</span></span>

<span data-ttu-id="c7be4-112">WFP 包含一組 [內建的子層](management-filtering-sublayer-identifiers.md)。</span><span class="sxs-lookup"><span data-stu-id="c7be4-112">WFP contains a set of [built-in sub-layers](management-filtering-sublayer-identifiers.md).</span></span> <span data-ttu-id="c7be4-113">每一層都會繼承所有內建的子層。</span><span class="sxs-lookup"><span data-stu-id="c7be4-113">Every layer inherits all the built-in sub-layers.</span></span> <span data-ttu-id="c7be4-114">使用者也可以新增自己的子層。</span><span class="sxs-lookup"><span data-stu-id="c7be4-114">Users can also add their own sub-layers.</span></span>

<span data-ttu-id="c7be4-115">篩選引擎圖層的清單是在 [**篩選層識別碼**](management-filtering-layer-identifiers-.md)的參考區段主題中提供。</span><span class="sxs-lookup"><span data-stu-id="c7be4-115">The list of filter engine layers is provided in the reference section topic [**Filtering Layer Identifiers**](management-filtering-layer-identifiers-.md).</span></span>

## <a name="filters"></a><span data-ttu-id="c7be4-116">篩選器</span><span class="sxs-lookup"><span data-stu-id="c7be4-116">Filters</span></span>

<span data-ttu-id="c7be4-117">*篩選準則* 是與傳入或傳出封包相符的規則。</span><span class="sxs-lookup"><span data-stu-id="c7be4-117">A *filter* is a rule that is matched against incoming or outgoing packets.</span></span> <span data-ttu-id="c7be4-118">此規則會告知篩選引擎要如何處理封包，包括呼叫用來進行深層封包或資料流程檢查的標注模組。</span><span class="sxs-lookup"><span data-stu-id="c7be4-118">The rule tells the filtering engine what to do with the packet, including to call a callout module for deep packet or stream inspection.</span></span> <span data-ttu-id="c7be4-119">例如，篩選可能會指定「封鎖 TCP 埠大於1024的流量」或「針對未受保護的所有流量呼叫識別碼」。</span><span class="sxs-lookup"><span data-stu-id="c7be4-119">For example, a filter may specify "Block traffic with a TCP port greater than 1024" or "Call out to IDS for all traffic that is not secured."</span></span>

<span data-ttu-id="c7be4-120">開機時間篩選器是一種篩選準則，當 TCP/IP 堆疊驅動程式 (tcpip.sys) 啟動時，就會在開機時強制執行。</span><span class="sxs-lookup"><span data-stu-id="c7be4-120">A boot-time filter is a filter that is enforced at boot-time as soon as the TCP/IP stack driver (tcpip.sys) starts.</span></span> <span data-ttu-id="c7be4-121">當 BFE 啟動時，會停用開機時間篩選器。</span><span class="sxs-lookup"><span data-stu-id="c7be4-121">A boot-time filter is disabled when BFE starts.</span></span> <span data-ttu-id="c7be4-122">當叫用 [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)時，會設定 [**FWPM \_ 篩選 \_ 旗標 \_ BOOTTIME**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0)旗標，將篩選標示為開機時間。</span><span class="sxs-lookup"><span data-stu-id="c7be4-122">A filter is marked as boot-time by setting the [**FWPM\_FILTER\_FLAG\_BOOTTIME**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0) flag when [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0) is invoked.</span></span>

<span data-ttu-id="c7be4-123">執行時間篩選準則是在 BFE 開始之後強制執行的篩選。</span><span class="sxs-lookup"><span data-stu-id="c7be4-123">A run-time filter is a filter that is enforced after BFE starts.</span></span> <span data-ttu-id="c7be4-124">執行時間篩選準則可以是靜態、動態或持續性，取決於建立的方式。</span><span class="sxs-lookup"><span data-stu-id="c7be4-124">A run-time filter can be static, dynamic, or persistent depending on the way it was created.</span></span> <span data-ttu-id="c7be4-125">如需不同類型的執行時間篩選和其存留期的詳細資訊，請參閱 [物件管理](object-management.md) 。</span><span class="sxs-lookup"><span data-stu-id="c7be4-125">See [Object Management](object-management.md) for more information on the different types of run-time filters and their lifetime.</span></span>

## <a name="shims"></a><span data-ttu-id="c7be4-126">墊片</span><span class="sxs-lookup"><span data-stu-id="c7be4-126">Shims</span></span>

<span data-ttu-id="c7be4-127">*填充碼* 是一種核心模式元件，可根據篩選引擎層分類來進行篩選決定。</span><span class="sxs-lookup"><span data-stu-id="c7be4-127">A *shim* is a kernel-mode component that makes filtering decisions by classifying against the filter engine layers.</span></span> <span data-ttu-id="c7be4-128">每個填充碼會針對一或多個圖層進行分類。</span><span class="sxs-lookup"><span data-stu-id="c7be4-128">Each shim classifies against one or more layers.</span></span> <span data-ttu-id="c7be4-129">例如，傳輸層模組填充碼會針對流量的第一個封包，分類為輸入傳輸層、輸出傳輸層，以及 ALE 連接和 Receive-Accept 層。</span><span class="sxs-lookup"><span data-stu-id="c7be4-129">For example, the Transport Layer Module shim classifies against the Inbound Transport layer, the Outbound Transport layer, and the ALE Connect and Receive-Accept layers for the first packet of a flow.</span></span>

<span data-ttu-id="c7be4-130">當封包、資料流程和事件跨越網路堆疊時，填充碼會將它們剖析以解壓縮資料條件和值，然後呼叫篩選引擎以針對指定層中的篩選進行評估。</span><span class="sxs-lookup"><span data-stu-id="c7be4-130">As packets, streams, and events traverse the network stack, the shims parse them to extract the classifiable conditions and values, and then call into the filter engine to evaluate them against the filters in a given layer.</span></span> <span data-ttu-id="c7be4-131">篩選引擎可能會叫用一或多個標注做為分類的一部分。</span><span class="sxs-lookup"><span data-stu-id="c7be4-131">The filter engine may invoke one or more callouts as part of the classification.</span></span> <span data-ttu-id="c7be4-132">填充碼會根據篩選引擎所執行的分類結果，執行實際的封包、資料流程和事件的卸載。</span><span class="sxs-lookup"><span data-stu-id="c7be4-132">The shims do the actual dropping of packets, streams, and events based on the result of the classification performed by the filter engine.</span></span>

## <a name="callouts"></a><span data-ttu-id="c7be4-133">圖說文字</span><span class="sxs-lookup"><span data-stu-id="c7be4-133">Callouts</span></span>

<span data-ttu-id="c7be4-134">注 *標是驅動* 程式所公開的一組函式，用於特製化篩選。</span><span class="sxs-lookup"><span data-stu-id="c7be4-134">A *callout* is a set of functions exposed by a driver and used for specialized filtering.</span></span> <span data-ttu-id="c7be4-135">它們是用來執行封包的分析和操作，例如病毒掃描、家長監護掃描是否有不當的內容，以及用於監視工具的封包資料剖析。</span><span class="sxs-lookup"><span data-stu-id="c7be4-135">They are used to perform analysis and manipulation of the packets, such as virus scan, parental controls scan for inappropriate content, packet data parsing for monitoring tools.</span></span> <span data-ttu-id="c7be4-136">某些標注（例如網路位址轉譯 (NAT) 驅動程式）已內建在作業系統中。</span><span class="sxs-lookup"><span data-stu-id="c7be4-136">Some callouts, such as the Network Address Translation (NAT) driver, are built into the operating system.</span></span> <span data-ttu-id="c7be4-137">其他（例如 HTTP 家長監護）或入侵偵測系統 (識別碼) 注標，可由獨立軟體廠商 (Isv) 提供。</span><span class="sxs-lookup"><span data-stu-id="c7be4-137">Others, such as an HTTP Parental Control callout or the Intrusion Detection System (IDS) callout, can be provided by independent software vendors (ISVs).</span></span> <span data-ttu-id="c7be4-138">當對應的標注篩選準則在指定的圖層符合時，篩選引擎會叫用注標函數。</span><span class="sxs-lookup"><span data-stu-id="c7be4-138">The callout functions are invoked by the filter engine when a corresponding callout filter is matched at a given layer.</span></span>

<span data-ttu-id="c7be4-139">您可以在任何核心模式的 WFP 層註冊標注。</span><span class="sxs-lookup"><span data-stu-id="c7be4-139">Callouts can be registered at any of the kernel-mode WFP layers.</span></span> <span data-ttu-id="c7be4-140">標注可以傳回 ( 「封鎖」、「允許」的動作，以及在執行資料流程檢查時「延遲」、「需要更多資料」、「卸載連線」 ) ，而且可以修改和保護輸入和輸出網路流量。</span><span class="sxs-lookup"><span data-stu-id="c7be4-140">Callouts can return an action ("Block", "Permit", and, when performing stream inspection, "Defer", "Need more data", "Drop connection") and can modify and secure inbound and outbound network traffic.</span></span>

<span data-ttu-id="c7be4-141">當標注已向篩選引擎註冊之後，它就可以接收要處理的網路流量。</span><span class="sxs-lookup"><span data-stu-id="c7be4-141">Once a callout is registered with the filter engine, it can receive network traffic to process.</span></span> <span data-ttu-id="c7be4-142">流量可能是封包、串流或事件，視層而定。</span><span class="sxs-lookup"><span data-stu-id="c7be4-142">The traffic may be packets, streams, or events depending on the layer.</span></span> <span data-ttu-id="c7be4-143">應用程式或防火牆代理程式會藉由新增動作為「標注」且其標注識別碼為該注標識別碼的篩選，來將流量傳遞至標注。</span><span class="sxs-lookup"><span data-stu-id="c7be4-143">An application or firewall agent causes traffic to be passed to a callout by adding a filter whose action is "Callout" and whose callout ID is that callout's identifier.</span></span> <span data-ttu-id="c7be4-144">標注可以指示篩選引擎將「區塊」或「允許」傳回填充碼。</span><span class="sxs-lookup"><span data-stu-id="c7be4-144">Callouts can instruct the filter engine to return "Block" or "Permit" to the shim.</span></span> <span data-ttu-id="c7be4-145">標注也可以傳回「繼續」，以允許其他篩選器處理封包。</span><span class="sxs-lookup"><span data-stu-id="c7be4-145">Callouts can also return "Continue" to allow other filters to process the packet.</span></span>

<span data-ttu-id="c7be4-146">一個注標驅動程式可能會公開多個標注。</span><span class="sxs-lookup"><span data-stu-id="c7be4-146">Multiple callouts may be exposed by one callout driver.</span></span>

<span data-ttu-id="c7be4-147">您必須使用 [**FwpmCalloutAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutadd0)) 將標注新增 (，並使用 [FwpsCalloutRegister](/windows-hardware/drivers/ddi/_netvista/)) 註冊 (，才能使用它。</span><span class="sxs-lookup"><span data-stu-id="c7be4-147">A callout needs to be added (with [**FwpmCalloutAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutadd0)) and registered (with [FwpsCalloutRegister](/windows-hardware/drivers/ddi/_netvista/)) before it can be used.</span></span> <span data-ttu-id="c7be4-148">在建立參考標注的篩選之前，必須先呼叫 **FwpmCalloutAdd0** 。</span><span class="sxs-lookup"><span data-stu-id="c7be4-148">A call to **FwpmCalloutAdd0** is required before the creation of filters that reference the callout.</span></span> <span data-ttu-id="c7be4-149">必須先呼叫 FwpsCalloutRegister，然後 WFP 才能在符合標注篩選準則時叫用標注。</span><span class="sxs-lookup"><span data-stu-id="c7be4-149">A call to FwpsCalloutRegister is required before WFP can invoke the callout when the callout filters are matched.</span></span> <span data-ttu-id="c7be4-150">依預設，篩選器會將已加入但尚未向篩選引擎註冊的參考標注視為「封鎖」篩選準則。</span><span class="sxs-lookup"><span data-stu-id="c7be4-150">By default filters that reference callouts that have been added but have not yet registered with the filter engine are treated as "Block" filters.</span></span> <span data-ttu-id="c7be4-151">呼叫 **FwpmCalloutAdd0** 和 FwpsCalloutRegister 的順序並不重要。</span><span class="sxs-lookup"><span data-stu-id="c7be4-151">The order of calling **FwpmCalloutAdd0** and FwpsCalloutRegister does not matter.</span></span> <span data-ttu-id="c7be4-152">持續性的注標只需要加入一次，而且必須在每次執行標注的驅動程式開始時註冊 (例如，在重新開機) 之後。</span><span class="sxs-lookup"><span data-stu-id="c7be4-152">A persistent callout needs to be added just once and needs to be registered every time the driver that implements the callout starts (for example, after a reboot).</span></span>

## <a name="classification"></a><span data-ttu-id="c7be4-153">分類</span><span class="sxs-lookup"><span data-stu-id="c7be4-153">Classification</span></span>

<span data-ttu-id="c7be4-154">分類是將篩選套用到網路流量 (封包、串流或事件) 的程式，以便判斷該流量的「允許」或「封鎖」結果。</span><span class="sxs-lookup"><span data-stu-id="c7be4-154">Classification is the process of applying filters to network traffic (packet, stream, or event) in order to determine a result of "Permit" or "Block" for that traffic.</span></span> <span data-ttu-id="c7be4-155">針對一個封包、串流或事件，每一層都有一個分類呼叫。</span><span class="sxs-lookup"><span data-stu-id="c7be4-155">For one packet, stream, or event there is one classification call per layer.</span></span>

<span data-ttu-id="c7be4-156">在分類期間， (的屬性（例如，封包、串流或事件的來源位址) ）會與在叫用分類的層級篩選準則上設定的篩選準則進行比較。</span><span class="sxs-lookup"><span data-stu-id="c7be4-156">During classification, the properties (for example, source address) of the packet, stream, or event are compared with filter conditions set on filters at the layer where the classification is invoked.</span></span> <span data-ttu-id="c7be4-157">找到相符專案時，就會使用 [篩選仲裁](filter-arbitration.md) 演算法來判斷分類程式的結果。</span><span class="sxs-lookup"><span data-stu-id="c7be4-157">When matches are found, the [Filter Arbitration](filter-arbitration.md) algorithm is used to determines the result of the classification process.</span></span>

<span data-ttu-id="c7be4-158">由填充碼觸發分類要求。</span><span class="sxs-lookup"><span data-stu-id="c7be4-158">A classification request is triggered by a shim.</span></span>

<span data-ttu-id="c7be4-159">分類動作可以是：</span><span class="sxs-lookup"><span data-stu-id="c7be4-159">Classification actions could be either:</span></span>

-   <span data-ttu-id="c7be4-160">允許</span><span class="sxs-lookup"><span data-stu-id="c7be4-160">Permit</span></span>
-   <span data-ttu-id="c7be4-161">封鎖</span><span class="sxs-lookup"><span data-stu-id="c7be4-161">Block</span></span>
-   <span data-ttu-id="c7be4-162">圖說文字</span><span class="sxs-lookup"><span data-stu-id="c7be4-162">Callout</span></span>
    -   <span data-ttu-id="c7be4-163">允許</span><span class="sxs-lookup"><span data-stu-id="c7be4-163">Permit</span></span>
    -   <span data-ttu-id="c7be4-164">封鎖</span><span class="sxs-lookup"><span data-stu-id="c7be4-164">Block</span></span>
    -   <span data-ttu-id="c7be4-165">繼續</span><span class="sxs-lookup"><span data-stu-id="c7be4-165">Continue</span></span>
    -   <span data-ttu-id="c7be4-166">推遲</span><span class="sxs-lookup"><span data-stu-id="c7be4-166">Defer</span></span>
    -   <span data-ttu-id="c7be4-167">需要更多資料</span><span class="sxs-lookup"><span data-stu-id="c7be4-167">Need more data</span></span>
    -   <span data-ttu-id="c7be4-168">捨棄連接</span><span class="sxs-lookup"><span data-stu-id="c7be4-168">Drop connection</span></span>

## <a name="wfp-operation"></a><span data-ttu-id="c7be4-169">WFP 操作</span><span class="sxs-lookup"><span data-stu-id="c7be4-169">WFP Operation</span></span>

<span data-ttu-id="c7be4-170">在開機時，只要 TCP/IP 堆疊驅動程式 (tcpip.sys) 啟動，核心模式篩選引擎就會透過開機時間篩選器強制執行系統的安全性原則。</span><span class="sxs-lookup"><span data-stu-id="c7be4-170">At boot-time, as soon as the TCP/IP stack driver (tcpip.sys) starts, the kernel-mode filter engine enforces the security policy of the system through boot-time filters.</span></span>

<span data-ttu-id="c7be4-171">當基礎篩選引擎 (BFE) 在使用者模式中啟動時，系統會將持續性篩選新增至平臺、停用開機時間篩選器，並將通知傳送至使用 [FwpmBfeStateSubscribeChanges0](/windows-hardware/drivers/ddi/fwpmk/nf-fwpmk-fwpmbfestatesubscribechanges0)訂閱的這些標注驅動程式。</span><span class="sxs-lookup"><span data-stu-id="c7be4-171">Once the Base Filtering Engine (BFE) starts in user mode, persistent filters are added to the platform, boot-time filters are disabled, and notifications are sent to those callout drivers that subscribed using [FwpmBfeStateSubscribeChanges0](/windows-hardware/drivers/ddi/fwpmk/nf-fwpmk-fwpmbfestatesubscribechanges0).</span></span> <span data-ttu-id="c7be4-172">當 BFE 初始化完成之後，就會立即分派通知。</span><span class="sxs-lookup"><span data-stu-id="c7be4-172">The notifications are dispatched immediately after the BFE initialization is completed.</span></span> <span data-ttu-id="c7be4-173">平臺現在已準備好要註冊的標注，以及要加入的執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="c7be4-173">The platform is now ready for callouts to be registered and for run-time objects to be added.</span></span>

<span data-ttu-id="c7be4-174">從開機到持續篩選的轉換可能會有數秒或甚至更長的時間在緩慢的電腦上。</span><span class="sxs-lookup"><span data-stu-id="c7be4-174">The transition from boot-time to persistent filters could be several seconds, or even longer on a slow machine.</span></span> <span data-ttu-id="c7be4-175">它是不可部分完成的，因此，如果提供者同時具有開機時間和持續性篩選，則沒有任何作用中的視窗將永遠不會出現。</span><span class="sxs-lookup"><span data-stu-id="c7be4-175">It is atomic, so if a provider has both a boot-time and a persistent filter, there will never be a window when neither is in effect.</span></span>

<span data-ttu-id="c7be4-176">BFE 啟動之後，防火牆代理程式或自訂防火牆解決方案可以新增執行時間篩選器。</span><span class="sxs-lookup"><span data-stu-id="c7be4-176">After BFE starts, run-time filters can be added by firewall agents, or by custom firewall solutions.</span></span> <span data-ttu-id="c7be4-177">BFE 會處理這些篩選，並將它們傳送至適當的篩選引擎層以進行強制。</span><span class="sxs-lookup"><span data-stu-id="c7be4-177">BFE processes these filters and sends them to the appropriate filter engine layer for enforcement.</span></span> <span data-ttu-id="c7be4-178">BFE 也接受驗證設定，並將這些設定傳送至 (IKE/AuthIP) 的 IPsec 加密模組。</span><span class="sxs-lookup"><span data-stu-id="c7be4-178">BFE also accepts authentication settings and sends these settings to the IPsec keying modules (IKE/AuthIP).</span></span> <span data-ttu-id="c7be4-179">如需詳細資訊，請參閱 [IPsec](ipsec-configuration.md) 設定。</span><span class="sxs-lookup"><span data-stu-id="c7be4-179">See [IPsec Configuration](ipsec-configuration.md) for more information.</span></span>

<span data-ttu-id="c7be4-180">在任何時間，您都可以透過 BFE 所公開的 RPC 介面，在系統中新增、移除或變更篩選和驗證設定。</span><span class="sxs-lookup"><span data-stu-id="c7be4-180">At any time, filters and authentication settings can be added, removed or changed in the system through the RPC interface exposed by the BFE.</span></span> <span data-ttu-id="c7be4-181">您可以同樣地新增或移除子層和標注模組。</span><span class="sxs-lookup"><span data-stu-id="c7be4-181">Sub-layers and callout modules can likewise be added or removed.</span></span>

<span data-ttu-id="c7be4-182">資料流程：</span><span class="sxs-lookup"><span data-stu-id="c7be4-182">Data flow:</span></span>

1.  <span data-ttu-id="c7be4-183">封包會進入網路堆疊。</span><span class="sxs-lookup"><span data-stu-id="c7be4-183">A packet comes into the network stack.</span></span>
2.  <span data-ttu-id="c7be4-184">網路堆疊會尋找並呼叫填充碼。</span><span class="sxs-lookup"><span data-stu-id="c7be4-184">The network stack finds and calls a shim.</span></span>
3.  <span data-ttu-id="c7be4-185">填充碼會在特定層級叫用分類進程。</span><span class="sxs-lookup"><span data-stu-id="c7be4-185">The shim invokes the classification process at a particular layer.</span></span>
4.  <span data-ttu-id="c7be4-186">在分類期間，會比對篩選，並採取結果動作。</span><span class="sxs-lookup"><span data-stu-id="c7be4-186">During classification, filters are matched and the resultant action is taken.</span></span> <span data-ttu-id="c7be4-187"> (參閱 [篩選準則仲裁](filter-arbitration.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="c7be4-187">(See [Filter Arbitration](filter-arbitration.md).)</span></span>
5.  <span data-ttu-id="c7be4-188">如果在分類程式期間符合任何標注篩選準則，則會叫用對應的標注。</span><span class="sxs-lookup"><span data-stu-id="c7be4-188">If any callout filters are matched during the classification process, the corresponding callouts are invoked.</span></span>
6.  <span data-ttu-id="c7be4-189">填充碼會作用於最終的篩選決策 (例如，卸載封包) 。</span><span class="sxs-lookup"><span data-stu-id="c7be4-189">The shim acts on the final filtering decision (for example, drop the packet).</span></span>

<span data-ttu-id="c7be4-190">輸出資料流程會遵循類似的模式。</span><span class="sxs-lookup"><span data-stu-id="c7be4-190">Outbound data flow follows a similar pattern.</span></span>

<span data-ttu-id="c7be4-191">下列主題將進一步描述 WFP 的操作。</span><span class="sxs-lookup"><span data-stu-id="c7be4-191">The following topics further describe the operation of the WFP.</span></span>

-   [<span data-ttu-id="c7be4-192">TCP 封包流程</span><span class="sxs-lookup"><span data-stu-id="c7be4-192">TCP Packet Flows</span></span>](tcp-packet-flows.md)
-   [<span data-ttu-id="c7be4-193">UDP 封包流程</span><span class="sxs-lookup"><span data-stu-id="c7be4-193">UDP Packet Flows</span></span>](udp-packet-flows.md)
-   [<span data-ttu-id="c7be4-194">篩選仲裁</span><span class="sxs-lookup"><span data-stu-id="c7be4-194">Filter Arbitration</span></span>](filter-arbitration.md)

## <a name="related-topics"></a><span data-ttu-id="c7be4-195">相關主題</span><span class="sxs-lookup"><span data-stu-id="c7be4-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7be4-196">物件模型</span><span class="sxs-lookup"><span data-stu-id="c7be4-196">Object Model</span></span>](object-model.md)
</dt> <dt>

[<span data-ttu-id="c7be4-197">物件管理</span><span class="sxs-lookup"><span data-stu-id="c7be4-197">Object Management</span></span>](object-management.md)
</dt> </dl>

 

 