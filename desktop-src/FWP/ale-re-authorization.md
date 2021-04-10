---
title: ALE 重新授權
description: 在應用層強制執行應用層的網路流量 (的 Windows 篩選平台的 ALE) 層 (WFP) 是由 ALE 流程篩選。
ms.assetid: 3cc7f78e-3f9d-4a91-8ea0-9b64c299068a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed05c4c0767d449ec128250f852c365455bd0dc7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682285"
---
# <a name="ale-reauthorization"></a><span data-ttu-id="c914e-103">ALE 重新授權</span><span class="sxs-lookup"><span data-stu-id="c914e-103">ALE Reauthorization</span></span>

<span data-ttu-id="c914e-104">在應用層強制執行應用層的網路流量 (的 Windows 篩選平台的 ALE) 層 (WFP) 是由 [ALE 流程](ale-stateful-filtering.md)篩選。</span><span class="sxs-lookup"><span data-stu-id="c914e-104">Network traffic at the Application Layer Enforcement (ALE) layers of the Windows Filtering Platform (WFP) is filtered by [ALE flows](ale-stateful-filtering.md).</span></span> <span data-ttu-id="c914e-105">一旦允許 ALE 流程，就會允許屬於 ALE 流程的所有流量。</span><span class="sxs-lookup"><span data-stu-id="c914e-105">Once an ALE flow has been permitted, all traffic that is part of the ALE flow is permitted.</span></span> <span data-ttu-id="c914e-106">重新授權是驗證 ALE 流程許可權的要求，通常是因為網路原則有變更。</span><span class="sxs-lookup"><span data-stu-id="c914e-106">Reauthorization is a request to validate the permissions of the ALE flow, typically due to a change in network policy.</span></span>

<span data-ttu-id="c914e-107">ALE 流程會根據觸發流程建立和授權的第一個封包方向，指派一個方向（輸入或輸出）。</span><span class="sxs-lookup"><span data-stu-id="c914e-107">ALE flows are assigned a direction, inbound or outbound, based on the direction of the first packet that triggered the creation and authorization of the flow.</span></span> <span data-ttu-id="c914e-108">輸入 ALE 流程是在 [**FWPM \_ 層的 \_ ale \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) 層建立和授權的。</span><span class="sxs-lookup"><span data-stu-id="c914e-108">Inbound ALE flows are created and authorized at the [**FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer.</span></span> <span data-ttu-id="c914e-109">**FWPM \_ LAYER \_ ale \_ AUTH \_ CONNECT \_ V {4 \| 6}** 層會建立和授權輸出 ALE 流程。</span><span class="sxs-lookup"><span data-stu-id="c914e-109">Outbound ALE flows are created and authorized at the **FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}** layer.</span></span> <span data-ttu-id="c914e-110">ALE 流程的方向不會限制屬於流程的封包方向。</span><span class="sxs-lookup"><span data-stu-id="c914e-110">The direction of the ALE flow does not limit the direction of packets that belong to the flow.</span></span> <span data-ttu-id="c914e-111">ALE 流程包含輸入和輸出封包，而不考慮 ALE 流程本身的方向。</span><span class="sxs-lookup"><span data-stu-id="c914e-111">ALE flows contain both inbound and outbound packets regardless of the direction of the ALE flow itself.</span></span>

<span data-ttu-id="c914e-112">系統會觸發 ALE 流程的重新授權，如下所示：</span><span class="sxs-lookup"><span data-stu-id="c914e-112">Reauthorization of an ALE flow is triggered by:</span></span>

-   <span data-ttu-id="c914e-113">在最初授權或建立 ALE 流程的層級變更原則。</span><span class="sxs-lookup"><span data-stu-id="c914e-113">A policy change at the layer where the ALE flow was originally authorized or created.</span></span>
-   <span data-ttu-id="c914e-114">抵達介面不同于原本授權或建立 ALE 流程的介面。</span><span class="sxs-lookup"><span data-stu-id="c914e-114">An arrival interface different from the interface where the ALE flow was originally authorized or created.</span></span>
-   <span data-ttu-id="c914e-115">暫止的連接。</span><span class="sxs-lookup"><span data-stu-id="c914e-115">A pending connection.</span></span>

<span data-ttu-id="c914e-116">重新授權可與初始授權區別，因為出現的 [**\_ \_ \_ 是已 \_ 重新授權旗標的 .fwp 條件旗**](filtering-condition-flags-.md) 標。</span><span class="sxs-lookup"><span data-stu-id="c914e-116">Reauthorization is distinguished from the initial authorization by the presence of the [**FWP\_CONDITION\_FLAG\_IS\_REAUTHORIZE**](filtering-condition-flags-.md) flag.</span></span>

<span data-ttu-id="c914e-117">重新授權只能在 [**FWPM \_ 層的 \_ ale \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) 和 **FWPM \_ LAYER \_ ale \_ auth \_ CONNECT \_ v {4 \| 6}** 層進行。</span><span class="sxs-lookup"><span data-stu-id="c914e-117">Reauthorization can take place only at the [**FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}**](management-filtering-layer-identifiers-.md) and **FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}** layers.</span></span>

### <a name="policy-change-reauthorization"></a><span data-ttu-id="c914e-118">原則-變更重新授權</span><span class="sxs-lookup"><span data-stu-id="c914e-118">Policy-Change Reauthorization</span></span>

<span data-ttu-id="c914e-119">原則變更會實作為在 ALE 層的新增或移除篩選。</span><span class="sxs-lookup"><span data-stu-id="c914e-119">A policy change is implemented as a filter addition or removal at an ALE layer.</span></span> <span data-ttu-id="c914e-120">一旦偵測到原則變更，系統將會指定第一個流經受影響層級所建立之 ALE 流程的封包，以重新授權至圖層。</span><span class="sxs-lookup"><span data-stu-id="c914e-120">Once a policy change is detected, the first packet that traverses an ALE flow created at the affected layer will be specified for reauthorization to the layer.</span></span> <span data-ttu-id="c914e-121">因此，在重新授權中，輸出封包完全有可能分類于 [**FWPM \_ 層 \_ ale \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) 層，並將輸入封包分類于 **FWPM \_ LAYER \_ ale \_ auth \_ CONNECT \_ V {4 \| 6}** 層。</span><span class="sxs-lookup"><span data-stu-id="c914e-121">Therefore, for reauthorization it is entirely possible that an outbound packet is classified at the [**FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer and that an inbound packet is classified at the **FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}** layer.</span></span>

<span data-ttu-id="c914e-122">這種混合方向分類的原因之一是，可能沒有來自原始方向的進一步網路流量 (例如，輸入的 ALE 流量) 的輸入封包。</span><span class="sxs-lookup"><span data-stu-id="c914e-122">One reason for this mixed-direction classification is that there might not be further network traffic from the original direction (for example, inbound packet for inbound ALE flow).</span></span> <span data-ttu-id="c914e-123">其中一個範例是在初始雙向交握之後的單向 UDP 串流。</span><span class="sxs-lookup"><span data-stu-id="c914e-123">One such example is one-way UDP streaming after an initial two-way handshake.</span></span> <span data-ttu-id="c914e-124">在此情況下，較好的做法是盡可能儘快卸載串流。</span><span class="sxs-lookup"><span data-stu-id="c914e-124">In this case it is more desirable to tear down the streaming as soon as possible.</span></span>

### <a name="arrival-interface-reauthorization"></a><span data-ttu-id="c914e-125">抵達介面重新授權</span><span class="sxs-lookup"><span data-stu-id="c914e-125">Arrival Interface Reauthorization</span></span>

<span data-ttu-id="c914e-126">從 Windows Server 2008 和 Windows Vista Service Pack 1 (SP1) 開始，可以使用抵達介面重新授權。</span><span class="sxs-lookup"><span data-stu-id="c914e-126">Arrival interface reauthorization is available starting with Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

<span data-ttu-id="c914e-127">屬於相同 ALE 流程的封包可以從多個介面抵達。</span><span class="sxs-lookup"><span data-stu-id="c914e-127">Packets belonging to the same ALE flow can arrive from multiple interfaces.</span></span> <span data-ttu-id="c914e-128">第一個要在與 ALE 流程的原始介面不同的介面上進入的封包是重新授權。</span><span class="sxs-lookup"><span data-stu-id="c914e-128">The first packet to come in over an interface different from the original interface of the ALE flow is reauthorized.</span></span>

<span data-ttu-id="c914e-129">在強式主機模型中（TCP/IP 堆疊的預設安全性模型），網路介面上的連線只接受在相同介面上的封包。</span><span class="sxs-lookup"><span data-stu-id="c914e-129">In a strong host model, which is the default security model for the TCP/IP stack, a connection on a network interface accepts only packets that come in on the same interface.</span></span> <span data-ttu-id="c914e-130">因此，不會在強式主機電腦上使用抵達介面重新授權。</span><span class="sxs-lookup"><span data-stu-id="c914e-130">Therefore, arrival interface reauthorization is not used on a strong host computer.</span></span>

<span data-ttu-id="c914e-131">在弱式主機模型中，網路介面上的連線允許傳入任何其他網路介面上的封包。</span><span class="sxs-lookup"><span data-stu-id="c914e-131">In a weak host model, a connection on a network interface allows packets coming in on any other network interface.</span></span> <span data-ttu-id="c914e-132">抵達介面重新授權用於弱式主機電腦上，以執行介面特定的原則。</span><span class="sxs-lookup"><span data-stu-id="c914e-132">Arrival interface reauthorization is used on a weak host computer to implement interface-specific policies.</span></span> <span data-ttu-id="c914e-133">如需詳細資訊，請參閱「 [纜線專家：強式和弱式主機模型」。](/previous-versions/technet-magazine/cc137807(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="c914e-133">For more information, see ["The Cable Guy: Strong and Weak Host Models."](/previous-versions/technet-magazine/cc137807(v=msdn.10))</span></span>

<span data-ttu-id="c914e-134">某些 [資料欄位](filtering-conditions.md) 在重新授權期間可能未知。</span><span class="sxs-lookup"><span data-stu-id="c914e-134">Some [classifiable fields](filtering-conditions.md) may be unknown during reauthorization.</span></span> <span data-ttu-id="c914e-135">例如，如果在 [**FWPM \_ 層的 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) 層重新授權輸出封包，則與抵達介面相關的所有欄位都是未知的。</span><span class="sxs-lookup"><span data-stu-id="c914e-135">For example, if an outbound packet is being reauthorized at the [**FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer, all the fields pertaining to the arrival interface are unknown.</span></span> <span data-ttu-id="c914e-136">在此情況下，未知欄位的值會表示為 [**.Fwp \_ 空白**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)。</span><span class="sxs-lookup"><span data-stu-id="c914e-136">In that case, the values of the unknown fields are indicated as [**FWP\_EMPTY**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span>

<span data-ttu-id="c914e-137">類型 [**\_ 為 .fwp 空白**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) 的欄位，可以比 [**對 \_ \_ 相等的 .fwp 相符**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type)。</span><span class="sxs-lookup"><span data-stu-id="c914e-137">Fields of type [**FWP\_EMPTY**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) can be matched with [**FWP\_MATCH\_EQUAL**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type).</span></span> <span data-ttu-id="c914e-138">因此，您可以設定原則來封鎖 reauthorizations，並在重新授權要求的 ALE 流量抵達時清除 ALE 流程。</span><span class="sxs-lookup"><span data-stu-id="c914e-138">Therefore, a policy can be set to block reauthorizations and tear down an ALE flow when reauthorization requests for the ALE flow arrive.</span></span>

## <a name="pending-connection-reauthorization"></a><span data-ttu-id="c914e-139">暫止連接重新授權</span><span class="sxs-lookup"><span data-stu-id="c914e-139">Pending Connection Reauthorization</span></span>

<span data-ttu-id="c914e-140">注標驅動程式可以延後 ALE 層級的分類作業，並在稍後安全地進行篩選決策時完成。</span><span class="sxs-lookup"><span data-stu-id="c914e-140">A callout driver may postpone a classify operation at ALE layers and complete it at a later time, when the filtering decision can be safely made.</span></span> <span data-ttu-id="c914e-141">ALE 延遲/完成功能是透過核心模式函式 [FwpsPendOperation0](/windows-hardware/drivers/ddi/fwpsk/nf-fwpsk-fwpspendoperation0) 和 [FwpsCompleteOperation0](/windows-hardware/drivers/ddi/fwpsk/nf-fwpsk-fwpscompleteoperation0)支援。</span><span class="sxs-lookup"><span data-stu-id="c914e-141">The ALE postpone/complete functionality is supported via the kernel-mode functions [FwpsPendOperation0](/windows-hardware/drivers/ddi/fwpsk/nf-fwpsk-fwpspendoperation0) and [FwpsCompleteOperation0](/windows-hardware/drivers/ddi/fwpsk/nf-fwpsk-fwpscompleteoperation0).</span></span>

<span data-ttu-id="c914e-142">重新授權會在 FwpsCompleteOperation0 呼叫之後立即觸發，並允許標注驅動程式允許或封鎖流程。</span><span class="sxs-lookup"><span data-stu-id="c914e-142">The reauthorization is triggered immediately following the FwpsCompleteOperation0 call, and it allows the callout driver to permit or to block the flow.</span></span>

<span data-ttu-id="c914e-143">只有初始授權可以延後。</span><span class="sxs-lookup"><span data-stu-id="c914e-143">Only an initial authorization can be postponed.</span></span> <span data-ttu-id="c914e-144">如果已設定 [ [**\_ 已設定 \_ \_ \_ 重新授權**](filtering-condition-flags-.md) 旗標] 旗標，呼叫 FwpsPendOperation0 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="c914e-144">A call to FwpsPendOperation0 will fail if [**FWP\_CONDITION\_FLAG\_IS\_REAUTHORIZE**](filtering-condition-flags-.md) flag is set.</span></span>

<span data-ttu-id="c914e-145">如需詳細資訊，請參閱 [Windows 驅動程式套件](/windows-hardware/drivers/ddi/_netvista/) 檔。</span><span class="sxs-lookup"><span data-stu-id="c914e-145">For more information, see the [Windows Driver Kit](/windows-hardware/drivers/ddi/_netvista/) documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c914e-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="c914e-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c914e-147">應用層強制 (ALE) </span><span class="sxs-lookup"><span data-stu-id="c914e-147">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="c914e-148">ALE 層</span><span class="sxs-lookup"><span data-stu-id="c914e-148">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="c914e-149">ALE 具狀態篩選</span><span class="sxs-lookup"><span data-stu-id="c914e-149">ALE Stateful Filtering</span></span>](ale-stateful-filtering.md)
</dt> <dt>

[<span data-ttu-id="c914e-150">ALE 多播/廣播流量</span><span class="sxs-lookup"><span data-stu-id="c914e-150">ALE Multicast/Broadcast Traffic</span></span>](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[<span data-ttu-id="c914e-151">ALE 流程自訂</span><span class="sxs-lookup"><span data-stu-id="c914e-151">ALE Flow Customization</span></span>](ale-flow-customization.md)
</dt> </dl>

 

 