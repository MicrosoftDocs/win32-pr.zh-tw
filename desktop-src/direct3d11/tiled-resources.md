---
title: 磚資源
description: 您可以將已平平的資源視為大型邏輯資源，其使用少量的實體記憶體。
ms.assetid: 03083460-192b-40cb-8ee1-76df6d95f72b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7c7e6aaf60f58f55274c9d7a135b9107933f640
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839432"
---
# <a name="tiled-resources"></a><span data-ttu-id="19591-103">磚資源</span><span class="sxs-lookup"><span data-stu-id="19591-103">Tiled resources</span></span>

<span data-ttu-id="19591-104">您可以將已平平的資源視為大型邏輯資源，其使用少量的實體記憶體。</span><span class="sxs-lookup"><span data-stu-id="19591-104">Tiled resources can be thought of as large logical resources that use small amounts of physical memory.</span></span>

<span data-ttu-id="19591-105">本節說明為何需要並排顯示的資源，以及如何建立和使用並排顯示的資源。</span><span class="sxs-lookup"><span data-stu-id="19591-105">This section describes why tiled resources are needed and how you create and use tiled resources.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="19591-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="19591-106">In this section</span></span>



| <span data-ttu-id="19591-107">主題</span><span class="sxs-lookup"><span data-stu-id="19591-107">Topic</span></span>                                                                                   | <span data-ttu-id="19591-108">描述</span><span class="sxs-lookup"><span data-stu-id="19591-108">Description</span></span>                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="19591-109">為何需要磚資源？</span><span class="sxs-lookup"><span data-stu-id="19591-109">Why are tiled resources needed?</span></span>](why-are-tiled-resources-needed-.md)<br/>       | <span data-ttu-id="19591-110">需要有並排的資源，因此 (GPU) 記憶體會浪費儲存應用程式知道將無法存取的介面區域，而且硬體可以瞭解如何在連續的磚之間進行篩選。</span><span class="sxs-lookup"><span data-stu-id="19591-110">Tiled resources are needed so less graphics processing unit (GPU) memory is wasted storing regions of surfaces that the application knows will not be accessed, and the hardware can understand how to filter across adjacent tiles.</span></span><br/>     |
| [<span data-ttu-id="19591-111">建立磚資源</span><span class="sxs-lookup"><span data-stu-id="19591-111">Creating tiled resources</span></span>](creating-tiled-resources.md)<br/>                     | <span data-ttu-id="19591-112">建立資源時，藉由指定 [**D3D11 \_ 資源的「 \_ 其他 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) 並排顯示」旗標來建立並排顯示的資源。</span><span class="sxs-lookup"><span data-stu-id="19591-112">Tiled resources are created by specifying the [**D3D11\_RESOURCE\_MISC\_TILED**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) flag when you create a resource.</span></span><br/>                                                                                          |
| [<span data-ttu-id="19591-113">磚資源 Api</span><span class="sxs-lookup"><span data-stu-id="19591-113">Tiled Resource APIs</span></span>](tiled-resource-apis.md)<br/>                               | <span data-ttu-id="19591-114">本節所述的 Api 適用于磚化的資源和磚集區。</span><span class="sxs-lookup"><span data-stu-id="19591-114">The APIs described in this section work with tiled resources and tile pool.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="19591-115">磚資源的管線存取</span><span class="sxs-lookup"><span data-stu-id="19591-115">Pipeline access to tiled resources</span></span>](pipeline-access-to-tiled-resources.md)<br/> | <span data-ttu-id="19591-116">磚資源可用於著色器資源檢視 (SRV) 、轉譯目標視圖 (RTV) 、深度樣板視圖 (DSV) 和未排序的存取權視圖 (UAV) ，以及某些未使用視圖的系結點，例如頂點緩衝區系結。</span><span class="sxs-lookup"><span data-stu-id="19591-116">Tiled resources can be used in shader resource views (SRV), render target views (RTV), depth stencil views (DSV) and unordered access views (UAV), as well as some bind points where views aren't used, such as vertex buffer bindings.</span></span> <br/> |
| [<span data-ttu-id="19591-117">磚資源功能層級</span><span class="sxs-lookup"><span data-stu-id="19591-117">Tiled resources features tiers</span></span>](tiled-resources-features-tiers.md)<br/>         | <span data-ttu-id="19591-118">Direct3D 11.2 會以 D3D11 並排顯示的 [**\_ \_ 資源 \_ 層級**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) 值，來公開兩個層級的並排資源支援。</span><span class="sxs-lookup"><span data-stu-id="19591-118">Direct3D 11.2 exposes tiled resources support in two tiers with the [**D3D11\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) values.</span></span> <br/>                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="19591-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="19591-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19591-120">資源</span><span class="sxs-lookup"><span data-stu-id="19591-120">Resources</span></span>](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 





