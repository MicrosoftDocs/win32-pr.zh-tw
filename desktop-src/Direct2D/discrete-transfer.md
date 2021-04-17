---
title: 離散傳送效果
description: 使用離散傳輸效果，利用從您提供的值清單建立的步驟轉移函式，來對應影像的色彩濃度。
ms.assetid: 5A612002-2B1D-4FC3-B364-AACD9FD44BEC
keywords:
- 離散傳送效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c05ef08f9ddf053eaa686cb0f88d4183194d9e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104559176"
---
# <a name="discrete-transfer-effect"></a><span data-ttu-id="95075-104">離散傳送效果</span><span class="sxs-lookup"><span data-stu-id="95075-104">Discrete transfer effect</span></span>

<span data-ttu-id="95075-105">使用離散傳輸效果，利用從您提供的值清單建立的步驟轉移函式，來對應影像的色彩濃度。</span><span class="sxs-lookup"><span data-stu-id="95075-105">Use the discrete transfer effect to map the color intensities of an image using a step transfer function created from a list of values you provide.</span></span>

<span data-ttu-id="95075-106">這項效果的 CLSID 是 CLSID \_ D2D1DiscreteTransfer。</span><span class="sxs-lookup"><span data-stu-id="95075-106">The CLSID for this effect is CLSID\_D2D1DiscreteTransfer.</span></span>

-   [<span data-ttu-id="95075-107">範例影像</span><span class="sxs-lookup"><span data-stu-id="95075-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="95075-108">效果屬性</span><span class="sxs-lookup"><span data-stu-id="95075-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="95075-109">需求</span><span class="sxs-lookup"><span data-stu-id="95075-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="95075-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="95075-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="95075-111">範例影像</span><span class="sxs-lookup"><span data-stu-id="95075-111">Example image</span></span>

<span data-ttu-id="95075-112">此處的影像顯示離散傳送效果的輸入和輸出。</span><span class="sxs-lookup"><span data-stu-id="95075-112">The image here shows the input and output of the discrete transfer effect.</span></span>



| <span data-ttu-id="95075-113">之前</span><span class="sxs-lookup"><span data-stu-id="95075-113">Before</span></span>                                                            |
|-------------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg)        |
| <span data-ttu-id="95075-115">After</span><span class="sxs-lookup"><span data-stu-id="95075-115">After</span></span>                                                             |
| ![轉換後的影像。](images/12-discretetransfer.png) |



 


```C++
ComPtr<ID2D1Effect> discreteTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DiscreteTransfer, &discreteTransferEffect);

discreteTransferEffect->SetInput(0, bitmap);

float table[3] = {0.0f, 0.5f, 1.0f};
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_RED_TABLE, table);
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_GREEN_TABLE, table);
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_BLUE_TABLE, table);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(discreteTransferEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="95075-117">傳送函式是以輸入清單為基礎： V = (V0、V1、V2、V3、V？</span><span class="sxs-lookup"><span data-stu-id="95075-117">The transfer function is based on the list of inputs: V=(V0,V1,V2,V3,V?</span></span> <span data-ttu-id="95075-118">，V<sub>n</sub>) 其中 N 是元素數目-1。</span><span class="sxs-lookup"><span data-stu-id="95075-118">,V<sub>N</sub>) where N is the number of elements - 1.</span></span>

<span data-ttu-id="95075-119">輸入圖元濃度以 C 表示。輸出圖元強度（C）會以方程式計算：</span><span class="sxs-lookup"><span data-stu-id="95075-119">The input pixel intensity is represented as C. The output pixel intensity, C  is calculated with the equation:</span></span>

<span data-ttu-id="95075-120">若為值 C，請挑選值 k，如下所示：</span><span class="sxs-lookup"><span data-stu-id="95075-120">For a value C, pick a value k, such that:</span></span>

![處理常式的公式。](images/discrete-transfer1.png)

<span data-ttu-id="95075-122">輸出 C 可以使用方程式： C ' = V 來計算：</span><span class="sxs-lookup"><span data-stu-id="95075-122">The output C  can be calculated using the equation: C' = V?</span></span>

<span data-ttu-id="95075-123">此效果適用于直接和預乘的 Alpha 影像。</span><span class="sxs-lookup"><span data-stu-id="95075-123">This effect works on straight and premultiplied alpha images.</span></span> <span data-ttu-id="95075-124">效果會輸出預乘的 Alpha 點陣圖。</span><span class="sxs-lookup"><span data-stu-id="95075-124">The effect outputs premultiplied alpha bitmaps.</span></span>

<span data-ttu-id="95075-125">以下是當輸入為時，離散傳送函式的圖表看起來的樣子 `[0.25, 0.5, 0.75, 1.0]` 。</span><span class="sxs-lookup"><span data-stu-id="95075-125">Here is what the graph of discrete transfer function looks like if the inputs are `[0.25, 0.5, 0.75, 1.0]`.</span></span>

![離散傳送函數的圖元濃度圖形。](images/discrete-transfer-graph.png)

## <a name="effect-properties"></a><span data-ttu-id="95075-127">效果屬性</span><span class="sxs-lookup"><span data-stu-id="95075-127">Effect properties</span></span>

> [!Note]  
> <span data-ttu-id="95075-128">離散傳輸屬性的所有通道值都不會用到，而且最小值為0.0 和1.0。</span><span class="sxs-lookup"><span data-stu-id="95075-128">The values of all channels of the discrete transfer properties are unitless and have a minimum of 0.0 and a maximum 1.0.</span></span>

 



| <span data-ttu-id="95075-129">顯示名稱和索引列舉</span><span class="sxs-lookup"><span data-stu-id="95075-129">Display name and index enumeration</span></span>                                              | <span data-ttu-id="95075-130">類型和預設值</span><span class="sxs-lookup"><span data-stu-id="95075-130">Type and default value</span></span>                       | <span data-ttu-id="95075-131">Description</span><span class="sxs-lookup"><span data-stu-id="95075-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95075-132">RedTable</span><span class="sxs-lookup"><span data-stu-id="95075-132">RedTable</span></span><br/> <span data-ttu-id="95075-133">D2D1 \_ DISCRETETRANSFER \_ 的 \_ 成分紅色 \_ 資料表</span><span class="sxs-lookup"><span data-stu-id="95075-133">D2D1\_DISCRETETRANSFER\_PROP\_RED\_TABLE</span></span><br/>         | <span data-ttu-id="95075-134">浮動\[\]</span><span class="sxs-lookup"><span data-stu-id="95075-134">FLOAT\[\]</span></span><br/> <span data-ttu-id="95075-135">{0.0 f、1.0 f}</span><span class="sxs-lookup"><span data-stu-id="95075-135">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="95075-136">值的清單，用來定義 Red 通道的傳送函式。</span><span class="sxs-lookup"><span data-stu-id="95075-136">The list of values used to define the transfer function for the Red channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="95075-137">RedDisable</span><span class="sxs-lookup"><span data-stu-id="95075-137">RedDisable</span></span><br/> <span data-ttu-id="95075-138">D2D1 \_ DISCRETETRANSFER \_ 的 \_ RED \_ DISABLE</span><span class="sxs-lookup"><span data-stu-id="95075-138">D2D1\_DISCRETETRANSFER\_PROP\_RED\_DISABLE</span></span><br/>     | <span data-ttu-id="95075-139">BOOL</span><span class="sxs-lookup"><span data-stu-id="95075-139">BOOL</span></span><br/> <span data-ttu-id="95075-140">FALSE</span><span class="sxs-lookup"><span data-stu-id="95075-140">FALSE</span></span><br/>             | <span data-ttu-id="95075-141">如果您將此設定為 TRUE，則效果不會將傳送函式套用至紅色通道。</span><span class="sxs-lookup"><span data-stu-id="95075-141">If you set this to TRUE the effect does not apply the transfer function to the Red channel.</span></span> <span data-ttu-id="95075-142">如果您將此設定為 FALSE，效果會將 RedDiscreteTransfer 函式套用至紅色通道。</span><span class="sxs-lookup"><span data-stu-id="95075-142">If you set this to FALSE the effect applies the RedDiscreteTransfer function to the Red channel.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="95075-143">GreenTable</span><span class="sxs-lookup"><span data-stu-id="95075-143">GreenTable</span></span><br/> <span data-ttu-id="95075-144">D2D1 \_ DISCRETETRANSFER \_ 的 \_ \_ 表表表</span><span class="sxs-lookup"><span data-stu-id="95075-144">D2D1\_DISCRETETRANSFER\_PROP\_GREEN\_TABLE</span></span><br/>     | <span data-ttu-id="95075-145">浮動\[\]</span><span class="sxs-lookup"><span data-stu-id="95075-145">FLOAT\[\]</span></span><br/> <span data-ttu-id="95075-146">{0.0 f、1.0 f}</span><span class="sxs-lookup"><span data-stu-id="95075-146">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="95075-147">值的清單，這些值會定義綠色通道的傳送函數。</span><span class="sxs-lookup"><span data-stu-id="95075-147">The list of values that define the transfer function for the Green channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="95075-148">GreenDisable</span><span class="sxs-lookup"><span data-stu-id="95075-148">GreenDisable</span></span><br/> <span data-ttu-id="95075-149">D2D1 \_ DISCRETETRANSFER，a \_ \_ 綠 \_ DISABLE</span><span class="sxs-lookup"><span data-stu-id="95075-149">D2D1\_DISCRETETRANSFER\_PROP\_GREEN\_DISABLE</span></span><br/> | <span data-ttu-id="95075-150">BOOL</span><span class="sxs-lookup"><span data-stu-id="95075-150">BOOL</span></span><br/> <span data-ttu-id="95075-151">FALSE</span><span class="sxs-lookup"><span data-stu-id="95075-151">FALSE</span></span><br/>             | <span data-ttu-id="95075-152">如果您將此設定為 TRUE，則效果不會將傳送函式套用至綠色通道。</span><span class="sxs-lookup"><span data-stu-id="95075-152">If you set this to TRUE the effect does not apply the transfer function to the Green channel.</span></span> <span data-ttu-id="95075-153">如果您將此設定為 FALSE，效果會將 GreenDiscreteTransfer 函式套用至綠色通道。</span><span class="sxs-lookup"><span data-stu-id="95075-153">If you set this to FALSE the effect applies the GreenDiscreteTransfer function to the Green channel.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="95075-154">BlueTable</span><span class="sxs-lookup"><span data-stu-id="95075-154">BlueTable</span></span><br/> <span data-ttu-id="95075-155">D2D1 \_ DISCRETETRANSFER \_ 的 \_ BLUE \_ 資料表</span><span class="sxs-lookup"><span data-stu-id="95075-155">D2D1\_DISCRETETRANSFER\_PROP\_BLUE\_TABLE</span></span><br/>       | <span data-ttu-id="95075-156">浮動\[\]</span><span class="sxs-lookup"><span data-stu-id="95075-156">FLOAT\[\]</span></span><br/> <span data-ttu-id="95075-157">{0.0 f、1.0 f}</span><span class="sxs-lookup"><span data-stu-id="95075-157">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="95075-158">值的清單，這些值會定義藍色通道的傳送函數。</span><span class="sxs-lookup"><span data-stu-id="95075-158">The list of values that define the transfer function for the Blue channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="95075-159">BlueDisable</span><span class="sxs-lookup"><span data-stu-id="95075-159">BlueDisable</span></span><br/> <span data-ttu-id="95075-160">D2D1 \_ DISCRETETRANSFER \_ 的 \_ BLUE \_ DISABLE</span><span class="sxs-lookup"><span data-stu-id="95075-160">D2D1\_DISCRETETRANSFER\_PROP\_BLUE\_DISABLE</span></span><br/>   | <span data-ttu-id="95075-161">BOOL</span><span class="sxs-lookup"><span data-stu-id="95075-161">BOOL</span></span><br/> <span data-ttu-id="95075-162">FALSE</span><span class="sxs-lookup"><span data-stu-id="95075-162">FALSE</span></span><br/>             | <span data-ttu-id="95075-163">如果您將此設定為 TRUE，則效果不會將傳送函式套用至藍色通道。</span><span class="sxs-lookup"><span data-stu-id="95075-163">If you set this to TRUE the effect does not apply the transfer function to the Blue channel.</span></span> <span data-ttu-id="95075-164">如果您將此設定為 FALSE，效果會將 BlueDiscreteTransfer 函式套用至藍色通道。</span><span class="sxs-lookup"><span data-stu-id="95075-164">If you set this to FALSE the effect applies the BlueDiscreteTransfer function to the Blue channel.</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="95075-165">AlphaTable</span><span class="sxs-lookup"><span data-stu-id="95075-165">AlphaTable</span></span><br/> <span data-ttu-id="95075-166">D2D1 \_ DISCRETETRANSFER \_ 的 \_ ALPHA \_ 表</span><span class="sxs-lookup"><span data-stu-id="95075-166">D2D1\_DISCRETETRANSFER\_PROP\_ALPHA\_TABLE</span></span><br/>     | <span data-ttu-id="95075-167">浮動\[\]</span><span class="sxs-lookup"><span data-stu-id="95075-167">FLOAT\[\]</span></span><br/> <span data-ttu-id="95075-168">{0.0 f、1.0 f}</span><span class="sxs-lookup"><span data-stu-id="95075-168">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="95075-169">值的清單，這些值會定義 Alpha 通道的傳送函式。</span><span class="sxs-lookup"><span data-stu-id="95075-169">The list of values that define the transfer function for the Alpha channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="95075-170">AlphaDisable</span><span class="sxs-lookup"><span data-stu-id="95075-170">AlphaDisable</span></span><br/> <span data-ttu-id="95075-171">D2D1 \_ DISCRETETRANSFER \_ 的 \_ ALPHA \_ 停用</span><span class="sxs-lookup"><span data-stu-id="95075-171">D2D1\_DISCRETETRANSFER\_PROP\_ALPHA\_DISABLE</span></span><br/> | <span data-ttu-id="95075-172">BOOL</span><span class="sxs-lookup"><span data-stu-id="95075-172">BOOL</span></span><br/> <span data-ttu-id="95075-173">FALSE</span><span class="sxs-lookup"><span data-stu-id="95075-173">FALSE</span></span><br/>             | <span data-ttu-id="95075-174">如果您將此設定為 TRUE，則效果不會將傳送函式套用至 Alpha 通道。</span><span class="sxs-lookup"><span data-stu-id="95075-174">If you set this to TRUE the effect does not apply the transfer function to the Alpha channel.</span></span> <span data-ttu-id="95075-175">如果您將此設定為 FALSE，效果會將 AlphaDiscreteTransfer 函式套用至 Alpha 色板。</span><span class="sxs-lookup"><span data-stu-id="95075-175">If you set this to FALSE the effect applies the AlphaDiscreteTransfer function to the Alpha channel.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="95075-176">ClampOutput</span><span class="sxs-lookup"><span data-stu-id="95075-176">ClampOutput</span></span><br/> <span data-ttu-id="95075-177">D2D1 DISCRETETRANSFER 的一種 \_ \_ \_ 夾具 \_ 輸出</span><span class="sxs-lookup"><span data-stu-id="95075-177">D2D1\_DISCRETETRANSFER\_PROP\_CLAMP\_OUTPUT</span></span><br/>   | <span data-ttu-id="95075-178">BOOL</span><span class="sxs-lookup"><span data-stu-id="95075-178">BOOL</span></span><br/> <span data-ttu-id="95075-179">FALSE</span><span class="sxs-lookup"><span data-stu-id="95075-179">FALSE</span></span><br/>             | <span data-ttu-id="95075-180">效果在效果之前個色彩值是否會將值傳遞給圖形中的下一個效果。</span><span class="sxs-lookup"><span data-stu-id="95075-180">Whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.</span></span> <span data-ttu-id="95075-181">效果會在 premultiplies Alpha 之前個值。</span><span class="sxs-lookup"><span data-stu-id="95075-181">The effect clamps the values before it premultiplies the alpha.</span></span><br/> <span data-ttu-id="95075-182">如果您將此設定為 TRUE，效果會將值設為夾具。</span><span class="sxs-lookup"><span data-stu-id="95075-182">If you set this to TRUE the effect will clamp the values.</span></span> <span data-ttu-id="95075-183">如果您將此值設定為 FALSE，效果將不會顯示色彩值，但其他效果和輸出介面可能會在這些值的精確度不夠高時，將這些值設定為夾具。</span><span class="sxs-lookup"><span data-stu-id="95075-183">If you set this to FALSE, the effect will not clamp the color values, but other effects and the output surface may clamp the values if they are not of high enough precision.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="95075-184">規格需求</span><span class="sxs-lookup"><span data-stu-id="95075-184">Requirements</span></span>



| <span data-ttu-id="95075-185">需求</span><span class="sxs-lookup"><span data-stu-id="95075-185">Requirement</span></span> | <span data-ttu-id="95075-186">值</span><span class="sxs-lookup"><span data-stu-id="95075-186">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="95075-187">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="95075-187">Minimum supported client</span></span> | <span data-ttu-id="95075-188">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95075-188">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="95075-189">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="95075-189">Minimum supported server</span></span> | <span data-ttu-id="95075-190">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95075-190">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="95075-191">標頭</span><span class="sxs-lookup"><span data-stu-id="95075-191">Header</span></span>                   | <span data-ttu-id="95075-192">d2d1effects。h</span><span class="sxs-lookup"><span data-stu-id="95075-192">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="95075-193">程式庫</span><span class="sxs-lookup"><span data-stu-id="95075-193">Library</span></span>                  | <span data-ttu-id="95075-194">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="95075-194">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="95075-195">相關主題</span><span class="sxs-lookup"><span data-stu-id="95075-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95075-196">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="95075-196">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

