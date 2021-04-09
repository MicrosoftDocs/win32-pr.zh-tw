---
description: 霧化參數是透過裝置轉譯狀態來控制。
ms.assetid: a3c5f439-6937-4ba9-991f-5a4154447cf9
title: " (Direct3D 9) 的霧化參數"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03104df36aba0868c15ccc0b8ddc78d1352bef7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846172"
---
# <a name="fog-parameters-direct3d-9"></a><span data-ttu-id="9d063-103"> (Direct3D 9) 的霧化參數</span><span class="sxs-lookup"><span data-stu-id="9d063-103">Fog Parameters (Direct3D 9)</span></span>

<span data-ttu-id="9d063-104">霧化參數是透過裝置轉譯狀態來控制。</span><span class="sxs-lookup"><span data-stu-id="9d063-104">Fog parameters are controlled through device render states.</span></span> <span data-ttu-id="9d063-105">圖元和頂點霧化類型都支援在 [ (Direct3D 9) 的霧化公式 ](fog-formulas.md)中引進的所有霧化公式。</span><span class="sxs-lookup"><span data-stu-id="9d063-105">Both pixel and vertex fog types support all the fog formulas introduced in [Fog Formulas (Direct3D 9)](fog-formulas.md).</span></span> <span data-ttu-id="9d063-106">[**D3DFOGMODE**](./d3dfogmode.md)列舉型別定義常數，可讓您用來識別您想要 Microsoft Direct3D 使用的霧化公式。</span><span class="sxs-lookup"><span data-stu-id="9d063-106">The [**D3DFOGMODE**](./d3dfogmode.md) enumerated type defines constants that you can use to identify the fog formula you want Microsoft Direct3D to use.</span></span> <span data-ttu-id="9d063-107">D3DRS \_ FOGTABLEMODE 轉譯狀態控制 Direct3D 用於圖元霧化的霧化模式，而 D3DRS FOGVERTEXMODE 轉譯狀態則 \_ 控制頂點霧化的模式。</span><span class="sxs-lookup"><span data-stu-id="9d063-107">The D3DRS\_FOGTABLEMODE render state controls the fog mode that Direct3D uses for pixel fog, and the D3DRS\_FOGVERTEXMODE render state controls the mode for vertex fog.</span></span>

<span data-ttu-id="9d063-108">使用線性霧化公式時，您可以透過 D3DRS \_ FOGSTART 和 D3DRS FOGEND 轉譯狀態來設定開始和結束距離 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9d063-108">When using the linear fog formula, you set the starting and ending distances through the D3DRS\_FOGSTART and D3DRS\_FOGEND render states.</span></span> <span data-ttu-id="9d063-109">系統解釋這些值的方式取決於您的應用程式所使用的霧化類型-圖元或頂點霧化，以及當使用圖元霧化時，如果使用以 z 為基礎或以 w 為基礎的深度。</span><span class="sxs-lookup"><span data-stu-id="9d063-109">How the system interprets these values depends on the type of fog your application uses - pixel or vertex fog - and, when using pixel fog, if z-based or w-based depth is being used.</span></span> <span data-ttu-id="9d063-110">下表匯總了霧型別及其開始與結束單位。</span><span class="sxs-lookup"><span data-stu-id="9d063-110">The following table summarizes fog types and their start and end units.</span></span>



| <span data-ttu-id="9d063-111">霧化類型</span><span class="sxs-lookup"><span data-stu-id="9d063-111">Fog type</span></span>  | <span data-ttu-id="9d063-112">霧化開始/結束單位</span><span class="sxs-lookup"><span data-stu-id="9d063-112">Fog start/end units</span></span>      |
|-----------|--------------------------|
| <span data-ttu-id="9d063-113">圖元 (Z) </span><span class="sxs-lookup"><span data-stu-id="9d063-113">Pixel (Z)</span></span> | <span data-ttu-id="9d063-114">裝置空間 \[ 0.0、1。0\]</span><span class="sxs-lookup"><span data-stu-id="9d063-114">Device space \[0.0,1.0\]</span></span> |
| <span data-ttu-id="9d063-115">圖元 (W) </span><span class="sxs-lookup"><span data-stu-id="9d063-115">Pixel (W)</span></span> | <span data-ttu-id="9d063-116">攝影機空間</span><span class="sxs-lookup"><span data-stu-id="9d063-116">Camera space</span></span>             |
| <span data-ttu-id="9d063-117">頂點</span><span class="sxs-lookup"><span data-stu-id="9d063-117">Vertex</span></span>    | <span data-ttu-id="9d063-118">攝影機空間</span><span class="sxs-lookup"><span data-stu-id="9d063-118">Camera space</span></span>             |



 

<span data-ttu-id="9d063-119">D3DRS \_ FOGDENSITY 轉譯狀態會控制啟用指數霧化公式時所套用的霧化密度。</span><span class="sxs-lookup"><span data-stu-id="9d063-119">The D3DRS\_FOGDENSITY render state controls the fog density applied when an exponential fog formula is enabled.</span></span> <span data-ttu-id="9d063-120">相較于從0.0 到 1.0 (內含) ，相較于調整指數中的距離值，霧化密度基本上是加權因數。</span><span class="sxs-lookup"><span data-stu-id="9d063-120">Fog density is essentially a weighting factor, ranging from 0.0 to 1.0 (inclusive), that scales the distance value in the exponent.</span></span>

<span data-ttu-id="9d063-121">系統用於霧化混色的色彩是透過 D3DRS \_ FOGCOLOR 裝置轉譯狀態來控制。</span><span class="sxs-lookup"><span data-stu-id="9d063-121">The color that the system uses for fog blending is controlled through the D3DRS\_FOGCOLOR device render state.</span></span> <span data-ttu-id="9d063-122">如需詳細資訊，請參閱 [ (direct3d 9 的霧化色彩) ](fog-color.md) 和 [ (direct3d 9) 的霧化 ](fog-blending.md)混色。</span><span class="sxs-lookup"><span data-stu-id="9d063-122">For more information, see [Fog Color (Direct3D 9)](fog-color.md) and [Fog Blending (Direct3D 9)](fog-blending.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d063-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="9d063-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d063-124">霧化類型</span><span class="sxs-lookup"><span data-stu-id="9d063-124">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 
