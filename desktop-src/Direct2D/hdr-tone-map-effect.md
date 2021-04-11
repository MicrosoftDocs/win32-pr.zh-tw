---
title: HDR 音調地圖效果
description: 此效果會調整影像的動態範圍，使其更符合輸出顯示功能的內容。
ms.topic: article
ms.date: 02/01/2019
ms.openlocfilehash: 4c9234e1b50e155173630a2ff7d94756c5be6130
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843760"
---
# <a name="hdr-tone-map-effect"></a><span data-ttu-id="a3fc9-103">HDR 音調地圖效果</span><span class="sxs-lookup"><span data-stu-id="a3fc9-103">HDR tone map effect</span></span>

<span data-ttu-id="a3fc9-104">此效果會調整影像的動態範圍，使其更符合輸出顯示功能的內容。</span><span class="sxs-lookup"><span data-stu-id="a3fc9-104">This effect adjusts the dynamic range of an image to better suit its content to the capability of the output display.</span></span>

<span data-ttu-id="a3fc9-105">這項效果的屬性是由 [**D2D1_HDRTONEMAP_PROP 列舉**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_prop)識別，而 CLSID 是 **CLSID_D2D1HdrToneMap**。</span><span class="sxs-lookup"><span data-stu-id="a3fc9-105">The properties for this effect are identified by the [**D2D1_HDRTONEMAP_PROP enumeration**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_prop), and the CLSID is **CLSID_D2D1HdrToneMap**.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="a3fc9-106">效果屬性</span><span class="sxs-lookup"><span data-stu-id="a3fc9-106">Effect properties</span></span>

| <span data-ttu-id="a3fc9-107">顯示名稱和索引列舉</span><span class="sxs-lookup"><span data-stu-id="a3fc9-107">Display name and index enumeration</span></span> | <span data-ttu-id="a3fc9-108">類型和預設值</span><span class="sxs-lookup"><span data-stu-id="a3fc9-108">Type and default value</span></span> | <span data-ttu-id="a3fc9-109">Description</span><span class="sxs-lookup"><span data-stu-id="a3fc9-109">Description</span></span> |
|-|-|-|
| <span data-ttu-id="a3fc9-110">InputMaxLuminance、D2D1_HDRTONEMAP_PROP_INPUT_MAX_LUMINANCE</span><span class="sxs-lookup"><span data-stu-id="a3fc9-110">InputMaxLuminance, D2D1_HDRTONEMAP_PROP_INPUT_MAX_LUMINANCE</span></span> | <span data-ttu-id="a3fc9-111">FLOAT</span><span class="sxs-lookup"><span data-stu-id="a3fc9-111">FLOAT</span></span> | <span data-ttu-id="a3fc9-112">影像的最大淺色 (或 MaxCLL) ，以 nits。</span><span class="sxs-lookup"><span data-stu-id="a3fc9-112">The maximum light level (or MaxCLL) of the image, in nits.</span></span> |
| <span data-ttu-id="a3fc9-113">OutputMaxLuminance、D2D1_HDRTONEMAP_PROP_OUTPUT_MAX_LUMINANCE</span><span class="sxs-lookup"><span data-stu-id="a3fc9-113">OutputMaxLuminance, D2D1_HDRTONEMAP_PROP_OUTPUT_MAX_LUMINANCE</span></span> | <span data-ttu-id="a3fc9-114">FLOAT</span><span class="sxs-lookup"><span data-stu-id="a3fc9-114">FLOAT</span></span> | <span data-ttu-id="a3fc9-115">輸出目標所支援的 MaxCLL，通常是在 nits 中 &mdash; 設定為顯示的 MaxCLL。</span><span class="sxs-lookup"><span data-stu-id="a3fc9-115">The MaxCLL supported by the output target, in nits&mdash;typically set to the MaxCLL of the display.</span></span> |
| <span data-ttu-id="a3fc9-116">>displaymode、D2D1_HDRTONEMAP_PROP_DISPLAY_MODE</span><span class="sxs-lookup"><span data-stu-id="a3fc9-116">DisplayMode, D2D1_HDRTONEMAP_PROP_DISPLAY_MODE</span></span> | [<span data-ttu-id="a3fc9-117">**D2D1_HDRTONEMAP_DISPLAY_MODE**</span><span class="sxs-lookup"><span data-stu-id="a3fc9-117">**D2D1_HDRTONEMAP_DISPLAY_MODE**</span></span>](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_display_mode) | <span data-ttu-id="a3fc9-118">當設定為 **_HDR** 時，音調對應曲線會調整為更符合一般 HDR 顯示器的行為。</span><span class="sxs-lookup"><span data-stu-id="a3fc9-118">When set to **_HDR**, the tone mapping curve is adjusted to better fit the fit the behavior of common HDR displays.</span></span> |

## <a name="remarks"></a><span data-ttu-id="a3fc9-119">備註</span><span class="sxs-lookup"><span data-stu-id="a3fc9-119">Remarks</span></span>
<span data-ttu-id="a3fc9-120">的值 `InputMaxLuminance` 通常衍生自影像中繼資料。</span><span class="sxs-lookup"><span data-stu-id="a3fc9-120">The value for `InputMaxLuminance` is typically derived from the image metadata.</span></span> <span data-ttu-id="a3fc9-121">如果中繼資料不存在，您可以使用 [Direct2D advanced color image 轉譯範例](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages)中的 **D2DAdvancedColorImagesRenderer：： ComputeHdrMetadata** 函式 () ，以在 nits 中計算影像的最大光源 (MaxCLL) 。</span><span class="sxs-lookup"><span data-stu-id="a3fc9-121">For cases where the metadata is not present, you can use the **D2DAdvancedColorImagesRenderer::ComputeHdrMetadata** function (in the [Direct2D advanced color image rendering sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages)) to compute the maximum light level (MaxCLL) of an image, in nits.</span></span>

<span data-ttu-id="a3fc9-122">的值 `OutputMaxLuminance` 是設計成使用 [**DXGI_OUTPUT_DESC1：： MaxLuminance**](/windows/desktop/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1)從顯示衍生的。</span><span class="sxs-lookup"><span data-stu-id="a3fc9-122">The value for `OutputMaxLuminance` is designed to be derived from the display, using [**DXGI_OUTPUT_DESC1::MaxLuminance**](/windows/desktop/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1).</span></span>

<span data-ttu-id="a3fc9-123">根據顯示器是 HDR 顯示器或 SDR/WCG 顯示，HDR 色調地圖效果會有不同的色調地圖曲線。</span><span class="sxs-lookup"><span data-stu-id="a3fc9-123">The HDR tone map effect has different tone map curves depending on whether the display is an HDR display or an SDR/WCG display.</span></span>

<span data-ttu-id="a3fc9-124">此效果旨在結合 [白色層級調整效果](white-level-adjustment-effect.md) ，可讓您在 Direct2D 中使用適當的色彩管理和色調對應轉譯 HDR 影像。</span><span class="sxs-lookup"><span data-stu-id="a3fc9-124">This effect is intended to be combined with the [White level adjustment effect](white-level-adjustment-effect.md) to allow you to render HDR images in Direct2D with proper color management and tone mapping.</span></span> <span data-ttu-id="a3fc9-125">它是以任何想要提供最多功能的 HDR 影像觀賞體驗來處理所有 Windows HDR 影像格式的架構為目標，並根據顯示 () 的 HDR 或 WCG/SDR 來調整其功能。</span><span class="sxs-lookup"><span data-stu-id="a3fc9-125">It's aimed at any framework that wants to provide a best-in-class HDR image viewing experience that handles all of the Windows HDR image formats, and adapts to the capabilities of the display (whether that's HDR or WCG/SDR).</span></span> <span data-ttu-id="a3fc9-126">這項效果的目的是要依序串連在一起，如下所述。</span><span class="sxs-lookup"><span data-stu-id="a3fc9-126">The effects are intended to be chained together in sequence, as described below.</span></span>

- <span data-ttu-id="a3fc9-127">取得輸入影像，其色彩空間由其編解碼器定義。</span><span class="sxs-lookup"><span data-stu-id="a3fc9-127">Take the input image, whose color space defined by its codec.</span></span> <span data-ttu-id="a3fc9-128">中繼資料可指定 whitePoint。</span><span class="sxs-lookup"><span data-stu-id="a3fc9-128">Metadata may specify whitePoint.</span></span> <span data-ttu-id="a3fc9-129">中繼資料可指定輸入的亮度等級。</span><span class="sxs-lookup"><span data-stu-id="a3fc9-129">Metadata may specify input luminance level.</span></span>
- <span data-ttu-id="a3fc9-130">套用色彩管理效果。</span><span class="sxs-lookup"><span data-stu-id="a3fc9-130">Apply the color management effect.</span></span> <span data-ttu-id="a3fc9-131">轉換成 scRGB (CCCS) 空間。</span><span class="sxs-lookup"><span data-stu-id="a3fc9-131">Convert to scRGB (CCCS) space.</span></span>
- <span data-ttu-id="a3fc9-132">套用 HDR 音調地圖效果。</span><span class="sxs-lookup"><span data-stu-id="a3fc9-132">Apply the HDR tone map effect.</span></span> <span data-ttu-id="a3fc9-133">將影像的淺色較低至所需的層級。</span><span class="sxs-lookup"><span data-stu-id="a3fc9-133">Lower the light level of the image to the desired level.</span></span>
- <span data-ttu-id="a3fc9-134">套用白色層級調整效果。</span><span class="sxs-lookup"><span data-stu-id="a3fc9-134">Apply the white level adjustment effect.</span></span> <span data-ttu-id="a3fc9-135">將影像的白色層級調整為交換鏈所需的白色層級。</span><span class="sxs-lookup"><span data-stu-id="a3fc9-135">Scale the white level of the image to the white level required by the swap chain.</span></span>
- <span data-ttu-id="a3fc9-136">再次套用色彩管理效果。</span><span class="sxs-lookup"><span data-stu-id="a3fc9-136">Apply the color management effect again.</span></span> <span data-ttu-id="a3fc9-137">如果轉譯為8bpc，則轉換成 sRGB。</span><span class="sxs-lookup"><span data-stu-id="a3fc9-137">If rendering to 8bpc, then convert to sRGB.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3fc9-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="a3fc9-138">Requirements</span></span>

| <span data-ttu-id="a3fc9-139">需求</span><span class="sxs-lookup"><span data-stu-id="a3fc9-139">Requirement</span></span> | <span data-ttu-id="a3fc9-140">值</span><span class="sxs-lookup"><span data-stu-id="a3fc9-140">Value</span></span> |
|-|-|
| <span data-ttu-id="a3fc9-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a3fc9-141">Minimum supported client</span></span> | <span data-ttu-id="a3fc9-142">Windows 10 版本 1809 (10.0;組建 17763) \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3fc9-142">Windows 10, version 1809 (10.0; Build 17763) \[desktop apps \| UWP apps\]</span></span> |
| <span data-ttu-id="a3fc9-143">標頭</span><span class="sxs-lookup"><span data-stu-id="a3fc9-143">Header</span></span> | <span data-ttu-id="a3fc9-144">d2d1effects \_ 2。h</span><span class="sxs-lookup"><span data-stu-id="a3fc9-144">d2d1effects\_2.h</span></span> |
| <span data-ttu-id="a3fc9-145">程式庫</span><span class="sxs-lookup"><span data-stu-id="a3fc9-145">Library</span></span> | <span data-ttu-id="a3fc9-146">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="a3fc9-146">d2d1.lib, dxguid.lib</span></span> |

## <a name="related-topics"></a><span data-ttu-id="a3fc9-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="a3fc9-147">Related topics</span></span>

* [<span data-ttu-id="a3fc9-148">ID2D1Effect 介面</span><span class="sxs-lookup"><span data-stu-id="a3fc9-148">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
* [<span data-ttu-id="a3fc9-149">D2D1_HDRTONEMAP_PROP 列舉</span><span class="sxs-lookup"><span data-stu-id="a3fc9-149">D2D1_HDRTONEMAP_PROP enumeration</span></span>](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_prop)
