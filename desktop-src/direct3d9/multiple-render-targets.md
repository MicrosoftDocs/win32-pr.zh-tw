---
description: " (的多個轉譯目標) 指的是轉譯成多個表面的能力 (請參閱使用單一繪製呼叫的 IDirect3D9Surface) 。"
ms.assetid: ae48c5ce-b7f5-4189-8b04-880836be3fe0
title: " (Direct3D 9) 的多個呈現目標"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb7aafeedb621e43abb288eb9bbceb17ddb0cc0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467773"
---
# <a name="multiple-render-targets-direct3d-9"></a><span data-ttu-id="a0da0-103"> (Direct3D 9) 的多個呈現目標</span><span class="sxs-lookup"><span data-stu-id="a0da0-103">Multiple Render Targets (Direct3D 9)</span></span>

<span data-ttu-id="a0da0-104"> (的多個轉譯目標) 指的是轉譯成多個表面的能力 (請參閱使用單一繪製呼叫的 [**IDirect3D9Surface**](/windows/desktop/api)) 。</span><span class="sxs-lookup"><span data-stu-id="a0da0-104">Multiple Render Targets (MRT) refers to the ability to render to multiple surfaces (see [**IDirect3D9Surface**](/windows/desktop/api)) with a single draw call.</span></span> <span data-ttu-id="a0da0-105">這些表面可以獨立建立。</span><span class="sxs-lookup"><span data-stu-id="a0da0-105">These surfaces can be created independently of each other.</span></span> <span data-ttu-id="a0da0-106">您可以使用 [**IDirect3DDevice9：： SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget)來設定呈現目標。</span><span class="sxs-lookup"><span data-stu-id="a0da0-106">Render targets can be set using [**IDirect3DDevice9::SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget).</span></span>

<span data-ttu-id="a0da0-107">多個呈現目標有下列限制：</span><span class="sxs-lookup"><span data-stu-id="a0da0-107">Multiple render targets have the following restrictions:</span></span>

-   <span data-ttu-id="a0da0-108">搭配使用的所有轉譯目標表面都必須具有相同的位深度，但可以是不同的格式，除非 \_ 已設定 D3DPMISCCAPS MRTINDEPENDENTBITDEPTHS 端點。</span><span class="sxs-lookup"><span data-stu-id="a0da0-108">All render target surfaces used together must have the same bit depth but can be of different formats, unless the D3DPMISCCAPS\_MRTINDEPENDENTBITDEPTHS cap is set.</span></span>
-   <span data-ttu-id="a0da0-109">多個呈現目標的所有表面都應該具有相同的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="a0da0-109">All surfaces of a multiple render target should have the same width and height.</span></span>
-   <span data-ttu-id="a0da0-110">某些實作為無法在多個轉譯目標上執行後續圖元著色器作業，包括：無遞色、Alpha 測試、無 fogging、無混色或遮罩（z 測試和樣板測試除外）。</span><span class="sxs-lookup"><span data-stu-id="a0da0-110">Some implementations cannot perform post-pixel shader operations on multiple render targets, including: no dithering, alpha test, no fogging, no blending or masking, except the z-test and stencil test.</span></span> <span data-ttu-id="a0da0-111">可支援後置圖元著色器作業的裝置會將 cap 位設定為 D3DPMISCCAPS \_ MRTPOSTPIXELSHADERBLENDING。</span><span class="sxs-lookup"><span data-stu-id="a0da0-111">Devices that can support post-pixel shader operations set the cap bit to D3DPMISCCAPS\_MRTPOSTPIXELSHADERBLENDING.</span></span>

    <span data-ttu-id="a0da0-112">\_設定 D3DPMISCCAPS MRTPOSTPIXELSHADERBLENDING cap 時，您必須先參考 [**IDirect3D9：： CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) ，並 \_ \_ \_ 針對特定的介面格式使用使用方式查詢 POSTPIXELSHADER 混合結果。</span><span class="sxs-lookup"><span data-stu-id="a0da0-112">When the D3DPMISCCAPS\_MRTPOSTPIXELSHADERBLENDING cap is set, you must first consult the [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) with the USAGE\_QUERY\_POSTPIXELSHADER\_BLENDING result for the specific surface format.</span></span> <span data-ttu-id="a0da0-113">如果為 false，則表示該特定表面格式無法使用任何的後置圖元著色器混合作業。</span><span class="sxs-lookup"><span data-stu-id="a0da0-113">If false, no post-pixel shader blending operations will be available for that specific surface format.</span></span> <span data-ttu-id="a0da0-114">若為 true，則裝置預期會將相同的狀態套用至所有同時呈現的目標，如下所示：</span><span class="sxs-lookup"><span data-stu-id="a0da0-114">If true, the device is expected to apply the same state to all simultaneous render targets as follows:</span></span>

    -   <span data-ttu-id="a0da0-115">Alpha blend： oCi 中的色彩值與第 i 個呈現目標混合。</span><span class="sxs-lookup"><span data-stu-id="a0da0-115">Alpha blend: The color value in oCi is blended with the ith render target.</span></span>
    -   <span data-ttu-id="a0da0-116">Alpha 測試： oC0 會進行比較。</span><span class="sxs-lookup"><span data-stu-id="a0da0-116">Alpha test: Comparison will happen with oC0.</span></span> <span data-ttu-id="a0da0-117">如果比較失敗，則會結束所有呈現目標的圖元測試。</span><span class="sxs-lookup"><span data-stu-id="a0da0-117">If the comparison fails, the pixel test is terminated for all render targets.</span></span>
    -   <span data-ttu-id="a0da0-118">霧化：轉譯目標0將會取得 fogged。</span><span class="sxs-lookup"><span data-stu-id="a0da0-118">Fog: Render target 0 will get fogged.</span></span> <span data-ttu-id="a0da0-119">未定義其他呈現目標。</span><span class="sxs-lookup"><span data-stu-id="a0da0-119">Other render targets are undefined.</span></span> <span data-ttu-id="a0da0-120">您可以選擇使用相同的狀態將它們全部霧化。</span><span class="sxs-lookup"><span data-stu-id="a0da0-120">Implementations can choose to fog them all using the same state.</span></span>
    -   <span data-ttu-id="a0da0-121">遞色：未定義。</span><span class="sxs-lookup"><span data-stu-id="a0da0-121">Dithering: Undefined.</span></span>

-   <span data-ttu-id="a0da0-122">不支援消除鋸齒。</span><span class="sxs-lookup"><span data-stu-id="a0da0-122">No antialiasing is supported.</span></span>
-   <span data-ttu-id="a0da0-123">部分的執行不會將輸出寫入遮罩套用 (D3DRS \_ COLORWRITEENABLE) 。</span><span class="sxs-lookup"><span data-stu-id="a0da0-123">Some of the implementations do not apply the output write mask (D3DRS\_COLORWRITEENABLE).</span></span> <span data-ttu-id="a0da0-124">可以有獨立色彩寫入遮罩的人。</span><span class="sxs-lookup"><span data-stu-id="a0da0-124">Those that can, have independent color write masks.</span></span> <span data-ttu-id="a0da0-125">這是使用新的功能位來表示。</span><span class="sxs-lookup"><span data-stu-id="a0da0-125">This is expressed using a new capability bit.</span></span> <span data-ttu-id="a0da0-126">可用的獨立色彩寫入遮罩數目將會等於裝置所能使用的元素數目上限。</span><span class="sxs-lookup"><span data-stu-id="a0da0-126">The number of independent color write masks available will be equal to the maximum number of elements the device is capable of.</span></span>

<span data-ttu-id="a0da0-127">新的硬體 cap：</span><span class="sxs-lookup"><span data-stu-id="a0da0-127">New hardware caps:</span></span>


```
D3DCAPS9.NumSimultaneousRTs         
// The value is 1 for all hardware except those that  
//   can support this feature. It is never 0.
D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS - True if the hardware can support it
D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING - True if the hardware can support it
```



## <a name="related-topics"></a><span data-ttu-id="a0da0-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="a0da0-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0da0-129">圖元管線</span><span class="sxs-lookup"><span data-stu-id="a0da0-129">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 
