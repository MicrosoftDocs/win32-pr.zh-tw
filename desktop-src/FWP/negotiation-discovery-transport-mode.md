---
title: 協商探索傳輸模式
description: 協商探索傳輸模式 IPsec 原則案例需要 IPsec 傳輸模式保護，才能使用所有相符的連入流量，並要求 IPsec 保護以進行相符的輸出流量。
ms.assetid: c08d9d03-7d77-43c2-8468-964b498b45f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df9477d18f2fe478f5c885c071f47d0bf2baaad8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842127"
---
# <a name="negotiation-discovery-transport-mode"></a><span data-ttu-id="1762f-103">協商探索傳輸模式</span><span class="sxs-lookup"><span data-stu-id="1762f-103">Negotiation Discovery Transport Mode</span></span>

<span data-ttu-id="1762f-104">協商探索傳輸模式 IPsec 原則案例需要 IPsec 傳輸模式保護，才能使用所有相符的連入流量，並要求 IPsec 保護以進行相符的輸出流量。</span><span class="sxs-lookup"><span data-stu-id="1762f-104">The Negotiation Discovery Transport Mode IPsec policy scenario requires IPsec transport mode protection for all matching inbound traffic, and requests IPsec protection for matching outbound traffic.</span></span> <span data-ttu-id="1762f-105">因此，當輸入連接不是時，允許輸出連線回復為純文字。</span><span class="sxs-lookup"><span data-stu-id="1762f-105">Therefore, outbound connections are allowed to fallback to clear-text while inbound connections are not.</span></span>

<span data-ttu-id="1762f-106">使用此原則時，當主機電腦嘗試新的輸出連線，而且沒有符合流量的現有 IPsec SA 時，主機會以純文字方式傳送封包，並啟動 IKE 或 AuthIP 的協商。</span><span class="sxs-lookup"><span data-stu-id="1762f-106">With this policy, when the host machine attempts a new outbound connection and there is no existing IPsec SA matching the traffic, the host simultaneously sends the packets in clear-text and starts an IKE or AuthIP negotiation.</span></span> <span data-ttu-id="1762f-107">如果協商成功，則連接會升級為受 IPsec 保護。</span><span class="sxs-lookup"><span data-stu-id="1762f-107">If the negotiation succeeds, the connection is upgraded to IPsec-protected.</span></span> <span data-ttu-id="1762f-108">否則，連接會保持為純文字。</span><span class="sxs-lookup"><span data-stu-id="1762f-108">Otherwise, the connection stays in clear-text.</span></span> <span data-ttu-id="1762f-109">受 IPsec 保護之後，連接永遠不會降級為純文字。</span><span class="sxs-lookup"><span data-stu-id="1762f-109">Once IPsec-protected, a connection can never be downgraded to clear-text.</span></span>

<span data-ttu-id="1762f-110">協調探索傳輸模式通常用於包含支援 IPsec 和非 IPsec 功能之電腦的環境中。</span><span class="sxs-lookup"><span data-stu-id="1762f-110">Negotiation Discovery Transport Mode is typically used in environments that include both IPsec capable and non-IPsec capable machines.</span></span>

<span data-ttu-id="1762f-111">可能的協商探索傳輸模式案例的其中一個範例是「使用 IPsec 傳輸模式保護所有單播資料流量（ICMP 除外），並啟用協調探索」。</span><span class="sxs-lookup"><span data-stu-id="1762f-111">An example of a possible Negotiation Discovery Transport Mode scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode, and enable negotiation discovery."</span></span>

<span data-ttu-id="1762f-112">若要以程式設計方式執行此範例，請使用下列 WFP 設定。</span><span class="sxs-lookup"><span data-stu-id="1762f-112">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="1762f-113">**在 FWPM \_ LAYER \_ IKEEXT \_ V {4 \| 6} 設定 MM 協商原則**</span><span class="sxs-lookup"><span data-stu-id="1762f-113">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} set up MM negotiation policy**</span></span>  

1.  <span data-ttu-id="1762f-114">新增下列一或兩個 MM 原則提供者內容。</span><span class="sxs-lookup"><span data-stu-id="1762f-114">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="1762f-115">針對 IKE， **FWPM \_ IPSEC \_ IKE \_ MM \_ coNtext** 型別的原則提供者內容。</span><span class="sxs-lookup"><span data-stu-id="1762f-115">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_MM\_CONTEXT**.</span></span>
    -   <span data-ttu-id="1762f-116">針對 AuthIP， **FWPM \_ IPSEC \_ AuthIP \_ MM \_ coNtext** 型別的原則提供者內容。</span><span class="sxs-lookup"><span data-stu-id="1762f-116">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT**.</span></span>

    > [!Note]  
    > <span data-ttu-id="1762f-117">系統將會協商一般的加密模組，並套用對應的 MM 原則。</span><span class="sxs-lookup"><span data-stu-id="1762f-117">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="1762f-118">如果支援 IKE 和 AuthIP，則 AuthIP 是慣用的金鑰模組。</span><span class="sxs-lookup"><span data-stu-id="1762f-118">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="1762f-119">針對步驟1中新增的每個內容，新增具有下列屬性的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="1762f-119">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 
    | <span data-ttu-id="1762f-120">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="1762f-120">Filter property</span></span>        | <span data-ttu-id="1762f-121">值</span><span class="sxs-lookup"><span data-stu-id="1762f-121">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="1762f-122">篩選準則</span><span class="sxs-lookup"><span data-stu-id="1762f-122">Filtering conditions</span></span>   | <span data-ttu-id="1762f-123">空白。</span><span class="sxs-lookup"><span data-stu-id="1762f-123">Empty.</span></span> <span data-ttu-id="1762f-124">所有流量都會符合篩選。</span><span class="sxs-lookup"><span data-stu-id="1762f-124">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="1762f-125">**providerCoNtextKey**</span><span class="sxs-lookup"><span data-stu-id="1762f-125">**providerContextKey**</span></span> | <span data-ttu-id="1762f-126">在步驟1中新增的 MM 提供者內容的 GUID。</span><span class="sxs-lookup"><span data-stu-id="1762f-126">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="1762f-127">**在 FWPM \_ 層， \_ IPSEC \_ V {4 \| 6} 設定 QM 和 EM 協商原則**</span><span class="sxs-lookup"><span data-stu-id="1762f-127">**At FWPM\_LAYER\_IPSEC\_V{4\|6} set up QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="1762f-128">新增下列一或兩個 QM 傳輸模式原則提供者內容，並設定 [**IPSEC \_ 原則 \_ 旗標 \_ ND \_ 安全**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) 旗標。</span><span class="sxs-lookup"><span data-stu-id="1762f-128">Add one or both of the following QM transport mode policy provider contexts and set the [**IPSEC\_POLICY\_FLAG\_ND\_SECURE**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) flag.</span></span>  
    -   <span data-ttu-id="1762f-129">針對 IKE，FWPM \_ IPSEC \_ IKE \_ QM \_ 傳輸 \_ 內容類型的原則提供者內容。</span><span class="sxs-lookup"><span data-stu-id="1762f-129">For IKE, a policy provider context of type FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT.</span></span>
    -   <span data-ttu-id="1762f-130">針對 AuthIP，FWPM IPSEC AuthIP 型別的原則提供者內容 \_ \_ \_ QM \_ 傳輸 \_ 內容。</span><span class="sxs-lookup"><span data-stu-id="1762f-130">For AuthIP, a policy provider context of type FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT.</span></span> <span data-ttu-id="1762f-131">此內容可以選擇性地包含 AuthIP 擴充模式 (EM) 的協商原則。</span><span class="sxs-lookup"><span data-stu-id="1762f-131">This context can optionally contain the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="1762f-132">系統將會協商一般的加密模組，並套用對應的 QM 原則。</span><span class="sxs-lookup"><span data-stu-id="1762f-132">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="1762f-133">如果支援 IKE 和 AuthIP，則 AuthIP 是慣用的金鑰模組。</span><span class="sxs-lookup"><span data-stu-id="1762f-133">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="1762f-134">針對步驟1中新增的每個內容，新增具有下列屬性的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="1762f-134">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 
    | <span data-ttu-id="1762f-135">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="1762f-135">Filter property</span></span>        | <span data-ttu-id="1762f-136">值</span><span class="sxs-lookup"><span data-stu-id="1762f-136">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="1762f-137">篩選準則</span><span class="sxs-lookup"><span data-stu-id="1762f-137">Filtering conditions</span></span>   | <span data-ttu-id="1762f-138">空白。</span><span class="sxs-lookup"><span data-stu-id="1762f-138">Empty.</span></span> <span data-ttu-id="1762f-139">所有流量都會符合篩選。</span><span class="sxs-lookup"><span data-stu-id="1762f-139">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="1762f-140">**providerCoNtextKey**</span><span class="sxs-lookup"><span data-stu-id="1762f-140">**providerContextKey**</span></span> | <span data-ttu-id="1762f-141">在步驟1中新增的 QM 提供者內容的 GUID。</span><span class="sxs-lookup"><span data-stu-id="1762f-141">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="1762f-142">**在 FWPM \_ 層 \_ 輸入 \_ 傳輸 \_ V {4 \| 6} 設定輸入的每個封包篩選規則**</span><span class="sxs-lookup"><span data-stu-id="1762f-142">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} set up inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="1762f-143">新增具有下列屬性的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="1762f-143">Add a filter with the following properties.</span></span> 
    | <span data-ttu-id="1762f-144">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="1762f-144">Filter property</span></span>                                                   | <span data-ttu-id="1762f-145">值</span><span class="sxs-lookup"><span data-stu-id="1762f-145">Value</span></span>                                                                                              |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="1762f-146">**FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="1762f-146">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="1762f-147">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="1762f-147">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | <span data-ttu-id="1762f-148">**動作。類型**</span><span class="sxs-lookup"><span data-stu-id="1762f-148">**action.type**</span></span>                                                   | <span data-ttu-id="1762f-149">**已 \_ 終止的 .FWP 動作 \_ 標注 \_**</span><span class="sxs-lookup"><span data-stu-id="1762f-149">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                              |
    | <span data-ttu-id="1762f-150">**calloutKey**</span><span class="sxs-lookup"><span data-stu-id="1762f-150">**action.calloutKey**</span></span>                                             | <span data-ttu-id="1762f-151">**FWPM \_ 標注 \_ IPSEC \_ 輸入 \_ 傳輸 \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="1762f-151">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                              |
    | <span data-ttu-id="1762f-152">**rawCoNtext**</span><span class="sxs-lookup"><span data-stu-id="1762f-152">**rawContext**</span></span>                                                    | [<span data-ttu-id="1762f-153">**FWPM \_ 內容 \_ IPSEC \_ 輸入 \_ 保存 \_ 連接 \_ 安全性**</span><span class="sxs-lookup"><span data-stu-id="1762f-153">**FWPM\_CONTEXT\_IPSEC\_INBOUND\_PERSIST\_CONNECTION\_SECURITY**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="1762f-154">藉由新增具有下列屬性的篩選準則，從 IPsec 豁免 ICMP 流量。</span><span class="sxs-lookup"><span data-stu-id="1762f-154">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>
    | <span data-ttu-id="1762f-155">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="1762f-155">Filter property</span></span>                                                   | <span data-ttu-id="1762f-156">值</span><span class="sxs-lookup"><span data-stu-id="1762f-156">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="1762f-157">**FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="1762f-157">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="1762f-158">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="1762f-158">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="1762f-159">**FWPM \_條件 \_ IP \_ 通訊協定** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="1762f-159">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="1762f-160">**IPPROTO \_ICMP {V6}** 這些常數定義于 winsock2. h 中。</span><span class="sxs-lookup"><span data-stu-id="1762f-160">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="1762f-161">**動作。類型**</span><span class="sxs-lookup"><span data-stu-id="1762f-161">**action.type**</span></span>                                                   | <span data-ttu-id="1762f-162">**已 \_ 允許的 .FWP 動作 \_**</span><span class="sxs-lookup"><span data-stu-id="1762f-162">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="1762f-163">**weight**</span><span class="sxs-lookup"><span data-stu-id="1762f-163">**weight**</span></span>                                                        | [<span data-ttu-id="1762f-164">**FWPM \_ 權數 \_ 範圍 \_ IKE \_ 豁免**</span><span class="sxs-lookup"><span data-stu-id="1762f-164">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="1762f-165">**在 FWPM \_ 層 \_ 輸出 \_ 傳輸 \_ V {4 \| 6} 上，設定每個封包篩選規則的輸出**</span><span class="sxs-lookup"><span data-stu-id="1762f-165">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} set up outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="1762f-166">新增具有下列屬性的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="1762f-166">Add a filter with the following properties.</span></span>
    | <span data-ttu-id="1762f-167">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="1762f-167">Filter property</span></span>                                                   | <span data-ttu-id="1762f-168">值</span><span class="sxs-lookup"><span data-stu-id="1762f-168">Value</span></span>                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | <span data-ttu-id="1762f-169">**FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="1762f-169">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="1762f-170">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="1762f-170">NlatUnicast</span></span>                                                                               |
    | <span data-ttu-id="1762f-171">**動作。類型**</span><span class="sxs-lookup"><span data-stu-id="1762f-171">**action.type**</span></span>                                                   | <span data-ttu-id="1762f-172">**已 \_ 終止的 .FWP 動作 \_ 標注 \_**</span><span class="sxs-lookup"><span data-stu-id="1762f-172">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                     |
    | <span data-ttu-id="1762f-173">**calloutKey**</span><span class="sxs-lookup"><span data-stu-id="1762f-173">**action.calloutKey**</span></span>                                             | <span data-ttu-id="1762f-174">**FWPM \_ 標注 \_ IPSEC \_ 輸出 \_ 傳輸 \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="1762f-174">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                    |
    | <span data-ttu-id="1762f-175">**rawCoNtext**</span><span class="sxs-lookup"><span data-stu-id="1762f-175">**rawContext**</span></span>                                                    | [<span data-ttu-id="1762f-176">**FWPM \_ 內容 \_ IPSEC \_ 輸出 \_ 協商 \_ 探索**</span><span class="sxs-lookup"><span data-stu-id="1762f-176">**FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_NEGOTIATE\_DISCOVER**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="1762f-177">藉由新增具有下列屬性的篩選準則，從 IPsec 豁免 ICMP 流量。</span><span class="sxs-lookup"><span data-stu-id="1762f-177">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>
    | <span data-ttu-id="1762f-178">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="1762f-178">Filter property</span></span>                                                   | <span data-ttu-id="1762f-179">值</span><span class="sxs-lookup"><span data-stu-id="1762f-179">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="1762f-180">**FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="1762f-180">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="1762f-181">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="1762f-181">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="1762f-182">**FWPM \_條件 \_ IP \_ 通訊協定** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="1762f-182">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="1762f-183">**IPPROTO \_ICMP {V6}** 這些常數定義于 winsock2. h 中。</span><span class="sxs-lookup"><span data-stu-id="1762f-183">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="1762f-184">**動作。類型**</span><span class="sxs-lookup"><span data-stu-id="1762f-184">**action.type**</span></span>                                                   | <span data-ttu-id="1762f-185">**已 \_ 允許的 .FWP 動作 \_**</span><span class="sxs-lookup"><span data-stu-id="1762f-185">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="1762f-186">**weight**</span><span class="sxs-lookup"><span data-stu-id="1762f-186">**weight**</span></span>                                                        | <span data-ttu-id="1762f-187">**FWPM \_ 權數 \_ 範圍 \_ IKE \_ 豁免**</span><span class="sxs-lookup"><span data-stu-id="1762f-187">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

<span data-ttu-id="1762f-188">**在 FWPM \_ 層的 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6} 設定輸入的每個連線篩選規則**</span><span class="sxs-lookup"><span data-stu-id="1762f-188">**At FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} set up inbound per-connection filtering rules**</span></span>  

1.  <span data-ttu-id="1762f-189">新增具有下列屬性的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="1762f-189">Add a filter with the following properties.</span></span> <span data-ttu-id="1762f-190">此篩選器只允許透過 IPsec 保護的輸入連接嘗試。</span><span class="sxs-lookup"><span data-stu-id="1762f-190">This filter will only allow inbound connection attempts if they are secured by IPsec.</span></span> 
    | <span data-ttu-id="1762f-191">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="1762f-191">Filter property</span></span>                                                   | <span data-ttu-id="1762f-192">值</span><span class="sxs-lookup"><span data-stu-id="1762f-192">Value</span></span>                                                        |
    |-------------------------------------------------------------------|--------------------------------------------------------------|
    | <span data-ttu-id="1762f-193">**FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="1762f-193">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="1762f-194">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="1762f-194">NlatUnicast</span></span>                                                  |
    | <span data-ttu-id="1762f-195">**動作。類型**</span><span class="sxs-lookup"><span data-stu-id="1762f-195">**action.type**</span></span>                                                   | <span data-ttu-id="1762f-196">**已 \_ 終止的 .FWP 動作 \_ 標注 \_**</span><span class="sxs-lookup"><span data-stu-id="1762f-196">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                        |
    | <span data-ttu-id="1762f-197">**calloutKey**</span><span class="sxs-lookup"><span data-stu-id="1762f-197">**action.calloutKey**</span></span>                                             | <span data-ttu-id="1762f-198">**FWPM \_ 標注 \_ IPSEC \_ 輸入 \_ 起始 \_ 安全 \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="1762f-198">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span> |

        
2.  <span data-ttu-id="1762f-199">藉由新增具有下列屬性的篩選準則，從 IPsec 豁免 ICMP 流量。</span><span class="sxs-lookup"><span data-stu-id="1762f-199">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>
    | <span data-ttu-id="1762f-200">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="1762f-200">Filter property</span></span>                                                   | <span data-ttu-id="1762f-201">值</span><span class="sxs-lookup"><span data-stu-id="1762f-201">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="1762f-202">**FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="1762f-202">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="1762f-203">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="1762f-203">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="1762f-204">**FWPM \_條件 \_ IP \_ 通訊協定** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="1762f-204">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="1762f-205">**IPPROTO \_ICMP {V6}** 這些常數定義于 winsock2. h 中。</span><span class="sxs-lookup"><span data-stu-id="1762f-205">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="1762f-206">**動作。類型**</span><span class="sxs-lookup"><span data-stu-id="1762f-206">**action.type**</span></span>                                                   | <span data-ttu-id="1762f-207">**已 \_ 允許的 .FWP 動作 \_**</span><span class="sxs-lookup"><span data-stu-id="1762f-207">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="1762f-208">**weight**</span><span class="sxs-lookup"><span data-stu-id="1762f-208">**weight**</span></span>                                                        | <span data-ttu-id="1762f-209">**FWPM \_ 權數 \_ 範圍 \_ IKE \_ 豁免**</span><span class="sxs-lookup"><span data-stu-id="1762f-209">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

</dl>

## <a name="related-topics"></a><span data-ttu-id="1762f-210">相關主題</span><span class="sxs-lookup"><span data-stu-id="1762f-210">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1762f-211">範例程式碼：使用傳輸模式</span><span class="sxs-lookup"><span data-stu-id="1762f-211">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="1762f-212">ALE 層</span><span class="sxs-lookup"><span data-stu-id="1762f-212">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="1762f-213">**內建的標注識別碼**</span><span class="sxs-lookup"><span data-stu-id="1762f-213">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="1762f-214">篩選準則</span><span class="sxs-lookup"><span data-stu-id="1762f-214">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="1762f-215">**篩選層識別碼**</span><span class="sxs-lookup"><span data-stu-id="1762f-215">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="1762f-216">**FWPM \_ ACTION0**</span><span class="sxs-lookup"><span data-stu-id="1762f-216">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="1762f-217">**FWPM \_ 提供者 \_ 內容 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="1762f-217">**FWPM\_PROVIDER\_CONTEXT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

