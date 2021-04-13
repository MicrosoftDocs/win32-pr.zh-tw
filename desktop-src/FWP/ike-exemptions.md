---
title: IKE/AuthIP 豁免
description: 網際網路金鑰交換 (IKE) 和已驗證的網際網路通訊協定 (AuthIP) ，為了正常運作，必須從 IPsec 篩選豁免其網路流量。
ms.assetid: 365bfebc-250a-440f-8056-ff9601daa030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d58a6d00ddd337d56c3c00a34b6949213be6ee26
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104374566"
---
# <a name="ikeauthip-exemptions"></a><span data-ttu-id="e189e-103">IKE/AuthIP 豁免</span><span class="sxs-lookup"><span data-stu-id="e189e-103">IKE/AuthIP Exemptions</span></span>

<span data-ttu-id="e189e-104">網際網路通訊協定安全性 (IPsec) 的加密模組、網際網路金鑰交換 (IKE) 和已驗證的網際網路通訊協定 (AuthIP) ，為了能夠運作，必須從 IPsec 篩選豁免網路流量。</span><span class="sxs-lookup"><span data-stu-id="e189e-104">The Internet Protocol security (IPsec) keying modules, Internet Key Exchange (IKE) and Authenticated Internet Protocol (AuthIP), in order to function, need to exempt their network traffic from the IPsec filtering.</span></span>

<span data-ttu-id="e189e-105">在 Windows 篩選平台 (WFP) 基礎篩選引擎 (BFE) 會在新增第一個 IKE 或 AuthIP 主要模式 (MM) 原則篩選器時自動新增 IKE 和 AuthIP 豁免篩選，並在刪除最後一個 IKE 或 AuthIP MM 原則篩選器時將其刪除。</span><span class="sxs-lookup"><span data-stu-id="e189e-105">In Windows Filtering Platform (WFP) the Base Filtering Engine (BFE) automatically adds IKE and AuthIP exemption filters when the first IKE or AuthIP main mode (MM) policy filter is added and deletes them when the last IKE or AuthIP MM policy filter is deleted.</span></span> <span data-ttu-id="e189e-106">如此一來，原則提供者不需要個別管理 IKE 和 AuthIP 篩選豁免。</span><span class="sxs-lookup"><span data-stu-id="e189e-106">This way, the policy providers do not have to manage IKE and AuthIP filtering exemptions individually.</span></span>

<span data-ttu-id="e189e-107">IKE MM 原則篩選器是引擎層 [**FWPM \_ 圖層 \_ IKEEXT \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) 中的篩選器，可參考 [**FWPM \_ IPSEC \_ IKE \_ MM \_ 內容**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)類型的提供者內容。</span><span class="sxs-lookup"><span data-stu-id="e189e-107">An IKE MM policy filter is a filter in the engine layer [**FWPM\_LAYER\_IKEEXT\_V{4\|6}**](management-filtering-layer-identifiers-.md) that references a provider context of type [**FWPM\_IPSEC\_IKE\_MM\_CONTEXT**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).</span></span>

<span data-ttu-id="e189e-108">AuthIP MM 原則篩選器是引擎層 [**FWPM \_ 圖層 \_ IKEEXT \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) 中的篩選器，其參考 [**FWPM \_ IPSEC \_ AuthIP \_ MM \_ 內容**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)類型的提供者內容。</span><span class="sxs-lookup"><span data-stu-id="e189e-108">An AuthIP MM policy filter is a filter in the engine layer [**FWPM\_LAYER\_IKEEXT\_V{4\|6}**](management-filtering-layer-identifiers-.md) that references a provider context of type [**FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).</span></span>

<span data-ttu-id="e189e-109">IKE 或 AuthIP 豁免篩選是「引擎層 [**FWPM 圖層內送 \_ \_ \_ 傳輸 \_ v {4 \| 6}**](management-filtering-layer-identifiers-.md) 中的篩選準則，或 **FWPM \_ 層 \_ 輸出 \_ 傳輸 \_ v {4 \| 6}** 在 [**FWPM \_ 權數 \_ 範圍 \_ IKE \_ 豁免**](filter-weight-identifiers.md) 權數範圍中自動加權。</span><span class="sxs-lookup"><span data-stu-id="e189e-109">An IKE or AuthIP exemption filter is a filter in the engine layer [**FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6}**](management-filtering-layer-identifiers-.md) or **FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6}** auto-weighted in the [**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**](filter-weight-identifiers.md) weight range.</span></span>

<span data-ttu-id="e189e-110">BFE 所實行的 IKE 和 AuthIP 豁免如下所示。</span><span class="sxs-lookup"><span data-stu-id="e189e-110">The IKE and AuthIP exemptions implemented by BFE are as follows.</span></span>

| <span data-ttu-id="e189e-111">IP 版本</span><span class="sxs-lookup"><span data-stu-id="e189e-111">IP version</span></span>      | <span data-ttu-id="e189e-112">連接埠</span><span class="sxs-lookup"><span data-stu-id="e189e-112">Port</span></span>                        | <span data-ttu-id="e189e-113">豁免</span><span class="sxs-lookup"><span data-stu-id="e189e-113">Exemption</span></span>                                                                                                                                                                                                                             |
|-----------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e189e-114">IPv4</span><span class="sxs-lookup"><span data-stu-id="e189e-114">IPv4</span></span><br/> | <span data-ttu-id="e189e-115">UDP： 500 UDP：4500</span><span class="sxs-lookup"><span data-stu-id="e189e-115">UDP:500 UDP:4500</span></span><br/> | <span data-ttu-id="e189e-116">允許輸入傳輸層和輸出傳輸層的 IKE 和 AuthIP 流量。</span><span class="sxs-lookup"><span data-stu-id="e189e-116">Permit IKE and AuthIP traffic at the inbound transport layer and at the outbound transport layer.</span></span> <br/> <span data-ttu-id="e189e-117">在 ALE 接收/接受並連接層級時允許 IKE 和 AuthIP 流量，但會將它限制為本機系統。</span><span class="sxs-lookup"><span data-stu-id="e189e-117">Permit IKE and AuthIP traffic at the ALE receive/accept and connect layers, but restrict it to local system.</span></span><br/> |
| <span data-ttu-id="e189e-118">IPv6</span><span class="sxs-lookup"><span data-stu-id="e189e-118">IPv6</span></span><br/> | <span data-ttu-id="e189e-119">UDP：500</span><span class="sxs-lookup"><span data-stu-id="e189e-119">UDP:500</span></span><br/>          | <span data-ttu-id="e189e-120">允許輸入傳輸層和輸出傳輸層的 IKE 和 AuthIP 流量。</span><span class="sxs-lookup"><span data-stu-id="e189e-120">Permit IKE and AuthIP traffic at the inbound transport layer and at the outbound transport layer.</span></span> <br/> <span data-ttu-id="e189e-121">在 ALE 接收/接受並連接層級時允許 IKE 和 AuthIP 流量，但會將它限制為本機系統。</span><span class="sxs-lookup"><span data-stu-id="e189e-121">Permit IKE and AuthIP traffic at the ALE receive/accept and connect layers, but restrict it to local system.</span></span><br/> |



 

<span data-ttu-id="e189e-122">IKE 和 AuthIP 豁免篩選器會開放給所有位址。</span><span class="sxs-lookup"><span data-stu-id="e189e-122">The IKE and AuthIP exemption filters are open to all addresses.</span></span> <span data-ttu-id="e189e-123">若要以更細微的控制來執行防火牆，原則提供者應該在加權範圍中新增比 [**FWPM \_ 權數 \_ 範圍 \_ IKE \_ 豁免**](filter-weight-identifiers.md)更高的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="e189e-123">To implement a firewall with more granular control, policy providers should add filters in a weight range higher than [**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**](filter-weight-identifiers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e189e-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="e189e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e189e-125">IPsec 設定</span><span class="sxs-lookup"><span data-stu-id="e189e-125">IPsec Configuration</span></span>](ipsec-configuration.md)
</dt> <dt>

[<span data-ttu-id="e189e-126">篩選器加權指派</span><span class="sxs-lookup"><span data-stu-id="e189e-126">Filter Weight Assignment</span></span>](filter-weight-assignment.md)
</dt> </dl>

 

 





