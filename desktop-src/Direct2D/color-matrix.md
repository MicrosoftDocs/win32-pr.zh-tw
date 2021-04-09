---
title: 色彩矩陣效果
description: 使用色彩矩陣效果來改變點陣圖的 RGBA 值。
ms.assetid: 093EEEF1-8C38-414E-8261-58A6C3DD930D
keywords:
- 色彩矩陣效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1078b1858bc68396546e1036c717e01acb1069c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024972"
---
# <a name="color-matrix-effect"></a><span data-ttu-id="136ea-104">色彩矩陣效果</span><span class="sxs-lookup"><span data-stu-id="136ea-104">Color matrix effect</span></span>

<span data-ttu-id="136ea-105">使用色彩矩陣效果來改變點陣圖的 RGBA 值。</span><span class="sxs-lookup"><span data-stu-id="136ea-105">Use the color matrix effect to alter the RGBA values of a bitmap.</span></span>

<span data-ttu-id="136ea-106">您可以使用此效果：</span><span class="sxs-lookup"><span data-stu-id="136ea-106">You can use this effect to:</span></span>

-   <span data-ttu-id="136ea-107">從影像中移除色彩通道。</span><span class="sxs-lookup"><span data-stu-id="136ea-107">Remove a color channel from an image.</span></span>
-   <span data-ttu-id="136ea-108">減少影像中的色彩。</span><span class="sxs-lookup"><span data-stu-id="136ea-108">Reduce the color in an image.</span></span>
-   <span data-ttu-id="136ea-109">交換色彩通道。</span><span class="sxs-lookup"><span data-stu-id="136ea-109">Swap color channels.</span></span>
-   <span data-ttu-id="136ea-110">結合色彩通道。</span><span class="sxs-lookup"><span data-stu-id="136ea-110">Combine color channels.</span></span>

<span data-ttu-id="136ea-111">許多內建效果都是色彩矩陣的特製化，已針對效果的預期用途進行優化。</span><span class="sxs-lookup"><span data-stu-id="136ea-111">Many built-in effects are specializations of color matrix that are optimized for the intended use of the effects.</span></span> <span data-ttu-id="136ea-112">範例包括 [飽和度](saturation.md)、 [色調旋轉](hue-rotate.md)、 [棕褐色](sepia-effect.md)和 [溫度和色調](temperature-and-tint-effect.md)。</span><span class="sxs-lookup"><span data-stu-id="136ea-112">Examples include [saturation](saturation.md), [hue rotate](hue-rotate.md), [sepia](sepia-effect.md), and [temperature and tint](temperature-and-tint-effect.md).</span></span>

<span data-ttu-id="136ea-113">這項效果的 CLSID 是 CLSID \_ D2D1ColorMatrix。</span><span class="sxs-lookup"><span data-stu-id="136ea-113">The CLSID for this effect is CLSID\_D2D1ColorMatrix.</span></span>

-   [<span data-ttu-id="136ea-114">範例影像</span><span class="sxs-lookup"><span data-stu-id="136ea-114">Example image</span></span>](#example-image)
-   [<span data-ttu-id="136ea-115">效果屬性</span><span class="sxs-lookup"><span data-stu-id="136ea-115">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="136ea-116">Alpha 模式</span><span class="sxs-lookup"><span data-stu-id="136ea-116">Alpha modes</span></span>](#alpha-modes)
-   [<span data-ttu-id="136ea-117">需求</span><span class="sxs-lookup"><span data-stu-id="136ea-117">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="136ea-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="136ea-118">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="136ea-119">範例影像</span><span class="sxs-lookup"><span data-stu-id="136ea-119">Example image</span></span>

<span data-ttu-id="136ea-120">此處的範例會顯示交換紅色和藍色通道之色彩矩陣效果的輸入和輸出影像。</span><span class="sxs-lookup"><span data-stu-id="136ea-120">The example here shows the input and output images of the color matrix effect that swaps the red and blue channels.</span></span>



| <span data-ttu-id="136ea-121">之前</span><span class="sxs-lookup"><span data-stu-id="136ea-121">Before</span></span>                                                       |
|--------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg)   |
| <span data-ttu-id="136ea-123">After</span><span class="sxs-lookup"><span data-stu-id="136ea-123">After</span></span>                                                        |
| ![轉換後的影像。](images/15-colormatrix.png) |



 


```C++
ComPtr<ID2D1Effect> colorMatrixEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ColorMatrix, &colorMatrixEffect);

colorMatrixEffect->SetInput(0, bitmap);
D2D1_MATRIX_5X4_F matrix = D2D1::Matrix5x4F(0, 0, 1, 0,   0, 1, 0, 0,   1, 0, 0, 0,   0, 0, 0, 1,   0, 0, 0, 0);
colorMatrixEffect->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(colorMatrixEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="136ea-125">此效果會將影像的 RGBA 值乘以此方程式所示的5x4、資料行主要矩陣。</span><span class="sxs-lookup"><span data-stu-id="136ea-125">This effect multiplies the RGBA values of the image by a 5x4, column major matrix as shown in this equation.</span></span>

![範例矩陣定義。](images/color-matrix-formula.png)

<span data-ttu-id="136ea-127">此效果適用于直接和預乘的 Alpha 影像。</span><span class="sxs-lookup"><span data-stu-id="136ea-127">This effect works on straight and premultiplied alpha images.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="136ea-128">效果屬性</span><span class="sxs-lookup"><span data-stu-id="136ea-128">Effect properties</span></span>



| <span data-ttu-id="136ea-129">顯示名稱和索引列舉</span><span class="sxs-lookup"><span data-stu-id="136ea-129">Display name and index enumeration</span></span>                                       | <span data-ttu-id="136ea-130">Description</span><span class="sxs-lookup"><span data-stu-id="136ea-130">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="136ea-131">ColorMatrix</span><span class="sxs-lookup"><span data-stu-id="136ea-131">ColorMatrix</span></span><br/> <span data-ttu-id="136ea-132">D2D1 \_ COLORMATRIX \_ 的 \_ 色彩 \_ 矩陣</span><span class="sxs-lookup"><span data-stu-id="136ea-132">D2D1\_COLORMATRIX\_PROP\_COLOR\_MATRIX</span></span><br/> | <span data-ttu-id="136ea-133">Float 值的5x4 矩陣。</span><span class="sxs-lookup"><span data-stu-id="136ea-133">A 5x4 matrix of float values.</span></span> <span data-ttu-id="136ea-134">矩陣中的元素未系結，而且沒有單位。</span><span class="sxs-lookup"><span data-stu-id="136ea-134">The elements in the matrix are not bounded and are unitless.</span></span><br/> <span data-ttu-id="136ea-135">預設值為識別矩陣。</span><span class="sxs-lookup"><span data-stu-id="136ea-135">The default is the identity matrix.</span></span><br/> <span data-ttu-id="136ea-136">此類型為 D2D1 \_ 矩陣 \_ 5X4 \_ F。</span><span class="sxs-lookup"><span data-stu-id="136ea-136">The type is D2D1\_MATRIX\_5X4\_F.</span></span><br/> <span data-ttu-id="136ea-137">預設值為 Matrix5x4F (1、0、0、0、0、1、0、0、0、0、1、0、0、0、0、1、0、0、0、0) 。</span><span class="sxs-lookup"><span data-stu-id="136ea-137">The default value is Matrix5x4F(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0).</span></span> <br/>                                                                                                                                                                                                                        |
| <span data-ttu-id="136ea-138">AlphaMode</span><span class="sxs-lookup"><span data-stu-id="136ea-138">AlphaMode</span></span><br/> <span data-ttu-id="136ea-139">D2D1 \_ COLORMATRIX \_ 的 \_ ALPHA \_ 模式</span><span class="sxs-lookup"><span data-stu-id="136ea-139">D2D1\_COLORMATRIX\_PROP\_ALPHA\_MODE</span></span><br/>     | <span data-ttu-id="136ea-140">輸出的 Alpha 模式。</span><span class="sxs-lookup"><span data-stu-id="136ea-140">The alpha mode of the output.</span></span> <span data-ttu-id="136ea-141">如需詳細資訊，請參閱 [Alpha 模式](#alpha-modes) 。</span><span class="sxs-lookup"><span data-stu-id="136ea-141">See [Alpha modes](#alpha-modes) for more info.</span></span> <br/> <span data-ttu-id="136ea-142">此類型為 D2D1 \_ COLORMATRIX \_ ALPHA \_ 模式。</span><span class="sxs-lookup"><span data-stu-id="136ea-142">The type is D2D1\_COLORMATRIX\_ALPHA\_MODE.</span></span><br/> <span data-ttu-id="136ea-143">預設值是預乘的 D2D1 \_ COLORMATRIX \_ ALPHA \_ 模式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="136ea-143">The default value is D2D1\_COLORMATRIX\_ALPHA\_MODE\_PREMULTIPLIED.</span></span><br/>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="136ea-144">ClampOutput</span><span class="sxs-lookup"><span data-stu-id="136ea-144">ClampOutput</span></span><br/> <span data-ttu-id="136ea-145">D2D1 COLORMATRIX 的一種 \_ \_ \_ 夾具 \_ 輸出</span><span class="sxs-lookup"><span data-stu-id="136ea-145">D2D1\_COLORMATRIX\_PROP\_CLAMP\_OUTPUT</span></span><br/> | <span data-ttu-id="136ea-146">效果在效果之前個色彩值是否會將值傳遞給圖形中的下一個效果。</span><span class="sxs-lookup"><span data-stu-id="136ea-146">Whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.</span></span> <span data-ttu-id="136ea-147">效果會在 premultiplies Alpha 之前個值。</span><span class="sxs-lookup"><span data-stu-id="136ea-147">The effect clamps the values before it premultiplies the alpha .</span></span><br/> <span data-ttu-id="136ea-148">如果您將此設定為 TRUE，效果會將值設為夾具。</span><span class="sxs-lookup"><span data-stu-id="136ea-148">If you set this to TRUE the effect will clamp the values.</span></span> <span data-ttu-id="136ea-149">如果您將此值設定為 FALSE，效果將不會顯示色彩值，但其他效果和輸出介面可能會在這些值的精確度不夠高時，將這些值設定為夾具。</span><span class="sxs-lookup"><span data-stu-id="136ea-149">If you set this to FALSE, the effect will not clamp the color values, but other effects and the output surface may clamp the values if they are not of high enough precision.</span></span><br/> <span data-ttu-id="136ea-150">此類型為 BOOL。</span><span class="sxs-lookup"><span data-stu-id="136ea-150">The type is BOOL.</span></span><br/> <span data-ttu-id="136ea-151">預設值為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="136ea-151">The default value is FALSE.</span></span><br/> |



 

## <a name="alpha-modes"></a><span data-ttu-id="136ea-152">Alpha 模式</span><span class="sxs-lookup"><span data-stu-id="136ea-152">Alpha modes</span></span>



| <span data-ttu-id="136ea-153">Name</span><span class="sxs-lookup"><span data-stu-id="136ea-153">Name</span></span>                                          | <span data-ttu-id="136ea-154">描述</span><span class="sxs-lookup"><span data-stu-id="136ea-154">Description</span></span>                                                                                               |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="136ea-155">預 \_ 乘的 D2D1 COLORMATRIX \_ ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="136ea-155">D2D1\_COLORMATRIX\_ALPHA\_MODE\_PREMULTIPLIED</span></span> | <span data-ttu-id="136ea-156">此效果會取消 premultiplies 輸入、套用色彩矩陣，以及 premultiplies 輸出。</span><span class="sxs-lookup"><span data-stu-id="136ea-156">The effect un-premultiplies the input, applies the color matrix, and premultiplies the output.</span></span><br/> |
| <span data-ttu-id="136ea-157">D2D1 \_ COLORMATRIX \_ ALPHA \_ 模式 \_ 直接</span><span class="sxs-lookup"><span data-stu-id="136ea-157">D2D1\_COLORMATRIX\_ALPHA\_MODE\_STRAIGHT</span></span>      | <span data-ttu-id="136ea-158">效果會將色彩矩陣直接套用至輸入，而且不會 premultiply 輸出。</span><span class="sxs-lookup"><span data-stu-id="136ea-158">The effect applies the color matrix directly to the input, and doesn't premultiply the output.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="136ea-159">規格需求</span><span class="sxs-lookup"><span data-stu-id="136ea-159">Requirements</span></span>



| <span data-ttu-id="136ea-160">需求</span><span class="sxs-lookup"><span data-stu-id="136ea-160">Requirement</span></span> | <span data-ttu-id="136ea-161">值</span><span class="sxs-lookup"><span data-stu-id="136ea-161">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="136ea-162">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="136ea-162">Minimum supported client</span></span> | <span data-ttu-id="136ea-163">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="136ea-163">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="136ea-164">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="136ea-164">Minimum supported server</span></span> | <span data-ttu-id="136ea-165">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="136ea-165">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="136ea-166">標頭</span><span class="sxs-lookup"><span data-stu-id="136ea-166">Header</span></span>                   | <span data-ttu-id="136ea-167">d2d1effects。h</span><span class="sxs-lookup"><span data-stu-id="136ea-167">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="136ea-168">程式庫</span><span class="sxs-lookup"><span data-stu-id="136ea-168">Library</span></span>                  | <span data-ttu-id="136ea-169">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="136ea-169">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="136ea-170">相關主題</span><span class="sxs-lookup"><span data-stu-id="136ea-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="136ea-171">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="136ea-171">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

