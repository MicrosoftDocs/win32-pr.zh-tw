---
title: ALE 多播/廣播流量
description: 在應用層強制執行 (ALE) 層的所有輸入多播和廣播流量都會對應到一個全域 ALE 流程。
ms.assetid: b10b9758-8fce-4256-a25d-917e01336456
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f30b56a6e2a27a209baf66d34948b704ae321644
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300732"
---
# <a name="ale-multicastbroadcast-traffic"></a><span data-ttu-id="a96b6-103">ALE 多播/廣播流量</span><span class="sxs-lookup"><span data-stu-id="a96b6-103">ALE Multicast/Broadcast Traffic</span></span>

<span data-ttu-id="a96b6-104">在應用層強制執行 (ALE) 層的所有輸入多播和廣播流量都會對應到一個全域 [ALE 流程](ale-stateful-filtering.md)。</span><span class="sxs-lookup"><span data-stu-id="a96b6-104">All inbound multicast and broadcast traffic at the Application Layer Enforcement (ALE) layers is mapped to one global [ALE flow](ale-stateful-filtering.md).</span></span> <span data-ttu-id="a96b6-105">輸入多播和廣播封包的回應流量會分類于 [**FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) 層，並為每個回應建立個別的 ale 流程。</span><span class="sxs-lookup"><span data-stu-id="a96b6-105">Response traffic for inbound multicast and broadcast packets is classified at the [**FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer and separate ALE flows are created for each response.</span></span>

<span data-ttu-id="a96b6-106">在 ALE 層級的輸出多播和廣播流量會建立4秒的 ALE 流程。</span><span class="sxs-lookup"><span data-stu-id="a96b6-106">Outbound multicast and broadcast traffic at the ALE layers creates a 4-second ALE flow.</span></span> <span data-ttu-id="a96b6-107">根據預設，輸出多播或廣播 ALE 封包的授權將允許來自任何遠端位址的輸入流量（無論是單播、多播或廣播），最長可達4秒。</span><span class="sxs-lookup"><span data-stu-id="a96b6-107">By default, the authorization of an outbound multicast or broadcast ALE packet will permit inbound traffic, whether unicast, multicast, or broadcast, from any remote address for up to 4 seconds.</span></span> <span data-ttu-id="a96b6-108">這類的 ALE 流程只能透過符合 ALE 流程的後續輸出流量來重新整理或保持運作。</span><span class="sxs-lookup"><span data-stu-id="a96b6-108">Such an ALE flow can only be refreshed or kept alive by subsequent outbound traffic that matches the ALE flow.</span></span>

> [!Note]  
> <span data-ttu-id="a96b6-109">4秒的存留期是由內建的 callout [**FWPM \_ callout \_ SET \_ OPTIONS \_ AUTH \_ CONNECT \_ LAYER \_ V {4 \| 6}**](built-in-callout-identifiers.md)所指定。</span><span class="sxs-lookup"><span data-stu-id="a96b6-109">The 4-second lifetime is specified by the built-in callout [**FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_CONNECT\_LAYER\_V{4\|6}**](built-in-callout-identifiers.md).</span></span> <span data-ttu-id="a96b6-110">若要改變4秒的預設存留期，請新增參考 **FWPM \_ CALLOUT \_ SET \_ OPTIONS \_ AUTH \_ CONNECT \_ LAYER \_ V {4 \| 6}** CALLOUT 的篩選。</span><span class="sxs-lookup"><span data-stu-id="a96b6-110">To alter the 4-second default lifetime, add a filter that references the **FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_CONNECT\_LAYER\_V{4\|6}** callout.</span></span> <span data-ttu-id="a96b6-111">如需詳細資訊，請參閱 [ALE 流程自訂](ale-flow-customization.md) 。</span><span class="sxs-lookup"><span data-stu-id="a96b6-111">See [ALE Flow Customization](ale-flow-customization.md) for more information.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a96b6-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="a96b6-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a96b6-113">應用層強制 (ALE) </span><span class="sxs-lookup"><span data-stu-id="a96b6-113">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="a96b6-114">ALE 層</span><span class="sxs-lookup"><span data-stu-id="a96b6-114">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="a96b6-115">ALE 具狀態篩選</span><span class="sxs-lookup"><span data-stu-id="a96b6-115">ALE Stateful Filtering</span></span>](ale-stateful-filtering.md)
</dt> <dt>

[<span data-ttu-id="a96b6-116">ALE 重新授權</span><span class="sxs-lookup"><span data-stu-id="a96b6-116">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="a96b6-117">ALE 流程自訂</span><span class="sxs-lookup"><span data-stu-id="a96b6-117">ALE Flow Customization</span></span>](ale-flow-customization.md)
</dt> </dl>

 

 




