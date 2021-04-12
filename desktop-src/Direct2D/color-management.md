---
title: 色彩管理效果
description: 使用色彩管理效果，將影像從一個 ICC (國際色彩協會) 色彩設定檔轉換成另一個。 效果會根據 ICC 規格來轉換影像。
ms.assetid: 7351C4B4-F289-4236-BB42-1B3BD8753248
keywords:
- 色彩管理效果
ms.topic: article
ms.date: 02/05/2019
ms.openlocfilehash: 5f3783132e0e2af511a99fd8c44d5f899e577a3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384498"
---
# <a name="color-management-effect"></a><span data-ttu-id="61c26-105">色彩管理效果</span><span class="sxs-lookup"><span data-stu-id="61c26-105">Color management effect</span></span>

<span data-ttu-id="61c26-106">使用色彩管理效果，將影像從一個 ICC (國際色彩協會) 色彩設定檔轉換成另一個。</span><span class="sxs-lookup"><span data-stu-id="61c26-106">Use the color management effect to transform an image from one ICC (International Color Consortium) color profile to another.</span></span> <span data-ttu-id="61c26-107">效果會根據 [ICC 規格](https://www.color.org)來轉換影像。</span><span class="sxs-lookup"><span data-stu-id="61c26-107">The effect transforms the image according to the [ICC specification](https://www.color.org).</span></span>

<span data-ttu-id="61c26-108">這項效果的 CLSID 是 CLSID \_ D2D1ColorManagement。</span><span class="sxs-lookup"><span data-stu-id="61c26-108">The CLSID for this effect is CLSID\_D2D1ColorManagement.</span></span>

- [<span data-ttu-id="61c26-109">效果屬性</span><span class="sxs-lookup"><span data-stu-id="61c26-109">Effect properties</span></span>](#effect-properties)
- [<span data-ttu-id="61c26-110">轉譯意圖模式</span><span class="sxs-lookup"><span data-stu-id="61c26-110">Rendering intent modes</span></span>](#rendering-intent-modes)
- [<span data-ttu-id="61c26-111">輸入影像 Alpha 模式</span><span class="sxs-lookup"><span data-stu-id="61c26-111">Input image alpha modes</span></span>](#input-image-alpha-modes)
- [<span data-ttu-id="61c26-112">符合 ICC 規格</span><span class="sxs-lookup"><span data-stu-id="61c26-112">Compliance with ICC specification</span></span>](#compliance-with-icc-specification)
- [<span data-ttu-id="61c26-113">Alpha 通道行為</span><span class="sxs-lookup"><span data-stu-id="61c26-113">Alpha channel behavior</span></span>](#alpha-channel-behavior)
- [<span data-ttu-id="61c26-114">品質模式</span><span class="sxs-lookup"><span data-stu-id="61c26-114">Quality modes</span></span>](#quality-modes)
- [<span data-ttu-id="61c26-115">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="61c26-115">Sample code</span></span>](#sample-code)
- [<span data-ttu-id="61c26-116">需求</span><span class="sxs-lookup"><span data-stu-id="61c26-116">Requirements</span></span>](#requirements)
- [<span data-ttu-id="61c26-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="61c26-117">Related topics</span></span>](#related-topics)

## <a name="effect-properties"></a><span data-ttu-id="61c26-118">效果屬性</span><span class="sxs-lookup"><span data-stu-id="61c26-118">Effect properties</span></span>

| <span data-ttu-id="61c26-119">顯示名稱和索引列舉</span><span class="sxs-lookup"><span data-stu-id="61c26-119">Display name and index enumeration</span></span> | <span data-ttu-id="61c26-120">Description</span><span class="sxs-lookup"><span data-stu-id="61c26-120">Description</span></span> |
|-|-|
| <span data-ttu-id="61c26-121">SourceContext</span><span class="sxs-lookup"><span data-stu-id="61c26-121">SourceContext</span></span><br/> <span data-ttu-id="61c26-122">D2D1 \_ COLORMANAGEMENT \_ 的 \_ \_ 內容來源色彩 \_ 內容</span><span class="sxs-lookup"><span data-stu-id="61c26-122">D2D1\_COLORMANAGEMENT\_PROP\_SOURCE\_COLOR\_CONTEXT</span></span><br/> | <span data-ttu-id="61c26-123">來源色彩空間資訊。</span><span class="sxs-lookup"><span data-stu-id="61c26-123">The source color space information.</span></span> <span data-ttu-id="61c26-124">此類型為 [**ID2D1ColorCoNtext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)。</span><span class="sxs-lookup"><span data-stu-id="61c26-124">The type is [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext).</span></span><br/> <span data-ttu-id="61c26-125">預設值是 NULL。</span><span class="sxs-lookup"><span data-stu-id="61c26-125">The default value is NULL.</span></span><br/> |
| <span data-ttu-id="61c26-126">SourceIntent</span><span class="sxs-lookup"><span data-stu-id="61c26-126">SourceIntent</span></span><br/> <span data-ttu-id="61c26-127">D2D1 \_ COLORMANAGEMENT \_ 的 \_ 版本 \_ 轉譯 \_ 意圖</span><span class="sxs-lookup"><span data-stu-id="61c26-127">D2D1\_COLORMANAGEMENT\_PROP\_SOURCE\_RENDERING\_INTENT</span></span><br/> | <span data-ttu-id="61c26-128">要使用哪一種 ICC 轉譯意圖。</span><span class="sxs-lookup"><span data-stu-id="61c26-128">Which ICC rendering intent to use.</span></span> <span data-ttu-id="61c26-129">此類型為 D2D1 \_ COLORMANAGEMENT \_ 轉譯 \_ 意圖。</span><span class="sxs-lookup"><span data-stu-id="61c26-129">The type is D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT.</span></span><br/> <span data-ttu-id="61c26-130">預設值為 D2D1 \_ COLORMANAGEMENT 轉譯 \_ 意圖 \_ 可 \_ 感知。</span><span class="sxs-lookup"><span data-stu-id="61c26-130">The default value is D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_PERCEPTUAL.</span></span><br/> |
| <span data-ttu-id="61c26-131">DestinationCoNtext</span><span class="sxs-lookup"><span data-stu-id="61c26-131">DestinationContext</span></span><br/> <span data-ttu-id="61c26-132">D2D1 \_ COLORMANAGEMENT \_ 的 \_ \_ 內容目的地色彩 \_ 內容</span><span class="sxs-lookup"><span data-stu-id="61c26-132">D2D1\_COLORMANAGEMENT\_PROP\_DESTINATION\_COLOR\_CONTEXT</span></span><br/> | <span data-ttu-id="61c26-133">目的地色彩空間資訊。</span><span class="sxs-lookup"><span data-stu-id="61c26-133">The destination color space information.</span></span> <span data-ttu-id="61c26-134">此類型為 [**ID2D1ColorCoNtext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)。</span><span class="sxs-lookup"><span data-stu-id="61c26-134">The type is [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext).</span></span><br/> <span data-ttu-id="61c26-135">預設值是 NULL。</span><span class="sxs-lookup"><span data-stu-id="61c26-135">The default value is NULL.</span></span><br/> |
| <span data-ttu-id="61c26-136">DestinationIntent</span><span class="sxs-lookup"><span data-stu-id="61c26-136">DestinationIntent</span></span><br/> <span data-ttu-id="61c26-137">D2D1 \_ COLORMANAGEMENT \_ 的 \_ \_ 外觀轉譯 \_ 意圖</span><span class="sxs-lookup"><span data-stu-id="61c26-137">D2D1\_COLORMANAGEMENT\_PROP\_DESTINATION\_RENDERING\_INTENT</span></span><br/> | <span data-ttu-id="61c26-138">要使用哪一種 ICC 轉譯意圖。</span><span class="sxs-lookup"><span data-stu-id="61c26-138">Which ICC rendering intent to use.</span></span> <span data-ttu-id="61c26-139">此類型為 D2D1 \_ COLORMANAGEMENT \_ 轉譯 \_ 意圖。</span><span class="sxs-lookup"><span data-stu-id="61c26-139">The type is D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT.</span></span><br/> <span data-ttu-id="61c26-140">預設值為 D2D1 \_ COLORMANAGEMENT 轉譯 \_ 意圖 \_ 可 \_ 感知。</span><span class="sxs-lookup"><span data-stu-id="61c26-140">The default value is D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_PERCEPTUAL.</span></span><br/> |
| <span data-ttu-id="61c26-141">AlphaMode</span><span class="sxs-lookup"><span data-stu-id="61c26-141">AlphaMode</span></span><br/> <span data-ttu-id="61c26-142">D2D1 \_ COLORMANAGEMENT \_ 的 \_ ALPHA \_ 模式</span><span class="sxs-lookup"><span data-stu-id="61c26-142">D2D1\_COLORMANAGEMENT\_PROP\_ALPHA\_MODE</span></span><br/> | <span data-ttu-id="61c26-143">如何解讀輸入影像中包含的 Alpha 資料。</span><span class="sxs-lookup"><span data-stu-id="61c26-143">How to interpret alpha data that is contained in the input image.</span></span> <span data-ttu-id="61c26-144">此類型為 D2D1 \_ COLORMANAGEMENT \_ ALPHA \_ 模式。</span><span class="sxs-lookup"><span data-stu-id="61c26-144">The type is D2D1\_COLORMANAGEMENT\_ALPHA\_MODE.</span></span><br/> <span data-ttu-id="61c26-145">預設值是預乘的 D2D1 \_ COLORMANAGEMENT \_ ALPHA \_ 模式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="61c26-145">The default value is D2D1\_COLORMANAGEMENT\_ALPHA\_MODE\_PREMULTIPLIED.</span></span><br/> |
| <span data-ttu-id="61c26-146">品質</span><span class="sxs-lookup"><span data-stu-id="61c26-146">Quality</span></span><br/> <span data-ttu-id="61c26-147">D2D1 \_ COLORMANAGEMENT \_ 的 \_ 品質</span><span class="sxs-lookup"><span data-stu-id="61c26-147">D2D1\_COLORMANAGEMENT\_PROP\_QUALITY</span></span><br/> | <span data-ttu-id="61c26-148">轉換的品質等級。</span><span class="sxs-lookup"><span data-stu-id="61c26-148">The quality level of the transform.</span></span> <span data-ttu-id="61c26-149">此類型為 D2D1 \_ COLORMANAGEMENT \_ QUALITY。</span><span class="sxs-lookup"><span data-stu-id="61c26-149">The type is D2D1\_COLORMANAGEMENT\_QUALITY.</span></span><br/> <span data-ttu-id="61c26-150">預設值為 D2D1 \_ COLORMANAGEMENT \_ QUALITY \_ NORMAL。</span><span class="sxs-lookup"><span data-stu-id="61c26-150">The default value is D2D1\_COLORMANAGEMENT\_QUALITY\_NORMAL.</span></span><br/> |

## <a name="rendering-intent-modes"></a><span data-ttu-id="61c26-151">轉譯意圖模式</span><span class="sxs-lookup"><span data-stu-id="61c26-151">Rendering intent modes</span></span>

| <span data-ttu-id="61c26-152">列舉型別</span><span class="sxs-lookup"><span data-stu-id="61c26-152">Enumeration</span></span> | <span data-ttu-id="61c26-153">描述</span><span class="sxs-lookup"><span data-stu-id="61c26-153">Description</span></span> |
|-|-|
| <span data-ttu-id="61c26-154">D2D1 \_ COLORMANAGEMENT \_ 轉譯 \_ 意圖的 \_ 視覺效果</span><span class="sxs-lookup"><span data-stu-id="61c26-154">D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_PERCEPTUAL</span></span> | <span data-ttu-id="61c26-155">效果會壓縮或展開影像的完整色彩範圍，以填滿裝置的色彩範圍，因此會保留灰色平衡，但不會保留色階的精確度。</span><span class="sxs-lookup"><span data-stu-id="61c26-155">The effect compresses or expands the full color gamut of the image to fill the color gamut of the device, so that gray balance is preserved but colorimetric accuracy may not be preserved.</span></span> |
| <span data-ttu-id="61c26-156">D2D1 \_ COLORMANAGEMENT \_ 轉譯 \_ 意圖 \_ 相對 \_ 色度</span><span class="sxs-lookup"><span data-stu-id="61c26-156">D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_RELATIVE\_COLORIMETRIC</span></span> | <span data-ttu-id="61c26-157">效果會以色調和亮度的可能費用，將色彩的色度保留在影像中。</span><span class="sxs-lookup"><span data-stu-id="61c26-157">The effect preserves the chroma of colors in the image at the possible expense of hue and lightness.</span></span> |
| <span data-ttu-id="61c26-158">D2D1 \_ COLORMANAGEMENT \_ 轉譯 \_ 意圖 \_ 飽和度</span><span class="sxs-lookup"><span data-stu-id="61c26-158">D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_SATURATION</span></span> | <span data-ttu-id="61c26-159">效果會調整輸出裝置呈現的色彩範圍超出最接近可用色彩的色彩。</span><span class="sxs-lookup"><span data-stu-id="61c26-159">The effect adjusts colors that fall outside the range of colors the output device renders to the closest color available.</span></span> <span data-ttu-id="61c26-160">它不會保留白色點。</span><span class="sxs-lookup"><span data-stu-id="61c26-160">It does not preserve the white point.</span></span> |
| <span data-ttu-id="61c26-161">D2D1 \_ COLORMANAGEMENT \_ 轉譯 \_ 意圖 \_ 絕對 \_ 色度</span><span class="sxs-lookup"><span data-stu-id="61c26-161">D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_ABSOLUTE\_COLORIMETRIC</span></span> | <span data-ttu-id="61c26-162">效果會調整在輸出裝置可轉譯為最接近可轉譯之色彩範圍之外的任何色彩。</span><span class="sxs-lookup"><span data-stu-id="61c26-162">The effect adjusts any colors that fall outside the range that the output device can render to the closest color that can be rendered.</span></span> <span data-ttu-id="61c26-163">效果不會變更其他色彩，並保留白色點。</span><span class="sxs-lookup"><span data-stu-id="61c26-163">The effect does not change the other colors and preserves the white point.</span></span> |

## <a name="input-image-alpha-modes"></a><span data-ttu-id="61c26-164">輸入影像 Alpha 模式</span><span class="sxs-lookup"><span data-stu-id="61c26-164">Input image alpha modes</span></span>

| <span data-ttu-id="61c26-165">列舉型別</span><span class="sxs-lookup"><span data-stu-id="61c26-165">Enumeration</span></span> | <span data-ttu-id="61c26-166">描述</span><span class="sxs-lookup"><span data-stu-id="61c26-166">Description</span></span> |
|-|-|
| <span data-ttu-id="61c26-167">預 \_ 乘的 D2D1 COLORMANAGEMENT \_ ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="61c26-167">D2D1\_COLORMANAGEMENT\_ALPHA\_MODE\_PREMULTIPLIED</span></span> | <span data-ttu-id="61c26-168">效果會假設 Alpha 模式為預乘。</span><span class="sxs-lookup"><span data-stu-id="61c26-168">The effect assumes the alpha mode is premultiplied.</span></span> |
| <span data-ttu-id="61c26-169">D2D1 \_ COLORMANAGEMENT \_ ALPHA \_ 模式 \_ 直接</span><span class="sxs-lookup"><span data-stu-id="61c26-169">D2D1\_COLORMANAGEMENT\_ALPHA\_MODE\_STRAIGHT</span></span> | <span data-ttu-id="61c26-170">效果會假設 Alpha 模式是直接的。</span><span class="sxs-lookup"><span data-stu-id="61c26-170">The effect assumes the alpha mode is straight.</span></span> |

## <a name="d2d1_gamma1_g2084-behavior-changes"></a><span data-ttu-id="61c26-171">D2D1_GAMMA1_G2084 行為變更</span><span class="sxs-lookup"><span data-stu-id="61c26-171">D2D1_GAMMA1_G2084 behavior changes</span></span>
    
<span data-ttu-id="61c26-172">如果您的應用程式使用 [D2D1_GAMMA1_G2084](/windows/desktop/api/d2d1_3/ne-d2d1_3-d2d1_gamma1) 空間，或是使用 2084 (可感知 Quantizer) 色彩空間的其中一個 [DXGI_COLOR_SPACE_TYPE](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) 列舉值，則應用程式打算使用 HDR 資料。</span><span class="sxs-lookup"><span data-stu-id="61c26-172">If your application uses the [D2D1_GAMMA1_G2084](/windows/desktop/api/d2d1_3/ne-d2d1_3-d2d1_gamma1) space, or one of the [DXGI_COLOR_SPACE_TYPE](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) enumeration values that use the SMPTE ST.2084 (Perceptual Quantizer) color space, then the application intends to work with HDR data.</span></span>

<span data-ttu-id="61c26-173">[**ID2D1DeviceCoNtext5：： CreateColorCoNtextFromSimpleColorProfile**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile__id2d1colorcontext1))和 [**ID2D1DeviceCoNtext5：： CreateColorCoNtextFromDxgiColorSpace**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace) api 不會考慮該情況;相反地，在 G2084 DeGamma 作業期間，會調整 HDR 內容以納入0-1 範圍。</span><span class="sxs-lookup"><span data-stu-id="61c26-173">The [**ID2D1DeviceContext5::CreateColorContextFromSimpleColorProfile**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile__id2d1colorcontext1)) and [**ID2D1DeviceContext5::CreateColorContextFromDxgiColorSpace**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace) APIs don't account for that; rather, the HDR content is scaled to fit in the 0-1 range during the G2084 DeGamma operation.</span></span>

<span data-ttu-id="61c26-174">實際上，在此 gamma 空間中編碼的內容會使用 10000 Nits 的參考 WhiteLevel，通常會在 CCCS 中表示為 10000/80 = 125.0。</span><span class="sxs-lookup"><span data-stu-id="61c26-174">In practice, content that is encoded in this gamma space uses a reference WhiteLevel of 10,000 Nits, which would normally be represented in CCCS as 10,000 / 80 = 125.0.</span></span> <span data-ttu-id="61c26-175">因此，為了更有效地加速您的應用程式，此 gamma 轉換最簡單，也就是將亮度調整為125的係數。</span><span class="sxs-lookup"><span data-stu-id="61c26-175">So, to better facilitate your app, it's simplest for this gamma conversion to also scale the luminance by a factor of 125.</span></span> <span data-ttu-id="61c26-176">從 Windows 10 版本 1809 (10.0;組建 17763) ，色彩管理效果的行為是套用此調整。</span><span class="sxs-lookup"><span data-stu-id="61c26-176">As of Windows 10, version 1809 (10.0; Build 17763), the behavior of the color management effect is such that it applies this scaling.</span></span> <span data-ttu-id="61c26-177">這表示，如同開發人員，您不需要將第二個 [白色層級調整效果](white-level-adjustment-effect.md) 套用至管線。</span><span class="sxs-lookup"><span data-stu-id="61c26-177">That means that you, as the developer, don't have to apply a second [White level adjustment effect](white-level-adjustment-effect.md) into the pipeline.</span></span>

## <a name="compliance-with-icc-specification"></a><span data-ttu-id="61c26-178">符合 ICC 規格</span><span class="sxs-lookup"><span data-stu-id="61c26-178">Compliance with ICC specification</span></span>

<span data-ttu-id="61c26-179">色彩管理效果與 ICC 4.3 規格相容，但有下列限制：</span><span class="sxs-lookup"><span data-stu-id="61c26-179">The color management effect is compliant with the ICC v4.3 specification, with these limitations:</span></span>

- <span data-ttu-id="61c26-180">效果支援1、3和4個通道色彩空間。</span><span class="sxs-lookup"><span data-stu-id="61c26-180">The effect supports 1, 3, and 4 channel color spaces.</span></span>
- <span data-ttu-id="61c26-181">效果不支援 ColorSpace 或命名色彩設定檔。</span><span class="sxs-lookup"><span data-stu-id="61c26-181">The effect doesn't support ColorSpace or Named Color profiles.</span></span>

## <a name="alpha-channel-behavior"></a><span data-ttu-id="61c26-182">Alpha 通道行為</span><span class="sxs-lookup"><span data-stu-id="61c26-182">Alpha channel behavior</span></span>

<span data-ttu-id="61c26-183">一般而言，如果來源影像中沒有任何 Alpha 資料，則效果會將 Alpha 設定為 1 (不透明) ，而且如果目的影像中沒有空間，則會捨棄 Alpha 資料。</span><span class="sxs-lookup"><span data-stu-id="61c26-183">In general, the effect sets alpha to 1 (opaque) if there is no alpha data in the source image and the alpha data is discarded if there is no room in the destination image.</span></span> <span data-ttu-id="61c26-184">此處的表格說明 Alpha 行為。</span><span class="sxs-lookup"><span data-stu-id="61c26-184">The table here describes the alpha behavior.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="61c26-185">來源 colorspace，像素格式</span><span class="sxs-lookup"><span data-stu-id="61c26-185">Source colorspace, pixel format</span></span></th>
<th><span data-ttu-id="61c26-186">目的地 colorspace，像素格式</span><span class="sxs-lookup"><span data-stu-id="61c26-186">Destination colorspace, pixel format</span></span></th>
<th><span data-ttu-id="61c26-187">Alpha 行為</span><span class="sxs-lookup"><span data-stu-id="61c26-187">Alpha behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="61c26-188">1個通道，R 像素格式 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="61c26-188">1 channel, R pixel format ${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="61c26-189">1個通道，R 像素格式</span><span class="sxs-lookup"><span data-stu-id="61c26-189">1 channel, R pixel format</span></span></td>
<td><span data-ttu-id="61c26-190"> (沒有任何 Alpha 資料) </span><span class="sxs-lookup"><span data-stu-id="61c26-190">(No alpha data)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61c26-191">1個通道，RGBA 像素格式</span><span class="sxs-lookup"><span data-stu-id="61c26-191">1 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="61c26-192">Alpha 資料設定為 1 (不透明) </span><span class="sxs-lookup"><span data-stu-id="61c26-192">Alpha data is set to 1 (opaque)</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="61c26-193">3通道，RGBA 像素格式</span><span class="sxs-lookup"><span data-stu-id="61c26-193">3 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="61c26-194">Alpha 資料設定為 1 (不透明) </span><span class="sxs-lookup"><span data-stu-id="61c26-194">Alpha data is set to 1 (opaque)</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="61c26-195">4通道，RGBA 像素格式</span><span class="sxs-lookup"><span data-stu-id="61c26-195">4 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="61c26-196"> (沒有任何 Alpha 資料) </span><span class="sxs-lookup"><span data-stu-id="61c26-196">(No alpha data)</span></span></td>

</tr>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="61c26-197">1個通道，RGBA 像素格式 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="61c26-197">1 channel, RGBA pixel format ${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="61c26-198">1個通道，R 像素格式</span><span class="sxs-lookup"><span data-stu-id="61c26-198">1 channel, R pixel format</span></span></td>
<td><span data-ttu-id="61c26-199">已捨棄 Alpha 資料</span><span class="sxs-lookup"><span data-stu-id="61c26-199">Alpha data is discarded</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61c26-200">1個通道，RGBA 像素格式</span><span class="sxs-lookup"><span data-stu-id="61c26-200">1 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="61c26-201">Alpha 資料的傳遞</span><span class="sxs-lookup"><span data-stu-id="61c26-201">Alpha data is passed through</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="61c26-202">3通道，RGBA 像素格式</span><span class="sxs-lookup"><span data-stu-id="61c26-202">3 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="61c26-203">Alpha 資料的傳遞</span><span class="sxs-lookup"><span data-stu-id="61c26-203">Alpha data is passed through</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="61c26-204">4通道，RGBA 像素格式</span><span class="sxs-lookup"><span data-stu-id="61c26-204">4 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="61c26-205">已捨棄 Alpha 資料</span><span class="sxs-lookup"><span data-stu-id="61c26-205">Alpha data is discarded</span></span></td>

</tr>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="61c26-206">3個通道，RGBA 像素格式 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="61c26-206">3 channel, RGBA pixel format ${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="61c26-207">1個通道，R 像素格式</span><span class="sxs-lookup"><span data-stu-id="61c26-207">1 channel, R pixel format</span></span></td>
<td><span data-ttu-id="61c26-208">已捨棄 Alpha 資料</span><span class="sxs-lookup"><span data-stu-id="61c26-208">Alpha data is discarded</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61c26-209">1個通道，RGBA 像素格式</span><span class="sxs-lookup"><span data-stu-id="61c26-209">1 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="61c26-210">Alpha 資料的傳遞</span><span class="sxs-lookup"><span data-stu-id="61c26-210">Alpha data is passed through</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="61c26-211">3通道，RGBA 像素格式</span><span class="sxs-lookup"><span data-stu-id="61c26-211">3 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="61c26-212">Alpha 資料的傳遞</span><span class="sxs-lookup"><span data-stu-id="61c26-212">Alpha data is passed through</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="61c26-213">4通道，RGBA 像素格式</span><span class="sxs-lookup"><span data-stu-id="61c26-213">4 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="61c26-214">已捨棄 Alpha 資料</span><span class="sxs-lookup"><span data-stu-id="61c26-214">Alpha data is discarded</span></span></td>

</tr>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="61c26-215">4個通道，RGBA 像素格式 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="61c26-215">4 channel, RGBA pixel format ${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="61c26-216">1個通道，R 像素格式</span><span class="sxs-lookup"><span data-stu-id="61c26-216">1 channel, R pixel format</span></span></td>
<td><span data-ttu-id="61c26-217"> (沒有任何 Alpha 資料) </span><span class="sxs-lookup"><span data-stu-id="61c26-217">(No alpha data)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61c26-218">1個通道，RGBA 像素格式</span><span class="sxs-lookup"><span data-stu-id="61c26-218">1 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="61c26-219">Alpha 資料設定為 1 (不透明) </span><span class="sxs-lookup"><span data-stu-id="61c26-219">Alpha data is set to 1 (opaque)</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="61c26-220">3通道，RGBA 像素格式</span><span class="sxs-lookup"><span data-stu-id="61c26-220">3 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="61c26-221">Alpha 資料設定為 1 (不透明) </span><span class="sxs-lookup"><span data-stu-id="61c26-221">Alpha data is set to 1 (opaque)</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="61c26-222">4通道，RGBA 像素格式</span><span class="sxs-lookup"><span data-stu-id="61c26-222">4 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="61c26-223"> (沒有任何 Alpha 資料) </span><span class="sxs-lookup"><span data-stu-id="61c26-223">(No alpha data)</span></span></td>

</tr>
</tbody>
</table>

## <a name="quality-modes"></a><span data-ttu-id="61c26-224">品質模式</span><span class="sxs-lookup"><span data-stu-id="61c26-224">Quality modes</span></span>

| <span data-ttu-id="61c26-225">[模式]</span><span class="sxs-lookup"><span data-stu-id="61c26-225">Mode</span></span> | <span data-ttu-id="61c26-226">描述</span><span class="sxs-lookup"><span data-stu-id="61c26-226">Description</span></span> |
|-|-|
| <span data-ttu-id="61c26-227">D2D1 \_ COLORMANAGEMENT \_ 品質 \_ 證明</span><span class="sxs-lookup"><span data-stu-id="61c26-227">D2D1\_COLORMANAGEMENT\_QUALITY\_PROOF</span></span> | <span data-ttu-id="61c26-228">最低品質模式。</span><span class="sxs-lookup"><span data-stu-id="61c26-228">The lowest quality mode.</span></span> <span data-ttu-id="61c26-229">此模式需要功能層級 9 \_ 1 或以上。</span><span class="sxs-lookup"><span data-stu-id="61c26-229">This mode requires feature level 9\_1 or above.</span></span> |
| <span data-ttu-id="61c26-230">D2D1 \_ COLORMANAGEMENT \_ 品質 \_ 正常</span><span class="sxs-lookup"><span data-stu-id="61c26-230">D2D1\_COLORMANAGEMENT\_QUALITY\_NORMAL</span></span> | <span data-ttu-id="61c26-231">標準品質模式。</span><span class="sxs-lookup"><span data-stu-id="61c26-231">Normal quality mode.</span></span> <span data-ttu-id="61c26-232">此模式需要功能層級 9 \_ 1 或以上。</span><span class="sxs-lookup"><span data-stu-id="61c26-232">This mode requires feature level 9\_1 or above.</span></span> |
| <span data-ttu-id="61c26-233">D2D1 \_ COLORMANAGEMENT \_ 品質 \_ 最佳</span><span class="sxs-lookup"><span data-stu-id="61c26-233">D2D1\_COLORMANAGEMENT\_QUALITY\_BEST</span></span> | <span data-ttu-id="61c26-234">最佳品質模式。</span><span class="sxs-lookup"><span data-stu-id="61c26-234">The best quality mode.</span></span> <span data-ttu-id="61c26-235">此模式需要功能層級 10 \_ 0 或以上，以及浮點精確度緩衝區。</span><span class="sxs-lookup"><span data-stu-id="61c26-235">This mode requires feature level 10\_0 or above, as well as floating point precision buffers.</span></span> <span data-ttu-id="61c26-236">此模式支援浮點精確度，以及在 ICC 4.3 規格中定義的延伸範圍。</span><span class="sxs-lookup"><span data-stu-id="61c26-236">This mode supports floating point precision as well as extended range as defined in the ICC v4.3 specification.</span></span> |

<span data-ttu-id="61c26-237">當應用程式要求的品質模式不受硬體支援時，色彩管理效果會失敗。</span><span class="sxs-lookup"><span data-stu-id="61c26-237">The color management effect fails when drawing if the application requests a quality mode that is not supported by the hardware.</span></span> <span data-ttu-id="61c26-238">您可以在呼叫 [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice)時判斷功能等級。</span><span class="sxs-lookup"><span data-stu-id="61c26-238">You can determine the feature level when you call [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice).</span></span> <span data-ttu-id="61c26-239">您可以藉由呼叫 [**ID2D1EffectCoNtext：： IsBufferPrecisionSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported) 與值 [**D2D1 \_ 緩衝區有效 \_ 位數 \_ 32BPC \_ FLOAT**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_buffer_precision)來檢查浮點緩衝區支援。</span><span class="sxs-lookup"><span data-stu-id="61c26-239">You can check for floating point buffer support by calling [**ID2D1EffectContext::IsBufferPrecisionSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported) with the value [**D2D1\_BUFFER\_PRECISION\_32BPC\_FLOAT**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_buffer_precision).</span></span>

## <a name="sample-code"></a><span data-ttu-id="61c26-240">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="61c26-240">Sample code</span></span>

<span data-ttu-id="61c26-241">如需此效果的範例，請下載 [Direct2D 效果相片調整範例](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)，並參閱範例的第4課。</span><span class="sxs-lookup"><span data-stu-id="61c26-241">For an example of this effect, download the [Direct2D effects photo adjustment sample](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment), and see Lesson 4 of the sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="61c26-242">規格需求</span><span class="sxs-lookup"><span data-stu-id="61c26-242">Requirements</span></span>

| <span data-ttu-id="61c26-243">需求</span><span class="sxs-lookup"><span data-stu-id="61c26-243">Requirement</span></span> | <span data-ttu-id="61c26-244">值</span><span class="sxs-lookup"><span data-stu-id="61c26-244">Value</span></span> |
|-|-|
| <span data-ttu-id="61c26-245">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="61c26-245">Minimum supported client</span></span> | <span data-ttu-id="61c26-246">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="61c26-246">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="61c26-247">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="61c26-247">Minimum supported server</span></span> | <span data-ttu-id="61c26-248">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="61c26-248">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="61c26-249">標頭</span><span class="sxs-lookup"><span data-stu-id="61c26-249">Header</span></span> | <span data-ttu-id="61c26-250">d2d1effects。h</span><span class="sxs-lookup"><span data-stu-id="61c26-250">d2d1effects.h</span></span> |
| <span data-ttu-id="61c26-251">程式庫</span><span class="sxs-lookup"><span data-stu-id="61c26-251">Library</span></span> | <span data-ttu-id="61c26-252">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="61c26-252">d2d1.lib, dxguid.lib</span></span> |

## <a name="related-topics"></a><span data-ttu-id="61c26-253">相關主題</span><span class="sxs-lookup"><span data-stu-id="61c26-253">Related topics</span></span>

* [<span data-ttu-id="61c26-254">ID2D1Effect 介面</span><span class="sxs-lookup"><span data-stu-id="61c26-254">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
