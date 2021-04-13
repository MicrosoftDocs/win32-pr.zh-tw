---
title: 遠端身分識別授權
description: 遠端身分識別授權 IPsec 原則案例要求輸入連線來自于 Windows 安全描述項中指定的一組特定遠端安全性主體 (SD) 存取控制清單 (ACL) 。
ms.assetid: 4d9f83d6-6f56-4416-8c35-d0260f9e888c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44022c9696dec25e709d9ab1e374ada295893ed
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375013"
---
# <a name="remote-identity-authorization"></a><span data-ttu-id="4c745-103">遠端身分識別授權</span><span class="sxs-lookup"><span data-stu-id="4c745-103">Remote Identity Authorization</span></span>

<span data-ttu-id="4c745-104">遠端身分識別授權 IPsec 原則案例要求輸入連線來自于 Windows 安全描述項中指定的一組特定遠端安全性主體 (SD) 存取控制清單 (ACL) 。</span><span class="sxs-lookup"><span data-stu-id="4c745-104">The Remote Identity Authorization IPsec policy scenario requires that inbound connections come from a specific set of remote security principals which are specified in a Windows security descriptor (SD) access control list (ACL).</span></span> <span data-ttu-id="4c745-105">如果遠端身分識別 (由 IPsec 所決定) 不符合允許的身分識別集合，則連線將會中斷。</span><span class="sxs-lookup"><span data-stu-id="4c745-105">If the remote identity (as determined by IPsec) does not match the set of allowed identities, the connection will be dropped.</span></span> <span data-ttu-id="4c745-106">此原則必須與其中一個傳輸模式原則選項一起指定。</span><span class="sxs-lookup"><span data-stu-id="4c745-106">This policy must be specified in conjunction with one of the transport mode policy options.</span></span>

<span data-ttu-id="4c745-107">如果已啟用 AuthIP，則可以指定兩個安全描述項，一個對應至 AuthIP 主要模式，另一個對應至 AuthIP 擴充模式。</span><span class="sxs-lookup"><span data-stu-id="4c745-107">If AuthIP is enabled, two security descriptors can be specified, one corresponding to AuthIP main mode, and the other corresponding to AuthIP extended mode.</span></span>

<span data-ttu-id="4c745-108">可能的協商探索傳輸模式案例的其中一個範例是「使用 IPsec 傳輸模式來保護所有的單播資料流量（ICMP 除外）、啟用協調探索，以及根據安全性描述項來限制允許的遠端身分識別的輸入存取權 SD1)  (對應到 SD2 的)  (的所有單點傳送流量，以對應至 TCP 本機埠5555。</span><span class="sxs-lookup"><span data-stu-id="4c745-108">An example of a possible Negotiation Discovery Transport Mode scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode, enable negotiation discovery, and restrict inbound access to remote identities allowed as per security descriptor SD1 (corresponding to IKE/AuthIP main mode) and security descriptor SD2 (corresponding to AuthIP extended mode), for all unicast traffic corresponding to TCP local port 5555."</span></span>

<span data-ttu-id="4c745-109">若要以程式設計方式執行此範例，請使用下列 WFP 設定。</span><span class="sxs-lookup"><span data-stu-id="4c745-109">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="4c745-110">**在 FWPM \_ LAYER \_ IKEEXT \_ V {4 \| 6} 安裝程式 MM 的協商原則**</span><span class="sxs-lookup"><span data-stu-id="4c745-110">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} setup MM negotiation policy**</span></span>  

1.  <span data-ttu-id="4c745-111">新增下列一或兩個 MM 原則提供者內容。</span><span class="sxs-lookup"><span data-stu-id="4c745-111">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="4c745-112">針對 IKE， **FWPM \_ IPSEC \_ IKE \_ MM \_ coNtext** 型別的原則提供者內容。</span><span class="sxs-lookup"><span data-stu-id="4c745-112">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_MM\_CONTEXT**.</span></span>
    -   <span data-ttu-id="4c745-113">針對 AuthIP， **FWPM \_ IPSEC \_ AuthIP \_ MM \_ coNtext** 型別的原則提供者內容。</span><span class="sxs-lookup"><span data-stu-id="4c745-113">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT**.</span></span>

    > [!Note]  
    > <span data-ttu-id="4c745-114">系統將會協商一般的加密模組，並套用對應的 MM 原則。</span><span class="sxs-lookup"><span data-stu-id="4c745-114">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="4c745-115">如果支援 IKE 和 AuthIP，則 AuthIP 是慣用的金鑰模組。</span><span class="sxs-lookup"><span data-stu-id="4c745-115">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="4c745-116">針對步驟1中新增的每個內容，新增具有下列屬性的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="4c745-116">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 
    | <span data-ttu-id="4c745-117">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="4c745-117">Filter property</span></span>        | <span data-ttu-id="4c745-118">值</span><span class="sxs-lookup"><span data-stu-id="4c745-118">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="4c745-119">篩選準則</span><span class="sxs-lookup"><span data-stu-id="4c745-119">Filtering conditions</span></span>   | <span data-ttu-id="4c745-120">空白。</span><span class="sxs-lookup"><span data-stu-id="4c745-120">Empty.</span></span> <span data-ttu-id="4c745-121">所有流量都會符合篩選。</span><span class="sxs-lookup"><span data-stu-id="4c745-121">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="4c745-122">**providerCoNtextKey**</span><span class="sxs-lookup"><span data-stu-id="4c745-122">**providerContextKey**</span></span> | <span data-ttu-id="4c745-123">在步驟1中新增的 MM 提供者內容的 GUID。</span><span class="sxs-lookup"><span data-stu-id="4c745-123">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="4c745-124">**在 FWPM \_ 層 \_ \_ ，IPSEC V {4 \| 6} 安裝 QM 和 EM 協商原則**</span><span class="sxs-lookup"><span data-stu-id="4c745-124">**At FWPM\_LAYER\_IPSEC\_V{4\|6} setup QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="4c745-125">新增下列一或兩個 QM 傳輸模式原則提供者內容，並設定 [**IPSEC \_ 原則 \_ 旗標 \_ ND \_ 安全**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) 旗標。</span><span class="sxs-lookup"><span data-stu-id="4c745-125">Add one or both of the following QM transport mode policy provider contexts and set the [**IPSEC\_POLICY\_FLAG\_ND\_SECURE**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) flag.</span></span>  
    -   <span data-ttu-id="4c745-126">針對 IKE， **FWPM \_ IPSEC \_ IKE \_ QM \_ 傳輸 \_ 內容** 類型的原則提供者內容。</span><span class="sxs-lookup"><span data-stu-id="4c745-126">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT**.</span></span>
    -   <span data-ttu-id="4c745-127">針對 AuthIP，FWPM IPSEC AuthIP 類型的原則提供者內容會 **\_ \_ \_ QM \_ 傳輸 \_ 內容** ，其中包含 AuthIP 延伸模式 (EM) 的協商原則。</span><span class="sxs-lookup"><span data-stu-id="4c745-127">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT** that contains the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="4c745-128">系統將會協商一般的加密模組，並套用對應的 QM 原則。</span><span class="sxs-lookup"><span data-stu-id="4c745-128">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="4c745-129">如果支援 IKE 和 AuthIP，則 AuthIP 是慣用的金鑰模組。</span><span class="sxs-lookup"><span data-stu-id="4c745-129">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="4c745-130">針對步驟1中新增的每個內容，新增具有下列屬性的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="4c745-130">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 
    | <span data-ttu-id="4c745-131">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="4c745-131">Filter property</span></span>        | <span data-ttu-id="4c745-132">值</span><span class="sxs-lookup"><span data-stu-id="4c745-132">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="4c745-133">篩選準則</span><span class="sxs-lookup"><span data-stu-id="4c745-133">Filtering conditions</span></span>   | <span data-ttu-id="4c745-134">空白。</span><span class="sxs-lookup"><span data-stu-id="4c745-134">Empty.</span></span> <span data-ttu-id="4c745-135">所有流量都會符合篩選。</span><span class="sxs-lookup"><span data-stu-id="4c745-135">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="4c745-136">**providerCoNtextKey**</span><span class="sxs-lookup"><span data-stu-id="4c745-136">**providerContextKey**</span></span> | <span data-ttu-id="4c745-137">在步驟1中新增的 QM 提供者內容的 GUID。</span><span class="sxs-lookup"><span data-stu-id="4c745-137">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="4c745-138">**在 FWPM \_ 層 \_ 輸入 \_ 傳輸 \_ V {4 \| 6} 設定輸入每個封包篩選規則**</span><span class="sxs-lookup"><span data-stu-id="4c745-138">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="4c745-139">新增具有下列屬性的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="4c745-139">Add a filter with the following properties.</span></span> 
    | <span data-ttu-id="4c745-140">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="4c745-140">Filter property</span></span>                                                   | <span data-ttu-id="4c745-141">值</span><span class="sxs-lookup"><span data-stu-id="4c745-141">Value</span></span>                                                                                              |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="4c745-142">**FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="4c745-142">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="4c745-143">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="4c745-143">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | <span data-ttu-id="4c745-144">**動作。類型**</span><span class="sxs-lookup"><span data-stu-id="4c745-144">**action.type**</span></span>                                                   | <span data-ttu-id="4c745-145">**已 \_ 終止的 .FWP 動作 \_ 標注 \_**</span><span class="sxs-lookup"><span data-stu-id="4c745-145">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                              |
    | <span data-ttu-id="4c745-146">**calloutKey**</span><span class="sxs-lookup"><span data-stu-id="4c745-146">**action.calloutKey**</span></span>                                             | <span data-ttu-id="4c745-147">**FWPM \_ 標注 \_ IPSEC \_ 輸入 \_ 傳輸 \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="4c745-147">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                              |
    | <span data-ttu-id="4c745-148">**rawCoNtext**</span><span class="sxs-lookup"><span data-stu-id="4c745-148">**rawContext**</span></span>                                                    | [<span data-ttu-id="4c745-149">**FWPM \_ 內容 \_ IPSEC \_ 輸入 \_ 保存 \_ 連接 \_ 安全性**</span><span class="sxs-lookup"><span data-stu-id="4c745-149">**FWPM\_CONTEXT\_IPSEC\_INBOUND\_PERSIST\_CONNECTION\_SECURITY**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="4c745-150">藉由新增具有下列屬性的篩選準則，從 IPsec 豁免 ICMP 流量。</span><span class="sxs-lookup"><span data-stu-id="4c745-150">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 
    | <span data-ttu-id="4c745-151">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="4c745-151">Filter property</span></span>                                                   | <span data-ttu-id="4c745-152">值</span><span class="sxs-lookup"><span data-stu-id="4c745-152">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="4c745-153">**FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="4c745-153">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="4c745-154">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="4c745-154">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="4c745-155">**FWPM \_條件 \_ IP \_ 通訊協定** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="4c745-155">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="4c745-156">**IPPROTO \_ICMP {V6}** 這些常數定義于 winsock2. h 中。</span><span class="sxs-lookup"><span data-stu-id="4c745-156">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="4c745-157">**動作。類型**</span><span class="sxs-lookup"><span data-stu-id="4c745-157">**action.type**</span></span>                                                   | <span data-ttu-id="4c745-158">已 \_ 允許的 .FWP 動作 \_</span><span class="sxs-lookup"><span data-stu-id="4c745-158">FWP\_ACTION\_PERMIT</span></span>                                                        |
    | <span data-ttu-id="4c745-159">**weight**</span><span class="sxs-lookup"><span data-stu-id="4c745-159">**weight**</span></span>                                                        | [<span data-ttu-id="4c745-160">**FWPM \_ 權數 \_ 範圍 \_ IKE \_ 豁免**</span><span class="sxs-lookup"><span data-stu-id="4c745-160">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="4c745-161">**在 FWPM \_ 層 \_ 輸出 \_ 傳輸 \_ V {4 \| 6} 上，設定每個封包篩選規則的輸出**</span><span class="sxs-lookup"><span data-stu-id="4c745-161">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="4c745-162">新增具有下列屬性的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="4c745-162">Add a filter with the following properties.</span></span> 
    | <span data-ttu-id="4c745-163">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="4c745-163">Filter property</span></span>                                                   | <span data-ttu-id="4c745-164">值</span><span class="sxs-lookup"><span data-stu-id="4c745-164">Value</span></span>                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | <span data-ttu-id="4c745-165">**FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="4c745-165">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="4c745-166">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="4c745-166">NlatUnicast</span></span>                                                                               |
    | <span data-ttu-id="4c745-167">**動作。類型**</span><span class="sxs-lookup"><span data-stu-id="4c745-167">**action.type**</span></span>                                                   | <span data-ttu-id="4c745-168">**已 \_ 終止的 .FWP 動作 \_ 標注 \_**</span><span class="sxs-lookup"><span data-stu-id="4c745-168">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                     |
    | <span data-ttu-id="4c745-169">**calloutKey**</span><span class="sxs-lookup"><span data-stu-id="4c745-169">**action.calloutKey**</span></span>                                             | <span data-ttu-id="4c745-170">**FWPM \_ 標注 \_ IPSEC \_ 輸出 \_ 傳輸 \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="4c745-170">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                    |
    | <span data-ttu-id="4c745-171">**rawCoNtext**</span><span class="sxs-lookup"><span data-stu-id="4c745-171">**rawContext**</span></span>                                                    | [<span data-ttu-id="4c745-172">**FWPM \_ 內容 \_ IPSEC \_ 輸出 \_ 協商 \_ 探索**</span><span class="sxs-lookup"><span data-stu-id="4c745-172">**FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_NEGOTIATE\_DISCOVER**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="4c745-173">藉由新增具有下列屬性的篩選準則，從 IPsec 豁免 ICMP 流量。</span><span class="sxs-lookup"><span data-stu-id="4c745-173">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 
    | <span data-ttu-id="4c745-174">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="4c745-174">Filter property</span></span>                                                   | <span data-ttu-id="4c745-175">值</span><span class="sxs-lookup"><span data-stu-id="4c745-175">Value</span></span>                                                                  |
    |-------------------------------------------------------------------|------------------------------------------------------------------------|
    | <span data-ttu-id="4c745-176">**FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="4c745-176">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="4c745-177">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="4c745-177">NlatUnicast</span></span>                                                            |
    | <span data-ttu-id="4c745-178">**FWPM \_條件 \_ IP \_ 通訊協定** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="4c745-178">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="4c745-179">IPPROTO \_ ICMP {V6} 這些常數定義于 winsock2. h 中。</span><span class="sxs-lookup"><span data-stu-id="4c745-179">IPPROTO\_ICMP{V6}These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="4c745-180">**動作。類型**</span><span class="sxs-lookup"><span data-stu-id="4c745-180">**action.type**</span></span>                                                   | <span data-ttu-id="4c745-181">**已 \_ 允許的 .FWP 動作 \_**</span><span class="sxs-lookup"><span data-stu-id="4c745-181">**FWP\_ACTION\_PERMIT**</span></span>                                                |
    | <span data-ttu-id="4c745-182">**weight**</span><span class="sxs-lookup"><span data-stu-id="4c745-182">**weight**</span></span>                                                        | <span data-ttu-id="4c745-183">**FWPM \_ 權數 \_ 範圍 \_ IKE \_ 豁免**</span><span class="sxs-lookup"><span data-stu-id="4c745-183">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                               |

        

<span data-ttu-id="4c745-184">**在 FWPM \_ 層的 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6} 安裝輸入的每個連線篩選規則**</span><span class="sxs-lookup"><span data-stu-id="4c745-184">**At FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} setup inbound per-connection filtering rules**</span></span>  

1.  <span data-ttu-id="4c745-185">新增具有下列屬性的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="4c745-185">Add a filter with the following properties.</span></span> <span data-ttu-id="4c745-186">此篩選器只允許透過 IPsec 保護的輸入連接嘗試。</span><span class="sxs-lookup"><span data-stu-id="4c745-186">This filter will only allow inbound connection attempts if they are secured by IPsec.</span></span> 
    | <span data-ttu-id="4c745-187">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="4c745-187">Filter property</span></span>                                                   | <span data-ttu-id="4c745-188">值</span><span class="sxs-lookup"><span data-stu-id="4c745-188">Value</span></span>                                                        |
    |-------------------------------------------------------------------|--------------------------------------------------------------|
    | <span data-ttu-id="4c745-189">**FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="4c745-189">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="4c745-190">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="4c745-190">NlatUnicast</span></span>                                                  |
    | <span data-ttu-id="4c745-191">**動作。類型**</span><span class="sxs-lookup"><span data-stu-id="4c745-191">**action.type**</span></span>                                                   | <span data-ttu-id="4c745-192">**已 \_ 終止的 .FWP 動作 \_ 標注 \_**</span><span class="sxs-lookup"><span data-stu-id="4c745-192">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                        |
    | <span data-ttu-id="4c745-193">**calloutKey**</span><span class="sxs-lookup"><span data-stu-id="4c745-193">**action.calloutKey**</span></span>                                             | <span data-ttu-id="4c745-194">**FWPM \_ 標注 \_ IPSEC \_ 輸入 \_ 起始 \_ 安全 \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="4c745-194">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span> |

        
2.  <span data-ttu-id="4c745-195">藉由新增具有下列屬性的篩選準則，從 IPsec 豁免 ICMP 流量。</span><span class="sxs-lookup"><span data-stu-id="4c745-195">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 
    | <span data-ttu-id="4c745-196">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="4c745-196">Filter property</span></span>                                                   | <span data-ttu-id="4c745-197">值</span><span class="sxs-lookup"><span data-stu-id="4c745-197">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="4c745-198">**FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="4c745-198">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="4c745-199">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="4c745-199">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="4c745-200">**FWPM \_條件 \_ IP \_ 通訊協定** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="4c745-200">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="4c745-201">**IPPROTO \_ICMP {V6}** 這些常數定義于 winsock2. h 中。</span><span class="sxs-lookup"><span data-stu-id="4c745-201">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="4c745-202">**動作。類型**</span><span class="sxs-lookup"><span data-stu-id="4c745-202">**action.type**</span></span>                                                   | <span data-ttu-id="4c745-203">**已 \_ 允許的 .FWP 動作 \_**</span><span class="sxs-lookup"><span data-stu-id="4c745-203">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="4c745-204">**weight**</span><span class="sxs-lookup"><span data-stu-id="4c745-204">**weight**</span></span>                                                        | <span data-ttu-id="4c745-205">**FWPM \_ 權數 \_ 範圍 \_ IKE \_ 豁免**</span><span class="sxs-lookup"><span data-stu-id="4c745-205">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        
3.  <span data-ttu-id="4c745-206">新增具有下列屬性的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="4c745-206">Add a filter with the following properties.</span></span> <span data-ttu-id="4c745-207">如果 SD1 和 SD2 允許對應的遠端識別，此篩選準則將允許 TCP 埠5555的輸入連接。</span><span class="sxs-lookup"><span data-stu-id="4c745-207">This filter will permit inbound connections to TCP port 5555 if the corresponding remote identities are allowed by both SD1 and SD2.</span></span> 
    | <span data-ttu-id="4c745-208">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="4c745-208">Filter property</span></span>                                                   | <span data-ttu-id="4c745-209">值</span><span class="sxs-lookup"><span data-stu-id="4c745-209">Value</span></span>                                                              |
    |-------------------------------------------------------------------|--------------------------------------------------------------------|
    | <span data-ttu-id="4c745-210">**FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="4c745-210">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="4c745-211">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="4c745-211">NlatUnicast</span></span>                                                        |
    | <span data-ttu-id="4c745-212">**FWPM \_條件 \_ IP \_ 通訊協定** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="4c745-212">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="4c745-213">**IPPROTO \_TCP** 此常數定義于 winsock2. h 中。</span><span class="sxs-lookup"><span data-stu-id="4c745-213">**IPPROTO\_TCP** This constant is defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="4c745-214">**FWPM \_條件 \_ IP \_ 本機 \_ 埠** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="4c745-214">**FWPM\_CONDITION\_IP\_LOCAL\_PORT** filtering condition</span></span>          | <span data-ttu-id="4c745-215">5555</span><span class="sxs-lookup"><span data-stu-id="4c745-215">5555</span></span>                                                               |
    | <span data-ttu-id="4c745-216">**FWPM \_ 條件 \_ ALE \_ 遠端 \_ 電腦 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="4c745-216">**FWPM\_CONDITION\_ALE\_REMOTE\_MACHINE\_ID**</span></span>                     | <span data-ttu-id="4c745-217">SD1</span><span class="sxs-lookup"><span data-stu-id="4c745-217">SD1</span></span>                                                                |
    | <span data-ttu-id="4c745-218">**FWPM \_ 條件 \_ ALE \_ 遠端 \_ 使用者 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="4c745-218">**FWPM\_CONDITION\_ALE\_REMOTE\_USER\_ID**</span></span>                        | <span data-ttu-id="4c745-219">SD2</span><span class="sxs-lookup"><span data-stu-id="4c745-219">SD2</span></span>                                                                |
    | <span data-ttu-id="4c745-220">**動作。類型**</span><span class="sxs-lookup"><span data-stu-id="4c745-220">**action.type**</span></span>                                                   | <span data-ttu-id="4c745-221">**已 \_ 終止的 .FWP 動作 \_ 標注 \_**</span><span class="sxs-lookup"><span data-stu-id="4c745-221">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                              |
    | <span data-ttu-id="4c745-222">**calloutKey**</span><span class="sxs-lookup"><span data-stu-id="4c745-222">**action.calloutKey**</span></span>                                             | <span data-ttu-id="4c745-223">**FWPM \_ 標注 \_ IPSEC \_ 輸入 \_ 起始 \_ 安全 \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="4c745-223">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span>       |

        
4.  <span data-ttu-id="4c745-224">新增具有下列屬性的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="4c745-224">Add a filter with the following properties.</span></span> <span data-ttu-id="4c745-225">此篩選準則會封鎖與先前篩選準則不相符的任何 TCP 埠5555的任何輸入連接。</span><span class="sxs-lookup"><span data-stu-id="4c745-225">This filter will block any other inbound connections to TCP port 5555 that did not match the previous filter.</span></span> 
    | <span data-ttu-id="4c745-226">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="4c745-226">Filter property</span></span>                                                   | <span data-ttu-id="4c745-227">值</span><span class="sxs-lookup"><span data-stu-id="4c745-227">Value</span></span>                                                              |
    |-------------------------------------------------------------------|--------------------------------------------------------------------|
    | <span data-ttu-id="4c745-228">**FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="4c745-228">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="4c745-229">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="4c745-229">NlatUnicast</span></span>                                                        |
    | <span data-ttu-id="4c745-230">**FWPM \_條件 \_ IP \_ 通訊協定** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="4c745-230">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="4c745-231">**IPPROTO \_TCP** 此常數定義于 winsock2. h 中。</span><span class="sxs-lookup"><span data-stu-id="4c745-231">**IPPROTO\_TCP** This constant is defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="4c745-232">**FWPM \_條件 \_ IP \_ 本機 \_ 埠** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="4c745-232">**FWPM\_CONDITION\_IP\_LOCAL\_PORT** filtering condition</span></span>          | <span data-ttu-id="4c745-233">5555</span><span class="sxs-lookup"><span data-stu-id="4c745-233">5555</span></span>                                                               |
    | <span data-ttu-id="4c745-234">**動作。類型**</span><span class="sxs-lookup"><span data-stu-id="4c745-234">**action.type**</span></span>                                                   | <span data-ttu-id="4c745-235">**.FWP \_ 動作 \_ 區塊**</span><span class="sxs-lookup"><span data-stu-id="4c745-235">**FWP\_ACTION\_BLOCK**</span></span>                                             |

        

</dl>

## <a name="related-topics"></a><span data-ttu-id="4c745-236">相關主題</span><span class="sxs-lookup"><span data-stu-id="4c745-236">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c745-237">範例程式碼：使用傳輸模式</span><span class="sxs-lookup"><span data-stu-id="4c745-237">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="4c745-238">ALE 層</span><span class="sxs-lookup"><span data-stu-id="4c745-238">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="4c745-239">**內建的標注識別碼**</span><span class="sxs-lookup"><span data-stu-id="4c745-239">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="4c745-240">篩選準則</span><span class="sxs-lookup"><span data-stu-id="4c745-240">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="4c745-241">**篩選層識別碼**</span><span class="sxs-lookup"><span data-stu-id="4c745-241">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="4c745-242">**FWPM \_ ACTION0**</span><span class="sxs-lookup"><span data-stu-id="4c745-242">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="4c745-243">**FWPM \_ 提供者 \_ 內容 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="4c745-243">**FWPM\_PROVIDER\_CONTEXT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

