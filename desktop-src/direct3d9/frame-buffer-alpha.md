---
description: 框架緩衝區 Alpha-混色與頂點 Alpha、材質 Alpha 和材質 Alpha 有點不同。
ms.assetid: 3664215d-ad03-400e-beab-b0421cf6b693
title: " (Direct3D 9) 的框架緩衝區 Alpha"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb310e2c66f43282e65425fd0d6c6a24961accaa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108740"
---
# <a name="frame-buffer-alpha-direct3d-9"></a><span data-ttu-id="dea43-103"> (Direct3D 9) 的框架緩衝區 Alpha</span><span class="sxs-lookup"><span data-stu-id="dea43-103">Frame Buffer Alpha (Direct3D 9)</span></span>

<span data-ttu-id="dea43-104">框架緩衝區 Alpha-混色與頂點 Alpha、材質 Alpha 和材質 Alpha 有點不同。</span><span class="sxs-lookup"><span data-stu-id="dea43-104">Frame buffer alpha-blending is a bit different than vertex alpha, material alpha, and texture alpha.</span></span> <span data-ttu-id="dea43-105">頂點、材質和材質 Alpha 設定的透明度值只用于目前的基本專案，而且本身不會影響其他基本專案。</span><span class="sxs-lookup"><span data-stu-id="dea43-105">Vertex, material, and texture alpha set transparency values that are used only for the current primitive, and by themselves have no effect on other primitives.</span></span> <span data-ttu-id="dea43-106">框架緩衝區 Alpha-混合控制目前的基本類型如何與框架緩衝區中的現有圖元結合，以產生最終圖元色彩。</span><span class="sxs-lookup"><span data-stu-id="dea43-106">Frame buffer alpha-blending controls how the current primitive is combined with existing pixels in the frame buffer to yield a final pixel color.</span></span>

<span data-ttu-id="dea43-107">執行 Alpha 混色時，會結合兩種色彩：來源色彩和目的色彩。</span><span class="sxs-lookup"><span data-stu-id="dea43-107">When performing alpha blending, two colors are being combined: a source color and a destination color.</span></span> <span data-ttu-id="dea43-108">來源色彩是來自透明物件，目的色彩是已在圖元位置的色彩。</span><span class="sxs-lookup"><span data-stu-id="dea43-108">The source color is from the transparent object, the destination color is the color already at the pixel location.</span></span> <span data-ttu-id="dea43-109">目的色彩是轉譯其他位於透明物件後方的物件（也就是可透過透明物件看見的物件）的結果。</span><span class="sxs-lookup"><span data-stu-id="dea43-109">The destination color is the result of rendering some other object that is behind the transparent object, that is, the object that will be visible through the transparent object.</span></span> <span data-ttu-id="dea43-110">Alpha 混色會使用公式來控制來源和目的地物件之間的比率。</span><span class="sxs-lookup"><span data-stu-id="dea43-110">Alpha blending uses a formula to control the ratio between the source and destination objects.</span></span>


```
Final Color = ObjectColor * SourceBlendFactor + PixelColor * DestinationBlendFactor 
```



<span data-ttu-id="dea43-111">ObjectColor 是在目前圖元位置轉譯的基本內容。</span><span class="sxs-lookup"><span data-stu-id="dea43-111">ObjectColor is the contribution from the primitive being rendered at the current pixel location.</span></span> <span data-ttu-id="dea43-112">PixelColor 是來自目前圖元位置的框架緩衝區所占的比重。</span><span class="sxs-lookup"><span data-stu-id="dea43-112">PixelColor is the contribution from the frame buffer at the current pixel location.</span></span>

<span data-ttu-id="dea43-113">以下列出一組可以使用的 Alpha blend 因素。</span><span class="sxs-lookup"><span data-stu-id="dea43-113">The set of alpha blend factors that can be used are listed below.</span></span>



| <span data-ttu-id="dea43-114">Blend 模式因數</span><span class="sxs-lookup"><span data-stu-id="dea43-114">Blend mode factor</span></span>         | <span data-ttu-id="dea43-115">Description</span><span class="sxs-lookup"><span data-stu-id="dea43-115">Description</span></span>                                                                                                                                                                              |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dea43-116">D3DBLEND \_ 零</span><span class="sxs-lookup"><span data-stu-id="dea43-116">D3DBLEND\_ZERO</span></span>            | <span data-ttu-id="dea43-117"> (0、0、0、0) </span><span class="sxs-lookup"><span data-stu-id="dea43-117">(0, 0, 0, 0)</span></span>                                                                                                                                                                             |
| <span data-ttu-id="dea43-118">D3DBLEND \_ 一</span><span class="sxs-lookup"><span data-stu-id="dea43-118">D3DBLEND\_ONE</span></span>             | <span data-ttu-id="dea43-119"> (1，1，1，1) </span><span class="sxs-lookup"><span data-stu-id="dea43-119">(1, 1, 1, 1)</span></span>                                                                                                                                                                             |
| <span data-ttu-id="dea43-120">D3DBLEND \_ SRCCOLOR</span><span class="sxs-lookup"><span data-stu-id="dea43-120">D3DBLEND\_SRCCOLOR</span></span>        | <span data-ttu-id="dea43-121"> (Rs、Gs、Bs) </span><span class="sxs-lookup"><span data-stu-id="dea43-121">(Rs, Gs, Bs, As)</span></span>                                                                                                                                                                         |
| <span data-ttu-id="dea43-122">D3DBLEND \_ INVSRCCOLOR</span><span class="sxs-lookup"><span data-stu-id="dea43-122">D3DBLEND\_INVSRCCOLOR</span></span>     | <span data-ttu-id="dea43-123"> (1-Rs、1-Gs、1-Bs、1-As) </span><span class="sxs-lookup"><span data-stu-id="dea43-123">(1-Rs, 1-Gs, 1-Bs, 1-As)</span></span>                                                                                                                                                                 |
| <span data-ttu-id="dea43-124">D3DBLEND \_ SRCALPHA</span><span class="sxs-lookup"><span data-stu-id="dea43-124">D3DBLEND\_SRCALPHA</span></span>        | <span data-ttu-id="dea43-125"> (As，as，as，as) </span><span class="sxs-lookup"><span data-stu-id="dea43-125">(As, As, As, As)</span></span>                                                                                                                                                                         |
| <span data-ttu-id="dea43-126">D3DBLEND \_ INVSRCALPHA</span><span class="sxs-lookup"><span data-stu-id="dea43-126">D3DBLEND\_INVSRCALPHA</span></span>     | <span data-ttu-id="dea43-127"> (1-As，1-as，1-As，1-As) </span><span class="sxs-lookup"><span data-stu-id="dea43-127">(1-As, 1-As, 1-As, 1-As)</span></span>                                                                                                                                                                 |
| <span data-ttu-id="dea43-128">D3DBLEND \_ DESTALPHA</span><span class="sxs-lookup"><span data-stu-id="dea43-128">D3DBLEND\_DESTALPHA</span></span>       | <span data-ttu-id="dea43-129"> (Ad、Ad、Ad、Ad) </span><span class="sxs-lookup"><span data-stu-id="dea43-129">(Ad, Ad, Ad, Ad)</span></span>                                                                                                                                                                         |
| <span data-ttu-id="dea43-130">D3DBLEND \_ INVDESTALPHA</span><span class="sxs-lookup"><span data-stu-id="dea43-130">D3DBLEND\_INVDESTALPHA</span></span>    | <span data-ttu-id="dea43-131"> (1-Ad、1-Ad、1-Ad、1-Ad) </span><span class="sxs-lookup"><span data-stu-id="dea43-131">(1-Ad, 1-Ad, 1-Ad, 1-Ad)</span></span>                                                                                                                                                                 |
| <span data-ttu-id="dea43-132">D3DBLEND \_ DESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="dea43-132">D3DBLEND\_DESTCOLOR</span></span>       | <span data-ttu-id="dea43-133"> (Rd、Gd、Bd、Ad) </span><span class="sxs-lookup"><span data-stu-id="dea43-133">(Rd, Gd, Bd, Ad)</span></span>                                                                                                                                                                         |
| <span data-ttu-id="dea43-134">D3DBLEND \_ INVDESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="dea43-134">D3DBLEND\_INVDESTCOLOR</span></span>    | <span data-ttu-id="dea43-135"> (1-Rd、1-Gd、1-Bd、1-Ad) </span><span class="sxs-lookup"><span data-stu-id="dea43-135">(1-Rd, 1-Gd, 1-Bd, 1-Ad)</span></span>                                                                                                                                                                 |
| <span data-ttu-id="dea43-136">D3DBLEND \_ SRCALPHASAT</span><span class="sxs-lookup"><span data-stu-id="dea43-136">D3DBLEND\_SRCALPHASAT</span></span>     | <span data-ttu-id="dea43-137"> (f、f、f、1) ;f = min (As，1-Ad) </span><span class="sxs-lookup"><span data-stu-id="dea43-137">(f, f, f, 1); f = min(As, 1-Ad)</span></span>                                                                                                                                                          |
| <span data-ttu-id="dea43-138">D3DBLEND \_ BOTHSRCALPHA</span><span class="sxs-lookup"><span data-stu-id="dea43-138">D3DBLEND\_BOTHSRCALPHA</span></span>    | <span data-ttu-id="dea43-139">DirectX 6 和更新版本已淘汰。</span><span class="sxs-lookup"><span data-stu-id="dea43-139">Obsolete for DirectX 6 and later.</span></span> <span data-ttu-id="dea43-140">您可以藉由將來源和目的地 blend 因數設定為 \_ \_ 在個別呼叫中 D3DBLEND SRCALPHA 和 D3DBLEND INVSRCALPHA 來達到相同的效果。</span><span class="sxs-lookup"><span data-stu-id="dea43-140">You can achieve the same effect by setting the source and destination blend factors to D3DBLEND\_SRCALPHA and D3DBLEND\_INVSRCALPHA in separate calls.</span></span> |
| <span data-ttu-id="dea43-141">D3DBLEND \_ BOTHINVSRCALPHA</span><span class="sxs-lookup"><span data-stu-id="dea43-141">D3DBLEND\_BOTHINVSRCALPHA</span></span> | <span data-ttu-id="dea43-142">DirectX 6 已淘汰。</span><span class="sxs-lookup"><span data-stu-id="dea43-142">Obsolete for DirectX 6.</span></span> <span data-ttu-id="dea43-143">您可以藉由將來源和目的地 blend 因數設定為 \_ \_ 在個別呼叫中 D3DBLEND INVSRCALPHA 和 D3DBLEND SRCALPHA 來達到相同的效果。</span><span class="sxs-lookup"><span data-stu-id="dea43-143">You can achieve the same effect by setting the source and destination blend factors to D3DBLEND\_INVSRCALPHA and D3DBLEND\_SRCALPHA in separate calls.</span></span>           |
| <span data-ttu-id="dea43-144">D3DBLEND \_ BLENDFACTOR</span><span class="sxs-lookup"><span data-stu-id="dea43-144">D3DBLEND\_BLENDFACTOR</span></span>     | <span data-ttu-id="dea43-145">使用 color. r、color. g、color. b 和 color。從 D3DRS BLENDFACTOR 設定取得的。 \_</span><span class="sxs-lookup"><span data-stu-id="dea43-145">Use color.r, color.g, color.b, and color.a obtained from the D3DRS\_BLENDFACTOR setting.</span></span>                                                                                                 |
| <span data-ttu-id="dea43-146">D3DBLEND \_ INVBLENDFACTOR</span><span class="sxs-lookup"><span data-stu-id="dea43-146">D3DBLEND\_INVBLENDFACTOR</span></span>  | <span data-ttu-id="dea43-147">使用 1-color、1-color. g、1-color. b 和1色彩。從 D3DRS BLENDFACTOR 設定取得的。 \_</span><span class="sxs-lookup"><span data-stu-id="dea43-147">Use 1-color.r, 1-color.g, 1-color.b, and 1-color.a obtained from the D3DRS\_BLENDFACTOR setting.</span></span>                                                                                         |



 

<span data-ttu-id="dea43-148">Direct3D 使用 D3DRS \_ ALPHABLENDENABLE 轉譯狀態來啟用 Alpha 透明度混合。</span><span class="sxs-lookup"><span data-stu-id="dea43-148">Direct3D uses the D3DRS\_ALPHABLENDENABLE render state to enable alpha transparency blending.</span></span> <span data-ttu-id="dea43-149">完成的 Alpha 混色類型取決於 D3DRS \_ SRCBLEND 和 D3DRS \_ DESTBLEND 轉譯狀態。</span><span class="sxs-lookup"><span data-stu-id="dea43-149">The type of alpha blending that is done depends on the D3DRS\_SRCBLEND and D3DRS\_DESTBLEND render states.</span></span> <span data-ttu-id="dea43-150">來源和目的地 blend 狀態會成對使用。</span><span class="sxs-lookup"><span data-stu-id="dea43-150">Source and destination blend states are used in pairs.</span></span> <span data-ttu-id="dea43-151">下列程式碼片段會將來源 blend 狀態設定為 D3DBLEND \_ SRCCOLOR，並將目的地 blend 狀態設定為 D3DBLEND \_ INVSRCCOLOR。</span><span class="sxs-lookup"><span data-stu-id="dea43-151">The following code fragment sets the source blend state to D3DBLEND\_SRCCOLOR and the destination blend state to D3DBLEND\_INVSRCCOLOR.</span></span>


```
// This code fragment assumes that lpD3DDevice is a 
//   valid pointer to a device.

// Enable alpha blending.
lpD3DDevice->SetRenderState(D3DRS_ALPHABLENDENABLE, 
                            TRUE);

// Set the source blend state.
lpD3DDevice->SetRenderState(D3DRS_SRCBLEND, 
                            D3DBLEND_SRCCOLOR);

// Set the destination blend state.
lpD3DDevice->SetRenderState(D3DRS_DESTBLEND, 
                            D3DBLEND_INVSRCCOLOR);
```



<span data-ttu-id="dea43-152">這段程式碼會在來源色彩之間執行線性 blend (在目前) 位置轉譯的基本型別，以及目的地色彩 (框架緩衝區) 中目前位置的色彩。</span><span class="sxs-lookup"><span data-stu-id="dea43-152">This code performs a linear blend between the source color (the color of the primitive being rendered at the current location) and the destination color (the color at the current location in the frame buffer).</span></span> <span data-ttu-id="dea43-153">產生的外觀類似于彩色玻璃，因為目的地物件的某些色彩似乎是透過來源物件傳輸;其餘的部分則會被吸收。</span><span class="sxs-lookup"><span data-stu-id="dea43-153">The resulting appearance is similar to tinted glass in that some of the color of the destination object seems to be transmitted through the source object; the rest of it appears to be absorbed.</span></span>

<span data-ttu-id="dea43-154">其中許多 blend 因數都需要材質中的 Alpha 值，才能正確運作。</span><span class="sxs-lookup"><span data-stu-id="dea43-154">Many of these blend factors require alpha values in the texture to operate correctly.</span></span> <span data-ttu-id="dea43-155">因此，使用頂點或材質 Alpha 時，應用程式會限制為會產生有趣結果的模式。</span><span class="sxs-lookup"><span data-stu-id="dea43-155">Thus, when using vertex or material alpha, the application is restricted as to which modes will produce interesting results.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dea43-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="dea43-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dea43-157">Alpha 混色</span><span class="sxs-lookup"><span data-stu-id="dea43-157">Alpha Blending</span></span>](alpha-blending.md)
</dt> </dl>

 

 



