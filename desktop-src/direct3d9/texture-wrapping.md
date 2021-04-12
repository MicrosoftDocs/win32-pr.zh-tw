---
description: 簡單地說，材質換行變更了 Direct3D 使用針對每個頂點指定的材質座標，來將紋理化多邊形進行柵格化的基本方式。
ms.assetid: 00683d3f-3e3c-4ee4-9aec-a0d7fd9c8941
title: " (Direct3D 9) 的材質換行"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d7c0f8cb6d7793536999d5f3df128849572d3dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510016"
---
# <a name="texture-wrapping-direct3d-9"></a><span data-ttu-id="e5b7b-103"> (Direct3D 9) 的材質換行</span><span class="sxs-lookup"><span data-stu-id="e5b7b-103">Texture Wrapping (Direct3D 9)</span></span>

<span data-ttu-id="e5b7b-104">簡單地說，材質換行變更了 Direct3D 使用針對每個頂點指定的材質座標，來將紋理化多邊形進行柵格化的基本方式。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-104">In short, texture wrapping changes the basic way that Direct3D rasterizes textured polygons using the texture coordinates specified for each vertex.</span></span> <span data-ttu-id="e5b7b-105">點陣化多邊形時，系統會藉由在多邊形每個頂點的紋理座標間進行插補，以決定多邊形的每個像素會使用哪些材質。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-105">While rasterizing a polygon, the system interpolates between the texture coordinates at each of the polygon's vertices to determine the texels that should be used for every pixel of the polygon.</span></span> <span data-ttu-id="e5b7b-106">一般來說，系統會將紋理視為 2D 平面，並藉著在紋理中選擇 A 點到 B 點之間最短的路徑以插入新的材質。若 A 點代表座標為 (0.8, 0.1) 的 u, v 位置， B 點則是 (0.1, 0.1)，則插補線會類似下列簡圖。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-106">Normally, the system treats the texture as a 2D plane, interpolating new texels by taking the shortest route from point A within a texture to point B. If point A represents the u, v position (0.8, 0.1), and point B is at (0.1,0.1), the line of interpolation looks like the following diagram.</span></span>

![兩個點之間插補線的簡圖](images/interp1.png)

<span data-ttu-id="e5b7b-108">注意：在此圖例中，A 點與 B 點之間最短的距離會約略通過紋理中間。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-108">Note that the shortest distance between A and B in this illustration runs roughly through the middle of the texture.</span></span> <span data-ttu-id="e5b7b-109">啟用 u 紋理或 v 紋理座標包裝，可變更 Direct3D 計算 u 方向與 v 方向上紋理座標之間最短距離的方式。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-109">Enabling u-texture or v-texture coordinate wrapping changes how Direct3D perceives the shortest route between texture coordinates in the u-direction and v-direction.</span></span> <span data-ttu-id="e5b7b-110">根據定義，假設 0.0 與 1.0 同時存在，則紋理包裝會使轉譯器在紋理座標組之間選擇最短的路徑。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-110">By definition, texture wrapping causes the rasterizer to take the shortest route between texture coordinate sets, assuming that 0.0 and 1.0 are coincident.</span></span> <span data-ttu-id="e5b7b-111">最後一段是較為棘手的部分︰您可以想像在單一方向啟用紋理包裝時，會導致系統彷彿將紋理包裝在圓柱體中。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-111">The last bit is the tricky part: You can imagine that enabling texture wrapping in one direction causes the system to treat a texture as though it were wrapped around a cylinder.</span></span> <span data-ttu-id="e5b7b-112">例如，請看下列圖表。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-112">For example, consider the following diagram.</span></span>

![一個紋理及兩個點包裝在一個圓柱體中的簡圖](images/interp2.png)

<span data-ttu-id="e5b7b-114">上述圖例呈現了在 u 方向上進行包裝時，影響系統於紋理座標間插補的情況。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-114">The preceding illustration shows how wrapping in the u - direction affects how the system interpolates texture coordinates.</span></span> <span data-ttu-id="e5b7b-115">在一般或是未包裝的紋理中使用與範例中相同的點，您可以看到 A 點與 B 點之間最短的距離不再通過紋理的中間了，而是通過 0.0 與 1.0 同時存在的邊框。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-115">Using the same points as in the example for normal, or nonwrapped, textures, you can see that the shortest route between points A and B is no longer across the middle of the texture; it's now across the border where 0.0 and 1.0 exist together.</span></span> <span data-ttu-id="e5b7b-116">在 v 方向上包裝時情況與先前的範例類似，只是紋理會包裝在躺臥在其側邊的圓柱體中。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-116">Wrapping in the v-direction is similar, except that it wraps the texture around a cylinder that is lying on its side.</span></span> <span data-ttu-id="e5b7b-117">在 u 方向 v 方向上同時進行包裝會更複雜。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-117">Wrapping in both the u-direction and v-direction is more complex.</span></span> <span data-ttu-id="e5b7b-118">此時，您可將紋理構想成環面體或是甜甜圈。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-118">In this situation, you can envision the texture as a torus, or doughnut.</span></span>

<span data-ttu-id="e5b7b-119">紋理包裝最常見的實際應用就是用來執行環境貼圖。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-119">The most common practical application for texture wrapping is to perform environment mapping.</span></span> <span data-ttu-id="e5b7b-120">通常，物件的紋理若為環境貼圖，其本身會帶有強烈的反射性，即完全呈現物件周遭環境的鏡映影像。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-120">Usually, an object textured with an environment map appears very reflective, showing a mirrored image of the object's surroundings in the scene.</span></span> <span data-ttu-id="e5b7b-121">為了更有效地進行討論，您可以想像一間有著四面牆的房間，每一面牆上都各自寫著 R、G、B，及 Y，並且繪有相對的顏色：紅色、綠色、藍色，及黃色。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-121">For the sake of this discussion, picture a room with four walls, each one painted with a letter R, G, B, Y and the corresponding colors: red, green, blue, and yellow.</span></span> <span data-ttu-id="e5b7b-122">該房間的環境貼圖可能如下列圖例所示。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-122">The environment map for such a simple room might look like the following illustration.</span></span>

![紅色、綠色、藍色，及黃色條文的圖例](images/envmap.png)

<span data-ttu-id="e5b7b-124">想像一根有著四個完全反射面的柱子支撐著房間的天花板。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-124">Imagine that the room's ceiling is held up by a perfectly reflective, four-sided, pillar.</span></span> <span data-ttu-id="e5b7b-125">將環境貼圖紋理貼至柱子本身相當簡單，然而若要試圖使柱子看起來就像是反射了牆上的字和顏色，相較之下就比較困難。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-125">Mapping the environment map texture to the pillar is simple; making the pillar look as though it is reflecting the letters and colors is not as easy.</span></span> <span data-ttu-id="e5b7b-126">以下簡圖呈現了在接近頂部頂點處列出適用紋理座標柱子的框線圖。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-126">The following diagram shows a wire frame of the pillar with the applicable texture coordinates listed near the top vertices.</span></span> <span data-ttu-id="e5b7b-127">虛線表示包裝會超過紋理邊緣的接縫處。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-127">The seam where wrapping will cross the edges of the texture is shown with a dotted line.</span></span>

![帶有二等分線矩形的簡圖](images/seam.png)

<span data-ttu-id="e5b7b-129">當包裝於 u 方向啟用時，已貼上紋理的柱子適當地呈現了環境貼圖中的色彩與符號，而在紋理前端的接縫處，轉譯器也適當地在紋理座標間選擇了最短的路徑。(假設 u 座標 0.0 與 1.0 共用相同的位置。)</span><span class="sxs-lookup"><span data-stu-id="e5b7b-129">With wrapping enabled in the u-direction, the textured pillar shows the colors and symbols from the environment map appropriately and, at the seam in the front of the texture, the rasterizer properly chooses the shortest route between the texture coordinates, assuming that u-coordinates 0.0 and 1.0 share the same location.</span></span> <span data-ttu-id="e5b7b-130">已貼上紋理的柱子外觀如下。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-130">The textured pillar looks like the following illustration.</span></span>

![由紅色、綠色、藍色，及黃色四等分色塊組成之柱子的圖例](images/tex-seam.png)

<span data-ttu-id="e5b7b-132">若不啟用紋理包裝，轉譯器就不會在必要的方向上進行插補，呈現出寫實的反射影像。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-132">If texture wrapping isn't enabled, the rasterizer does not interpolate in the direction needed to generate a believable, reflected image.</span></span> <span data-ttu-id="e5b7b-133">而是在柱子的前方呈現 u 座標 0.175 及 0.875 間紋理的水平壓縮版本，因為其通過了紋理的中心。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-133">Rather, the area at the front of the pillar contains a horizontally compressed version of the texels between u-coordinates 0.175 and 0.875, as they pass through the center of the texture.</span></span> <span data-ttu-id="e5b7b-134">包裝效果因此失去作用。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-134">The wrap effect is ruined.</span></span>

## <a name="using-texture-wrapping"></a><span data-ttu-id="e5b7b-135">使用材質換行</span><span class="sxs-lookup"><span data-stu-id="e5b7b-135">Using Texture Wrapping</span></span>

<span data-ttu-id="e5b7b-136">若要啟用材質換行，請呼叫 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-136">To enable texture wrapping, call the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method as shown in the code example below.</span></span>


```
d3dDevice->SetRenderState(D3DRS_WRAP0, D3DWRAPCOORD_0);
```



<span data-ttu-id="e5b7b-137">[**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)所接受的第一個參數是要設定的呈現狀態。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-137">The first parameter accepted by [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) is a render state to set.</span></span> <span data-ttu-id="e5b7b-138">指定其中一個 D3DRS \_ WRAP0 至 D3DRS \_ WRAP7 列舉值，以指定要設定包裝的材質層級。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-138">Specify one of the D3DRS\_WRAP0 through D3DRS\_WRAP7 enumerated values which specify which texture level to set the wrapping for.</span></span> <span data-ttu-id="e5b7b-139">在 \_ \_ 第二個參數中指定 D3DWRAPCOORD 0 到 D3DWRAPCOORD 3 的旗標，以便在對應的方向中換行，或結合它們來啟用多個方向的換行。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-139">Specify the D3DWRAPCOORD\_0 through D3DWRAPCOORD\_3 flags in the second parameter to enable texture wrapping in the corresponding direction, or combine them to enable wrapping in multiple directions.</span></span> <span data-ttu-id="e5b7b-140">如果您省略旗標，則會停用對應方向的材質換行。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-140">If you omit a flag, texture wrapping in the corresponding direction is disabled.</span></span> <span data-ttu-id="e5b7b-141">若要停用一組紋理座標的材質換行，請將對應轉譯狀態的值設定為0。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-141">To disable texture wrapping for a set of texture coordinates, set the value for the corresponding render state to 0.</span></span>

<span data-ttu-id="e5b7b-142">請勿將「紋理包裝」與有著相似名稱的「紋理定址模式」混淆。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-142">Do not confuse texture wrapping with the similarly named texture addressing modes.</span></span> <span data-ttu-id="e5b7b-143">紋理包裝會在紋理定址之前執行。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-143">Texture wrapping is performed before texture addressing.</span></span> <span data-ttu-id="e5b7b-144">請確定材質包裝資料未包含0.0、1.0 範圍以外的任何材質座標 \[ ， \] 因為這會產生未定義的結果。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-144">Be sure the texture wrapping data does not contain any texture coordinates outside of the range of \[0.0, 1.0\] because this will produce undefined results.</span></span> <span data-ttu-id="e5b7b-145">如需紋理定址的詳細資訊，請參閱 [ (Direct3D 9) 的材質定址模式 ](texture-addressing-modes.md)。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-145">For more information about texture addressing, see [Texture Addressing Modes (Direct3D 9)](texture-addressing-modes.md).</span></span>

## <a name="displacement-map-wrapping"></a><span data-ttu-id="e5b7b-146">置換地圖換行</span><span class="sxs-lookup"><span data-stu-id="e5b7b-146">Displacement Map Wrapping</span></span>

<span data-ttu-id="e5b7b-147">置換貼圖由花格引擎進行插補。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-147">Displacement maps are interpolated by the tesselation engine.</span></span> <span data-ttu-id="e5b7b-148">由於花格引擎無法指定包裝模式，紋理包裝無法在置換貼圖上使用。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-148">Because the wrap mode cannot be specified for the tessellation engine, texture wrapping cannot be performed with displacement maps.</span></span> <span data-ttu-id="e5b7b-149">應用程式可選擇使用一組強制插補於任一方向進行的頂點。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-149">An application is able to use a set of vertices that forces the interpolation to wrap in any direction.</span></span> <span data-ttu-id="e5b7b-150">應用程式也可指定插補使用簡單線性插補完成。</span><span class="sxs-lookup"><span data-stu-id="e5b7b-150">The application can also specify the interpolation to be done as a simple linear interpolation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5b7b-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="e5b7b-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5b7b-152">Direct3D 紋理</span><span class="sxs-lookup"><span data-stu-id="e5b7b-152">Direct3D Textures</span></span>](direct3d-textures.md)
</dt> </dl>

 

 
