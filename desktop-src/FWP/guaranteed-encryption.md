---
title: 保證加密
description: 保證的加密 IPsec 原則案例需要所有相符流量的 IPsec 加密。 此原則必須與其中一個傳輸模式原則選項一起指定。
ms.assetid: 68758f0c-f134-4b7a-820a-313e2a82f280
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7120e9cb794b6010e16dd5f61accb07ca0ab9cb8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375217"
---
# <a name="guaranteed-encryption"></a><span data-ttu-id="5c84d-104">保證加密</span><span class="sxs-lookup"><span data-stu-id="5c84d-104">Guaranteed Encryption</span></span>

<span data-ttu-id="5c84d-105">保證的加密 IPsec 原則案例需要所有相符流量的 IPsec 加密。</span><span class="sxs-lookup"><span data-stu-id="5c84d-105">The Guaranteed Encryption IPsec policy scenario requires IPsec encryption for all matching traffic.</span></span> <span data-ttu-id="5c84d-106">此原則必須與其中一個傳輸模式原則選項一起指定。</span><span class="sxs-lookup"><span data-stu-id="5c84d-106">This policy must be specified in conjunction with one of the transport mode policy options.</span></span>

<span data-ttu-id="5c84d-107">保證加密通常用來加密每個應用程式的機密流量。</span><span class="sxs-lookup"><span data-stu-id="5c84d-107">Guaranteed Encryption is typically used to encrypt sensitive traffic on a per application basis.</span></span>

<span data-ttu-id="5c84d-108">可能保證加密案例的其中一個範例是「使用 IPsec 傳輸模式保護所有單播資料流量（ICMP 除外）、啟用協調探索，以及要求所有連入流量的保證加密（對應至 TCP 本機埠5555）。</span><span class="sxs-lookup"><span data-stu-id="5c84d-108">An example of a possible Guaranteed Encryption scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode, enable negotiation discovery, and require guaranteed encryption for all unicast traffic corresponding to TCP local port 5555."</span></span>

<span data-ttu-id="5c84d-109">若要以程式設計方式執行此範例，請使用下列 WFP 設定。</span><span class="sxs-lookup"><span data-stu-id="5c84d-109">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="5c84d-110">**在 FWPM \_ LAYER \_ IKEEXT \_ V {4 \| 6} 安裝程式 MM 的協商原則**</span><span class="sxs-lookup"><span data-stu-id="5c84d-110">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} setup MM negotiation policy**</span></span>  

1.  <span data-ttu-id="5c84d-111">新增下列一或兩個 MM 原則提供者內容。</span><span class="sxs-lookup"><span data-stu-id="5c84d-111">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="5c84d-112">針對 IKE，FWPM \_ IPSEC \_ IKE \_ MM coNtext 型別的原則提供者內容 \_ 。</span><span class="sxs-lookup"><span data-stu-id="5c84d-112">For IKE, a policy provider context of type FWPM\_IPSEC\_IKE\_MM\_CONTEXT.</span></span>
    -   <span data-ttu-id="5c84d-113">針對 AuthIP，FWPM \_ IPSEC \_ AuthIP \_ MM coNtext 型別的原則提供者內容 \_ 。</span><span class="sxs-lookup"><span data-stu-id="5c84d-113">For AuthIP, a policy provider context of type FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT.</span></span>

    > [!Note]  
    > <span data-ttu-id="5c84d-114">系統將會協商一般的加密模組，並套用對應的 MM 原則。</span><span class="sxs-lookup"><span data-stu-id="5c84d-114">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="5c84d-115">如果支援 IKE 和 AuthIP，則 AuthIP 是慣用的金鑰模組。</span><span class="sxs-lookup"><span data-stu-id="5c84d-115">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="5c84d-116">針對步驟1中新增的每個內容，新增具有下列屬性的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="5c84d-116">For each of the contexts added in step 1, add a filter with the following properties.</span></span>
    | <span data-ttu-id="5c84d-117">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="5c84d-117">Filter property</span></span>        | <span data-ttu-id="5c84d-118">值</span><span class="sxs-lookup"><span data-stu-id="5c84d-118">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="5c84d-119">篩選準則</span><span class="sxs-lookup"><span data-stu-id="5c84d-119">Filtering conditions</span></span>   | <span data-ttu-id="5c84d-120">空白。</span><span class="sxs-lookup"><span data-stu-id="5c84d-120">Empty.</span></span> <span data-ttu-id="5c84d-121">所有流量都會符合篩選。</span><span class="sxs-lookup"><span data-stu-id="5c84d-121">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="5c84d-122">**providerCoNtextKey**</span><span class="sxs-lookup"><span data-stu-id="5c84d-122">**providerContextKey**</span></span> | <span data-ttu-id="5c84d-123">在步驟1中新增的 MM 提供者內容的 GUID。</span><span class="sxs-lookup"><span data-stu-id="5c84d-123">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="5c84d-124">**在 FWPM \_ 層 \_ \_ ，IPSEC V {4 \| 6} 安裝 QM 和 EM 協商原則**</span><span class="sxs-lookup"><span data-stu-id="5c84d-124">**At FWPM\_LAYER\_IPSEC\_V{4\|6} setup QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="5c84d-125">新增下列一或兩個 QM 傳輸模式原則提供者內容，並設定 [**IPSEC \_ 原則 \_ 旗標 \_ ND \_ 安全**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) 旗標。</span><span class="sxs-lookup"><span data-stu-id="5c84d-125">Add one or both of the following QM transport mode policy provider contexts and set the [**IPSEC\_POLICY\_FLAG\_ND\_SECURE**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) flag.</span></span>  
    -   <span data-ttu-id="5c84d-126">針對 IKE， **FWPM \_ IPSEC \_ IKE \_ QM \_ 傳輸 \_ 內容** 類型的原則提供者內容。</span><span class="sxs-lookup"><span data-stu-id="5c84d-126">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT**.</span></span>
    -   <span data-ttu-id="5c84d-127">針對 AuthIP，FWPM IPSEC AuthIP 型別的原則提供者內容 **\_ \_ \_ QM \_ 傳輸 \_ 內容**。</span><span class="sxs-lookup"><span data-stu-id="5c84d-127">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT**.</span></span> <span data-ttu-id="5c84d-128">此內容可以選擇性地包含 AuthIP 擴充模式 (EM) 的協商原則。</span><span class="sxs-lookup"><span data-stu-id="5c84d-128">This context can optionally contain the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="5c84d-129">系統將會協商一般的加密模組，並套用對應的 QM 原則。</span><span class="sxs-lookup"><span data-stu-id="5c84d-129">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="5c84d-130">如果支援 IKE 和 AuthIP，則 AuthIP 是慣用的金鑰模組。</span><span class="sxs-lookup"><span data-stu-id="5c84d-130">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="5c84d-131">針對步驟1中新增的每個內容，新增具有下列屬性的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="5c84d-131">For each of the contexts added in step 1, add a filter with the following properties.</span></span>
    | <span data-ttu-id="5c84d-132">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="5c84d-132">Filter property</span></span>        | <span data-ttu-id="5c84d-133">值</span><span class="sxs-lookup"><span data-stu-id="5c84d-133">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="5c84d-134">篩選準則</span><span class="sxs-lookup"><span data-stu-id="5c84d-134">Filtering conditions</span></span>   | <span data-ttu-id="5c84d-135">空白。</span><span class="sxs-lookup"><span data-stu-id="5c84d-135">Empty.</span></span> <span data-ttu-id="5c84d-136">所有流量都會符合篩選。</span><span class="sxs-lookup"><span data-stu-id="5c84d-136">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="5c84d-137">**providerCoNtextKey**</span><span class="sxs-lookup"><span data-stu-id="5c84d-137">**providerContextKey**</span></span> | <span data-ttu-id="5c84d-138">在步驟1中新增的 QM 提供者內容的 GUID。</span><span class="sxs-lookup"><span data-stu-id="5c84d-138">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="5c84d-139">**在 FWPM \_ 層 \_ 輸入 \_ 傳輸 \_ V {4 \| 6} 設定輸入每個封包篩選規則**</span><span class="sxs-lookup"><span data-stu-id="5c84d-139">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="5c84d-140">新增具有下列屬性的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="5c84d-140">Add a filter with the following properties.</span></span> 
    | <span data-ttu-id="5c84d-141">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="5c84d-141">Filter property</span></span>                                               | <span data-ttu-id="5c84d-142">值</span><span class="sxs-lookup"><span data-stu-id="5c84d-142">Value</span></span>                                                                                              |
    |---------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="5c84d-143">FWPM \_ 條件 \_ IP \_ 本機 \_ 位址 \_ 類型篩選準則</span><span class="sxs-lookup"><span data-stu-id="5c84d-143">FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE filtering condition</span></span> | [<span data-ttu-id="5c84d-144">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="5c84d-144">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | <span data-ttu-id="5c84d-145">**動作。類型**</span><span class="sxs-lookup"><span data-stu-id="5c84d-145">**action.type**</span></span>                                               | <span data-ttu-id="5c84d-146">**已 \_ 終止的 .FWP 動作 \_ 標注 \_**</span><span class="sxs-lookup"><span data-stu-id="5c84d-146">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                              |
    | <span data-ttu-id="5c84d-147">**calloutKey**</span><span class="sxs-lookup"><span data-stu-id="5c84d-147">**action.calloutKey**</span></span>                                         | <span data-ttu-id="5c84d-148">**FWPM \_ 標注 \_ IPSEC \_ 輸入 \_ 傳輸 \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="5c84d-148">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                              |
    | <span data-ttu-id="5c84d-149">**rawCoNtext**</span><span class="sxs-lookup"><span data-stu-id="5c84d-149">**rawContext**</span></span>                                                | [<span data-ttu-id="5c84d-150">**FWPM \_ 內容 \_ IPSEC \_ 輸入 \_ 保存 \_ 連接 \_ 安全性**</span><span class="sxs-lookup"><span data-stu-id="5c84d-150">**FWPM\_CONTEXT\_IPSEC\_INBOUND\_PERSIST\_CONNECTION\_SECURITY**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="5c84d-151">藉由新增具有下列屬性的篩選準則，從 IPsec 豁免 ICMP 流量。</span><span class="sxs-lookup"><span data-stu-id="5c84d-151">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>
    | <span data-ttu-id="5c84d-152">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="5c84d-152">Filter property</span></span>                                                   | <span data-ttu-id="5c84d-153">值</span><span class="sxs-lookup"><span data-stu-id="5c84d-153">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="5c84d-154">**FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="5c84d-154">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="5c84d-155">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="5c84d-155">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="5c84d-156">**FWPM \_條件 \_ IP \_ 通訊協定** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="5c84d-156">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="5c84d-157">**IPPROTO \_ICMP {V6}** 這些常數定義于 winsock2. h 中。</span><span class="sxs-lookup"><span data-stu-id="5c84d-157">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="5c84d-158">**動作。類型**</span><span class="sxs-lookup"><span data-stu-id="5c84d-158">**action.type**</span></span>                                                   | <span data-ttu-id="5c84d-159">**已 \_ 允許的 .FWP 動作 \_**</span><span class="sxs-lookup"><span data-stu-id="5c84d-159">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="5c84d-160">**weight**</span><span class="sxs-lookup"><span data-stu-id="5c84d-160">**weight**</span></span>                                                        | [<span data-ttu-id="5c84d-161">**FWPM \_ 權數 \_ 範圍 \_ IKE \_ 豁免**</span><span class="sxs-lookup"><span data-stu-id="5c84d-161">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="5c84d-162">**在 FWPM \_ 層 \_ 輸出 \_ 傳輸 \_ V {4 \| 6} 上，設定每個封包篩選規則的輸出**</span><span class="sxs-lookup"><span data-stu-id="5c84d-162">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="5c84d-163">新增具有下列屬性的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="5c84d-163">Add a filter with the following properties.</span></span>
    | <span data-ttu-id="5c84d-164">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="5c84d-164">Filter property</span></span>                                                   | <span data-ttu-id="5c84d-165">值</span><span class="sxs-lookup"><span data-stu-id="5c84d-165">Value</span></span>                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | <span data-ttu-id="5c84d-166">**FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="5c84d-166">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="5c84d-167">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="5c84d-167">NlatUnicast</span></span>                                                                               |
    | <span data-ttu-id="5c84d-168">**動作。類型**</span><span class="sxs-lookup"><span data-stu-id="5c84d-168">**action.type**</span></span>                                                   | <span data-ttu-id="5c84d-169">**已 \_ 終止的 .FWP 動作 \_ 標注 \_**</span><span class="sxs-lookup"><span data-stu-id="5c84d-169">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                     |
    | <span data-ttu-id="5c84d-170">**calloutKey**</span><span class="sxs-lookup"><span data-stu-id="5c84d-170">**action.calloutKey**</span></span>                                             | <span data-ttu-id="5c84d-171">**FWPM \_ 標注 \_ IPSEC \_ 輸出 \_ 傳輸 \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="5c84d-171">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                    |
    | <span data-ttu-id="5c84d-172">**rawCoNtext**</span><span class="sxs-lookup"><span data-stu-id="5c84d-172">**rawContext**</span></span>                                                    | [<span data-ttu-id="5c84d-173">**FWPM \_ 內容 \_ IPSEC \_ 輸出 \_ 協商 \_ 探索**</span><span class="sxs-lookup"><span data-stu-id="5c84d-173">**FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_NEGOTIATE\_DISCOVER**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="5c84d-174">藉由新增具有下列屬性的篩選準則，從 IPsec 豁免 ICMP 流量。</span><span class="sxs-lookup"><span data-stu-id="5c84d-174">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>
    | <span data-ttu-id="5c84d-175">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="5c84d-175">Filter property</span></span>                                                   | <span data-ttu-id="5c84d-176">值</span><span class="sxs-lookup"><span data-stu-id="5c84d-176">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="5c84d-177">**FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="5c84d-177">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="5c84d-178">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="5c84d-178">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="5c84d-179">**FWPM \_條件 \_ IP \_ 通訊協定** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="5c84d-179">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="5c84d-180">**IPPROTO \_ICMP {V6}** 這些常數定義于 winsock2. h 中。</span><span class="sxs-lookup"><span data-stu-id="5c84d-180">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="5c84d-181">**動作。類型**</span><span class="sxs-lookup"><span data-stu-id="5c84d-181">**action.type**</span></span>                                                   | <span data-ttu-id="5c84d-182">**已 \_ 允許的 .FWP 動作 \_**</span><span class="sxs-lookup"><span data-stu-id="5c84d-182">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="5c84d-183">**weight**</span><span class="sxs-lookup"><span data-stu-id="5c84d-183">**weight**</span></span>                                                        | <span data-ttu-id="5c84d-184">**FWPM \_ 權數 \_ 範圍 \_ IKE \_ 豁免**</span><span class="sxs-lookup"><span data-stu-id="5c84d-184">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

<span data-ttu-id="5c84d-185">**在 FWPM \_ 層的 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6} 安裝輸入的每個連線篩選規則**</span><span class="sxs-lookup"><span data-stu-id="5c84d-185">**At FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} setup inbound per-connection filtering rules**</span></span>  

1.  <span data-ttu-id="5c84d-186">新增具有下列屬性的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="5c84d-186">Add a filter with the following properties.</span></span> <span data-ttu-id="5c84d-187">此篩選器只允許透過 IPsec 保護的輸入連接嘗試。</span><span class="sxs-lookup"><span data-stu-id="5c84d-187">This filter will only allow inbound connection attempts if they are secured by IPsec.</span></span> 
    | <span data-ttu-id="5c84d-188">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="5c84d-188">Filter property</span></span>                                                   | <span data-ttu-id="5c84d-189">值</span><span class="sxs-lookup"><span data-stu-id="5c84d-189">Value</span></span>                                                        |
    |-------------------------------------------------------------------|--------------------------------------------------------------|
    | <span data-ttu-id="5c84d-190">**FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="5c84d-190">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="5c84d-191">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="5c84d-191">NlatUnicast</span></span>                                                  |
    | <span data-ttu-id="5c84d-192">**動作。類型**</span><span class="sxs-lookup"><span data-stu-id="5c84d-192">**action.type**</span></span>                                                   | <span data-ttu-id="5c84d-193">**已 \_ 終止的 .FWP 動作 \_ 標注 \_**</span><span class="sxs-lookup"><span data-stu-id="5c84d-193">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                        |
    | <span data-ttu-id="5c84d-194">**calloutKey**</span><span class="sxs-lookup"><span data-stu-id="5c84d-194">**action.calloutKey**</span></span>                                             | <span data-ttu-id="5c84d-195">**FWPM \_ 標注 \_ IPSEC \_ 輸入 \_ 起始 \_ 安全 \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="5c84d-195">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span> |

        
2.  <span data-ttu-id="5c84d-196">藉由新增具有下列屬性的篩選準則，從 IPsec 豁免 ICMP 流量。</span><span class="sxs-lookup"><span data-stu-id="5c84d-196">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>
    | <span data-ttu-id="5c84d-197">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="5c84d-197">Filter property</span></span>                                                   | <span data-ttu-id="5c84d-198">值</span><span class="sxs-lookup"><span data-stu-id="5c84d-198">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="5c84d-199">**FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="5c84d-199">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="5c84d-200">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="5c84d-200">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="5c84d-201">**FWPM \_條件 \_ IP \_ 通訊協定** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="5c84d-201">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="5c84d-202">**IPPROTO \_ICMP {V6}** 這些常數定義于 winsock2. h 中。</span><span class="sxs-lookup"><span data-stu-id="5c84d-202">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="5c84d-203">**動作。類型**</span><span class="sxs-lookup"><span data-stu-id="5c84d-203">**action.type**</span></span>                                                   | <span data-ttu-id="5c84d-204">**已 \_ 允許的 .FWP 動作 \_**</span><span class="sxs-lookup"><span data-stu-id="5c84d-204">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="5c84d-205">**weight**</span><span class="sxs-lookup"><span data-stu-id="5c84d-205">**weight**</span></span>                                                        | <span data-ttu-id="5c84d-206">**FWPM \_ 權數 \_ 範圍 \_ IKE \_ 豁免**</span><span class="sxs-lookup"><span data-stu-id="5c84d-206">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        
3.  <span data-ttu-id="5c84d-207">新增具有下列屬性的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="5c84d-207">Add a filter with the following properties.</span></span> <span data-ttu-id="5c84d-208">此篩選器只允許 TCP 埠5555的輸入連接（如果已加密）。</span><span class="sxs-lookup"><span data-stu-id="5c84d-208">This filter will only permit inbound connections to TCP port 5555 if they are encrypted.</span></span>
    | <span data-ttu-id="5c84d-209">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="5c84d-209">Filter property</span></span>                                                   | <span data-ttu-id="5c84d-210">值</span><span class="sxs-lookup"><span data-stu-id="5c84d-210">Value</span></span>                                                                                                 |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="5c84d-211">**FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="5c84d-211">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="5c84d-212">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="5c84d-212">NlatUnicast</span></span>                                                                                           |
    | <span data-ttu-id="5c84d-213">**FWPM \_條件 \_ IP \_ 通訊協定** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="5c84d-213">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="5c84d-214">**IPPROTO \_TCP** 此常數定義于 winsock2. h 中。</span><span class="sxs-lookup"><span data-stu-id="5c84d-214">**IPPROTO\_TCP** This constant is defined in winsock2.h.</span></span><br/>                                    |
    | <span data-ttu-id="5c84d-215">**FWPM \_條件 \_ IP \_ 本機 \_ 埠** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="5c84d-215">**FWPM\_CONDITION\_IP\_LOCAL\_PORT** filtering condition</span></span>          | <span data-ttu-id="5c84d-216">5555</span><span class="sxs-lookup"><span data-stu-id="5c84d-216">5555</span></span>                                                                                                  |
    | <span data-ttu-id="5c84d-217">**動作。類型**</span><span class="sxs-lookup"><span data-stu-id="5c84d-217">**action.type**</span></span>                                                   | <span data-ttu-id="5c84d-218">**已 \_ 終止的 .FWP 動作 \_ 標注 \_**</span><span class="sxs-lookup"><span data-stu-id="5c84d-218">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                                 |
    | <span data-ttu-id="5c84d-219">**calloutKey**</span><span class="sxs-lookup"><span data-stu-id="5c84d-219">**action.calloutKey**</span></span>                                             | <span data-ttu-id="5c84d-220">**FWPM \_ 標注 \_ IPSEC \_ 輸入 \_ 起始 \_ 安全 \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="5c84d-220">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span>                                          |
    | <span data-ttu-id="5c84d-221">**rawCoNtext**</span><span class="sxs-lookup"><span data-stu-id="5c84d-221">**rawContext**</span></span>                                                    | [<span data-ttu-id="5c84d-222">**FWPM \_ 內容 \_ ALE \_ 設定 \_ 連接 \_ 需要 \_ IPSEC \_ 加密**</span><span class="sxs-lookup"><span data-stu-id="5c84d-222">**FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_REQUIRE\_IPSEC\_ENCRYPTION**</span></span>](filter-context-identifiers.md) |

        

<span data-ttu-id="5c84d-223">**At FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V {4 \| 6} 設定輸出的每一連線篩選規則**</span><span class="sxs-lookup"><span data-stu-id="5c84d-223">**At FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6} setup outbound per-connection filtering rules**</span></span>

-   <span data-ttu-id="5c84d-224">新增具有下列屬性的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="5c84d-224">Add a filter with the following properties.</span></span> <span data-ttu-id="5c84d-225">此篩選器只允許來自 TCP 埠5555的輸出連接（如果已加密）。</span><span class="sxs-lookup"><span data-stu-id="5c84d-225">This filter will only permit outbound connections from TCP port 5555 if they are encrypted.</span></span>
    | <span data-ttu-id="5c84d-226">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="5c84d-226">Filter property</span></span>                                                   | <span data-ttu-id="5c84d-227">值</span><span class="sxs-lookup"><span data-stu-id="5c84d-227">Value</span></span>                                                                                                 |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="5c84d-228">**FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="5c84d-228">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="5c84d-229">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="5c84d-229">NlatUnicast</span></span>                                                                                           |
    | <span data-ttu-id="5c84d-230">**FWPM \_條件 \_ IP \_ 通訊協定** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="5c84d-230">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="5c84d-231">**IPPROTO \_TCP** 此常數定義于 winsock2. h 中。</span><span class="sxs-lookup"><span data-stu-id="5c84d-231">**IPPROTO\_TCP** This constant is defined in winsock2.h.</span></span><br/>                                    |
    | <span data-ttu-id="5c84d-232">**FWPM \_條件 \_ IP \_ 本機 \_ 埠** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="5c84d-232">**FWPM\_CONDITION\_IP\_LOCAL\_PORT** filtering condition</span></span>          | <span data-ttu-id="5c84d-233">5555</span><span class="sxs-lookup"><span data-stu-id="5c84d-233">5555</span></span>                                                                                                  |
    | <span data-ttu-id="5c84d-234">**動作。類型**</span><span class="sxs-lookup"><span data-stu-id="5c84d-234">**action.type**</span></span>                                                   | <span data-ttu-id="5c84d-235">**已 \_ 終止的 .FWP 動作 \_ 標注 \_**</span><span class="sxs-lookup"><span data-stu-id="5c84d-235">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                                 |
    | <span data-ttu-id="5c84d-236">**calloutKey**</span><span class="sxs-lookup"><span data-stu-id="5c84d-236">**action.calloutKey**</span></span>                                             | <span data-ttu-id="5c84d-237">**FWPM \_ 標注 \_ IPSEC \_ ALE \_ CONNECT \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="5c84d-237">**FWPM\_CALLOUT\_IPSEC\_ALE\_CONNECT\_V{4\|6}**</span></span>                                                       |
    | <span data-ttu-id="5c84d-238">**rawCoNtext**</span><span class="sxs-lookup"><span data-stu-id="5c84d-238">**rawContext**</span></span>                                                    | [<span data-ttu-id="5c84d-239">**FWPM \_ 內容 \_ ALE \_ 設定 \_ 連接 \_ 需要 \_ IPSEC \_ 加密**</span><span class="sxs-lookup"><span data-stu-id="5c84d-239">**FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_REQUIRE\_IPSEC\_ENCRYPTION**</span></span>](filter-context-identifiers.md) |

      

  
</dl>

## <a name="related-topics"></a><span data-ttu-id="5c84d-240">相關主題</span><span class="sxs-lookup"><span data-stu-id="5c84d-240">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c84d-241">範例程式碼：使用傳輸模式</span><span class="sxs-lookup"><span data-stu-id="5c84d-241">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="5c84d-242">ALE 層</span><span class="sxs-lookup"><span data-stu-id="5c84d-242">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="5c84d-243">**內建的標注識別碼**</span><span class="sxs-lookup"><span data-stu-id="5c84d-243">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="5c84d-244">篩選準則</span><span class="sxs-lookup"><span data-stu-id="5c84d-244">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="5c84d-245">**篩選層識別碼**</span><span class="sxs-lookup"><span data-stu-id="5c84d-245">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="5c84d-246">**FWPM \_ ACTION0**</span><span class="sxs-lookup"><span data-stu-id="5c84d-246">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="5c84d-247">**FWPM \_ 提供者 \_ 內容 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="5c84d-247">**FWPM\_PROVIDER\_CONTEXT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

