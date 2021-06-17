---
description: 深入瞭解 Alpha 混色。 Alpha 混色用來顯示具有透明或半透明圖元的影像。
ms.assetid: 553b0bc8-1bd8-4282-9260-cdc5f2b8788d
title: " (Direct3D 9) 的 Alpha 混色"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd79c622778e17c5acb9b17d52b6d5db278b1508
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262000"
---
# <a name="alpha-blending-direct3d-9"></a><span data-ttu-id="c9f8f-104"> (Direct3D 9) 的 Alpha 混色</span><span class="sxs-lookup"><span data-stu-id="c9f8f-104">Alpha Blending (Direct3D 9)</span></span>

<span data-ttu-id="c9f8f-105">Alpha 混色用來顯示具有透明或半透明圖元的影像。</span><span class="sxs-lookup"><span data-stu-id="c9f8f-105">Alpha blending is used to display an image that has transparent or semi-transparent pixels.</span></span> <span data-ttu-id="c9f8f-106">除了紅色、綠色和藍色色頻外，Alpha 點陣圖中的每個圖元都有一個透明元件，稱為 Alpha 色板。</span><span class="sxs-lookup"><span data-stu-id="c9f8f-106">In addition to a red, green, and blue color channel, each pixel in an alpha bitmap has a transparency component known as its alpha channel.</span></span> <span data-ttu-id="c9f8f-107">Alpha 色板通常會包含與色頻一樣多的位數。</span><span class="sxs-lookup"><span data-stu-id="c9f8f-107">The alpha channel typically contains as many bits as a color channel.</span></span> <span data-ttu-id="c9f8f-108">例如，8位 Alpha 色板可以代表256的透明度層級，從 0 (整個圖元都是透明) 至 255 (整個圖元都不是不透明的) 。</span><span class="sxs-lookup"><span data-stu-id="c9f8f-108">For example, an 8-bit alpha channel can represent 256 levels of transparency, from 0 (the entire pixel is transparent) to 255 (the entire pixel is opaque).</span></span> <span data-ttu-id="c9f8f-109">下列清單顯示您可以使用 Alpha 混合建立的一些特殊效果。</span><span class="sxs-lookup"><span data-stu-id="c9f8f-109">The list below shows some special effects you can create using alpha blending.</span></span>

<span data-ttu-id="c9f8f-110">您可以使用或不使用 Alpha 值來定義色彩。</span><span class="sxs-lookup"><span data-stu-id="c9f8f-110">Color can be defined with or without alpha values.</span></span> <span data-ttu-id="c9f8f-111">沒有 Alpha 的色彩是 RGB 色彩，Alpha 會儲存為 ARGB。</span><span class="sxs-lookup"><span data-stu-id="c9f8f-111">Color without alpha is RGB color with alpha is stored as ARGB.</span></span> <span data-ttu-id="c9f8f-112">頂點資料、材質資料和材質資料可以用來提供物件的透明度。</span><span class="sxs-lookup"><span data-stu-id="c9f8f-112">Vertex data, material data and texture data can be used to give object's transparency.</span></span> <span data-ttu-id="c9f8f-113">框架緩衝區也可以用來產生透明度效果。</span><span class="sxs-lookup"><span data-stu-id="c9f8f-113">The frame buffer can also be used to generate transparency effects.</span></span>

-   [<span data-ttu-id="c9f8f-114"> (Direct3D 9) 的頂點 Alpha </span><span class="sxs-lookup"><span data-stu-id="c9f8f-114">Vertex Alpha (Direct3D 9)</span></span>](vertex-alpha.md)
-   [<span data-ttu-id="c9f8f-115"> (Direct3D 9 的材質 Alpha) </span><span class="sxs-lookup"><span data-stu-id="c9f8f-115">Material Alpha (Direct3D 9)</span></span>](material-alpha.md)
-   [<span data-ttu-id="c9f8f-116"> (Direct3D 9) 的材質 Alpha </span><span class="sxs-lookup"><span data-stu-id="c9f8f-116">Texture Alpha (Direct3D 9)</span></span>](texture-alpha.md)
-   [<span data-ttu-id="c9f8f-117"> (Direct3D 9) 的框架緩衝區 Alpha </span><span class="sxs-lookup"><span data-stu-id="c9f8f-117">Frame Buffer Alpha (Direct3D 9)</span></span>](frame-buffer-alpha.md)
-   [<span data-ttu-id="c9f8f-118">轉譯目標 Alpha (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="c9f8f-118">Render Target Alpha (Direct3D 9)</span></span>](render-target-alpha.md)

<span data-ttu-id="c9f8f-119">示範 Alpha 的範例包括：</span><span class="sxs-lookup"><span data-stu-id="c9f8f-119">Samples that demonstrate alpha include:</span></span>

-   [<span data-ttu-id="c9f8f-120">Billboarding (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="c9f8f-120">Billboarding (Direct3D 9)</span></span>](billboarding.md)
-   [<span data-ttu-id="c9f8f-121"> (Direct3D 9) 的雲端、冒煙和蒸氣軌跡 </span><span class="sxs-lookup"><span data-stu-id="c9f8f-121">Clouds, Smoke, and Vapor Trails (Direct3D 9)</span></span>](clouds--smoke--and-vapor-trails.md)
-   [<span data-ttu-id="c9f8f-122">)  (Direct3D 9 的火災、光暈和爆炸 </span><span class="sxs-lookup"><span data-stu-id="c9f8f-122">Fire, Flares, and Explosions (Direct3D 9)</span></span>](fire--flares--and-explosions.md)

## <a name="related-topics"></a><span data-ttu-id="c9f8f-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="c9f8f-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9f8f-124">Direct3D 轉譯</span><span class="sxs-lookup"><span data-stu-id="c9f8f-124">Direct3D Rendering</span></span>](direct3d-rendering.md)
</dt> </dl>

 

 



