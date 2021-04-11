---
description: 圖元霧化會從設備磁碟機中以每圖元為基礎計算的事實取得其名稱。
ms.assetid: 6fcfb9fa-cacc-4dbc-bfc6-85d533dbfbf8
title: " (Direct3D 9) 的圖元霧化"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f62a597820fa009207d8dda7836d161cdf34c88
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845735"
---
# <a name="pixel-fog-direct3d-9"></a><span data-ttu-id="56743-103"> (Direct3D 9) 的圖元霧化</span><span class="sxs-lookup"><span data-stu-id="56743-103">Pixel Fog (Direct3D 9)</span></span>

<span data-ttu-id="56743-104">圖元霧化會從設備磁碟機中以每圖元為基礎計算的事實取得其名稱。</span><span class="sxs-lookup"><span data-stu-id="56743-104">Pixel fog gets its name from the fact that it is calculated on a per-pixel basis in the device driver.</span></span> <span data-ttu-id="56743-105">這與頂點霧化不同，它是在轉換和光源計算期間由管線所計算。</span><span class="sxs-lookup"><span data-stu-id="56743-105">This is different from vertex fog, which is computed by the pipeline during transformation and lighting calculations.</span></span> <span data-ttu-id="56743-106">圖元霧化有時稱為資料表霧化，因為某些驅動程式會使用預先計算的查閱資料表來決定霧化因數，並使用每個圖元的深度來套用混合計算。</span><span class="sxs-lookup"><span data-stu-id="56743-106">Pixel fog is sometimes called table fog because some drivers use a precalculated lookup table to determine the fog factor, using the depth of each pixel to apply in blending computations.</span></span> <span data-ttu-id="56743-107">您可以使用 [**D3DFOGMODE**](./d3dfogmode.md) 列舉型別成員所識別的任何霧化公式來套用它。</span><span class="sxs-lookup"><span data-stu-id="56743-107">It can be applied using any fog formula identified by members of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span> <span data-ttu-id="56743-108">這些公式的實作為特定驅動程式。</span><span class="sxs-lookup"><span data-stu-id="56743-108">The implementations of these formulas are driver-specific.</span></span> <span data-ttu-id="56743-109">如果驅動程式不支援複雜的霧化公式，它應該會降級為較不復雜的公式。</span><span class="sxs-lookup"><span data-stu-id="56743-109">If a driver doesn't support a complex fog formula, it should degrade to a less complex formula.</span></span>

## <a name="eye-relative-vs-z-based-depth"></a><span data-ttu-id="56743-110">Eye-Relative 與以 Z 為基礎的深度</span><span class="sxs-lookup"><span data-stu-id="56743-110">Eye-Relative vs. Z-Based Depth</span></span>

<span data-ttu-id="56743-111">若要減少深度緩衝區中不平均分佈的霧化相關圖形成品，大部分的硬體裝置都會使用眼睛相對深度，而非以 z 為基礎的深度值進行圖元霧化。</span><span class="sxs-lookup"><span data-stu-id="56743-111">To alleviate fog-related graphic artifacts caused by uneven distribution of z-values in a depth buffer, most hardware devices use eye-relative depth instead of z-based depth values for pixel fog.</span></span> <span data-ttu-id="56743-112">眼睛相對深度基本上就是來自同質座標集合的 w 元素。</span><span class="sxs-lookup"><span data-stu-id="56743-112">Eye-relative depth is essentially the w element from a homogeneous coordinate set.</span></span> <span data-ttu-id="56743-113">Microsoft Direct3D 會從裝置空間座標設定 RHW 元素，以重現 true w。</span><span class="sxs-lookup"><span data-stu-id="56743-113">Microsoft Direct3D takes the reciprocal of the RHW element from a device space coordinate set to reproduce true w.</span></span> <span data-ttu-id="56743-114">如果裝置支援眼睛相關的霧化，則當您呼叫 [**IDirect3DDevice9：： GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps)方法時，它會在 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)結構的 RasterCaps 成員中設定 **D3DPRASTERCAPS \_ WFOG** 旗標。</span><span class="sxs-lookup"><span data-stu-id="56743-114">If a device supports eye-relative fog, it sets the **D3DPRASTERCAPS\_WFOG** flag in the RasterCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure when you call the [**IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) method.</span></span> <span data-ttu-id="56743-115">除了參考轉譯器之外，軟體裝置一律會使用 z 來計算圖元霧化效果。</span><span class="sxs-lookup"><span data-stu-id="56743-115">With the exception of the reference rasterizer, software devices always use z to calculate pixel fog effects.</span></span>

<span data-ttu-id="56743-116">當支援眼睛相關的霧化時，如果提供的投射矩陣在世界空間中產生的 z 值相當於裝置空間中的 w 值，系統會自動使用眼睛相關深度，而不是以 z 為基礎的深度。</span><span class="sxs-lookup"><span data-stu-id="56743-116">When eye-relative fog is supported, the system automatically uses eye-relative depth rather than z-based depth if the provided projection matrix produces z-values in world space that are equivalent to w-values in device space.</span></span> <span data-ttu-id="56743-117">您可以藉由呼叫 [**IDirect3DDevice9：： SetTransform**](/windows/desktop/api) 方法來設定投影矩陣，並使用 D3DTS \_ 投射值並傳遞代表所需矩陣的 [**D3DMATRIX**](d3dmatrix.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="56743-117">You set the projection matrix by calling the [**IDirect3DDevice9::SetTransform**](/windows/desktop/api) method, using the D3DTS\_PROJECTION value and passing a [**D3DMATRIX**](d3dmatrix.md) structure that represents the desired matrix.</span></span> <span data-ttu-id="56743-118">如果投射矩陣不符合這項需求，則不會正確套用霧化效果。</span><span class="sxs-lookup"><span data-stu-id="56743-118">If the projection matrix isn't compliant with this requirement, fog effects are not applied properly.</span></span> <span data-ttu-id="56743-119">如需有關產生相容矩陣的詳細資訊，請參閱 [ (Direct3D 9) 的投射轉換 ](projection-transform.md)。</span><span class="sxs-lookup"><span data-stu-id="56743-119">For details about producing a compliant matrix, see [Projection Transform (Direct3D 9)](projection-transform.md).</span></span>

<span data-ttu-id="56743-120">Direct3D 使用目前以 w 型深度計算的投影矩陣。</span><span class="sxs-lookup"><span data-stu-id="56743-120">Direct3D uses the currently set projection matrix in its w-based depth calculations.</span></span> <span data-ttu-id="56743-121">如此一來，應用程式就必須設定符合規範的投射矩陣，才能收到所需的 w 型功能，即使它不使用 Direct3D 轉換管線也一樣。</span><span class="sxs-lookup"><span data-stu-id="56743-121">As a result, an application must set a compliant projection matrix to receive the desired w-based features, even if it does not use the Direct3D transformation pipeline.</span></span>

<span data-ttu-id="56743-122">Direct3D 會檢查投射矩陣的第四個數據行。</span><span class="sxs-lookup"><span data-stu-id="56743-122">Direct3D checks the fourth column of the projection matrix.</span></span> <span data-ttu-id="56743-123">如果係數為 \[ 0、0、0、1 \] (用於仿射投影) 系統將使用以 z 為基礎的深度值進行霧化。</span><span class="sxs-lookup"><span data-stu-id="56743-123">If the coefficients are \[0,0,0,1\] (for an affine projection) the system will use z-based depth values for fog.</span></span> <span data-ttu-id="56743-124">在此情況下，您也必須指定裝置空間中線性模糊效果的開始和結束距離，範圍從0.0 到最接近使用者的位置，以及最遠的1.0。</span><span class="sxs-lookup"><span data-stu-id="56743-124">In this case, you must also specify the start and end distances for linear fog effects in device space, which ranges from 0.0 at the nearest point to the user, and 1.0 at the farthest point.</span></span>

## <a name="using-pixel-fog"></a><span data-ttu-id="56743-125">使用圖元霧化</span><span class="sxs-lookup"><span data-stu-id="56743-125">Using Pixel Fog</span></span>

<span data-ttu-id="56743-126">使用下列步驟，在您的應用程式中啟用圖元霧化。</span><span class="sxs-lookup"><span data-stu-id="56743-126">Use the following steps to enable pixel fog in your application.</span></span>

1.  <span data-ttu-id="56743-127">將 D3DRS \_ FOGENABLE 轉譯狀態設為 **TRUE**，以啟用霧化混合。</span><span class="sxs-lookup"><span data-stu-id="56743-127">Enable fog blending by setting the D3DRS\_FOGENABLE render state to **TRUE**.</span></span>
2.  <span data-ttu-id="56743-128">在 D3DRS FOGCOLOR 轉譯狀態中設定所需的霧化色彩 \_ 。</span><span class="sxs-lookup"><span data-stu-id="56743-128">Set the desired fog color in the D3DRS\_FOGCOLOR render state.</span></span>
3.  <span data-ttu-id="56743-129">將 D3DRS \_ FOGTABLEMODE 轉譯狀態設定為 [**D3DFOGMODE**](./d3dfogmode.md) 列舉型別的對應成員，以選擇要使用的霧化公式。</span><span class="sxs-lookup"><span data-stu-id="56743-129">Choose the fog formula to use by setting the D3DRS\_FOGTABLEMODE render state to the corresponding member of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span>
4.  <span data-ttu-id="56743-130">在相關聯的轉譯狀態中，為選取的霧化模式設定所需的霧化參數。</span><span class="sxs-lookup"><span data-stu-id="56743-130">Set the fog parameters as desired for the selected fog mode in the associated render states.</span></span> <span data-ttu-id="56743-131">這包括線性霧化的開始和結束距離，以及指數霧化模式的霧化密度。</span><span class="sxs-lookup"><span data-stu-id="56743-131">This includes the start and end distances for linear fog, and fog density for exponential fog mode.</span></span>

<span data-ttu-id="56743-132">下列範例會顯示這些步驟在程式碼中的樣子。</span><span class="sxs-lookup"><span data-stu-id="56743-132">The following example shows what these steps might look like in code.</span></span>


```
// For brevity, error values in this example are not checked 
//   after each call. A real-world application should check 
//   these values appropriately.
//
// For the purposes of this example, g_pDevice is a valid
//   pointer to an IDirect3DDevice9 interface.
void SetupPixelFog(DWORD Color, DWORD Mode)
{
    float Start   = 0.5f;    // For linear mode
    float End     = 0.8f;
    float Density = 0.66f;   // For exponential modes
 
    // Enable fog blending.
    g_pDevice->SetRenderState(D3DRS_FOGENABLE, TRUE);
 
    // Set the fog color.
    g_pDevice->SetRenderState(D3DRS_FOGCOLOR, Color);
    
    // Set fog parameters.
    if( Mode == D3DFOG_LINEAR )
    {
        g_pDevice->SetRenderState(D3DRS_FOGTABLEMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGSTART, *(DWORD *)(&Start));
        g_pDevice->SetRenderState(D3DRS_FOGEND,   *(DWORD *)(&End));
    }
    else
    {
        g_pDevice->SetRenderState(D3DRS_FOGTABLEMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGDENSITY, *(DWORD *)(&Density));
    }
```



<span data-ttu-id="56743-133">由於 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法只接受第二個參數中的 DWORD 值，因此某些霧化參數必須是浮點值。</span><span class="sxs-lookup"><span data-stu-id="56743-133">Some fog parameters are required as floating-point values, even though the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts only DWORD values in the second parameter.</span></span> <span data-ttu-id="56743-134">上述範例會將浮點變數的位址轉換為 DWORD 指標，然後將其取值，以將浮點值提供給 **IDirect3DDevice9：： graphicsdevice** 而不需要資料轉譯。</span><span class="sxs-lookup"><span data-stu-id="56743-134">The preceding example provides the floating-point values to **IDirect3DDevice9::SetRenderState** without data translation by casting the addresses of the floating-point variables as DWORD pointers, and then dereferencing them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="56743-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="56743-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56743-136">霧化類型</span><span class="sxs-lookup"><span data-stu-id="56743-136">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 
