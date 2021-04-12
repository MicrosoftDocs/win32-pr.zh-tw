---
description: 使用預先轉換的頂點轉譯2D 輸出時，必須小心確保每個材質區域都正確對應到單一圖元區域，否則可能會發生材質扭曲。
ms.assetid: 6faeb1e3-ea6e-4cb1-a1e6-2a9a81b4c0c7
title: 將材質直接對應至 (Direct3D 9) 的圖元
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f86e9d05acff402128ddb83fc97898ff6a21d7c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187497"
---
# <a name="directly-mapping-texels-to-pixels-direct3d-9"></a><span data-ttu-id="206b9-103">將材質直接對應至 (Direct3D 9) 的圖元</span><span class="sxs-lookup"><span data-stu-id="206b9-103">Directly Mapping Texels to Pixels (Direct3D 9)</span></span>

<span data-ttu-id="206b9-104">使用預先轉換的頂點轉譯2D 輸出時，必須小心確保每個材質區域都正確對應到單一圖元區域，否則可能會發生材質扭曲。</span><span class="sxs-lookup"><span data-stu-id="206b9-104">When rendering 2D output using pre-transformed vertices, care must be taken to ensure that each texel area correctly corresponds to a single pixel area, otherwise texture distortion can occur.</span></span> <span data-ttu-id="206b9-105">藉由瞭解 Direct3D 在將三角形進行點陣化時遵循的程式基本概念，您可以確保 Direct3D 應用程式正確轉譯2D 輸出。</span><span class="sxs-lookup"><span data-stu-id="206b9-105">By understanding the basics of the process that Direct3D follows when rasterizing and texturing triangles, you can ensure your Direct3D application correctly renders 2D output.</span></span>

![6x6 解析度顯示的圖例](images/maptex-fig1.png)

<span data-ttu-id="206b9-107">上圖顯示模型化為正方形的圖元。</span><span class="sxs-lookup"><span data-stu-id="206b9-107">The preceding diagram shows pixels that are modeled as squares.</span></span> <span data-ttu-id="206b9-108">不過實際上，圖元是點，而不是正方形。</span><span class="sxs-lookup"><span data-stu-id="206b9-108">In reality, however, pixels are dots, not squares.</span></span> <span data-ttu-id="206b9-109">上圖中的每個正方形表示圖元所亮的區域，但是圖元一律只是正方形中央的點。</span><span class="sxs-lookup"><span data-stu-id="206b9-109">Each square in the preceding diagram indicates the area lit by the pixel, but a pixel is always just a dot at the center of a square.</span></span> <span data-ttu-id="206b9-110">這項區別雖然很小，但卻很重要。</span><span class="sxs-lookup"><span data-stu-id="206b9-110">This distinction, though seemingly small, is important.</span></span> <span data-ttu-id="206b9-111">下圖顯示相同顯示的更好圖例。</span><span class="sxs-lookup"><span data-stu-id="206b9-111">A better illustration of the same display is shown in the following diagram.</span></span>

![由圖元組成之顯示器的圖例](images/maptex-fig2.png)

<span data-ttu-id="206b9-113">上述圖表會將每個實體圖元正確顯示為每個資料格中央的某個點。</span><span class="sxs-lookup"><span data-stu-id="206b9-113">The preceding diagram correctly shows each physical pixel as a point in the center of each cell.</span></span> <span data-ttu-id="206b9-114">螢幕空間座標 (0、0) 是直接位於左上角圖元，因此位於左上角儲存格的中央。</span><span class="sxs-lookup"><span data-stu-id="206b9-114">The screen space coordinate (0, 0) is located directly at the top-left pixel, and therefore at the center of the top-left cell.</span></span> <span data-ttu-id="206b9-115">因此，顯示的左上角是在 (-0.5，-0.5) ，因為它是從左上圖元往左和0.5 儲存格的0.5 儲存格。</span><span class="sxs-lookup"><span data-stu-id="206b9-115">The top-left corner of the display is therefore at (-0.5, -0.5) because it is 0.5 cells to the left and 0.5 cells up from the top-left pixel.</span></span> <span data-ttu-id="206b9-116">Direct3D 會以 (0、0) 和 (4，4) 呈現四個角落，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="206b9-116">Direct3D will render a quad with corners at (0, 0) and (4, 4), as shown in the following illustration.</span></span>

![ (0、0) 和 (4，4) 之間 unrasterized 四的外框圖例](images/maptex-fig3.png)

<span data-ttu-id="206b9-118">上圖顯示數學四與顯示器之間的關聯性，但不會顯示當 Direct3D 將它柵格化並將其傳送至顯示器之後的四種外觀。</span><span class="sxs-lookup"><span data-stu-id="206b9-118">The preceding illustration shows where the mathematical quad is in relation to the display, but does not show what the quad will look like once Direct3D rasterizes it and sends it to the display.</span></span> <span data-ttu-id="206b9-119">事實上，因為四色的邊緣與圖元儲存格之間的界限不一致，所以點陣顯示器無法完全填滿上述的四顆部分。</span><span class="sxs-lookup"><span data-stu-id="206b9-119">In fact, it is impossible for a raster display to fill the quad exactly as shown because the edges of the quad do not coincide with the boundaries between pixel cells.</span></span> <span data-ttu-id="206b9-120">換句話說，由於每個圖元只能顯示單一色彩，因此每個圖元儲存格只會填入單一色彩;如果顯示的呈現方式與顯示的完全相同，則四個邊緣的圖元儲存格必須顯示兩個不同的色彩：藍色，在四和白色的範圍中，只顯示背景。</span><span class="sxs-lookup"><span data-stu-id="206b9-120">In other words, because each pixel can only display a single color, each pixel cell is filled with only a single color; if the display were to render the quad exactly as shown, the pixel cells along the quad's edge would need to show two distinct colors: blue where covered by the quad and white where only the background is visible.</span></span>

<span data-ttu-id="206b9-121">相反地，圖形硬體會負責決定應填滿的圖元以接近四顆四。</span><span class="sxs-lookup"><span data-stu-id="206b9-121">Instead, the graphics hardware is tasked with determining which pixels should be filled to approximate the quad.</span></span> <span data-ttu-id="206b9-122">此程式稱為「點陣化」，在 [ (Direct3D 9) 的點陣化規則 ](rasterization-rules.md)中有詳細說明。</span><span class="sxs-lookup"><span data-stu-id="206b9-122">This process is called rasterization, and is detailed in [Rasterization Rules (Direct3D 9)](rasterization-rules.md).</span></span> <span data-ttu-id="206b9-123">在此特定案例中，下圖顯示的柵格化四項。</span><span class="sxs-lookup"><span data-stu-id="206b9-123">For this particular case, the rasterized quad is shown in the following illustration.</span></span>

![uNtextured 從 (0、0) 到 (4、4所繪製的四個圖例) ](images/maptex-fig4.png)

<span data-ttu-id="206b9-125">請注意，傳遞給 Direct3D 的四個邊角有 (0、0) 和 (4、4) ，但在上圖中 (的點陣化輸出) 的角落為 (-0.5、-0.5) 和 (3.5、3.5) 。</span><span class="sxs-lookup"><span data-stu-id="206b9-125">Note that the quad passed to Direct3D has corners at (0, 0) and (4, 4), but the rasterized output (the preceding illustration) has corners at (-0.5,-0.5) and (3.5,3.5).</span></span> <span data-ttu-id="206b9-126">比較前面的兩個圖例以呈現差異。</span><span class="sxs-lookup"><span data-stu-id="206b9-126">Compare the preceding two illustrations for rendering differences.</span></span> <span data-ttu-id="206b9-127">您可以看到顯示實際上呈現的內容是正確的大小，但已在 x 和 y 方向以-0.5 儲存格移位。</span><span class="sxs-lookup"><span data-stu-id="206b9-127">You can see that what the display actually renders is the correct size, but has been shifted by -0.5 cells in the x and y directions.</span></span> <span data-ttu-id="206b9-128">但是，除了多重取樣技術，這是最適合四個的近似值。</span><span class="sxs-lookup"><span data-stu-id="206b9-128">However, except for multi-sampling techniques, this is the best possible approximation to the quad.</span></span> <span data-ttu-id="206b9-129"> (請參閱 [消除鋸齒範例](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx) ，以徹底涵蓋多個取樣。 ) 請注意，如果轉譯器填滿四個十字格，則產生的區域會是維度 5 x 5，而不是所需的 4 x 4。</span><span class="sxs-lookup"><span data-stu-id="206b9-129">(See the [Antialias Sample](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx) for thorough coverage of multi-sampling.) Be aware that if the rasterizer filled every cell the quad crossed, the resulting area would be of dimension 5 x 5 instead of the desired 4 x 4.</span></span>

<span data-ttu-id="206b9-130">如果您假設螢幕座標源自于顯示格線的左上角，而不是左上角的圖元，則會如預期般地出現四顆四。</span><span class="sxs-lookup"><span data-stu-id="206b9-130">If you assume that screen coordinates originate at the top-left corner of the display grid instead of the top-left pixel, the quad appears exactly as expected.</span></span> <span data-ttu-id="206b9-131">不過，當四個材質獲得材質時，差異就變得很清楚。</span><span class="sxs-lookup"><span data-stu-id="206b9-131">However, the difference becomes clear when the quad is given a texture.</span></span> <span data-ttu-id="206b9-132">下圖顯示 4 x 4 材質，您將直接對應到四個材質。</span><span class="sxs-lookup"><span data-stu-id="206b9-132">The following illustration shows the 4 x 4 texture you'll map directly onto the quad.</span></span>

![4x4 材質的圖例](images/maptex-fig5.png)

<span data-ttu-id="206b9-134">因為材質是 4 x 4 材質，而四個四個圖元的四個圖元，所以您可能會希望有紋理的四種外觀與材質一模一樣</span><span class="sxs-lookup"><span data-stu-id="206b9-134">Because the texture is 4 x 4 texels and the quad is 4 x 4 pixels, you might expect the textured quad to appear exactly like the texture regardless of the location on the screen where the quad is drawn.</span></span> <span data-ttu-id="206b9-135">不過，這不是這種情況;即使是位置稍微改變，也會影響材質的顯示方式。</span><span class="sxs-lookup"><span data-stu-id="206b9-135">However, this is not the case; even slight changes in position influence how the texture is displayed.</span></span> <span data-ttu-id="206b9-136">下圖顯示 (0、0) 和 (4）之間的四個，在進行柵格化和紋理之後，會如何顯示 4) 。</span><span class="sxs-lookup"><span data-stu-id="206b9-136">The following illustration shows how a quad between (0, 0) and (4, 4) is displayed after being rasterized and textured.</span></span>

![從 (0、0) 和 (4，4) 繪製的材質四個圖](images/maptex-fig6.png)

<span data-ttu-id="206b9-138">在上圖中繪製的四個範例顯示有紋理的輸出 (具有線性篩選模式，以及使用重迭的點陣化輪廓) 的夾具定址模式。</span><span class="sxs-lookup"><span data-stu-id="206b9-138">The quad drawn in the preceding illustration shows the textured output (with a linear filtering mode and a clamp addressing mode) with the superimposed rasterized outline.</span></span> <span data-ttu-id="206b9-139">本文的其餘部分將說明輸出看起來的樣子，而不是像材質一樣，但是對於需要解決方案的人而言，它是：輸入的邊緣必須在圖元儲存格之間的界限線上。</span><span class="sxs-lookup"><span data-stu-id="206b9-139">The rest of this article explains exactly why the output looks the way it does instead of looking like the texture, but for those who want the solution, here it is: The edges of the input quad need to lie upon the boundary lines between pixel cells.</span></span> <span data-ttu-id="206b9-140">只要將 x 和 y 四倍座標以-0.5 單位來移動，材質儲存格就能完全涵蓋圖元儲存格，而且可以完全在螢幕上重建四顆四。</span><span class="sxs-lookup"><span data-stu-id="206b9-140">By simply shifting the x and y quad coordinates by -0.5 units, texel cells will perfectly cover pixel cells and the quad can be perfectly recreated on the screen.</span></span> <span data-ttu-id="206b9-141"> (本主題中的最後一個圖例，會以修正的座標顯示四個。 ) </span><span class="sxs-lookup"><span data-stu-id="206b9-141">(The last illustration in this topic shows the quad at the corrected coordinates.)</span></span>

<span data-ttu-id="206b9-142">為什麼點陣化輸出只會對輸入材質造成輕微非常相似的詳細資料，與 Direct3D 定址和範例紋理的方式直接相關。</span><span class="sxs-lookup"><span data-stu-id="206b9-142">The details of why the rasterized output only bears slight resemblance to the input texture are directly related to the way Direct3D addresses and samples textures.</span></span> <span data-ttu-id="206b9-143">接下來會假設您已充分瞭解 [材質座標空間](texture-coordinates.md) 和 [雙線性材質篩選](bilinear-texture-filtering.md)。</span><span class="sxs-lookup"><span data-stu-id="206b9-143">What follows assumes you have a good understanding of [texture coordinate space](texture-coordinates.md) And [bilinear texture filtering](bilinear-texture-filtering.md).</span></span>

<span data-ttu-id="206b9-144">回頭查看奇怪的圖元輸出，將輸出色彩追蹤回圖元著色器是合理的：圖元著色器是針對每個選取要成為柵格化圖形一部分的圖元來呼叫。</span><span class="sxs-lookup"><span data-stu-id="206b9-144">Getting back to our investigation of the strange pixel output, it makes sense to trace the output color back to the pixel shader: The pixel shader is called for each pixel selected to be part of the rasterized shape.</span></span> <span data-ttu-id="206b9-145">先前圖例中所描述的藍色四顆四色可能會有特別簡單的著色器：</span><span class="sxs-lookup"><span data-stu-id="206b9-145">The solid blue quad depicted in an earlier illustration could have a particularly simple shader:</span></span>


```
float4 SolidBluePS() : COLOR
{ 
    return float4( 0, 0, 1, 1 );
} 
```



<span data-ttu-id="206b9-146">針對有紋理的四個四個圖元，必須稍微變更圖元著色器：</span><span class="sxs-lookup"><span data-stu-id="206b9-146">For the textured quad, the pixel shader has to be changed slightly:</span></span>


```
texture MyTexture;

sampler MySampler = 
sampler_state 
{ 
    Texture = <MyTexture>;
    MinFilter = Linear;
    MagFilter = Linear;
    AddressU = Clamp;
    AddressV = Clamp;
};

float4 TextureLookupPS( float2 vTexCoord : TEXCOORD0 ) : COLOR
{
    return tex2D( MySampler, vTexCoord );
} 
```



<span data-ttu-id="206b9-147">該程式碼假設 4 x 4 材質儲存在 MyTexture 中。</span><span class="sxs-lookup"><span data-stu-id="206b9-147">That code assumes the 4 x 4 texture is stored in MyTexture.</span></span> <span data-ttu-id="206b9-148">如圖所示，MySampler 材質取樣器設定為在 MyTexture 上執行雙線性篩選。</span><span class="sxs-lookup"><span data-stu-id="206b9-148">As shown, the MySampler texture sampler is set to perform bilinear filtering on MyTexture.</span></span> <span data-ttu-id="206b9-149">圖元著色器會針對每個柵格化圖元呼叫一次，而且每次傳回的色彩是取樣的材質色彩時，vTexCoord。</span><span class="sxs-lookup"><span data-stu-id="206b9-149">The pixel shader gets called once for each rasterized pixel, and each time the returned color is the sampled texture color at vTexCoord.</span></span> <span data-ttu-id="206b9-150">每次呼叫圖元著色器時，vTexCoord 引數都會設定為該圖元的材質座標。</span><span class="sxs-lookup"><span data-stu-id="206b9-150">Each time the pixel shader is called, the vTexCoord argument is set to the texture coordinates at that pixel.</span></span> <span data-ttu-id="206b9-151">這表示著色器會在圖元的確切位置要求紋理取樣器，以篩選紋理色彩，如下圖所述。</span><span class="sxs-lookup"><span data-stu-id="206b9-151">That means the shader is asking the texture sampler for the filtered texture color at the exact location of the pixel, as detailed in the following illustration.</span></span>

![紋理座標取樣位置的圖例](images/maptex-fig7.png)

<span data-ttu-id="206b9-153">顯示重迭) 的材質 (會直接在圖元位置取樣 (以黑色點) 顯示。</span><span class="sxs-lookup"><span data-stu-id="206b9-153">The texture (shown superimposed) is sampled directly at pixel locations (shown as black dots).</span></span> <span data-ttu-id="206b9-154">材質座標不受點陣 (的影響，它們會保留在原始四) 的投射螢幕空間中。</span><span class="sxs-lookup"><span data-stu-id="206b9-154">Texture coordinates are not affected by rasterization (they remain in the projected screen-space of the original quad).</span></span> <span data-ttu-id="206b9-155">黑色點會顯示點陣化圖元的位置。</span><span class="sxs-lookup"><span data-stu-id="206b9-155">The black dots show where the rasterization pixels are.</span></span> <span data-ttu-id="206b9-156">每個圖元的材質座標都可以藉由將儲存在每個頂點的座標插值來輕鬆地判斷：位於 (0 的圖元，0) 與 (0、0) ; 的頂點相符;因此，該圖元的材質座標只是儲存在該頂點的材質座標，也就是 UV (0.0，0.0) 。</span><span class="sxs-lookup"><span data-stu-id="206b9-156">The texture coordinates at each pixel are easily determined by interpolating the coordinates stored at each vertex: The pixel at (0,0) coincides with the vertex at (0, 0); therefore, the texture coordinates at that pixel are simply the texture coordinates stored at that vertex, UV (0.0, 0.0).</span></span> <span data-ttu-id="206b9-157">針對 (3，1) 的圖元，插補座標為 UV (0.75，0.25) ，因為該圖元位於材質寬度的三 fourths 和其高度的四分之一。</span><span class="sxs-lookup"><span data-stu-id="206b9-157">For the pixel at (3, 1), the interpolated coordinates are UV (0.75, 0.25) because that pixel is located at three-fourths of the texture's width and one-fourth of its height.</span></span> <span data-ttu-id="206b9-158">這些插補座標是傳遞給圖元著色器的結果。</span><span class="sxs-lookup"><span data-stu-id="206b9-158">These interpolated coordinates are what get passed to the pixel shader.</span></span>

<span data-ttu-id="206b9-159">在此範例中，材質不會對齊圖元;每個圖元都 (，因此每個取樣點) 都會放置在四個材質的角落。</span><span class="sxs-lookup"><span data-stu-id="206b9-159">The texels do not line up with the pixels in this example; each pixel (and therefore each sampling point) is positioned at the corner of four texels.</span></span> <span data-ttu-id="206b9-160">由於篩選模式設定為線性，因此取樣器會平均共用該角落四個材質的色彩。</span><span class="sxs-lookup"><span data-stu-id="206b9-160">Because the filtering mode is set to Linear, the sampler will average the colors of the four texels sharing that corner.</span></span> <span data-ttu-id="206b9-161">這會說明為什麼圖元必須是紅色的，其實是三 fourths 的灰色，加上第四個紅色，則應為綠色的圖元是一半灰色，加上第四個紅色加上第四個綠色，依此類推。</span><span class="sxs-lookup"><span data-stu-id="206b9-161">This explains why the pixel expected to be red is actually three-fourths gray plus one-fourth red, the pixel expected to be green is one-half gray plus one-fourth red plus one-fourth green, and so on.</span></span>

<span data-ttu-id="206b9-162">若要修正這個問題，您只需要將四個四個圖元正確地對應到圖元，就能正確地將材質對應到圖元。</span><span class="sxs-lookup"><span data-stu-id="206b9-162">To fix this problem, all you need to do is correctly map the quad to the pixels to which it will be rasterized, and thereby correctly map the texels to pixels.</span></span> <span data-ttu-id="206b9-163">下圖顯示在 (-0.5、-0.5) 和 (3.5 3.5) 之間繪製相同四種的結果，這是一開始的四項設計。</span><span class="sxs-lookup"><span data-stu-id="206b9-163">The following illustration shows the results of drawing the same quad between (-0.5, -0.5) and (3.5, 3.5), which is the quad intended from the outset.</span></span>

![符合柵格化四顆紋理的四顆紋理圖](images/maptex-fig8.png)

<span data-ttu-id="206b9-165">上圖說明從 (-0.5，-0.5) 到 (3.5，3.5) ) 所顯示的四 (完全符合柵格化區域。</span><span class="sxs-lookup"><span data-stu-id="206b9-165">The preceding illustration demonstrates that the quad (shown outlined from (-0.5, -0.5) to (3.5, 3.5)) exactly matches the rasterized area.</span></span>

## <a name="summary"></a><span data-ttu-id="206b9-166">總結</span><span class="sxs-lookup"><span data-stu-id="206b9-166">Summary</span></span>

<span data-ttu-id="206b9-167">總而言之，圖元和材質實際上是點，而非穩固的區塊。</span><span class="sxs-lookup"><span data-stu-id="206b9-167">In summary, pixels and texels are actually points, not solid blocks.</span></span> <span data-ttu-id="206b9-168">螢幕空間源自左上角圖元，但材質座標源自材質方格的左上角。</span><span class="sxs-lookup"><span data-stu-id="206b9-168">Screen space originates at the top-left pixel, but texture coordinates originate at the top-left corner of the texture's grid.</span></span> <span data-ttu-id="206b9-169">最重要的是，當您在轉換的螢幕空間中工作時，請記得從頂點位置的 x 和 y 元件減去0.5 單位，以便正確地對齊材質與圖元。</span><span class="sxs-lookup"><span data-stu-id="206b9-169">Most importantly, remember to subtract 0.5 units from the x and y components of your vertex positions when working in transformed screen space in order to correctly align texels with pixels.</span></span>

<span data-ttu-id="206b9-170">下列程式碼範例會將256的頂點偏移256正方形，以適當地在轉換的螢幕空間中顯示 256 x 256 紋理。</span><span class="sxs-lookup"><span data-stu-id="206b9-170">The following code is an example of offsetting the vertices of a 256 by 256 square to properly display a 256 by 256 texture in transformed screen space.</span></span>


```C++
//define FVF with vertex values in transformed screen space
#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZRHW|D3DFVF_TEX1)

struct CUSTOMVERTEX
{
    FLOAT x, y, z, rhw; // position
    FLOAT tu, tv;       // texture coordinates
};

//unadjusted vertex values
float left = 0.0f;
float right = 255.0f;
float top = 0.0f;
float bottom = 255.0f;


//256 by 256 rectangle matching 256 by 256 texture
CUSTOMVERTEX vertices[] =
{
    { left,  top,    0.5f, 1.0f, 0.0f, 0.0f}, // x, y, z, rhw, u, v
    { right, top,    0.5f, 1.0f, 1.0f, 0.0f},
    { right, bottom, 0.5f, 1.0f, 1.0f, 1.0f},
    { left,  top,    0.5f, 1.0f, 0.0f, 0.0f},
    { right, bottom, 0.5f, 1.0f, 1.0f, 1.0f},
    { left,  bottom, 0.5f, 1.0f, 0.0f, 1.0f},
    
};
```




```C++
//adjust all the vertices to correctly line up texels with pixels 
for (int i=0; i<6; i++)
{
    vertices[i].x -= 0.5f;
    vertices[i].y -= 0.5f;
}
```



## <a name="related-topics"></a><span data-ttu-id="206b9-171">相關主題</span><span class="sxs-lookup"><span data-stu-id="206b9-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="206b9-172">材質座標</span><span class="sxs-lookup"><span data-stu-id="206b9-172">Texture Coordinates</span></span>](texture-coordinates.md)
</dt> </dl>

 

 



