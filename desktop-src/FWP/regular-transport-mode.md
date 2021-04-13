---
title: 傳輸模式
description: 傳輸模式 IPsec 原則案例需要所有相符流量的 IPsec 傳輸模式保護。
ms.assetid: 303f7cdc-fb7a-4e5c-8291-cadcb45035cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfb927aff1b3f0e3c7fd13a192f0fcb18fc3ec45
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375140"
---
# <a name="transport-mode"></a><span data-ttu-id="a67da-103">傳輸模式</span><span class="sxs-lookup"><span data-stu-id="a67da-103">Transport Mode</span></span>

<span data-ttu-id="a67da-104">傳輸模式 IPsec 原則案例需要所有相符流量的 IPsec 傳輸模式保護。</span><span class="sxs-lookup"><span data-stu-id="a67da-104">The Transport Mode IPsec policy scenario requires IPsec transport mode protection for all matching traffic.</span></span> <span data-ttu-id="a67da-105">任何相符的純文字流量都會中斷，直到 IKE 或 AuthIP 協商順利完成為止。</span><span class="sxs-lookup"><span data-stu-id="a67da-105">Any matching clear text traffic is dropped until the IKE or AuthIP negotiation has completed successfully.</span></span> <span data-ttu-id="a67da-106">如果協商失敗，與對應 IP 位址的連線仍會中斷。</span><span class="sxs-lookup"><span data-stu-id="a67da-106">If the negotiation fails, connectivity with the corresponding IP address will remain broken.</span></span>

<span data-ttu-id="a67da-107">可能的傳輸模式案例的範例是「使用 IPsec 傳輸模式保護所有單播資料流量（ICMP 除外）。」</span><span class="sxs-lookup"><span data-stu-id="a67da-107">An example of a possible Transport Mode scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode."</span></span>

<span data-ttu-id="a67da-108">若要以程式設計方式執行此範例，請使用下列 WFP 設定。</span><span class="sxs-lookup"><span data-stu-id="a67da-108">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="a67da-109">**在 FWPM \_ LAYER \_ IKEEXT \_ V {4 \| 6} 安裝程式 MM 的協商原則**</span><span class="sxs-lookup"><span data-stu-id="a67da-109">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} setup MM negotiation policy**</span></span>  

1.  <span data-ttu-id="a67da-110">新增下列一或兩個 MM 原則提供者內容。</span><span class="sxs-lookup"><span data-stu-id="a67da-110">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="a67da-111">針對 IKE， **FWPM \_ IPSEC \_ IKE \_ MM \_ coNtext** 型別的原則提供者內容。</span><span class="sxs-lookup"><span data-stu-id="a67da-111">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_MM\_CONTEXT**.</span></span>
    -   <span data-ttu-id="a67da-112">針對 AuthIP， **FWPM \_ IPSEC \_ AuthIP \_ MM \_ coNtext** 型別的原則提供者內容。</span><span class="sxs-lookup"><span data-stu-id="a67da-112">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT**.</span></span>

    > [!Note]  
    > <span data-ttu-id="a67da-113">系統將會協商一般的加密模組，並套用對應的 MM 原則。</span><span class="sxs-lookup"><span data-stu-id="a67da-113">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="a67da-114">如果支援 IKE 和 AuthIP，則 AuthIP 是慣用的金鑰模組。</span><span class="sxs-lookup"><span data-stu-id="a67da-114">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="a67da-115">針對步驟1中新增的每個內容，新增具有下列屬性的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="a67da-115">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 
    | <span data-ttu-id="a67da-116">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="a67da-116">Filter property</span></span>        | <span data-ttu-id="a67da-117">值</span><span class="sxs-lookup"><span data-stu-id="a67da-117">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="a67da-118">篩選準則</span><span class="sxs-lookup"><span data-stu-id="a67da-118">Filtering conditions</span></span>   | <span data-ttu-id="a67da-119">空白。</span><span class="sxs-lookup"><span data-stu-id="a67da-119">Empty.</span></span> <span data-ttu-id="a67da-120">所有流量都會符合篩選。</span><span class="sxs-lookup"><span data-stu-id="a67da-120">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="a67da-121">**providerCoNtextKey**</span><span class="sxs-lookup"><span data-stu-id="a67da-121">**providerContextKey**</span></span> | <span data-ttu-id="a67da-122">在步驟1中新增的 MM 提供者內容的 GUID。</span><span class="sxs-lookup"><span data-stu-id="a67da-122">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="a67da-123">**在 FWPM \_ 層 \_ \_ ，IPSEC V {4 \| 6} 安裝 QM 和 EM 協商原則**</span><span class="sxs-lookup"><span data-stu-id="a67da-123">**At FWPM\_LAYER\_IPSEC\_V{4\|6} setup QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="a67da-124">新增下列一或兩個 QM 傳輸模式原則提供者內容。</span><span class="sxs-lookup"><span data-stu-id="a67da-124">Add one or both of the following QM transport mode policy provider contexts.</span></span>  
    -   <span data-ttu-id="a67da-125">針對 IKE， **FWPM \_ IPSEC \_ IKE \_ QM \_ 傳輸 \_ 內容** 類型的原則提供者內容。</span><span class="sxs-lookup"><span data-stu-id="a67da-125">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT**.</span></span>
    -   <span data-ttu-id="a67da-126">針對 AuthIP，FWPM IPSEC AuthIP 型別的原則提供者內容 **\_ \_ \_ QM \_ 傳輸 \_ 內容**。</span><span class="sxs-lookup"><span data-stu-id="a67da-126">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT**.</span></span> <span data-ttu-id="a67da-127">此內容可以選擇性地包含 AuthIP 擴充模式 (EM) 的協商原則。</span><span class="sxs-lookup"><span data-stu-id="a67da-127">This context can optionally contain the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="a67da-128">系統將會協商一般的加密模組，並套用對應的 QM 原則。</span><span class="sxs-lookup"><span data-stu-id="a67da-128">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="a67da-129">如果支援 IKE 和 AuthIP，則 AuthIP 是慣用的金鑰模組。</span><span class="sxs-lookup"><span data-stu-id="a67da-129">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="a67da-130">針對步驟1中新增的每個內容，新增具有下列屬性的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="a67da-130">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 
    | <span data-ttu-id="a67da-131">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="a67da-131">Filter property</span></span>        | <span data-ttu-id="a67da-132">值</span><span class="sxs-lookup"><span data-stu-id="a67da-132">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="a67da-133">篩選準則</span><span class="sxs-lookup"><span data-stu-id="a67da-133">Filtering conditions</span></span>   | <span data-ttu-id="a67da-134">空白。</span><span class="sxs-lookup"><span data-stu-id="a67da-134">Empty.</span></span> <span data-ttu-id="a67da-135">所有流量都會符合篩選。</span><span class="sxs-lookup"><span data-stu-id="a67da-135">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="a67da-136">**providerCoNtextKey**</span><span class="sxs-lookup"><span data-stu-id="a67da-136">**providerContextKey**</span></span> | <span data-ttu-id="a67da-137">在步驟1中新增的 QM 提供者內容的 GUID。</span><span class="sxs-lookup"><span data-stu-id="a67da-137">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="a67da-138">**在 FWPM \_ 層 \_ 輸入 \_ 傳輸 \_ V {4 \| 6} 設定輸入每個封包篩選規則**</span><span class="sxs-lookup"><span data-stu-id="a67da-138">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="a67da-139">新增具有下列屬性的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="a67da-139">Add a filter with the following properties.</span></span> 
    | <span data-ttu-id="a67da-140">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="a67da-140">Filter property</span></span>                                                   | <span data-ttu-id="a67da-141">值</span><span class="sxs-lookup"><span data-stu-id="a67da-141">Value</span></span>                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | <span data-ttu-id="a67da-142">**FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="a67da-142">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="a67da-143">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="a67da-143">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | <span data-ttu-id="a67da-144">**動作。類型**</span><span class="sxs-lookup"><span data-stu-id="a67da-144">**action.type**</span></span>                                                   | <span data-ttu-id="a67da-145">已 \_ 終止的 .FWP 動作 \_ 標注 \_</span><span class="sxs-lookup"><span data-stu-id="a67da-145">FWP\_ACTION\_CALLOUT\_TERMINATING</span></span>                             |
    | <span data-ttu-id="a67da-146">**calloutKey**</span><span class="sxs-lookup"><span data-stu-id="a67da-146">**action.calloutKey**</span></span>                                             | <span data-ttu-id="a67da-147">FWPM \_ 標注 \_ IPSEC \_ 輸入 \_ 傳輸 \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="a67da-147">FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}</span></span>             |

        
2.  <span data-ttu-id="a67da-148">藉由新增具有下列屬性的篩選準則，從 IPsec 豁免 ICMP 流量。</span><span class="sxs-lookup"><span data-stu-id="a67da-148">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>
    | <span data-ttu-id="a67da-149">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="a67da-149">Filter property</span></span>                                                  | <span data-ttu-id="a67da-150">值</span><span class="sxs-lookup"><span data-stu-id="a67da-150">Value</span></span>                                                                     |
    |------------------------------------------------------------------|---------------------------------------------------------------------------|
    | <span data-ttu-id="a67da-151">**FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="a67da-151">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="a67da-152">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="a67da-152">NlatUnicast</span></span>                                                               |
    | <span data-ttu-id="a67da-153">**FWPM \_條件 \_ IP \_ 通訊協定** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="a67da-153">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>            | <span data-ttu-id="a67da-154">IPPROTO \_ ICMP {V6} 這些常數定義于 winsock2. h 中。</span><span class="sxs-lookup"><span data-stu-id="a67da-154">IPPROTO\_ICMP{V6}These constants are defined in winsock2.h.</span></span><br/>    |
    | <span data-ttu-id="a67da-155">**動作。類型**</span><span class="sxs-lookup"><span data-stu-id="a67da-155">**action.type**</span></span>                                                  | <span data-ttu-id="a67da-156">已 \_ 允許的 .FWP 動作 \_</span><span class="sxs-lookup"><span data-stu-id="a67da-156">FWP\_ACTION\_PERMIT</span></span>                                                       |
    | <span data-ttu-id="a67da-157">**weight**</span><span class="sxs-lookup"><span data-stu-id="a67da-157">**weight**</span></span>                                                       | [<span data-ttu-id="a67da-158">**FWPM \_ 權數 \_ 範圍 \_ IKE \_ 豁免**</span><span class="sxs-lookup"><span data-stu-id="a67da-158">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md) |

        

<span data-ttu-id="a67da-159">**在 FWPM \_ 層 \_ 輸出 \_ 傳輸 \_ V {4 \| 6} 上，設定每個封包篩選規則的輸出**</span><span class="sxs-lookup"><span data-stu-id="a67da-159">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="a67da-160">新增具有下列屬性的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="a67da-160">Add a filter with the following properties.</span></span>
    | <span data-ttu-id="a67da-161">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="a67da-161">Filter property</span></span>                                                   | <span data-ttu-id="a67da-162">值</span><span class="sxs-lookup"><span data-stu-id="a67da-162">Value</span></span>                                              |
    |-------------------------------------------------------------------|----------------------------------------------------|
    | <span data-ttu-id="a67da-163">**FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="a67da-163">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="a67da-164">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="a67da-164">NlatUnicast</span></span>                                        |
    | <span data-ttu-id="a67da-165">**動作。類型**</span><span class="sxs-lookup"><span data-stu-id="a67da-165">**action.type**</span></span>                                                   | <span data-ttu-id="a67da-166">**已 \_ 終止的 .FWP 動作 \_ 標注 \_**</span><span class="sxs-lookup"><span data-stu-id="a67da-166">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>              |
    | <span data-ttu-id="a67da-167">**calloutKey**</span><span class="sxs-lookup"><span data-stu-id="a67da-167">**action.calloutKey**</span></span>                                             | <span data-ttu-id="a67da-168">FWPM \_ 標注 \_ IPSEC \_ 輸出 \_ 傳輸 \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="a67da-168">FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}</span></span> |

        
2.  <span data-ttu-id="a67da-169">藉由新增具有下列屬性的篩選準則，從 IPsec 豁免 ICMP 流量。</span><span class="sxs-lookup"><span data-stu-id="a67da-169">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>
    | <span data-ttu-id="a67da-170">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="a67da-170">Filter property</span></span>                                                   | <span data-ttu-id="a67da-171">值</span><span class="sxs-lookup"><span data-stu-id="a67da-171">Value</span></span>                                                                  |
    |-------------------------------------------------------------------|------------------------------------------------------------------------|
    | <span data-ttu-id="a67da-172">**FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="a67da-172">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="a67da-173">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="a67da-173">NlatUnicast</span></span>                                                            |
    | <span data-ttu-id="a67da-174">**FWPM \_條件 \_ IP \_ 通訊協定** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="a67da-174">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="a67da-175">IPPROTO \_ ICMP {V6} 這些常數定義于 winsock2. h 中。</span><span class="sxs-lookup"><span data-stu-id="a67da-175">IPPROTO\_ICMP{V6}These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="a67da-176">**動作。類型**</span><span class="sxs-lookup"><span data-stu-id="a67da-176">**action.type**</span></span>                                                   | <span data-ttu-id="a67da-177">已 \_ 允許的 .FWP 動作 \_</span><span class="sxs-lookup"><span data-stu-id="a67da-177">FWP\_ACTION\_PERMIT</span></span>                                                    |
    | <span data-ttu-id="a67da-178">**weight**</span><span class="sxs-lookup"><span data-stu-id="a67da-178">**weight**</span></span>                                                        | <span data-ttu-id="a67da-179">FWPM \_ 權數 \_ 範圍 \_ IKE \_ 豁免</span><span class="sxs-lookup"><span data-stu-id="a67da-179">FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS</span></span>                                   |

        

</dl>

## <a name="related-topics"></a><span data-ttu-id="a67da-180">相關主題</span><span class="sxs-lookup"><span data-stu-id="a67da-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a67da-181">範例程式碼：使用傳輸模式</span><span class="sxs-lookup"><span data-stu-id="a67da-181">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="a67da-182">**篩選層識別碼**</span><span class="sxs-lookup"><span data-stu-id="a67da-182">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="a67da-183">**提供者內容類型**</span><span class="sxs-lookup"><span data-stu-id="a67da-183">**Provider Context Types**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> <dt>

[<span data-ttu-id="a67da-184">篩選準則</span><span class="sxs-lookup"><span data-stu-id="a67da-184">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="a67da-185">**FWPM \_ ACTION0**</span><span class="sxs-lookup"><span data-stu-id="a67da-185">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="a67da-186">**內建的標注識別碼**</span><span class="sxs-lookup"><span data-stu-id="a67da-186">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> </dl>

 

