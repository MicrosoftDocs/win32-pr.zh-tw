---
description: 應用程式會使用樣板緩衝區來遮罩影像中的圖元。 遮罩控制是否繪製像素。 一些比較常見的效果如下所示。
ms.assetid: 984f0a98-4a74-44c3-a9d0-f5d3f12f7e4e
title: " (Direct3D 9) 的樣板緩衝區技巧"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c2dcc05475a3ddfc13e456faf60ec2d11e271a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385836"
---
# <a name="stencil-buffer-techniques-direct3d-9"></a><span data-ttu-id="b8d8c-105"> (Direct3D 9) 的樣板緩衝區技巧</span><span class="sxs-lookup"><span data-stu-id="b8d8c-105">Stencil Buffer Techniques (Direct3D 9)</span></span>

<span data-ttu-id="b8d8c-106">應用程式會使用樣板緩衝區來遮罩影像中的圖元。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-106">Applications use the stencil buffer to mask pixels in an image.</span></span> <span data-ttu-id="b8d8c-107">遮罩控制是否繪製像素。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-107">The mask controls whether the pixel is drawn or not.</span></span> <span data-ttu-id="b8d8c-108">一些比較常見的效果如下所示。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-108">Some of the more common effects are shown below.</span></span>

-   [<span data-ttu-id="b8d8c-109">合成</span><span class="sxs-lookup"><span data-stu-id="b8d8c-109">Compositing</span></span>](compositing.md)
-   [<span data-ttu-id="b8d8c-110">Decaling</span><span class="sxs-lookup"><span data-stu-id="b8d8c-110">Decaling</span></span>](decaling.md)
-   [<span data-ttu-id="b8d8c-111">溶解、淡化和撥動</span><span class="sxs-lookup"><span data-stu-id="b8d8c-111">Dissolves, Fades, and Swipes</span></span>](dissolves--fades--and-swipes.md)
-   [<span data-ttu-id="b8d8c-112">大綱和 Silhouettes</span><span class="sxs-lookup"><span data-stu-id="b8d8c-112">Outlines and Silhouettes</span></span>](outlines-and-silhouettes.md)
-   [<span data-ttu-id="b8d8c-113">雙側範本</span><span class="sxs-lookup"><span data-stu-id="b8d8c-113">Two-Sided Stencil</span></span>](two-sided-stencil.md)

<span data-ttu-id="b8d8c-114">樣板緩衝區啟用或停用依據個別像素的轉譯目標表面繪圖。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-114">The stencil buffer enables or disables drawing to the rendering target surface on a pixel-by-pixel basis.</span></span> <span data-ttu-id="b8d8c-115">在最基本層級，它可以讓應用程式遮罩轉譯影像的區段，讓它們不會顯示。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-115">At its most fundamental level, it enables applications to mask sections of the rendered image so that they are not displayed.</span></span> <span data-ttu-id="b8d8c-116">應用程式通常會將樣板緩衝區用於特殊效果，例如溶解、印花，以及外框。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-116">Applications often use stencil buffers for special effects such as dissolves, decaling, and outlining.</span></span>

<span data-ttu-id="b8d8c-117">樣板緩衝區資訊內嵌於 z 緩衝資料。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-117">Stencil buffer information is embedded in the z-buffer data.</span></span> <span data-ttu-id="b8d8c-118">您的應用程式可以使用 [**IDirect3D9：： CheckDeviceFormat**](/windows/desktop/api) 方法來檢查硬體範本支援，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-118">Your application can use the [**IDirect3D9::CheckDeviceFormat**](/windows/desktop/api) method to check for hardware stencil support, as shown in the following code example.</span></span>


```
// Reject devices that cannot perform 8-bit stencil buffering. 
// The following example assumes that pCaps is a valid pointer 
// to an initialized D3DCAPS9 structure. 

if( FAILED( m_pD3D->CheckDeviceFormat( pCaps->AdapterOrdinal,
                                       pCaps->DeviceType,  
                                       Format,  
                                       D3DUSAGE_DEPTHSTENCIL, 
                                       D3DRTYPE_SURFACE,
                                       D3DFMT_D24S8 ) ) )
return E_FAIL;
```



<span data-ttu-id="b8d8c-119">[**IDirect3D9：： CheckDeviceFormat**](/windows/desktop/api) 可讓您根據裝置的功能，選擇要建立的裝置。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-119">[**IDirect3D9::CheckDeviceFormat**](/windows/desktop/api) allows you to choose a device to create based on the capabilities of that device.</span></span> <span data-ttu-id="b8d8c-120">在此情況下，不支援8位樣板緩衝區的裝置將會遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-120">In this case, devices that do not support 8-bit stencil buffers are rejected.</span></span> <span data-ttu-id="b8d8c-121">請注意，這只是 **IDirect3D9：： CheckDeviceFormat**; 的一個可能用途如需詳細資訊，請參閱 [判斷 (Direct3D 9) 的硬體支援](determining-hardware-support.md)。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-121">Note that this is only one possible use for **IDirect3D9::CheckDeviceFormat**; for details see [Determining Hardware Support (Direct3D 9)](determining-hardware-support.md).</span></span>

## <a name="how-the-stencil-buffer-works"></a><span data-ttu-id="b8d8c-122">樣板緩衝區的運作方式</span><span class="sxs-lookup"><span data-stu-id="b8d8c-122">How the Stencil Buffer Works</span></span>

<span data-ttu-id="b8d8c-123">Direct3D 依據個別像素在樣板緩衝區的內容執行測試。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-123">Direct3D performs a test on the contents of the stencil buffer on a pixel-by-pixel basis.</span></span> <span data-ttu-id="b8d8c-124">對於目標表面的每一個像素，它會使用樣板緩衝區中的對應值、樣板參考值，以及樣板遮罩值來執行測試。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-124">For each pixel in the target surface, it performs a test using the corresponding value in the stencil buffer, a stencil reference value, and a stencil mask value.</span></span> <span data-ttu-id="b8d8c-125">如果通過測試，Direct3D 執行動作。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-125">If the test passes, Direct3D performs an action.</span></span> <span data-ttu-id="b8d8c-126">使用下列步驟執行測試。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-126">The test is performed using the following steps.</span></span>

1.  <span data-ttu-id="b8d8c-127">執行樣板參考值與樣板遮罩的位元 AND 運算。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-127">Perform a bitwise AND operation of the stencil reference value with the stencil mask.</span></span>
2.  <span data-ttu-id="b8d8c-128">執行目前像素之樣板緩衝區值與樣板遮罩的位元 AND 運算。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-128">Perform a bitwise AND operation of the stencil buffer value for the current pixel with the stencil mask.</span></span>
3.  <span data-ttu-id="b8d8c-129">使用比較函式，比較步驟 1 的結果與步驟 2 的結果。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-129">Compare the result of step 1 to the result of step 2, using the comparison function.</span></span>

<span data-ttu-id="b8d8c-130">下列程式碼範例會顯示這些步驟。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-130">These steps are shown in the following code example.</span></span>


```
(StencilRef & StencilMask) CompFunc (StencilBufferValue & StencilMask)
```




```
StencilBufferValue
```



<span data-ttu-id="b8d8c-131">這是目前圖元的樣板緩衝區內容。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-131">is the contents of the stencil buffer for the current pixel.</span></span> <span data-ttu-id="b8d8c-132">這個程式碼範例會使用 & 符號 (&) 符號來表示位 AND 運算。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-132">This code example uses the ampersand (&) symbol to represent the bitwise AND operation.</span></span>


```
StencilMask
```



<span data-ttu-id="b8d8c-133">表示樣板遮罩的值，以及</span><span class="sxs-lookup"><span data-stu-id="b8d8c-133">represents the value of the stencil mask, and</span></span>


```
StencilRef
```



<span data-ttu-id="b8d8c-134">表示樣板參考值。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-134">represents the stencil reference value.</span></span>


```
CompFunc
```



<span data-ttu-id="b8d8c-135">這是比較函數。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-135">is the comparison function.</span></span>

<span data-ttu-id="b8d8c-136">如果樣板測試通過，目前像素會寫入目標表面，否則會略過。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-136">The current pixel is written to the target surface if the stencil test passes, and is ignored otherwise.</span></span> <span data-ttu-id="b8d8c-137">預設的比較行為是撰寫圖元，不論每位位運算的結果為何 (D3DCMP \_ 一律) 。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-137">The default comparison behavior is to write the pixel, no matter how each bitwise operation turns out (D3DCMP\_ALWAYS).</span></span> <span data-ttu-id="b8d8c-138">您可以變更此行為，方法是變更 D3DRS STENCILFUNC 轉譯 \_ 狀態的值，傳遞 [**D3DCMPFUNC**](./d3dcmpfunc.md) 列舉型別的成員，以識別所需的比較函數。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-138">You can change this behavior by changing the value of the D3DRS\_STENCILFUNC render state, passing a member of the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type to identify the desired comparison function.</span></span>

<span data-ttu-id="b8d8c-139">您的應用程式可自訂樣板緩衝區的作業。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-139">Your application can customize the operation of the stencil buffer.</span></span> <span data-ttu-id="b8d8c-140">它可以設定比較函式、樣板遮罩和樣板參考值。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-140">It can set the comparison function, the stencil mask, and the stencil reference value.</span></span> <span data-ttu-id="b8d8c-141">它也可以控制樣板測試通過或失敗時，Direct3D 採取的動作。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-141">It can also control the action that Direct3D takes when the stencil test passes or fails.</span></span> <span data-ttu-id="b8d8c-142">如需詳細資訊，請參閱 [ (Direct3D 9 的樣板緩衝區狀態) ](stencil-buffer-state.md)。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-142">For more information, see [Stencil Buffer State (Direct3D 9)](stencil-buffer-state.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b8d8c-143">範例</span><span class="sxs-lookup"><span data-stu-id="b8d8c-143">Examples</span></span>

<span data-ttu-id="b8d8c-144">下列程式碼範例示範如何設定樣板緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-144">The following code examples demonstrate setting up the stencil buffer.</span></span>


```
// Enable stencil testing
pDevice->SetRenderState(D3DRS_STENCILENABLE, TRUE);

// Specify the stencil comparison function
pDevice->SetRenderState(D3DRS_STENCILFUNC, D3DCMP_EQUAL);

// Set the comparison reference value
pDevice->SetRenderState(D3DRS_STENCILREF, 0);

//  Specify a stencil mask 
pDevice->SetRenderState(D3DRS_STENCILMASK, 0);
```



<span data-ttu-id="b8d8c-145">範本參考值預設為零。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-145">By default, the stencil reference value is zero.</span></span> <span data-ttu-id="b8d8c-146">任何整數值都有效。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-146">Any integer value is valid.</span></span> <span data-ttu-id="b8d8c-147">Direct3D 會執行樣板參考值的位 and，以及樣板測試之前的樣板遮罩值。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-147">Direct3D performs a bitwise AND of the stencil reference value and a stencil mask value before the stencil test.</span></span>

<span data-ttu-id="b8d8c-148">您可以根據樣板的比較，來控制要寫出的圖元資訊。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-148">You can control what pixel information is written out depending on the stencil comparison.</span></span>


```
// A write mask controls what is written
pDevice->SetRenderState(D3DRS_STENCILWRITEMASK, D3DSTENCILOP_KEEP);
// Specify when to write stencil data
pDevice->SetRenderState(D3DRS_STENCILFAIL, D3DSTENCILOP_KEEP);
```



<span data-ttu-id="b8d8c-149">您可以針對要寫入樣板緩衝區的值撰寫自己的公式，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="b8d8c-149">You can write your own formula for the value you want written into the stencil buffer as shown in the following example.</span></span>


```
NewStencilBufferValue = (StencilBufferValue & ~StencilWriteMask) | 
                        (StencilWriteMask & StencilOp(StencilBufferValue))
```



## <a name="related-topics"></a><span data-ttu-id="b8d8c-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="b8d8c-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8d8c-151">圖元管線</span><span class="sxs-lookup"><span data-stu-id="b8d8c-151">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 
