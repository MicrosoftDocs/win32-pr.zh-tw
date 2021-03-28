---
title: Direct3D 11.3 功能
description: 下列各節說明 Direct3D 11.3 中已新增的功能。 這些功能也可在 Direct3D 12 中使用。
ms.assetid: CA79A315-22C4-4141-8E66-89C0DCF29191
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc256b9b85dd807e2e6c923affdec496fe92e075
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104383353"
---
# <a name="direct3d-113-features"></a><span data-ttu-id="e5fe5-104">Direct3D 11.3 功能</span><span class="sxs-lookup"><span data-stu-id="e5fe5-104">Direct3D 11.3 Features</span></span>

<span data-ttu-id="e5fe5-105">下列各節說明 Direct3D 11.3 中已新增的功能。</span><span class="sxs-lookup"><span data-stu-id="e5fe5-105">The following sections describe the functionality has been added in Direct3D 11.3.</span></span> <span data-ttu-id="e5fe5-106">這些功能也可在 Direct3D 12 中使用。</span><span class="sxs-lookup"><span data-stu-id="e5fe5-106">These features are also available in Direct3D 12.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="e5fe5-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="e5fe5-107">In this section</span></span>



| <span data-ttu-id="e5fe5-108">主題</span><span class="sxs-lookup"><span data-stu-id="e5fe5-108">Topic</span></span>                                                                                               | <span data-ttu-id="e5fe5-109">描述</span><span class="sxs-lookup"><span data-stu-id="e5fe5-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5fe5-110">保守的點陣化</span><span class="sxs-lookup"><span data-stu-id="e5fe5-110">Conservative Rasterization</span></span>](conservative-rasterization.md)<br/>                             | <span data-ttu-id="e5fe5-111">保守地柵格化可為圖元轉譯新增一些確定性，這對碰撞偵測演算法特別有用。</span><span class="sxs-lookup"><span data-stu-id="e5fe5-111">Conservative rasterization adds some certainty to pixel rendering, which is helpful in particular to collision detection algorithms.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="e5fe5-112">預設材質對應</span><span class="sxs-lookup"><span data-stu-id="e5fe5-112">Default Texture Mapping</span></span>](default-texture-mapping.md)<br/>                                   | <span data-ttu-id="e5fe5-113">使用預設材質對應可減少在 GPU 和 CPU 之間共用映射資料時的複製和記憶體使用量。</span><span class="sxs-lookup"><span data-stu-id="e5fe5-113">The use of default texture mapping reduces copying and memory usage while sharing image data between the GPU and the CPU.</span></span> <span data-ttu-id="e5fe5-114">不過，它應該只在特定情況下使用。</span><span class="sxs-lookup"><span data-stu-id="e5fe5-114">However, it should only be used in specific situations.</span></span> <span data-ttu-id="e5fe5-115">標準 swizzle 配置可避免複製或 swizzling 多個版面配置中的資料。</span><span class="sxs-lookup"><span data-stu-id="e5fe5-115">The standard swizzle layout avoids copying or swizzling data in multiple layouts.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="e5fe5-116">轉譯器順序視圖</span><span class="sxs-lookup"><span data-stu-id="e5fe5-116">Rasterizer Order Views</span></span>](rasterizer-order-views.md)<br/>                                     | <span data-ttu-id="e5fe5-117">以轉譯器排序的視圖 (ROVs) 允許圖元著色器程式碼將 UAV 系結標示為會改變 UAVs 圖形管線結果順序的一般需求。</span><span class="sxs-lookup"><span data-stu-id="e5fe5-117">Rasterizer ordered views (ROVs) allow pixel shader code to mark UAV bindings with a declaration that alters the normal requirements for the order of graphics pipeline results for UAVs.</span></span> <span data-ttu-id="e5fe5-118">這可讓您 (OIT) 演算法來運作，以提供更好的轉譯結果，當多個透明物件在視圖中彼此對齊時，可提供更好的呈現結果。</span><span class="sxs-lookup"><span data-stu-id="e5fe5-118">This enables Order Independent Transparency (OIT) algorithms to work, which give much better rendering results when multiple transparent objects are in line with each other in a view.</span></span> <br/> |
| [<span data-ttu-id="e5fe5-119">著色器指定的樣板參考值</span><span class="sxs-lookup"><span data-stu-id="e5fe5-119">Shader Specified Stencil Reference Value</span></span>](shader-specified-stencil-reference-value.md)<br/> | <span data-ttu-id="e5fe5-120">啟用圖元著色器以輸出樣板參考值，而不是使用 API 指定的值，讓您能夠對樣板作業進行細微的控制。</span><span class="sxs-lookup"><span data-stu-id="e5fe5-120">Enabling pixel shaders to output the Stencil Reference Value, rather than using the API-specified one, enables a very fine granular control over stencil operations.</span></span><br/>                                                                                                                                                                                                              |
| [<span data-ttu-id="e5fe5-121">具類型的未排序存取視圖載入</span><span class="sxs-lookup"><span data-stu-id="e5fe5-121">Typed Unordered Access View Loads</span></span>](typed-unordered-access-view-loads.md)<br/>               | <span data-ttu-id="e5fe5-122">未排序的存取視圖 (UAV) 具類型的負載，是可讓著色器從具有特定 DXGI 格式的 UAV 讀取的能力 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e5fe5-122">Unordered Access View (UAV) Typed Load is the ability for a shader to read from a UAV with a specific DXGI\_FORMAT.</span></span><br/>                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="e5fe5-123">統一記憶體架構</span><span class="sxs-lookup"><span data-stu-id="e5fe5-123">Unified Memory Architecture</span></span>](unified-memory-architecture.md)<br/>                           | <span data-ttu-id="e5fe5-124">查詢是否支援統一記憶體架構 (UMA) 可協助判斷如何處理某些資源。</span><span class="sxs-lookup"><span data-stu-id="e5fe5-124">Querying for whether Unified Memory Architecture (UMA) is supported can help determine how to handle some resources.</span></span><br/>                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="e5fe5-125">磁片區磚資源</span><span class="sxs-lookup"><span data-stu-id="e5fe5-125">Volume Tiled Resources</span></span>](volume-tiled-resources.md)<br/>                                     | <span data-ttu-id="e5fe5-126">磁片區 (3D) 材質可以用來做為並排的資源，請注意磚解析度是三維。</span><span class="sxs-lookup"><span data-stu-id="e5fe5-126">Volume (3D) textures can be used as tiled resources, noting that tile resolution is three-dimensional.</span></span><br/>                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="e5fe5-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="e5fe5-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5fe5-128">Direct3D 11 的新功能</span><span class="sxs-lookup"><span data-stu-id="e5fe5-128">What's new in Direct3D 11</span></span>](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 





