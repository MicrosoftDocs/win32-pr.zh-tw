---
title: 磚資源功能層級
description: Direct3D 11.2 會以 D3D11 並排顯示的 \_ \_ 資源 \_ 層級值，來公開兩個層級的並排資源支援。
ms.assetid: E6A6565B-079B-47DB-A80C-CA5B5413BA32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2282cde1dfc8c4249672d18e303a4529338d4fbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931968"
---
# <a name="tiled-resources-features-tiers"></a><span data-ttu-id="12134-103">磚資源功能層級</span><span class="sxs-lookup"><span data-stu-id="12134-103">Tiled resources features tiers</span></span>

<span data-ttu-id="12134-104">Direct3D 11.2 會以 D3D11 並排顯示的 [**\_ \_ 資源 \_ 層級**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) 值，來公開兩個層級的並排資源支援。</span><span class="sxs-lookup"><span data-stu-id="12134-104">Direct3D 11.2 exposes tiled resources support in two tiers with the [**D3D11\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) values.</span></span>

<span data-ttu-id="12134-105">若要查詢硬體和驅動程式是否支援並排顯示的資源和階層層級，請將 [**D3D11 \_ FEATURE \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature)值傳遞給 [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)的 *feature* 參數。</span><span class="sxs-lookup"><span data-stu-id="12134-105">To query whether the hardware and driver support tiled resources and at what tier level, pass the [**D3D11\_FEATURE\_D3D11\_OPTIONS1**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) value to the *Feature* parameter of [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport).</span></span> <span data-ttu-id="12134-106">此外，將 [**D3D11 \_ 功能 \_ 資料 \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1) 結構的指標傳遞至 *pFeatureSupportData* 參數，並將 **D3D11 \_ 功能 \_ 資料 \_ D3D11 \_ OPTIONS1** 結構的大小傳遞給 *FeatureSupportDataSize* 參數。</span><span class="sxs-lookup"><span data-stu-id="12134-106">Also, pass a pointer to the [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1) structure to the *pFeatureSupportData* parameter, and pass the size of the **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS1** structure to the *FeatureSupportDataSize* parameter.</span></span> <span data-ttu-id="12134-107">**CheckFeatureSupport** 會在 **D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS1** 的 **TiledResourcesTier** 成員中，以 D3D11 並排顯示的 [**\_ \_ 資源 \_ 層**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier)級值傳回階層層級。</span><span class="sxs-lookup"><span data-stu-id="12134-107">**CheckFeatureSupport** returns the tier level as a [**D3D11\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) value in the **TiledResourcesTier** member of **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS1**.</span></span>

<span data-ttu-id="12134-108">本節說明這兩個層級。</span><span class="sxs-lookup"><span data-stu-id="12134-108">This section describes these two tiers.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="12134-109">本節內容</span><span class="sxs-lookup"><span data-stu-id="12134-109">In this section</span></span>



| <span data-ttu-id="12134-110">主題</span><span class="sxs-lookup"><span data-stu-id="12134-110">Topic</span></span>                           | <span data-ttu-id="12134-111">描述</span><span class="sxs-lookup"><span data-stu-id="12134-111">Description</span></span>                                       |
|---------------------------------|---------------------------------------------------|
| [<span data-ttu-id="12134-112">第 1 層</span><span class="sxs-lookup"><span data-stu-id="12134-112">Tier 1</span></span>](tier-1.md)<br/> | <span data-ttu-id="12134-113">本節描述第 1 層支援。</span><span class="sxs-lookup"><span data-stu-id="12134-113">This section describes tier 1 support.</span></span><br/> |
| [<span data-ttu-id="12134-114">第 2 層</span><span class="sxs-lookup"><span data-stu-id="12134-114">Tier 2</span></span>](tier-2.md)<br/> | <span data-ttu-id="12134-115">本節說明第2層支援。</span><span class="sxs-lookup"><span data-stu-id="12134-115">This section describes tier 2 support.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="12134-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="12134-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12134-117">磚資源</span><span class="sxs-lookup"><span data-stu-id="12134-117">Tiled resources</span></span>](tiled-resources.md)
</dt> </dl>

 

 





