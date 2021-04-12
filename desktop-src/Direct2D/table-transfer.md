---
title: 資料表傳送效果
description: 使用表格傳輸效果，以使用從插即您提供的值清單來建立的傳送函式，來對應影像的色彩濃度。
ms.assetid: FB426909-3C91-4709-9E3A-E45C7AE345A3
keywords:
- 資料表傳送效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d590e7f232ac3d4cecd434786353dfc5b8ea80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465332"
---
# <a name="table-transfer-effect"></a><span data-ttu-id="f311b-104">資料表傳送效果</span><span class="sxs-lookup"><span data-stu-id="f311b-104">Table transfer effect</span></span>

<span data-ttu-id="f311b-105">使用表格傳輸效果，以使用從插即您提供的值清單來建立的傳送函式，來對應影像的色彩濃度。</span><span class="sxs-lookup"><span data-stu-id="f311b-105">Use the table transfer effect to map the color intensities of an image using a transfer function created from interpolating a list of values you provide.</span></span>

<span data-ttu-id="f311b-106">這項效果的 CLSID 是 CLSID \_ D2D1TableTransfer。</span><span class="sxs-lookup"><span data-stu-id="f311b-106">The CLSID for this effect is CLSID\_D2D1TableTransfer.</span></span>

-   [<span data-ttu-id="f311b-107">範例影像</span><span class="sxs-lookup"><span data-stu-id="f311b-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="f311b-108">效果屬性</span><span class="sxs-lookup"><span data-stu-id="f311b-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="f311b-109">需求</span><span class="sxs-lookup"><span data-stu-id="f311b-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="f311b-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="f311b-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="f311b-111">範例影像</span><span class="sxs-lookup"><span data-stu-id="f311b-111">Example image</span></span>

<span data-ttu-id="f311b-112">此處的影像顯示資料表傳送效果的輸入和輸出。</span><span class="sxs-lookup"><span data-stu-id="f311b-112">The image here shows the input and output of the table transfer effect.</span></span>



| <span data-ttu-id="f311b-113">之前</span><span class="sxs-lookup"><span data-stu-id="f311b-113">Before</span></span>                                                         |
|----------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg)     |
| <span data-ttu-id="f311b-115">After</span><span class="sxs-lookup"><span data-stu-id="f311b-115">After</span></span>                                                          |
| ![轉換後的影像。](images/11-tabletransfer.png) |



 


```C++
ComPtr<ID2D1Effect> tableTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1TableTransfer, &tableTransferEffect);

tableTransferEffect->SetInput(0, bitmap);

float table[2] = {0.75f, 1.0f};
tableTransferEffect->SetValue(D2D1_TABLETRANSFER_PROP_BLUE_TABLE, table);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(tableTransferEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="f311b-117">傳送函式是根據輸入的清單 V = (V0、V1、V2、V3、V？</span><span class="sxs-lookup"><span data-stu-id="f311b-117">The transfer function is based on a list of inputs V=(V0,V1,V2,V3, V?</span></span> <span data-ttu-id="f311b-118">，V<sub>n</sub>) 其中 N 是元素數目-1。</span><span class="sxs-lookup"><span data-stu-id="f311b-118">,V<sub>N</sub>) where N is the number of elements - 1.</span></span>

<span data-ttu-id="f311b-119">輸入圖元濃度以 C 表示。輸出圖元濃度，C 可以使用方程式來計算。</span><span class="sxs-lookup"><span data-stu-id="f311b-119">The input pixel intensity is represented as C. The output pixel intensity, C  can be calculated with the equation.</span></span>

<span data-ttu-id="f311b-120">若為值 C，請挑選值 k，例如： k/N = C < (k + 1) /N</span><span class="sxs-lookup"><span data-stu-id="f311b-120">For a value C, pick a value k, such that: k/N = C < (k+1)/N</span></span>

<span data-ttu-id="f311b-121">輸出 C 使用下列方程式計算： C ' = V？</span><span class="sxs-lookup"><span data-stu-id="f311b-121">The output C  is calculated using the following equation: C' = V?</span></span> <span data-ttu-id="f311b-122">+ (C-k/N) \* n \* (V???單?</span><span class="sxs-lookup"><span data-stu-id="f311b-122">+ (C -  k/N) \* N \* (V???1?</span></span> <span data-ttu-id="f311b-123">-V？ ) </span><span class="sxs-lookup"><span data-stu-id="f311b-123">- V?)</span></span>

<span data-ttu-id="f311b-124">此效果適用于直接和預乘的 Alpha 影像。</span><span class="sxs-lookup"><span data-stu-id="f311b-124">This effect works on straight and premultiplied alpha images.</span></span> <span data-ttu-id="f311b-125">效果會輸出預乘的 Alpha 點陣圖。</span><span class="sxs-lookup"><span data-stu-id="f311b-125">The effect outputs premultiplied alpha bitmaps.</span></span>

<span data-ttu-id="f311b-126">以下是當 table 屬性設定為時，資料表傳送函式的圖表看起來的樣子 `[0.0, 0.25, 1.0]` 。</span><span class="sxs-lookup"><span data-stu-id="f311b-126">Here is what the graph of table transfer function looks like if the table property is set to `[0.0, 0.25, 1.0]`.</span></span>

![表格傳送函數的圖元濃度圖形。](images/table-transfer-graph.png)

## <a name="effect-properties"></a><span data-ttu-id="f311b-128">效果屬性</span><span class="sxs-lookup"><span data-stu-id="f311b-128">Effect properties</span></span>

> [!Note]  
> <span data-ttu-id="f311b-129">資料表傳輸屬性的所有通道值都不會有任何限制，而且最小值為0.0 和1.0。</span><span class="sxs-lookup"><span data-stu-id="f311b-129">The values of all channels of the table transfer properties are unitless and have a minimum of 0.0 and a maximum 1.0.</span></span>

 



| <span data-ttu-id="f311b-130">顯示名稱和索引列舉</span><span class="sxs-lookup"><span data-stu-id="f311b-130">Display name and index enumeration</span></span>                                           | <span data-ttu-id="f311b-131">類型和預設值</span><span class="sxs-lookup"><span data-stu-id="f311b-131">Type and default value</span></span>                       | <span data-ttu-id="f311b-132">Description</span><span class="sxs-lookup"><span data-stu-id="f311b-132">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f311b-133">RedTable</span><span class="sxs-lookup"><span data-stu-id="f311b-133">RedTable</span></span><br/> <span data-ttu-id="f311b-134">D2D1 \_ TABLETRANSFER \_ 的 \_ 成分紅色 \_ 資料表</span><span class="sxs-lookup"><span data-stu-id="f311b-134">D2D1\_TABLETRANSFER\_PROP\_RED\_TABLE</span></span><br/>         | <span data-ttu-id="f311b-135">浮動\[\]</span><span class="sxs-lookup"><span data-stu-id="f311b-135">FLOAT\[\]</span></span><br/> <span data-ttu-id="f311b-136">{0.0 f、1.0 f}</span><span class="sxs-lookup"><span data-stu-id="f311b-136">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="f311b-137">值的清單，用來定義 Red 通道的傳送函式。</span><span class="sxs-lookup"><span data-stu-id="f311b-137">The list of values used to define the transfer function for the Red channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="f311b-138">RedDisable</span><span class="sxs-lookup"><span data-stu-id="f311b-138">RedDisable</span></span><br/> <span data-ttu-id="f311b-139">D2D1 \_ TABLETRANSFER \_ 的 \_ RED \_ DISABLE</span><span class="sxs-lookup"><span data-stu-id="f311b-139">D2D1\_TABLETRANSFER\_PROP\_RED\_DISABLE</span></span><br/>     | <span data-ttu-id="f311b-140">BOOL</span><span class="sxs-lookup"><span data-stu-id="f311b-140">BOOL</span></span><br/> <span data-ttu-id="f311b-141">FALSE</span><span class="sxs-lookup"><span data-stu-id="f311b-141">FALSE</span></span><br/>             | <span data-ttu-id="f311b-142">如果您將此設定為 TRUE，則效果不會將傳送函式套用至紅色通道。</span><span class="sxs-lookup"><span data-stu-id="f311b-142">If you set this to TRUE the effect does not apply the transfer function to the Red channel.</span></span> <span data-ttu-id="f311b-143">如果您將此設定為 FALSE，則會將 RedTableTransfer 函式套用至紅色通道。</span><span class="sxs-lookup"><span data-stu-id="f311b-143">If you set this to FALSE it applies the RedTableTransfer function to the Red channel.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="f311b-144">GreenTable</span><span class="sxs-lookup"><span data-stu-id="f311b-144">GreenTable</span></span><br/> <span data-ttu-id="f311b-145">D2D1 \_ TABLETRANSFER \_ 的 \_ \_ 表表表</span><span class="sxs-lookup"><span data-stu-id="f311b-145">D2D1\_TABLETRANSFER\_PROP\_GREEN\_TABLE</span></span><br/>     | <span data-ttu-id="f311b-146">浮動\[\]</span><span class="sxs-lookup"><span data-stu-id="f311b-146">FLOAT\[\]</span></span><br/> <span data-ttu-id="f311b-147">{0.0 f、1.0 f}</span><span class="sxs-lookup"><span data-stu-id="f311b-147">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="f311b-148">值的清單，用來定義綠色通道的傳送函數。</span><span class="sxs-lookup"><span data-stu-id="f311b-148">The list of values used to define the transfer function for the Green channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="f311b-149">GreenDisable</span><span class="sxs-lookup"><span data-stu-id="f311b-149">GreenDisable</span></span><br/> <span data-ttu-id="f311b-150">D2D1 \_ TABLETRANSFER，a \_ \_ 綠 \_ DISABLE</span><span class="sxs-lookup"><span data-stu-id="f311b-150">D2D1\_TABLETRANSFER\_PROP\_GREEN\_DISABLE</span></span><br/> | <span data-ttu-id="f311b-151">BOOL</span><span class="sxs-lookup"><span data-stu-id="f311b-151">BOOL</span></span><br/> <span data-ttu-id="f311b-152">FALSE</span><span class="sxs-lookup"><span data-stu-id="f311b-152">FALSE</span></span><br/>             | <span data-ttu-id="f311b-153">如果您將此設定為 TRUE，則效果不會將傳送函式套用至綠色通道。</span><span class="sxs-lookup"><span data-stu-id="f311b-153">If you set this to TRUE the effect does not apply the transfer function to the Green channel.</span></span> <span data-ttu-id="f311b-154">如果您將此設定為 FALSE，則會將 GreenTableTransfer 函式套用至綠色通道。</span><span class="sxs-lookup"><span data-stu-id="f311b-154">If you set this to FALSE it applies the GreenTableTransfer function to the Green channel.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="f311b-155">BlueTable</span><span class="sxs-lookup"><span data-stu-id="f311b-155">BlueTable</span></span><br/> <span data-ttu-id="f311b-156">D2D1 \_ TABLETRANSFER \_ 的 \_ BLUE \_ 資料表</span><span class="sxs-lookup"><span data-stu-id="f311b-156">D2D1\_TABLETRANSFER\_PROP\_BLUE\_TABLE</span></span><br/>       | <span data-ttu-id="f311b-157">浮動\[\]</span><span class="sxs-lookup"><span data-stu-id="f311b-157">FLOAT\[\]</span></span><br/> <span data-ttu-id="f311b-158">{0.0 f、1.0 f}</span><span class="sxs-lookup"><span data-stu-id="f311b-158">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="f311b-159">值的清單，用來定義藍色通道的傳送函數。</span><span class="sxs-lookup"><span data-stu-id="f311b-159">The list of values used to define the transfer function for the Blue channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="f311b-160">BlueDisable</span><span class="sxs-lookup"><span data-stu-id="f311b-160">BlueDisable</span></span><br/> <span data-ttu-id="f311b-161">D2D1 \_ TABLETRANSFER \_ 的 \_ BLUE \_ DISABLE</span><span class="sxs-lookup"><span data-stu-id="f311b-161">D2D1\_TABLETRANSFER\_PROP\_BLUE\_DISABLE</span></span><br/>   | <span data-ttu-id="f311b-162">BOOL</span><span class="sxs-lookup"><span data-stu-id="f311b-162">BOOL</span></span><br/> <span data-ttu-id="f311b-163">FALSE</span><span class="sxs-lookup"><span data-stu-id="f311b-163">FALSE</span></span><br/>             | <span data-ttu-id="f311b-164">如果您將此設定為 TRUE，則效果不會將傳送函式套用至藍色通道。</span><span class="sxs-lookup"><span data-stu-id="f311b-164">If you set this to TRUE the effect does not apply the transfer function to the Blue channel.</span></span> <span data-ttu-id="f311b-165">如果您將此設定為 FALSE，則會將 BlueTableTransfer 函式套用至藍色通道。</span><span class="sxs-lookup"><span data-stu-id="f311b-165">If you set this to FALSE it applies the BlueTableTransfer function to the Blue channel.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="f311b-166">AlphaTable</span><span class="sxs-lookup"><span data-stu-id="f311b-166">AlphaTable</span></span><br/> <span data-ttu-id="f311b-167">D2D1 \_ 資料表 \_ 傳送 \_ 的 \_ ALPHA \_ 表</span><span class="sxs-lookup"><span data-stu-id="f311b-167">D2D1\_TABLE\_TRANSFER\_PROP\_ALPHA\_TABLE</span></span><br/>   | <span data-ttu-id="f311b-168">浮動\[\]</span><span class="sxs-lookup"><span data-stu-id="f311b-168">FLOAT\[\]</span></span><br/> <span data-ttu-id="f311b-169">{0.0 f、1.0 f}</span><span class="sxs-lookup"><span data-stu-id="f311b-169">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="f311b-170">值的清單，用來定義 Alpha 色板的傳送函數。</span><span class="sxs-lookup"><span data-stu-id="f311b-170">The list of values used to define the transfer function for the Alpha channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="f311b-171">AlphaDisable</span><span class="sxs-lookup"><span data-stu-id="f311b-171">AlphaDisable</span></span><br/> <span data-ttu-id="f311b-172">D2D1 \_ TABLETRANSFER \_ 的 \_ ALPHA \_ 停用</span><span class="sxs-lookup"><span data-stu-id="f311b-172">D2D1\_TABLETRANSFER\_PROP\_ALPHA\_DISABLE</span></span><br/> | <span data-ttu-id="f311b-173">BOOL</span><span class="sxs-lookup"><span data-stu-id="f311b-173">BOOL</span></span><br/> <span data-ttu-id="f311b-174">FALSE</span><span class="sxs-lookup"><span data-stu-id="f311b-174">FALSE</span></span><br/>             | <span data-ttu-id="f311b-175">如果您將此設定為 TRUE，則效果不會將傳送函式套用至 Alpha 通道。</span><span class="sxs-lookup"><span data-stu-id="f311b-175">If you set this to TRUE the effect does not apply the transfer function to the Alpha channel.</span></span> <span data-ttu-id="f311b-176">如果您將此設定為 FALSE，則會將 AlphaTableTransfer 函式套用至 Alpha 色板。</span><span class="sxs-lookup"><span data-stu-id="f311b-176">If you set this to FALSE it applies the AlphaTableTransfer function to the Alpha channel.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="f311b-177">ClampOutput</span><span class="sxs-lookup"><span data-stu-id="f311b-177">ClampOutput</span></span><br/> <span data-ttu-id="f311b-178">D2D1 TABLETRANSFER 的一種 \_ \_ \_ 夾具 \_ 輸出</span><span class="sxs-lookup"><span data-stu-id="f311b-178">D2D1\_TABLETRANSFER\_PROP\_CLAMP\_OUTPUT</span></span><br/>   | <span data-ttu-id="f311b-179">BOOL</span><span class="sxs-lookup"><span data-stu-id="f311b-179">BOOL</span></span><br/> <span data-ttu-id="f311b-180">FALSE</span><span class="sxs-lookup"><span data-stu-id="f311b-180">FALSE</span></span><br/>             | <span data-ttu-id="f311b-181">效果在效果之前個色彩值是否會將值傳遞給圖形中的下一個效果。</span><span class="sxs-lookup"><span data-stu-id="f311b-181">Whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.</span></span> <span data-ttu-id="f311b-182">效果會在 premultiplies Alpha 之前個值。</span><span class="sxs-lookup"><span data-stu-id="f311b-182">The effect clamps the values before it premultiplies the alpha .</span></span><br/> <span data-ttu-id="f311b-183">如果您將此設定為 TRUE，效果會將值設為夾具。</span><span class="sxs-lookup"><span data-stu-id="f311b-183">If you set this to TRUE the effect will clamp the values.</span></span> <span data-ttu-id="f311b-184">如果您將此值設定為 FALSE，效果將不會顯示色彩值，但其他效果和輸出介面可能會在這些值的精確度不夠高時，將這些值設定為夾具。</span><span class="sxs-lookup"><span data-stu-id="f311b-184">If you set this to FALSE, the effect will not clamp the color values, but other effects and the output surface may clamp the values if they are not of high enough precision.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f311b-185">規格需求</span><span class="sxs-lookup"><span data-stu-id="f311b-185">Requirements</span></span>



| <span data-ttu-id="f311b-186">需求</span><span class="sxs-lookup"><span data-stu-id="f311b-186">Requirement</span></span> | <span data-ttu-id="f311b-187">值</span><span class="sxs-lookup"><span data-stu-id="f311b-187">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f311b-188">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f311b-188">Minimum supported client</span></span> | <span data-ttu-id="f311b-189">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f311b-189">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="f311b-190">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f311b-190">Minimum supported server</span></span> | <span data-ttu-id="f311b-191">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f311b-191">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="f311b-192">標頭</span><span class="sxs-lookup"><span data-stu-id="f311b-192">Header</span></span>                   | <span data-ttu-id="f311b-193">d2d1effects。h</span><span class="sxs-lookup"><span data-stu-id="f311b-193">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="f311b-194">程式庫</span><span class="sxs-lookup"><span data-stu-id="f311b-194">Library</span></span>                  | <span data-ttu-id="f311b-195">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="f311b-195">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="f311b-196">相關主題</span><span class="sxs-lookup"><span data-stu-id="f311b-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f311b-197">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="f311b-197">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

