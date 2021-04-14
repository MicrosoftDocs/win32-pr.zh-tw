---
description: 紋理一律會從左上角的 (0.0、0.0) 、到右下角 (1.0、1.0) ，如下圖所示。
ms.assetid: 16fb04b9-4476-4dbe-a24f-51c0813a7917
title: " (Direct3D 9) 的雙線性材質篩選"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51213e5187c775963de2fa740847d55084c5be2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385988"
---
# <a name="bilinear-texture-filtering-direct3d-9"></a><span data-ttu-id="266d0-103"> (Direct3D 9) 的雙線性材質篩選</span><span class="sxs-lookup"><span data-stu-id="266d0-103">Bilinear Texture Filtering (Direct3D 9)</span></span>

<span data-ttu-id="266d0-104">紋理一律會從左上角的 (0.0、0.0) 、到右下角 (1.0、1.0) ，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="266d0-104">Textures are always linearly addressed from (0.0, 0.0) at the top-left corner to (1.0, 1.0) at the bottom-right corner, as shown in the following illustration.</span></span>

![4 x 4 色彩純色區塊的紋理圖例](images/bilinear-fig7a.png)

<span data-ttu-id="266d0-106">紋理的呈現方式通常將它們視為是由色彩純色區塊所組成，但如果您將紋理視為和光柵顯示相同的話，就更為正確︰每個材質都被定義在方格資料格的正中央，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="266d0-106">Textures are usually represented as if they were composed of solid blocks of color, but it's actually more correct to think of textures the same way you should think of the raster display: Each texel is defined at the exact center of a grid cell, as shown in the following illustration.</span></span>

![材質定義於方格資料格正中央的 4 x 4 紋理圖例](images/bilinear-fig7b.png)

<span data-ttu-id="266d0-108">如果您向紋理取樣工具請求此紋理在 UV 座標 (0.375, 0.375) 上的色彩，您會取得紅色 (255,0,0)。</span><span class="sxs-lookup"><span data-stu-id="266d0-108">If you ask the texture sampler for this texture's color at UV coordinates (0.375, 0.375) you'll get solid red (255, 0, 0).</span></span> <span data-ttu-id="266d0-109">這非常合理，因為 red 材質資料格的確切中心位於 UV (0.375 0.375) 。</span><span class="sxs-lookup"><span data-stu-id="266d0-109">That makes perfect sense because the exact center of the red texel cell is at UV (0.375, 0.375).</span></span> <span data-ttu-id="266d0-110">如果您向取樣工具請求 UV (0.25, 0.25)上的紋理色彩呢？</span><span class="sxs-lookup"><span data-stu-id="266d0-110">What if you ask the sampler for the texture's color at UV (0.25, 0.25)?</span></span> <span data-ttu-id="266d0-111">這並不簡單，因為位於 UV (0.25 的點，0.25) 位於4材質的確切角落。</span><span class="sxs-lookup"><span data-stu-id="266d0-111">That's not quite as easy, because the point at UV (0.25, 0.25) lies at the exact corner of 4 texels.</span></span>

<span data-ttu-id="266d0-112">最簡單的配置只是讓取樣器傳回最接近材質的色彩;這稱為「點篩選」 (查看 [ (Direct3D 9) ) 的最接近點取樣 ](nearest-point-sampling.md) ，通常是因為有顆粒狀或 blocky 結果所致。</span><span class="sxs-lookup"><span data-stu-id="266d0-112">The simplest scheme is simply to have the sampler return the color of the closest texel; this is called Point filtering (see [Nearest-Point Sampling (Direct3D 9)](nearest-point-sampling.md)), and is usually undesirable due to grainy or blocky results.</span></span> <span data-ttu-id="266d0-113">如果為我們在 UV (0.25, 0.25) 的紋理進行點取樣，會顯示出其他細微的最近點篩選問題︰有四種材質和取樣點等距，因此沒有最接近的材質。</span><span class="sxs-lookup"><span data-stu-id="266d0-113">Point-sampling our texture at UV (0.25, 0.25) shows another subtle problem with nearest-point filtering: there are four texels equidistant from the sampling point, so there's no single nearest texel.</span></span> <span data-ttu-id="266d0-114">這四項材質中的其中一個會被選為傳回的色彩，但選擇取決於座標進位的方式，這可能會造成卸除成品 (請參閱 SDK 中的最近點取樣文章)。</span><span class="sxs-lookup"><span data-stu-id="266d0-114">One of those four texels will be chosen as the returned color, but the selection depends on how the coordinate is rounded, which may introduce tearing artifacts (see the Nearest-Point Sampling article in the SDK).</span></span>

<span data-ttu-id="266d0-115">稍微更精確且更常見的篩選配置，是計算最接近取樣點的4個材質的加權平均;這稱為雙線性篩選，而額外的計算成本通常是微不足道的，因為此常式是在新式圖形硬體中執行。</span><span class="sxs-lookup"><span data-stu-id="266d0-115">A slightly more accurate and more common filtering scheme is to calculate the weighted average of the 4 texels closest to the sampling point; this is called Bilinear filtering, and the extra computational cost is usually negligible because this routine is implemented in modern graphics hardware.</span></span> <span data-ttu-id="266d0-116">以下是我們使用線性篩選，在幾個不同的範例點上取得的色彩︰</span><span class="sxs-lookup"><span data-stu-id="266d0-116">Here are the colors we get at a few different sample points using bilinear filtering:</span></span>


```
UV: (0.5, 0.5)
```



<span data-ttu-id="266d0-117">此點恰好位於紅色、藍色和白色材質之間的邊界上。</span><span class="sxs-lookup"><span data-stu-id="266d0-117">This point is at the exact border between red, green, blue, and white texels.</span></span> <span data-ttu-id="266d0-118">取樣工具傳回的色彩是灰色︰</span><span class="sxs-lookup"><span data-stu-id="266d0-118">The color the sampler returns is gray:</span></span>


```
  0.25 * (255, 0, 0)
  0.25 * (0, 255, 0) 
  0.25 * (0, 0, 255) 
## + 0.25 * (255, 255, 255) 
------------------------
= (128, 128, 128)
```




```
UV: (0.5, 0.375)
```



<span data-ttu-id="266d0-119">此點位於紅色和綠色材質交界處的中間點。</span><span class="sxs-lookup"><span data-stu-id="266d0-119">This point is at the midpoint of the border between red and green texels.</span></span> <span data-ttu-id="266d0-120">取樣工具傳回的色彩是黃灰色 (請注意，藍色與白色材質的比重被調整至 0)︰</span><span class="sxs-lookup"><span data-stu-id="266d0-120">The color the sampler returns is yellow-gray (note that the contributions of the blue and white texels are scaled to 0):</span></span>


```
  0.5 * (255, 0, 0)
  0.5 * (0, 255, 0) 
  0.0 * (0, 0, 255) 
## + 0.0 * (255, 255, 255) 
------------------------
= (128, 128, 0)
```




```
UV: (0.375, 0.375)
```



<span data-ttu-id="266d0-121">這是紅色材質的位址，而紅色也就是傳回的色彩 (所有其他材質在篩選計算中的權重為 0)︰</span><span class="sxs-lookup"><span data-stu-id="266d0-121">This is the address of the red texel, which is the returned color (all other texels in the filtering calculation are weighted to 0):</span></span>


```
  1.0 * (255, 0, 0)
  0.0 * (0, 255, 0) 
  0.0 * (0, 0, 255) 
## + 0.0 * (255, 255, 255) 
------------------------
= (255, 0, 0)
```



<span data-ttu-id="266d0-122">將這些計算和下圖進行比較，該圖顯示出如果線性篩選在 4 x 4 紋理的每個紋理位址進行計算，會產生怎麼樣的結果。</span><span class="sxs-lookup"><span data-stu-id="266d0-122">Compare these calculations against the following illustration, which shows what happens if the bilinear filtering calculation is performed at every texture address across the 4x4 texture.</span></span>

![在每個紋理位址進行雙線性篩選的 4 x 4 紋理圖例](images/bilinear-fig7c.jpg)

## <a name="related-topics"></a><span data-ttu-id="266d0-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="266d0-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="266d0-125">材質篩選</span><span class="sxs-lookup"><span data-stu-id="266d0-125">Texture Filtering</span></span>](texture-filtering.md)
</dt> </dl>

 

 



