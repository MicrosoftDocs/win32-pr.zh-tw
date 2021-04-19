---
title: 手動 SA
description: " (SA) IPsec 原則案例的手動安全性關聯，可讓呼叫者藉由直接指定 IPsec SAs 來保護任何網路流量，以略過內建的 IPsec 加密模組 (IKE 和 AuthIP) 。"
ms.assetid: 2bcc0b40-ca43-43c6-b1e4-b64426ef7ff4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beeef4486e3a07dea2e83d924c2354a3dabca241
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314571"
---
# <a name="manual-sa"></a><span data-ttu-id="ebafd-103">手動 SA</span><span class="sxs-lookup"><span data-stu-id="ebafd-103">Manual SA</span></span>

<span data-ttu-id="ebafd-104"> (SA) IPsec 原則案例的手動安全性關聯，可讓呼叫者藉由直接指定 IPsec SAs 來保護任何網路流量，以略過內建的 IPsec 加密模組 (IKE 和 AuthIP) 。</span><span class="sxs-lookup"><span data-stu-id="ebafd-104">The Manual Security Association (SA) IPsec policy scenario allows callers to bypass the built-in IPsec keying modules (IKE and AuthIP) by directly specifying IPsec SAs to secure any network traffic.</span></span>

<span data-ttu-id="ebafd-105">可能的手動 SA 案例範例是「新增 IPsec SA 組以保護 IP 位址之間的所有單播資料流量 1.1.1.1 & 2.2.2.2，ICMP 除外，使用 IPsec 傳輸模式。」</span><span class="sxs-lookup"><span data-stu-id="ebafd-105">An example of a possible Manual SA scenario is "Add an IPsec SA pair to secure all unicast data traffic between IP addresses 1.1.1.1 & 2.2.2.2, except ICMP, using IPsec transport mode."</span></span>

> [!Note]  
> <span data-ttu-id="ebafd-106">您必須在具有適當設定 IP 位址的兩部電腦上執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="ebafd-106">The following steps must be executed on both machines with IP addresses appropriately set.</span></span>

 

<span data-ttu-id="ebafd-107">若要以程式設計方式執行此範例，請使用下列 WFP 設定。</span><span class="sxs-lookup"><span data-stu-id="ebafd-107">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="ebafd-108">**在 FWPM \_ 層 \_ 輸入 \_ 傳輸 \_ V {4 \| 6} 設定輸入每個封包篩選規則**</span><span class="sxs-lookup"><span data-stu-id="ebafd-108">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="ebafd-109">新增具有下列屬性的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="ebafd-109">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="ebafd-110">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="ebafd-110">Filter property</span></span>                                                   | <span data-ttu-id="ebafd-111">值</span><span class="sxs-lookup"><span data-stu-id="ebafd-111">Value</span></span>                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | <span data-ttu-id="ebafd-112">**FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="ebafd-112">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="ebafd-113">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="ebafd-113">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | <span data-ttu-id="ebafd-114">**FWPM \_ 條件 \_ IP \_ 本機 \_ 位址**</span><span class="sxs-lookup"><span data-stu-id="ebafd-114">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS**</span></span>                           | <span data-ttu-id="ebafd-115">適當的本機位址 (1.1.1.1 或 2.2.2.2) 。</span><span class="sxs-lookup"><span data-stu-id="ebafd-115">The appropriate local address (1.1.1.1 or 2.2.2.2).</span></span>           |
    | <span data-ttu-id="ebafd-116">**FWPM \_ 條件 \_ IP \_ 遠端 \_ 位址**</span><span class="sxs-lookup"><span data-stu-id="ebafd-116">**FWPM\_CONDITION\_IP\_REMOTE\_ADDRESS**</span></span>                          | <span data-ttu-id="ebafd-117">適當的遠端位址 (1.1.1.1 或 2.2.2.2) 。</span><span class="sxs-lookup"><span data-stu-id="ebafd-117">The appropriate remote address (1.1.1.1 or 2.2.2.2).</span></span>          |
    | <span data-ttu-id="ebafd-118">**動作。類型**</span><span class="sxs-lookup"><span data-stu-id="ebafd-118">**action.type**</span></span>                                                   | <span data-ttu-id="ebafd-119">**已 \_ 終止的 .FWP 動作 \_ 標注 \_**</span><span class="sxs-lookup"><span data-stu-id="ebafd-119">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                         |
    | <span data-ttu-id="ebafd-120">**calloutKey**</span><span class="sxs-lookup"><span data-stu-id="ebafd-120">**action.calloutKey**</span></span>                                             | <span data-ttu-id="ebafd-121">**FWPM \_ 標注 \_ IPSEC \_ 輸入 \_ 傳輸 \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="ebafd-121">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>         |

        
2.  <span data-ttu-id="ebafd-122">藉由新增具有下列屬性的篩選準則，從 IPsec 豁免 ICMP 流量。</span><span class="sxs-lookup"><span data-stu-id="ebafd-122">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 

    | <span data-ttu-id="ebafd-123">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="ebafd-123">Filter property</span></span>                                                   | <span data-ttu-id="ebafd-124">值</span><span class="sxs-lookup"><span data-stu-id="ebafd-124">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="ebafd-125">**FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="ebafd-125">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="ebafd-126">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="ebafd-126">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="ebafd-127">**FWPM \_條件 \_ IP \_ 通訊協定** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="ebafd-127">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="ebafd-128">**IPPROTO \_ICMP {V6}** 這些常數定義于 winsock2. h 中。</span><span class="sxs-lookup"><span data-stu-id="ebafd-128">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="ebafd-129">**動作。類型**</span><span class="sxs-lookup"><span data-stu-id="ebafd-129">**action.type**</span></span>                                                   | <span data-ttu-id="ebafd-130">**已 \_ 允許的 .FWP 動作 \_**</span><span class="sxs-lookup"><span data-stu-id="ebafd-130">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="ebafd-131">**weight**</span><span class="sxs-lookup"><span data-stu-id="ebafd-131">**weight**</span></span>                                                        | [<span data-ttu-id="ebafd-132">**FWPM \_ 權數 \_ 範圍 \_ IKE \_ 豁免**</span><span class="sxs-lookup"><span data-stu-id="ebafd-132">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="ebafd-133">**在 FWPM \_ 層 \_ 輸出 \_ 傳輸 \_ V {4 \| 6} 上，設定每個封包篩選規則的輸出**</span><span class="sxs-lookup"><span data-stu-id="ebafd-133">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="ebafd-134">新增具有下列屬性的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="ebafd-134">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="ebafd-135">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="ebafd-135">Filter property</span></span>                                                   | <span data-ttu-id="ebafd-136">值</span><span class="sxs-lookup"><span data-stu-id="ebafd-136">Value</span></span>                                                  |
    |-------------------------------------------------------------------|--------------------------------------------------------|
    | <span data-ttu-id="ebafd-137">**FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="ebafd-137">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="ebafd-138">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="ebafd-138">NlatUnicast</span></span>                                            |
    | <span data-ttu-id="ebafd-139">**FWPM \_條件 \_ IP \_ 本機 \_ 位址** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="ebafd-139">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS** filtering condition</span></span>       | <span data-ttu-id="ebafd-140">適當的本機位址 (1.1.1.1 或 2.2.2.2) 。</span><span class="sxs-lookup"><span data-stu-id="ebafd-140">The appropriate local address (1.1.1.1 or 2.2.2.2).</span></span>    |
    | <span data-ttu-id="ebafd-141">**FWPM \_條件 \_ IP \_ 遠端 \_ 位址** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="ebafd-141">**FWPM\_CONDITION\_IP\_REMOTE\_ADDRESS** filtering condition</span></span>      | <span data-ttu-id="ebafd-142">適當的遠端位址 (1.1.1.1 或 2.2.2.2) 。</span><span class="sxs-lookup"><span data-stu-id="ebafd-142">The appropriate remote address (1.1.1.1 or 2.2.2.2).</span></span>   |
    | <span data-ttu-id="ebafd-143">**動作。類型**</span><span class="sxs-lookup"><span data-stu-id="ebafd-143">**action.type**</span></span>                                                   | <span data-ttu-id="ebafd-144">**已 \_ 終止的 .FWP 動作 \_ 標注 \_**</span><span class="sxs-lookup"><span data-stu-id="ebafd-144">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                  |
    | <span data-ttu-id="ebafd-145">**calloutKey**</span><span class="sxs-lookup"><span data-stu-id="ebafd-145">**action.calloutKey**</span></span>                                             | <span data-ttu-id="ebafd-146">**FWPM \_ 標注 \_ IPSEC \_ 輸出 \_ 傳輸 \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="ebafd-146">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span> |

        
2.  <span data-ttu-id="ebafd-147">藉由新增具有下列屬性的篩選準則，從 IPsec 豁免 ICMP 流量。</span><span class="sxs-lookup"><span data-stu-id="ebafd-147">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 

    | <span data-ttu-id="ebafd-148">篩選屬性</span><span class="sxs-lookup"><span data-stu-id="ebafd-148">Filter property</span></span>                                                   | <span data-ttu-id="ebafd-149">值</span><span class="sxs-lookup"><span data-stu-id="ebafd-149">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="ebafd-150">**FWPM \_條件 \_ IP \_ 本機 \_ 位址 \_ 類型** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="ebafd-150">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="ebafd-151">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="ebafd-151">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="ebafd-152">**FWPM \_條件 \_ IP \_ 通訊協定** 篩選準則</span><span class="sxs-lookup"><span data-stu-id="ebafd-152">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="ebafd-153">**IPPROTO \_ICMP {V6}** 這些常數定義于 winsock2. h 中。</span><span class="sxs-lookup"><span data-stu-id="ebafd-153">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="ebafd-154">**動作。類型**</span><span class="sxs-lookup"><span data-stu-id="ebafd-154">**action.type**</span></span>                                                   | <span data-ttu-id="ebafd-155">**已 \_ 允許的 .FWP 動作 \_**</span><span class="sxs-lookup"><span data-stu-id="ebafd-155">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="ebafd-156">**weight**</span><span class="sxs-lookup"><span data-stu-id="ebafd-156">**weight**</span></span>                                                        | <span data-ttu-id="ebafd-157">**FWPM \_ 權數 \_ 範圍 \_ IKE \_ 豁免**</span><span class="sxs-lookup"><span data-stu-id="ebafd-157">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

<span data-ttu-id="ebafd-158">**設定輸入和輸出安全性關聯**</span><span class="sxs-lookup"><span data-stu-id="ebafd-158">**Setup inbound and outbound security associations**</span></span>

1.  <span data-ttu-id="ebafd-159">使用 *outboundTraffic* 參數（其中包含作為 1.1.1.1 & 2.2.2.2 的 IP 位址）來呼叫 [**IPsecSaCoNtextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)，並將 **ipsecFilterId** 作為上面新增的輸出傳輸層 IPsec 標注篩選器的 LUID。</span><span class="sxs-lookup"><span data-stu-id="ebafd-159">Call [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), with the *outboundTraffic* parameter containing the IP addresses as 1.1.1.1 & 2.2.2.2, and **ipsecFilterId** as the LUID of the outbound transport layer IPsec callout filter added above.</span></span>
2.  <span data-ttu-id="ebafd-160">使用 *id* 參數（其中包含從 [**IPsecSaCoNtextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)傳回的內容識別碼）和 *getSpi* 參數（包含 IPsecSaCoNtextGetSpi0 的 IP 位址）來呼叫 [](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)，並以 1.1.1.1 & 2.2.2.2）和 **ipsecFilterId** 作為上述新增的輸入傳輸層 IPsec 標注篩選器的 LUID。</span><span class="sxs-lookup"><span data-stu-id="ebafd-160">Call [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0), with the *id* parameter containing the context ID returned from [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), and the *getSpi* parameter containing the IP addresses as 1.1.1.1 & 2.2.2.2, and **ipsecFilterId** as the LUID of the inbound transport layer IPsec callout filter added above.</span></span> <span data-ttu-id="ebafd-161">傳回的 SPI 值是用來做為本機電腦的輸入 SA SPI，以及對應遠端電腦的輸出 SA SPI。</span><span class="sxs-lookup"><span data-stu-id="ebafd-161">The returned SPI value is meant to be used as the inbound SA SPI by the local machine and as the outbound SA SPI by the corresponding remote machine.</span></span> <span data-ttu-id="ebafd-162">這兩部電腦都必須使用頻外的方式來交換 SPI 值。</span><span class="sxs-lookup"><span data-stu-id="ebafd-162">Both machines must use some out-of-band means to exchange the SPI values.</span></span>
3.  <span data-ttu-id="ebafd-163">使用 *識別碼* 參數（其中包含從 [**IPsecSaCoNtextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)傳回的內容識別碼）和 *inboundBundle* 參數（描述輸入 SA 的 (，例如輸入 sa SPI、轉換類型、演算法類型、金鑰) 等）來呼叫 [**IPsecSaCoNtextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)。</span><span class="sxs-lookup"><span data-stu-id="ebafd-163">Call [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0), with the *id* parameter containing the context ID returned from [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), and the *inboundBundle* parameter describing the properties of the inbound SA bundle (such as the inbound SA SPI, transform type, algorithm types, keys, etc).</span></span>
4.  <span data-ttu-id="ebafd-164">使用 *識別碼* 參數（其中包含從 [**IPsecSaCoNtextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)傳回的內容識別碼）和 *outboundBundle* 參數（描述輸出 SA 的 (，例如輸出 sa SPI、轉換類型、演算法類型、金鑰) 等）來呼叫 [**IPsecSaCoNtextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)。</span><span class="sxs-lookup"><span data-stu-id="ebafd-164">Call [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0), with the *id* parameter containing the context ID returned from [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), and the *outboundBundle* parameter describing the properties of the outbound SA bundle (such as the outbound SA SPI, transform type, algorithm types, keys, etc).</span></span>

  
</dl>

## <a name="related-topics"></a><span data-ttu-id="ebafd-165">相關主題</span><span class="sxs-lookup"><span data-stu-id="ebafd-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebafd-166">範例程式碼：手動 SA 加密</span><span class="sxs-lookup"><span data-stu-id="ebafd-166">Sample code: Manual SA Keying</span></span>](manual-sa-keying.md)
</dt> <dt>

[<span data-ttu-id="ebafd-167">**內建的標注識別碼**</span><span class="sxs-lookup"><span data-stu-id="ebafd-167">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="ebafd-168">**篩選層識別碼**</span><span class="sxs-lookup"><span data-stu-id="ebafd-168">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="ebafd-169">**FWPM \_ ACTION0**</span><span class="sxs-lookup"><span data-stu-id="ebafd-169">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> </dl>

 

