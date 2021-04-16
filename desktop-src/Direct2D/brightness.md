---
title: 亮度效果
description: 使用亮度效果來控制影像的亮度。
ms.assetid: 5088D4D4-DFC8-45D3-B1C3-D576742D931C
keywords:
- 亮度效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88dd9797aa125e7099ba4a706bac730a30715f6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104561538"
---
# <a name="brightness-effect"></a><span data-ttu-id="4e9cc-104">亮度效果</span><span class="sxs-lookup"><span data-stu-id="4e9cc-104">Brightness effect</span></span>

<span data-ttu-id="4e9cc-105">使用亮度效果來控制影像的亮度。</span><span class="sxs-lookup"><span data-stu-id="4e9cc-105">Use the brightness effect to control the brightness of the image.</span></span>

<span data-ttu-id="4e9cc-106">這項效果的 CLSID 是 CLSID \_ D2D1Brightness。</span><span class="sxs-lookup"><span data-stu-id="4e9cc-106">The CLSID for this effect is CLSID\_D2D1Brightness.</span></span>

-   [<span data-ttu-id="4e9cc-107">範例影像</span><span class="sxs-lookup"><span data-stu-id="4e9cc-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="4e9cc-108">效果屬性</span><span class="sxs-lookup"><span data-stu-id="4e9cc-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="4e9cc-109">輸出點陣圖</span><span class="sxs-lookup"><span data-stu-id="4e9cc-109">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="4e9cc-110">需求</span><span class="sxs-lookup"><span data-stu-id="4e9cc-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="4e9cc-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="4e9cc-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="4e9cc-112">範例影像</span><span class="sxs-lookup"><span data-stu-id="4e9cc-112">Example image</span></span>



| <span data-ttu-id="4e9cc-113">之前</span><span class="sxs-lookup"><span data-stu-id="4e9cc-113">Before</span></span>                                                      |
|-------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg)  |
| <span data-ttu-id="4e9cc-115">After</span><span class="sxs-lookup"><span data-stu-id="4e9cc-115">After</span></span>                                                       |
| ![轉換後的影像。](images/34-brightness.png) |



 


```C++
ComPtr<ID2D1Effect> brightnessEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Brightness, &brightnessEffect);

brightnessEffect->SetValue(D2D1_BRIGHTNESS_PROP_BLACK_POINT, D2D1::Vector2F(0.0f, 0.2f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(brightnessEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="4e9cc-117">效果屬性</span><span class="sxs-lookup"><span data-stu-id="4e9cc-117">Effect properties</span></span>



| <span data-ttu-id="4e9cc-118">屬性顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4e9cc-118">Property Display Name</span></span>                                                 | <span data-ttu-id="4e9cc-119">類型和預設值</span><span class="sxs-lookup"><span data-stu-id="4e9cc-119">Type and default value</span></span>                              | <span data-ttu-id="4e9cc-120">Description</span><span class="sxs-lookup"><span data-stu-id="4e9cc-120">Description</span></span>                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e9cc-121">WhitePoint</span><span class="sxs-lookup"><span data-stu-id="4e9cc-121">WhitePoint</span></span><br/> <span data-ttu-id="4e9cc-122">D2D1 \_ 亮度 \_ 主張的 \_ 白色 \_ 點</span><span class="sxs-lookup"><span data-stu-id="4e9cc-122">D2D1\_BRIGHTNESS\_PROP\_WHITE\_POINT</span></span><br/> | <span data-ttu-id="4e9cc-123">D2D1 \_ 向量 \_ 2f</span><span class="sxs-lookup"><span data-stu-id="4e9cc-123">D2D1\_VECTOR\_2F</span></span><br/> <span data-ttu-id="4e9cc-124">{1.0 f、1.0 f}</span><span class="sxs-lookup"><span data-stu-id="4e9cc-124">{1.0f, 1.0f}</span></span><br/> | <span data-ttu-id="4e9cc-125">亮度傳輸曲線的上半部。</span><span class="sxs-lookup"><span data-stu-id="4e9cc-125">The upper portion of the brightness transfer curve.</span></span> <span data-ttu-id="4e9cc-126">白色點會調整影像最亮部分的外觀。</span><span class="sxs-lookup"><span data-stu-id="4e9cc-126">The white point adjusts the appearance of the brighter portions of the image.</span></span> <span data-ttu-id="4e9cc-127">此屬性適用于 x 值和 y 值（依該順序）。</span><span class="sxs-lookup"><span data-stu-id="4e9cc-127">This property is for both the x value and the y value, in that order.</span></span> <span data-ttu-id="4e9cc-128">這個屬性的每個值都介於0和1（含）之間。</span><span class="sxs-lookup"><span data-stu-id="4e9cc-128">Each of the values of this property are between 0 and 1, inclusive.</span></span> |
| <span data-ttu-id="4e9cc-129">BlackPoint</span><span class="sxs-lookup"><span data-stu-id="4e9cc-129">BlackPoint</span></span><br/> <span data-ttu-id="4e9cc-130">D2D1 \_ 亮度 \_ 的 \_ 黑色 \_ 點</span><span class="sxs-lookup"><span data-stu-id="4e9cc-130">D2D1\_BRIGHTNESS\_PROP\_BLACK\_POINT</span></span><br/> | <span data-ttu-id="4e9cc-131">D2D1 \_ 向量 \_ 2f</span><span class="sxs-lookup"><span data-stu-id="4e9cc-131">D2D1\_VECTOR\_2F</span></span><br/> <span data-ttu-id="4e9cc-132">{0.0 f，0.0 f}</span><span class="sxs-lookup"><span data-stu-id="4e9cc-132">{0.0f, 0.0f}</span></span><br/> | <span data-ttu-id="4e9cc-133">亮度轉印曲線的下半部。</span><span class="sxs-lookup"><span data-stu-id="4e9cc-133">The lower portion of the brightness transfer curve.</span></span> <span data-ttu-id="4e9cc-134">黑色點會調整影像較暗部分的外觀。</span><span class="sxs-lookup"><span data-stu-id="4e9cc-134">The black point adjusts the appearance of the darker portions of the image.</span></span> <span data-ttu-id="4e9cc-135">此屬性適用于 x 值和 y 值（依該順序）。</span><span class="sxs-lookup"><span data-stu-id="4e9cc-135">This property is for both the x value and the y value, in that order.</span></span> <span data-ttu-id="4e9cc-136">這個屬性的每個值都介於0和1（含）之間。</span><span class="sxs-lookup"><span data-stu-id="4e9cc-136">Each of the values of this property are between 0 and 1, inclusive.</span></span>   |



 

<span data-ttu-id="4e9cc-137">這種效果會使用指定的白色和黑色點來產生用來調整點陣圖的傳送函數。</span><span class="sxs-lookup"><span data-stu-id="4e9cc-137">This effect uses the specified white and black points to generate a transfer function used to adjust the bitmap.</span></span> <span data-ttu-id="4e9cc-138">下一個方程式描述傳送函式。</span><span class="sxs-lookup"><span data-stu-id="4e9cc-138">The next equation describes the transfer function.</span></span> <span data-ttu-id="4e9cc-139">輸入濃度的定義介於0和1之間。</span><span class="sxs-lookup"><span data-stu-id="4e9cc-139">The input intensities are defined between 0 and 1.</span></span>

![亮度演算法](images/brightness-formula1.png)

<span data-ttu-id="4e9cc-141">效果演算法會執行建立傳送函式的方程式。</span><span class="sxs-lookup"><span data-stu-id="4e9cc-141">The effect algorithm implements an equation that creates the transfer function.</span></span> <span data-ttu-id="4e9cc-142">我們會使用此函數來調整影像圖元。</span><span class="sxs-lookup"><span data-stu-id="4e9cc-142">We use this function to adjust the image pixels.</span></span> <span data-ttu-id="4e9cc-143">黑色點和白色點的 x 和 y 值是兩個維度中連接來形成轉換的座標。</span><span class="sxs-lookup"><span data-stu-id="4e9cc-143">The x and y values of the black point and the white point are the coordinates in two dimensions that are connected to form the transform.</span></span> <span data-ttu-id="4e9cc-144">最終輸出方程式的每個部分：</span><span class="sxs-lookup"><span data-stu-id="4e9cc-144">Each part of the final output equation:</span></span>

1.  <span data-ttu-id="4e9cc-145">使用這個方程式，將影像資料從線性空間轉換成非線性空間：</span><span class="sxs-lookup"><span data-stu-id="4e9cc-145">Converts the image data from linear space to non-linear space using this equation:</span></span>![helper 函式1](images/brightness-formula2.png)

2.  <span data-ttu-id="4e9cc-147">根據下列值調整影像：</span><span class="sxs-lookup"><span data-stu-id="4e9cc-147">Adjusts the image according to these values:</span></span>
    -   <span data-ttu-id="4e9cc-148">*輸入* 是從0到1的輸入影像圖元濃度值。</span><span class="sxs-lookup"><span data-stu-id="4e9cc-148">*input* is the input image pixel intensity values from 0 to 1.</span></span>

    -   <span data-ttu-id="4e9cc-149">*(x，y) 亮色* 圖元濃度的轉換曲線位置。</span><span class="sxs-lookup"><span data-stu-id="4e9cc-149">*White Pt. (x, y)* the location of the transform curve for brighter pixel intensities.</span></span>

    -   <span data-ttu-id="4e9cc-150">*黑色的 (x，y)* 是變暗圖元濃度的轉換曲線位置。</span><span class="sxs-lookup"><span data-stu-id="4e9cc-150">*Black Pt. (x, y)* is the location of the transform curve for dimmer pixel intensities.</span></span>

3.  <span data-ttu-id="4e9cc-151">使用這個方程式，將影像資料轉換回線性空間：</span><span class="sxs-lookup"><span data-stu-id="4e9cc-151">Converts the image data back to linear space using this equation:</span></span> ![helper 函數2](images/brightness-formula3.png)

<span data-ttu-id="4e9cc-153">最後的輸出方程式和元件部分如下所示。</span><span class="sxs-lookup"><span data-stu-id="4e9cc-153">The final output equation and the component parts are shown here.</span></span>

![亮度調整的完整計算](images/brightness-formula4.png)

## <a name="output-bitmap"></a><span data-ttu-id="4e9cc-155">輸出點陣圖</span><span class="sxs-lookup"><span data-stu-id="4e9cc-155">Output bitmap</span></span>

<span data-ttu-id="4e9cc-156">輸出點陣圖大小與輸入點陣圖大小相同。</span><span class="sxs-lookup"><span data-stu-id="4e9cc-156">The output bitmap size is the same as the input bitmap size.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e9cc-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="4e9cc-157">Requirements</span></span>



| <span data-ttu-id="4e9cc-158">需求</span><span class="sxs-lookup"><span data-stu-id="4e9cc-158">Requirement</span></span> | <span data-ttu-id="4e9cc-159">值</span><span class="sxs-lookup"><span data-stu-id="4e9cc-159">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4e9cc-160">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4e9cc-160">Minimum supported client</span></span> | <span data-ttu-id="4e9cc-161">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4e9cc-161">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="4e9cc-162">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4e9cc-162">Minimum supported server</span></span> | <span data-ttu-id="4e9cc-163">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4e9cc-163">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="4e9cc-164">標頭</span><span class="sxs-lookup"><span data-stu-id="4e9cc-164">Header</span></span>                   | <span data-ttu-id="4e9cc-165">d2d1effects。h</span><span class="sxs-lookup"><span data-stu-id="4e9cc-165">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="4e9cc-166">程式庫</span><span class="sxs-lookup"><span data-stu-id="4e9cc-166">Library</span></span>                  | <span data-ttu-id="4e9cc-167">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="4e9cc-167">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="4e9cc-168">相關主題</span><span class="sxs-lookup"><span data-stu-id="4e9cc-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e9cc-169">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="4e9cc-169">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

