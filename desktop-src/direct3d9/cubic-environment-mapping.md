---
description: 三層環境對應（有時稱為 cube 對應）是包含代表物件周圍場景之影像資料的材質，如同物件位於 cube 中央一樣。
ms.assetid: 4879d59b-e6d3-4811-ab2c-bcce8f214e1c
title: " (Direct3D 9) 的三次環境對應"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cecac83db067224195883485bcbd282aa82ae4b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386000"
---
# <a name="cubic-environment-mapping-direct3d-9"></a><span data-ttu-id="57dcb-103"> (Direct3D 9) 的三次環境對應</span><span class="sxs-lookup"><span data-stu-id="57dcb-103">Cubic Environment Mapping (Direct3D 9)</span></span>

<span data-ttu-id="57dcb-104">三層環境對應（有時稱為 cube 對應）是包含代表物件周圍場景之影像資料的材質，如同物件位於 cube 中央一樣。</span><span class="sxs-lookup"><span data-stu-id="57dcb-104">Cubic environment maps - sometimes referred to as cube maps - are textures that contain image data representing the scene surrounding an object, as if the object were in the center of a cube.</span></span> <span data-ttu-id="57dcb-105">每個三面的環境對應都涵蓋水準和垂直的90度視野，而且每個立方體圖都有六個臉部。</span><span class="sxs-lookup"><span data-stu-id="57dcb-105">Each face of the cubic environment map covers a 90-degree field of view in the horizontal and vertical, and there are six faces per cube map.</span></span> <span data-ttu-id="57dcb-106">臉部的方向如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="57dcb-106">The orientation of the faces is shown in the following illustration.</span></span>

![具有垂直于 cube 臉部之中央座標軸的 cube 圖例](images/cubemap-cube.png)

<span data-ttu-id="57dcb-108">Cube 的每個臉部都是在世界空間中的 x/y、y/z 或 x/z 平面垂直方向。</span><span class="sxs-lookup"><span data-stu-id="57dcb-108">Each face of the cube is oriented perpendicular to the x/y, y/z, or x/z plane, in world space.</span></span> <span data-ttu-id="57dcb-109">下圖顯示每個平面如何對應至臉部。</span><span class="sxs-lookup"><span data-stu-id="57dcb-109">The following illustration shows how each plane corresponds to a face.</span></span>

![使用平面座標投射的 cube 臉部圖例](images/cube-faces.png)

<span data-ttu-id="57dcb-111">三層環境對應會實作為一系列的材質物件。</span><span class="sxs-lookup"><span data-stu-id="57dcb-111">Cubic environment maps are implemented as a series of texture objects.</span></span> <span data-ttu-id="57dcb-112">應用程式可以使用靜態映射進行三次環境對應，也可以轉譯成 cube 對應的臉部，以執行動態環境對應。</span><span class="sxs-lookup"><span data-stu-id="57dcb-112">Applications can use static images for cubic environment mapping, or they can render into the faces of the cube map to perform dynamic environment mapping.</span></span> <span data-ttu-id="57dcb-113">這項技術會要求 cube 對應介面必須是有效的呈現目標介面，並已設定 D3DUSAGE \_ RENDERTARGET 旗標。</span><span class="sxs-lookup"><span data-stu-id="57dcb-113">This technique requires that the cube-map surfaces be valid render-target surfaces, created with the D3DUSAGE\_RENDERTARGET flag set.</span></span>

<span data-ttu-id="57dcb-114">立方體圖的臉部不需要包含周圍場景的極詳細轉譯。</span><span class="sxs-lookup"><span data-stu-id="57dcb-114">The faces of a cube map don't need to contain extremely detailed renderings of the surrounding scene.</span></span> <span data-ttu-id="57dcb-115">在大部分的情況下，會將環境對應套用至曲線表面。</span><span class="sxs-lookup"><span data-stu-id="57dcb-115">In most cases, environment maps are applied to curved surfaces.</span></span> <span data-ttu-id="57dcb-116">由於大多數應用程式使用的曲率數量，產生的反射失真會在環境對應中大幅詳細地顯示記憶體和轉譯的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="57dcb-116">Given the amount of curvature used by most applications, the resulting reflective distortion makes extreme detail in the environment map wasteful in terms of memory and rendering overhead.</span></span>

## <a name="mipmapped-cubic-environment-maps"></a><span data-ttu-id="57dcb-117">Mipmapped 立方環境對應</span><span class="sxs-lookup"><span data-stu-id="57dcb-117">Mipmapped Cubic Environment Maps</span></span>

<span data-ttu-id="57dcb-118">Cube 對應可以是 mipmapped 的。</span><span class="sxs-lookup"><span data-stu-id="57dcb-118">Cube maps can be mipmapped.</span></span> <span data-ttu-id="57dcb-119">若要建立 mipmapped cube 對應，請將 [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) 方法的 [層級] 參數設定為您想要的層級數目。</span><span class="sxs-lookup"><span data-stu-id="57dcb-119">To create a mipmapped cube map, set the Levels parameter of the [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) method to the number of levels that you want.</span></span> <span data-ttu-id="57dcb-120">您可以想像這些表面的拓撲，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="57dcb-120">You can envision the topography of these surfaces as shown in the following diagram.</span></span>

![具有 n 個 mip 層級之 mipmapped cube 地圖的圖表](images/cubemap-mipped.png)

<span data-ttu-id="57dcb-122">建立 mipmapped 立方環境對應的應用程式，可以藉由呼叫 [**GetCubeMapSurface**](/windows/desktop/api) 方法來存取每個臉部。</span><span class="sxs-lookup"><span data-stu-id="57dcb-122">Applications that create mipmapped cubic environment maps can access each face by calling the [**GetCubeMapSurface**](/windows/desktop/api) method.</span></span> <span data-ttu-id="57dcb-123">從 [**D3DCUBEMAP \_ 臉部**](./d3dcubemap-faces.md) 列舉型別設定適當的值開始，如 [)  (Direct3D 9 中建立三種環境的地圖](creating-cubic-environment-map-surfaces.md)介面所述。</span><span class="sxs-lookup"><span data-stu-id="57dcb-123">Start by setting the appropriate value from the [**D3DCUBEMAP\_FACES**](./d3dcubemap-faces.md) enumerated type, as discussed in [Creating Cubic Environment Map Surfaces (Direct3D 9)](creating-cubic-environment-map-surfaces.md).</span></span> <span data-ttu-id="57dcb-124">接下來，將 **GetCubeMapSurface** 層級參數設定為您想要的 mipmap 層級，以選取要抓取的層級。</span><span class="sxs-lookup"><span data-stu-id="57dcb-124">Next, select the level to retrieve by setting the **GetCubeMapSurface** level parameter to the mipmap level that you want.</span></span> <span data-ttu-id="57dcb-125">請記住，0會對應到最上層影像。</span><span class="sxs-lookup"><span data-stu-id="57dcb-125">Remember that 0 corresponds with the top-level image.</span></span>

## <a name="texture-coordinates-for-cubic-environment-maps"></a><span data-ttu-id="57dcb-126">三層環境對應的材質座標</span><span class="sxs-lookup"><span data-stu-id="57dcb-126">Texture Coordinates for Cubic Environment Maps</span></span>

<span data-ttu-id="57dcb-127">使用標準紋理套用時，以三種方式建立索引三種環境對應的材質座標不是簡單的 u、v 樣式座標。</span><span class="sxs-lookup"><span data-stu-id="57dcb-127">Texture coordinates that index a cubic environment map aren't simple u, v style coordinates, as used when standard textures are applied.</span></span> <span data-ttu-id="57dcb-128">事實上，三層環境對應根本不會使用材質座標。</span><span class="sxs-lookup"><span data-stu-id="57dcb-128">In fact, cubic environment maps don't use texture coordinates at all.</span></span> <span data-ttu-id="57dcb-129">為了取代一組紋理座標，三層環境對應需要3D 向量。</span><span class="sxs-lookup"><span data-stu-id="57dcb-129">In place of a set of texture coordinates, cubic environment maps require a 3D vector.</span></span> <span data-ttu-id="57dcb-130">您必須小心指定適當的頂點格式。</span><span class="sxs-lookup"><span data-stu-id="57dcb-130">You must take care to specify a proper vertex format.</span></span> <span data-ttu-id="57dcb-131">除了告訴系統您的應用程式所使用的材質座標集合數目之外，您還必須提供每個集合中有多少個元素的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="57dcb-131">In addition to telling the system how many sets of texture coordinates your application uses, you must provide information about how many elements are in each set.</span></span> <span data-ttu-id="57dcb-132">基於這個目的，Direct3D 提供了 [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) 的宏集。</span><span class="sxs-lookup"><span data-stu-id="57dcb-132">Direct3D offers the [**D3DFVF\_TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) set of macros for this purpose.</span></span> <span data-ttu-id="57dcb-133">這些宏會接受單一參數，以識別要描述其大小的材質座標集合的索引。</span><span class="sxs-lookup"><span data-stu-id="57dcb-133">These macros accept a single parameter, identifying the index of the texture coordinate set for which the size is being described.</span></span> <span data-ttu-id="57dcb-134">在3D 向量的案例中，您會包含 D3DFVF TEXCOORDSIZE3 宏所建立的位模式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="57dcb-134">In the case of a 3D vector, you include the bit pattern created by the D3DFVF\_TEXCOORDSIZE3 macro.</span></span> <span data-ttu-id="57dcb-135">下列程式碼範例顯示如何使用這個宏。</span><span class="sxs-lookup"><span data-stu-id="57dcb-135">The following code example shows how this macro is used.</span></span>


```
// Create a flexible vertex format descriptor for a vertex that contains
//   a position, normal, and one set of 3D texture coordinates.

DWORD dwFVF = D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_TEX1 | D3DFVF_TEXCOORDSIZE3(0); 
```



<span data-ttu-id="57dcb-136">在某些情況下（例如漫射燈光對應），您可以使用向量的相機空間頂點。</span><span class="sxs-lookup"><span data-stu-id="57dcb-136">In some cases, such as diffuse light mapping, you use the camera-space vertex normal for the vector.</span></span> <span data-ttu-id="57dcb-137">在其他情況下（例如反射環境對應），您會使用反映向量。</span><span class="sxs-lookup"><span data-stu-id="57dcb-137">In other cases, like specular environment mapping, you use a reflection vector.</span></span> <span data-ttu-id="57dcb-138">由於可廣泛瞭解轉換的頂點法線，此處的資訊著重于計算反映向量。</span><span class="sxs-lookup"><span data-stu-id="57dcb-138">Because transformed vertex normals are widely understood, the information here concentrates on computing a reflection vector.</span></span>

<span data-ttu-id="57dcb-139">您必須瞭解每個頂點的位置，以及從視點到該頂點的向量，才能自行計算反映向量。</span><span class="sxs-lookup"><span data-stu-id="57dcb-139">Computing a reflection vector on your own requires understanding of the position of each vertex, and of a vector from the viewpoint to that vertex.</span></span> <span data-ttu-id="57dcb-140">Direct3D 可以自動計算您幾何的反射向量。</span><span class="sxs-lookup"><span data-stu-id="57dcb-140">Direct3D can automatically compute the reflection vectors for your geometry.</span></span> <span data-ttu-id="57dcb-141">使用這項功能可節省記憶體，因為您不需要包含環境對應的材質座標。</span><span class="sxs-lookup"><span data-stu-id="57dcb-141">Using this feature saves memory because you don't need to include texture coordinates for the environment map.</span></span> <span data-ttu-id="57dcb-142">它也會減少頻寬，而在 T&L HAL 裝置的情況下，它可能會比您的應用程式本身所能產生的計算速度快很多。</span><span class="sxs-lookup"><span data-stu-id="57dcb-142">It also reduces bandwidth and, in the case of a T&L HAL Device, it can be significantly faster than the computations that your application can make on its own.</span></span> <span data-ttu-id="57dcb-143">若要使用這項功能，請在包含三層環境對應的材質階段中，將 [D3DTSS \_ TEXCOORDINDEX 材質階段] 狀態設定為 \_ CAMERASPACEREFLECTIONVECTOR 的 D3DTSS TCI \_ D3DTEXTURESTAGESTATETYPE 成員和紋理座標集合的索引組合。 [](./d3dtexturestagestatetype.md)</span><span class="sxs-lookup"><span data-stu-id="57dcb-143">To use this feature, in the texture stage that contains the cubic environment map, set the D3DTSS\_TEXCOORDINDEX texture stage state to a combination of the D3DTSS\_TCI\_CAMERASPACEREFLECTIONVECTOR member of [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) and the index of a texture coordinate set.</span></span> <span data-ttu-id="57dcb-144">在某些情況下（例如，擴散燈光對應），您可以使用 D3DTEXTURESTAGESTATETYPE 的 D3DTSS \_ TCI \_ CAMERASPACENORMAL 成員，這會導致系統使用轉換的相機空間、頂點標準作為材質的定址向量。 </span><span class="sxs-lookup"><span data-stu-id="57dcb-144">In some situations, like diffuse light mapping, you might use the D3DTSS\_TCI\_CAMERASPACENORMAL member of **D3DTEXTURESTAGESTATETYPE**, which causes the system to use the transformed, camera-space, vertex normal as the addressing vector for the texture.</span></span> <span data-ttu-id="57dcb-145">索引僅供系統用來判斷材質的包裝模式。</span><span class="sxs-lookup"><span data-stu-id="57dcb-145">The index is only used by the system to determine the wrapping mode for the texture.</span></span>

<span data-ttu-id="57dcb-146">下列程式碼範例顯示如何使用此值。</span><span class="sxs-lookup"><span data-stu-id="57dcb-146">The following code example shows how this value is used.</span></span>


```
// The m_d3dDevice variable is a valid pointer
// to an IDirect3DDevice9 interface.

// Automatically generate texture coordinates for stage 2.
// This assumes that stage 2 is assigned a cube map.
// Use the wrap mode from the texture coordinate set at index 1.

m_d3dDevice->SetTextureStageState( 2, D3DTSS_TEXCOORDINDEX,
                                   D3DTSS_TCI_CAMERASPACEREFLECTIONVECTOR | 1); 
```



<span data-ttu-id="57dcb-147">當您啟用自動材質座標產生時，系統會使用兩個公式中的一個來計算每個頂點的反射向量。</span><span class="sxs-lookup"><span data-stu-id="57dcb-147">When you enable automatic texture coordinate generation, the system uses one of two formulas to compute the reflection vector for each vertex.</span></span> <span data-ttu-id="57dcb-148">當 D3DRS \_ LOCALVIEWER 轉譯狀態設為 **TRUE** 時，會使用下列公式。</span><span class="sxs-lookup"><span data-stu-id="57dcb-148">When the D3DRS\_LOCALVIEWER render state is set to **TRUE**, the following formula is used.</span></span>

![反映向量的公式 (r = 2 (exn) n-e) ](images/reflection-vector-local.png)

<span data-ttu-id="57dcb-150">在上述公式中，R 是正在計算的反映向量，E 是正規化的位置向量，而 N 是相機空間頂點正常。</span><span class="sxs-lookup"><span data-stu-id="57dcb-150">In the preceding formula, R is the reflection vector being computed, E is the normalized position-to-eye vector, and N is the camera-space vertex normal.</span></span>

<span data-ttu-id="57dcb-151">當 D3DRS \_ LOCALVIEWER 轉譯狀態設為 **FALSE** 時，系統會使用下列公式。</span><span class="sxs-lookup"><span data-stu-id="57dcb-151">When the D3DRS\_LOCALVIEWER render state is set to **FALSE**, the system uses the following formula.</span></span>

![反映向量 (r = 2nzn-i) 的公式](images/reflection-vector-nonlocal.png)

<span data-ttu-id="57dcb-153">此公式中的 R 和 N 元素與先前的公式相同。</span><span class="sxs-lookup"><span data-stu-id="57dcb-153">The R and N elements in this formula are identical to the previous formula.</span></span> <span data-ttu-id="57dcb-154">N<sub>Z</sub> 的元素是頂點法線的世界空間 Z，而 I 是 (0，0，1) 無限遠的觀點。</span><span class="sxs-lookup"><span data-stu-id="57dcb-154">The N<sub>Z</sub> element is the world-space z of the vertex normal, and I is the vector (0,0,1) of an infinitely distant viewpoint.</span></span> <span data-ttu-id="57dcb-155">系統會從任一公式使用反映向量，以選取並處理 cube 地圖的適當臉部。</span><span class="sxs-lookup"><span data-stu-id="57dcb-155">The system uses the reflection vector from either formula to select and address the appropriate face of the cube map.</span></span>

> [!Note]  
> <span data-ttu-id="57dcb-156">在大多數情況下，應用程式應該啟用頂點法線的自動正規化。</span><span class="sxs-lookup"><span data-stu-id="57dcb-156">In most cases, applications should enable automatic normalization of vertex normals.</span></span> <span data-ttu-id="57dcb-157">若要這樣做，請將 D3DRS \_ NORMALIZENORMALS 設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="57dcb-157">To do this, set D3DRS\_NORMALIZENORMALS to **TRUE**.</span></span> <span data-ttu-id="57dcb-158">如果您未啟用此呈現狀態，則環境對應的外觀會與您預期的不同。</span><span class="sxs-lookup"><span data-stu-id="57dcb-158">If you do not enable this render state, the appearance of the environment map will be drastically different than you might expect.</span></span>

 

<span data-ttu-id="57dcb-159">下列主題包含其他資訊。</span><span class="sxs-lookup"><span data-stu-id="57dcb-159">Additional information is contained in the following topic.</span></span>

-   [<span data-ttu-id="57dcb-160"> (Direct3D 9) 建立三個環境的地圖表面 </span><span class="sxs-lookup"><span data-stu-id="57dcb-160">Creating Cubic Environment Map Surfaces (Direct3D 9)</span></span>](creating-cubic-environment-map-surfaces.md)

## <a name="related-topics"></a><span data-ttu-id="57dcb-161">相關主題</span><span class="sxs-lookup"><span data-stu-id="57dcb-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57dcb-162">環境對應</span><span class="sxs-lookup"><span data-stu-id="57dcb-162">Environment Mapping</span></span>](environment-mapping.md)
</dt> </dl>

 

 
