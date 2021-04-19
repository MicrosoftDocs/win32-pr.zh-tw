---
title: 界限模式中的協商探索傳輸模式
description: 界限模式 IPsec 原則案例中的協商探索傳輸模式會要求所有相符流量的 IPsec 傳輸模式保護。
ms.assetid: 36ae74b3-30f5-49bd-8855-6f3c0fb04d70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9869be61923bff1c392c5abe2bd98099a0c3c89f
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314591"
---
# <a name="negotiation-discovery-transport-mode-in-boundary-mode"></a><span data-ttu-id="7cc9b-103">界限模式中的協商探索傳輸模式</span><span class="sxs-lookup"><span data-stu-id="7cc9b-103">Negotiation Discovery Transport Mode in Boundary Mode</span></span>

<span data-ttu-id="7cc9b-104">界限模式 IPsec 原則案例中的協商探索傳輸模式會要求所有相符流量的 IPsec 傳輸模式保護。</span><span class="sxs-lookup"><span data-stu-id="7cc9b-104">The Negotiation Discovery Transport Mode in Boundary Mode IPsec policy scenario requests IPsec transport mode protection for all matching traffic.</span></span> <span data-ttu-id="7cc9b-105">如果 IKE/AuthIP 協商失敗，則會允許輸入和輸出連接回復為純文字。</span><span class="sxs-lookup"><span data-stu-id="7cc9b-105">If the IKE/AuthIP negotiation fails, both inbound and outbound connections are allowed to fallback to clear-text .</span></span>

<span data-ttu-id="7cc9b-106">此 IPsec 原則通常用於受 IPsec 支援和非 IPsec 功能的電腦所存取的電腦。</span><span class="sxs-lookup"><span data-stu-id="7cc9b-106">This IPsec policy is typically used on machines that are accessed by both IPsec capable and non-IPsec capable machines.</span></span>

<span data-ttu-id="7cc9b-107">可能的「協商探索」傳輸模式案例的範例是「使用 IPsec 傳輸模式保護所有單播資料流量（ICMP 除外），並在界限模式中啟用協調探索」。</span><span class="sxs-lookup"><span data-stu-id="7cc9b-107">An example of a potential Negotiation Discovery Transport Mode scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode and enable negotiation discovery in boundary mode."</span></span>

<span data-ttu-id="7cc9b-108">若要以程式設計方式執行此範例，請使用下列 WFP 設定。</span><span class="sxs-lookup"><span data-stu-id="7cc9b-108">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="7cc9b-109">**在 FWPM \_ LAYER \_ IKEEXT \_ V {4 \| 6} 安裝程式 MM 的協商原則**</span><span class="sxs-lookup"><span data-stu-id="7cc9b-109">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} setup MM negotiation policy**</span></span>  

1.  <span data-ttu-id="7cc9b-110">新增下列一或兩個 MM 原則提供者內容。</span><span class="sxs-lookup"><span data-stu-id="7cc9b-110">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="7cc9b-111">針對 IKE，FWPM \_ IPSEC \_ IKE \_ MM coNtext 型別的原則提供者內容 \_ 。</span><span class="sxs-lookup"><span data-stu-id="7cc9b-111">For IKE, a policy provider context of type FWPM\_IPSEC\_IKE\_MM\_CONTEXT.</span></span>
    -   <span data-ttu-id="7cc9b-112">針對 AuthIP，FWPM \_ IPSEC \_ AuthIP \_ MM coNtext 型別的原則提供者內容 \_ 。</span><span class="sxs-lookup"><span data-stu-id="7cc9b-112">For AuthIP, a policy provider context of type FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT.</span></span>

    > [!Note]  
    > <span data-ttu-id="7cc9b-113">系統將會協商一般的加密模組，並套用對應的 MM 原則。</span><span class="sxs-lookup"><span data-stu-id="7cc9b-113">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="7cc9b-114">如果支援 IKE 和 AuthIP，則 AuthIP 是慣用的金鑰模組。</span><span class="sxs-lookup"><span data-stu-id="7cc9b-114">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="7cc9b-115">針對步驟1中新增的每個內容，新增具有下列屬性的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="7cc9b-115">For each of the contexts added in step 1, add a filter with the following properties.</span></span>

    | <span data-ttu-id="7cc9b-116">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="7cc9b-116">Filter property</span></span>        | <span data-ttu-id="7cc9b-117">值</span><span class="sxs-lookup"><span data-stu-id="7cc9b-117">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="7cc9b-118">篩選準則</span><span class="sxs-lookup"><span data-stu-id="7cc9b-118">Filtering conditions</span></span>   | <span data-ttu-id="7cc9b-119">空白。</span><span class="sxs-lookup"><span data-stu-id="7cc9b-119">Empty.</span></span> <span data-ttu-id="7cc9b-120">所有流量都會符合篩選。</span><span class="sxs-lookup"><span data-stu-id="7cc9b-120">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="7cc9b-121">**providerCoNtextKey**</span><span class="sxs-lookup"><span data-stu-id="7cc9b-121">**providerContextKey**</span></span> | <span data-ttu-id="7cc9b-122">在步驟1中新增的 MM 提供者內容的 GUID。</span><span class="sxs-lookup"><span data-stu-id="7cc9b-122">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="7cc9b-123">**在 FWPM \_ 層 \_ \_ ，IPSEC V {4 \| 6} 安裝 QM 和 EM 協商原則**</span><span class="sxs-lookup"><span data-stu-id="7cc9b-123">**At FWPM\_LAYER\_IPSEC\_V{4\|6} setup QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="7cc9b-124">新增下列一或兩個 QM 傳輸模式原則提供者內容，並設定 [**IPSEC \_ 原則 \_ 旗標 \_ ND \_ 界限**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) 旗標。</span><span class="sxs-lookup"><span data-stu-id="7cc9b-124">Add one or both of the following QM transport mode policy provider contexts and set the [**IPSEC\_POLICY\_FLAG\_ND\_BOUNDARY**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) flag.</span></span>  
    -   <span data-ttu-id="7cc9b-125">針對 IKE， **FWPM \_ IPSEC \_ IKE \_ QM \_ 傳輸 \_ 內容** 類型的原則提供者內容。</span><span class="sxs-lookup"><span data-stu-id="7cc9b-125">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT**.</span></span>
    -   <span data-ttu-id="7cc9b-126">針對 AuthIP，FWPM IPSEC AuthIP 型別的原則提供者內容 **\_ \_ \_ QM \_ 傳輸 \_ 內容**。</span><span class="sxs-lookup"><span data-stu-id="7cc9b-126">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT**.</span></span> <span data-ttu-id="7cc9b-127">此內容可以選擇性地包含 AuthIP 擴充模式 (EM) 的協商原則。</span><span class="sxs-lookup"><span data-stu-id="7cc9b-127">This context can optionally contain the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="7cc9b-128">系統將會協商一般的加密模組，並套用對應的 QM 原則。</span><span class="sxs-lookup"><span data-stu-id="7cc9b-128">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="7cc9b-129">如果支援 IKE 和 AuthIP，則 AuthIP 是慣用的金鑰模組。</span><span class="sxs-lookup"><span data-stu-id="7cc9b-129">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="7cc9b-130">針對步驟1中新增的每個內容，新增具有下列屬性的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="7cc9b-130">For each of the contexts added in step 1, add a filter with the following properties.</span></span>

    | <span data-ttu-id="7cc9b-131">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="7cc9b-131">Filter property</span></span>        | <span data-ttu-id="7cc9b-132">值</span><span class="sxs-lookup"><span data-stu-id="7cc9b-132">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="7cc9b-133">篩選準則</span><span class="sxs-lookup"><span data-stu-id="7cc9b-133">Filtering conditions</span></span>   | <span data-ttu-id="7cc9b-134">空白。</span><span class="sxs-lookup"><span data-stu-id="7cc9b-134">Empty.</span></span> <span data-ttu-id="7cc9b-135">所有流量都會符合篩選。</span><span class="sxs-lookup"><span data-stu-id="7cc9b-135">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="7cc9b-136">**providerCoNtextKey**</span><span class="sxs-lookup"><span data-stu-id="7cc9b-136">**providerContextKey**</span></span> | <span data-ttu-id="7cc9b-137">在步驟1中新增的 QM 提供者內容的 GUID。</span><span class="sxs-lookup"><span data-stu-id="7cc9b-137">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="7cc9b-138">**在 FWPM \_ 層 \_ 輸入 \_ 傳輸 \_ V {4 \| 6} 設定輸入每個封包篩選規則**</span><span class="sxs-lookup"><span data-stu-id="7cc9b-138">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="7cc9b-139">新增具有下列屬性的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="7cc9b-139">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="7cc9b-140">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="7cc9b-140">Filter property</span></span>                                                   | <span data-ttu-id="7cc9b-141">值</span><span class="sxs-lookup"><span data-stu-id="7cc9b-141">Value</span></span>                                                                                              |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="7cc9b-142">**FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="7cc9b-142">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="7cc9b-143">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="7cc9b-143">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | <span data-ttu-id="7cc9b-144">**動作。類型**</span><span class="sxs-lookup"><span data-stu-id="7cc9b-144">**action.type**</span></span>                                                   | <span data-ttu-id="7cc9b-145">**已 \_ 終止的 .FWP 動作 \_ 標注 \_**</span><span class="sxs-lookup"><span data-stu-id="7cc9b-145">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                              |
    | <span data-ttu-id="7cc9b-146">**calloutKey**</span><span class="sxs-lookup"><span data-stu-id="7cc9b-146">**action.calloutKey**</span></span>                                             | <span data-ttu-id="7cc9b-147">**FWPM \_ 標注 \_ IPSEC \_ 輸入 \_ 傳輸 \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="7cc9b-147">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                              |
    | <span data-ttu-id="7cc9b-148">**rawCoNtext**</span><span class="sxs-lookup"><span data-stu-id="7cc9b-148">**rawContext**</span></span>                                                    | [<span data-ttu-id="7cc9b-149">**FWPM \_ 內容 \_ IPSEC \_ 輸入 \_ 保存 \_ 連接 \_ 安全性**</span><span class="sxs-lookup"><span data-stu-id="7cc9b-149">**FWPM\_CONTEXT\_IPSEC\_INBOUND\_PERSIST\_CONNECTION\_SECURITY**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="7cc9b-150">藉由新增具有下列屬性的篩選準則，從 IPsec 豁免 ICMP 流量。</span><span class="sxs-lookup"><span data-stu-id="7cc9b-150">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="7cc9b-151">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="7cc9b-151">Filter property</span></span>                                                   | <span data-ttu-id="7cc9b-152">值</span><span class="sxs-lookup"><span data-stu-id="7cc9b-152">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="7cc9b-153">**FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="7cc9b-153">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="7cc9b-154">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="7cc9b-154">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="7cc9b-155">**FWPM \_條件 \_ IP \_ 通訊協定** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="7cc9b-155">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="7cc9b-156">**IPPROTO \_ICMP {V6}** 這些常數定義于 winsock2. h 中。</span><span class="sxs-lookup"><span data-stu-id="7cc9b-156">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="7cc9b-157">**動作。類型**</span><span class="sxs-lookup"><span data-stu-id="7cc9b-157">**action.type**</span></span>                                                   | <span data-ttu-id="7cc9b-158">已 \_ 允許的 .FWP 動作 \_</span><span class="sxs-lookup"><span data-stu-id="7cc9b-158">FWP\_ACTION\_PERMIT</span></span>                                                        |
    | <span data-ttu-id="7cc9b-159">**weight**</span><span class="sxs-lookup"><span data-stu-id="7cc9b-159">**weight**</span></span>                                                        | [<span data-ttu-id="7cc9b-160">**FWPM \_ 權數 \_ 範圍 \_ IKE \_ 豁免**</span><span class="sxs-lookup"><span data-stu-id="7cc9b-160">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="7cc9b-161">**在 FWPM \_ 層 \_ 輸出 \_ 傳輸 \_ V {4 \| 6} 上，設定每個封包篩選規則的輸出**</span><span class="sxs-lookup"><span data-stu-id="7cc9b-161">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="7cc9b-162">新增具有下列屬性的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="7cc9b-162">Add a filter with the following properties.</span></span>

    | <span data-ttu-id="7cc9b-163">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="7cc9b-163">Filter property</span></span>                                                   | <span data-ttu-id="7cc9b-164">值</span><span class="sxs-lookup"><span data-stu-id="7cc9b-164">Value</span></span>                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | <span data-ttu-id="7cc9b-165">**FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="7cc9b-165">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="7cc9b-166">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="7cc9b-166">NlatUnicast</span></span>                                                                               |
    | <span data-ttu-id="7cc9b-167">**動作。類型**</span><span class="sxs-lookup"><span data-stu-id="7cc9b-167">**action.type**</span></span>                                                   | <span data-ttu-id="7cc9b-168">**已 \_ 終止的 .FWP 動作 \_ 標注 \_**</span><span class="sxs-lookup"><span data-stu-id="7cc9b-168">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                     |
    | <span data-ttu-id="7cc9b-169">**calloutKey**</span><span class="sxs-lookup"><span data-stu-id="7cc9b-169">**action.calloutKey**</span></span>                                             | <span data-ttu-id="7cc9b-170">**FWPM \_ 標注 \_ IPSEC \_ 輸出 \_ 傳輸 \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="7cc9b-170">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                    |
    | <span data-ttu-id="7cc9b-171">**rawCoNtext**</span><span class="sxs-lookup"><span data-stu-id="7cc9b-171">**rawContext**</span></span>                                                    | [<span data-ttu-id="7cc9b-172">**FWPM \_ 內容 \_ IPSEC \_ 輸出 \_ 協商 \_ 探索**</span><span class="sxs-lookup"><span data-stu-id="7cc9b-172">**FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_NEGOTIATE\_DISCOVER**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="7cc9b-173">藉由新增具有下列屬性的篩選準則，從 IPsec 豁免 ICMP 流量。</span><span class="sxs-lookup"><span data-stu-id="7cc9b-173">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="7cc9b-174">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="7cc9b-174">Filter property</span></span>                                                   | <span data-ttu-id="7cc9b-175">值</span><span class="sxs-lookup"><span data-stu-id="7cc9b-175">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="7cc9b-176">**FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="7cc9b-176">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="7cc9b-177">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="7cc9b-177">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="7cc9b-178">**FWPM \_條件 \_ IP \_ 通訊協定** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="7cc9b-178">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="7cc9b-179">**IPPROTO \_ICMP {V6}** 這些常數定義于 winsock2. h 中。</span><span class="sxs-lookup"><span data-stu-id="7cc9b-179">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="7cc9b-180">**動作。類型**</span><span class="sxs-lookup"><span data-stu-id="7cc9b-180">**action.type**</span></span>                                                   | <span data-ttu-id="7cc9b-181">**已 \_ 允許的 .FWP 動作 \_**</span><span class="sxs-lookup"><span data-stu-id="7cc9b-181">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="7cc9b-182">**weight**</span><span class="sxs-lookup"><span data-stu-id="7cc9b-182">**weight**</span></span>                                                        | <span data-ttu-id="7cc9b-183">**FWPM \_ 權數 \_ 範圍 \_ IKE \_ 豁免**</span><span class="sxs-lookup"><span data-stu-id="7cc9b-183">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

</dl>

> [!Note]  
> <span data-ttu-id="7cc9b-184">相對於協商探索傳輸模式，在界限模式原則中的協商探索傳輸模式，不需要在 **FWPM \_ 層的 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}** 層中新增篩選，因為此原則允許輸入未受保護的純文字連接。</span><span class="sxs-lookup"><span data-stu-id="7cc9b-184">As opposed to Negotiation Discovery Transport Mode, for Negotiation Discovery Transport Mode in Boundary Mode policy there is no need to add a filter at the **FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}** layers because this policy allows inbound unprotected clear-text connections.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="7cc9b-185">相關主題</span><span class="sxs-lookup"><span data-stu-id="7cc9b-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cc9b-186">範例程式碼：使用傳輸模式</span><span class="sxs-lookup"><span data-stu-id="7cc9b-186">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="7cc9b-187">ALE 層</span><span class="sxs-lookup"><span data-stu-id="7cc9b-187">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="7cc9b-188">**內建的標注識別碼**</span><span class="sxs-lookup"><span data-stu-id="7cc9b-188">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="7cc9b-189">篩選準則</span><span class="sxs-lookup"><span data-stu-id="7cc9b-189">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="7cc9b-190">**篩選層識別碼**</span><span class="sxs-lookup"><span data-stu-id="7cc9b-190">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="7cc9b-191">**FWPM \_ ACTION0**</span><span class="sxs-lookup"><span data-stu-id="7cc9b-191">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="7cc9b-192">**FWPM \_ 提供者 \_ 內容 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="7cc9b-192">**FWPM\_PROVIDER\_CONTEXT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

