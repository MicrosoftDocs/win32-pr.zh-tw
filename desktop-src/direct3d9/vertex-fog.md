---
description: 當系統執行頂點 fogging 時，它會在多邊形中的每個頂點上套用霧化計算，然後在點陣化期間將結果插到多邊形的臉部。
ms.assetid: 76989eb3-cd95-4dfc-ba0f-7563860b531c
title: " (Direct3D 9) 的頂點霧化"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35cd880bda7ebffd36bd95bec5f8565e104eaa15
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108392"
---
# <a name="vertex-fog-direct3d-9"></a><span data-ttu-id="5222e-103"> (Direct3D 9) 的頂點霧化</span><span class="sxs-lookup"><span data-stu-id="5222e-103">Vertex Fog (Direct3D 9)</span></span>

<span data-ttu-id="5222e-104">當系統執行頂點 fogging 時，它會在多邊形中的每個頂點上套用霧化計算，然後在點陣化期間將結果插到多邊形的臉部。</span><span class="sxs-lookup"><span data-stu-id="5222e-104">When the system performs vertex fogging, it applies fog calculations at each vertex in a polygon, and then interpolates the results across the face of the polygon during rasterization.</span></span> <span data-ttu-id="5222e-105">頂點霧化效果是由 Direct3D 光源和轉換引擎所計算。</span><span class="sxs-lookup"><span data-stu-id="5222e-105">Vertex fog effects are computed by the Direct3D lighting and transformation engine.</span></span> <span data-ttu-id="5222e-106">如需詳細資訊，請參閱 [ (Direct3D 9) 的霧化參數 ](fog-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="5222e-106">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md).</span></span>

<span data-ttu-id="5222e-107">如果您的應用程式未使用 Direct3D 進行轉換和光源，應用程式必須執行霧化計算。</span><span class="sxs-lookup"><span data-stu-id="5222e-107">If your application does not use Direct3D for transformation and lighting, the application must perform fog calculations.</span></span> <span data-ttu-id="5222e-108">在此情況下，請放置在每個頂點之反射色彩的 Alpha 元件中計算的霧化因數。</span><span class="sxs-lookup"><span data-stu-id="5222e-108">In this case, place the fog factor that is computed in the alpha component of the specular color for each vertex.</span></span> <span data-ttu-id="5222e-109">您可以隨意使用任何想要的公式-範圍型、體積型，或其他任何公式。</span><span class="sxs-lookup"><span data-stu-id="5222e-109">You are free to use whatever formulas you want - range-based, volumetric, or otherwise.</span></span> <span data-ttu-id="5222e-110">Direct3D 會使用提供的霧化因數，以在每個多邊形的臉部之間進行插補。</span><span class="sxs-lookup"><span data-stu-id="5222e-110">Direct3D uses the supplied fog factor to interpolate across the face of each polygon.</span></span> <span data-ttu-id="5222e-111">執行自己的轉換和光源的應用程式也必須執行自己的頂點霧化計算。</span><span class="sxs-lookup"><span data-stu-id="5222e-111">Applications that perform their own transformation and lighting must also perform their own vertex fog calculations.</span></span> <span data-ttu-id="5222e-112">如此一來，這類應用程式只需要啟用霧化混合，並透過相關聯的轉譯狀態設定霧化色彩，如 [ (direct3d 9) ](fog-blending.md) 和 [ (direct3d 9) ](fog-color.md)的霧化色彩中所述。</span><span class="sxs-lookup"><span data-stu-id="5222e-112">As a result, such an application need only enable fog blending and set the fog color through the associated render states, as described in [Fog Blending (Direct3D 9)](fog-blending.md) and [Fog Color (Direct3D 9)](fog-color.md).</span></span>

> [!Note]  
> <span data-ttu-id="5222e-113">使用頂點著色器時，您必須使用頂點霧化。</span><span class="sxs-lookup"><span data-stu-id="5222e-113">When using a vertex shader, you must use vertex fog.</span></span> <span data-ttu-id="5222e-114">這是使用頂點著色器將每個頂點的霧化濃度寫入 oFog 註冊來完成的。</span><span class="sxs-lookup"><span data-stu-id="5222e-114">This is accomplished by using the vertex shader to write the per-vertex fog intensity to the oFog register.</span></span> <span data-ttu-id="5222e-115">圖元著色器完成後，會使用 oFog 資料以線性方式插補與霧化色彩。</span><span class="sxs-lookup"><span data-stu-id="5222e-115">After the pixel shader completes, the oFog data is used to linearly interpolate with the fog color.</span></span> <span data-ttu-id="5222e-116">圖元著色器無法使用此強度。</span><span class="sxs-lookup"><span data-stu-id="5222e-116">This intensity is not available in a pixel shader.</span></span>

 

## <a name="range-based-fog"></a><span data-ttu-id="5222e-117">Range-Based 霧化</span><span class="sxs-lookup"><span data-stu-id="5222e-117">Range-Based Fog</span></span>

> [!Note]  
> <span data-ttu-id="5222e-118">只有在搭配 Direct3D 轉換和光源引擎使用頂點霧化時，Direct3D 才會使用範圍型的霧化計算。</span><span class="sxs-lookup"><span data-stu-id="5222e-118">Direct3D uses range-based fog calculations only when using vertex fog with the Direct3D transformation and lighting engine.</span></span> <span data-ttu-id="5222e-119">這是因為在設備磁碟機中會實作為圖元霧化，而且目前沒有硬體可支援每個圖元範圍的霧化。</span><span class="sxs-lookup"><span data-stu-id="5222e-119">This is because pixel fog is implemented in the device driver, and no hardware currently exists to support per-pixel range-based fog.</span></span> <span data-ttu-id="5222e-120">如果您的應用程式會執行自己的轉換和光源，它必須執行自己的霧化計算（以範圍為基礎或其他）。</span><span class="sxs-lookup"><span data-stu-id="5222e-120">If your application performs its own transformation and lighting, it must perform its own fog calculations, range-based or otherwise.</span></span>

 

<span data-ttu-id="5222e-121">有時候，使用霧化可能會導入圖形成品，以 nonintuitive 方式將物件與霧化色彩混合。</span><span class="sxs-lookup"><span data-stu-id="5222e-121">Sometimes, using fog can introduce graphic artifacts that cause objects to be blended with the fog color in nonintuitive ways.</span></span> <span data-ttu-id="5222e-122">例如，假設有一個場景，其中有兩個可見的物件：一段距離足以受到霧化的影響，而另一個則接近不受影響。</span><span class="sxs-lookup"><span data-stu-id="5222e-122">For example, imagine a scene in which there are two visible objects: one distant enough to be affected by fog, and the other near enough to be unaffected.</span></span> <span data-ttu-id="5222e-123">如果視圖區域就地旋轉，則可能會變更明顯的霧化效果，即使物件是固定的也一樣。</span><span class="sxs-lookup"><span data-stu-id="5222e-123">If the viewing area rotates in place, the apparent fog effects can change, even if the objects are stationary.</span></span> <span data-ttu-id="5222e-124">下圖顯示這種情況的由上而下的觀點。</span><span class="sxs-lookup"><span data-stu-id="5222e-124">The following diagram shows a top-down view of such a situation.</span></span>

![兩個視點的圖表，以及它們對兩個物件的霧化有何影響](images/artifog.png)

<span data-ttu-id="5222e-126">以範圍為基礎的霧化是判斷霧化效果的另一個更精確的方式。</span><span class="sxs-lookup"><span data-stu-id="5222e-126">Range-based fog is another, more accurate, way to determine the fog effects.</span></span> <span data-ttu-id="5222e-127">在以範圍為基礎的霧化中，Direct3D 會使用從視點到頂點的實際距離來進行霧化計算。</span><span class="sxs-lookup"><span data-stu-id="5222e-127">In range-based fog, Direct3D uses the actual distance from the viewpoint to a vertex for its fog calculations.</span></span> <span data-ttu-id="5222e-128">Direct3D 會增加霧的影響，因為這兩個點之間的距離會增加，而不是場景內頂點的深度，藉以避免旋轉成品。</span><span class="sxs-lookup"><span data-stu-id="5222e-128">Direct3D increases the effect of fog as the distance between the two points increases, rather than the depth of the vertex within in the scene, thereby avoiding rotational artifacts.</span></span>

<span data-ttu-id="5222e-129">如果目前的裝置支援以範圍為基礎的霧化，則 \_ 當您呼叫 [**IDirect3DDevice9：： GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps)方法時，它會在 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 RasterCaps 成員中設定 D3DPRASTERCAPS FOGRANGE 值。</span><span class="sxs-lookup"><span data-stu-id="5222e-129">If the current device supports range-based fog, it will set the D3DPRASTERCAPS\_FOGRANGE value in the RasterCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) when you call the [**IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) method.</span></span> <span data-ttu-id="5222e-130">若要啟用以範圍為基礎的霧化，請將 D3DRS \_ RANGEFOGENABLE 轉譯狀態設為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="5222e-130">To enable range-based fog, set the D3DRS\_RANGEFOGENABLE render state to **TRUE**.</span></span>

<span data-ttu-id="5222e-131">以範圍為基礎的霧化是由 Direct3D 在轉換和光源期間計算。</span><span class="sxs-lookup"><span data-stu-id="5222e-131">Range-based fog is computed by Direct3D during transformation and lighting.</span></span> <span data-ttu-id="5222e-132">未使用 Direct3D 轉換和光源引擎的應用程式也必須執行自己的頂點霧化計算。</span><span class="sxs-lookup"><span data-stu-id="5222e-132">Applications that don't use the Direct3D transformation and lighting engine must also perform their own vertex fog calculations.</span></span> <span data-ttu-id="5222e-133">在此情況下，請針對每個頂點，在反射元件的 Alpha 元件中提供範圍型霧化係數。</span><span class="sxs-lookup"><span data-stu-id="5222e-133">In this case, provide the range-based fog factor in the alpha component of the specular component for each vertex.</span></span>

## <a name="using-vertex-fog"></a><span data-ttu-id="5222e-134">使用頂點霧化</span><span class="sxs-lookup"><span data-stu-id="5222e-134">Using Vertex Fog</span></span>

<span data-ttu-id="5222e-135">使用下列步驟，在您的應用程式中啟用頂點霧化。</span><span class="sxs-lookup"><span data-stu-id="5222e-135">Use the following steps to enable vertex fog in your application.</span></span>

1.  <span data-ttu-id="5222e-136">將 D3DRS \_ FOGENABLE 設定為 **TRUE**，以啟用霧化混合。</span><span class="sxs-lookup"><span data-stu-id="5222e-136">Enable fog blending by setting D3DRS\_FOGENABLE to **TRUE**.</span></span>
2.  <span data-ttu-id="5222e-137">設定 D3DRS FOGCOLOR 轉譯狀態中的 [霧化色彩] \_ 。</span><span class="sxs-lookup"><span data-stu-id="5222e-137">Set the fog color in the D3DRS\_FOGCOLOR render state.</span></span>
3.  <span data-ttu-id="5222e-138">將 D3DRS \_ FOGVERTEXMODE 轉譯狀態設定為 [**D3DFOGMODE**](./d3dfogmode.md) 列舉型別的成員，以選擇所需的霧化公式。</span><span class="sxs-lookup"><span data-stu-id="5222e-138">Choose the desired fog formula by setting the D3DRS\_FOGVERTEXMODE render state to a member of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span>
4.  <span data-ttu-id="5222e-139">在轉譯狀態中，為選取的霧化公式設定所需的霧化參數。</span><span class="sxs-lookup"><span data-stu-id="5222e-139">Set the fog parameters as desired for the selected fog formula in the render states.</span></span>

<span data-ttu-id="5222e-140">下列以 c + + 撰寫的範例會顯示這些步驟在程式碼中的樣子。</span><span class="sxs-lookup"><span data-stu-id="5222e-140">The following example, written in C++, shows what these steps might look like in code.</span></span>


```
// For brevity, error values in this example are not checked 
//   after each call. A real-world application should check 
//   these values appropriately.
//
// For the purposes of this example, g_pDevice is a valid
//   pointer to an IDirect3DDevice9 interface.
void SetupVertexFog(DWORD Color, DWORD Mode, BOOL UseRange, FLOAT Density)
{
    float Start = 0.5f,    // Linear fog distances
          End   = 0.8f;
 
    // Enable fog blending.
    g_pDevice->SetRenderState(D3DRS_FOGENABLE, TRUE);
 
    // Set the fog color.
    g_pDevice->SetRenderState(D3DRS_FOGCOLOR, Color);
    
    // Set fog parameters.
    if(D3DFOG_LINEAR == Mode)
    {
        g_pDevice->SetRenderState(D3DRS_FOGVERTEXMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGSTART, *(DWORD *)(&Start));
        g_pDevice->SetRenderState(D3DRS_FOGEND,   *(DWORD *)(&End));
    }
    else
    {
        g_pDevice->SetRenderState(D3DRS_FOGVERTEXMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGDENSITY, *(DWORD *)(&Density));
    }

    // Enable range-based fog if desired (only supported for
    //   vertex fog). For this example, it is assumed that UseRange
    //   is set to a nonzero value only if the driver exposes the 
    //   D3DPRASTERCAPS_FOGRANGE capability.
    // Note: This is slightly more performance intensive
    //   than non-range-based fog.
    if(UseRange)
        g_pDevice->SetRenderState(D3DRS_RANGEFOGENABLE, TRUE);
}
```



<span data-ttu-id="5222e-141">某些霧化參數是浮點值的必要參數，即使 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法只接受第二個參數中的 DWORD 值也是一樣。</span><span class="sxs-lookup"><span data-stu-id="5222e-141">Some fog parameters are required as floating-point values, even though the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method only accepts DWORD values in the second parameter.</span></span> <span data-ttu-id="5222e-142">這個範例會將浮點變數的位址轉換成 DWORD 指標，然後將它們取值，以成功提供這些方法的浮點值給這些方法，而不需要資料轉譯。</span><span class="sxs-lookup"><span data-stu-id="5222e-142">This example successfully provides the floating-point values to these methods without data translation by casting the addresses of the floating-point variables as DWORD pointers, and then dereferencing them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5222e-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="5222e-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5222e-144">霧化類型</span><span class="sxs-lookup"><span data-stu-id="5222e-144">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 
