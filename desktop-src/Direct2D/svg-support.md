---
title: SVG 支援
description: 從 Windows 10 年度更新版開始，Direct2D 支援包含 SVG 圖像大綱的轉譯色彩字型，如 OpenType 規格中所述 (看到「SVG」資料表) 。
ms.assetid: 5cb4cb7c-9b96-e110-bff9-d75ad1980010
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678c5d9ef42a53c854bb2f175fac63816345c519
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375408"
---
# <a name="svg-support"></a><span data-ttu-id="f5d78-103">SVG 支援</span><span class="sxs-lookup"><span data-stu-id="f5d78-103">SVG Support</span></span>

<span data-ttu-id="f5d78-104">從 Windows 10 年度更新版開始，Direct2D 支援包含 SVG 圖像大綱的轉譯 [色彩](../directwrite/color-fonts.md) 字型，如 [OpenType 規格](/typography/opentype/spec/) 中所述 (參閱 [svg 表格](/typography/opentype/spec/svg)) 。</span><span class="sxs-lookup"><span data-stu-id="f5d78-104">Beginning in Windows 10 Anniversary Update, Direct2D supports rendering [color fonts](../directwrite/color-fonts.md) that contain SVG glyph outlines, as described in the [OpenType specification](/typography/opentype/spec/) (see [The SVG table](/typography/opentype/spec/svg)).</span></span> <span data-ttu-id="f5d78-105">從 Windows 10 Creators Update 開始，Direct2D 也支援呈現獨立 SVG 影像。</span><span class="sxs-lookup"><span data-stu-id="f5d78-105">Beginning in Windows 10 Creators Update, Direct2D also supports rendering standalone SVG images.</span></span> <span data-ttu-id="f5d78-106">不過，在 OpenType SVG 字型內不允許某些 SVG 功能，而且 Direct2D 目前不支援某些 SVG 功能。</span><span class="sxs-lookup"><span data-stu-id="f5d78-106">However, certain SVG features are disallowed within OpenType SVG fonts, and certain SVG features are currently unsupported by Direct2D.</span></span>  

<span data-ttu-id="f5d78-107">本主題指出 Windows 10 年度更新版和更新版本中 Direct2D 所支援的 [SVG 1.1](https://www.w3.org/TR/SVG11/) 功能集。</span><span class="sxs-lookup"><span data-stu-id="f5d78-107">This topic identifies the set of [SVG 1.1](https://www.w3.org/TR/SVG11/) features supported by Direct2D in Windows 10 Anniversary Update and newer.</span></span> <span data-ttu-id="f5d78-108">本檔適用于 OpenType 字型中的 SVG，以及獨立 SVG 影像。</span><span class="sxs-lookup"><span data-stu-id="f5d78-108">This document applies to SVG in OpenType fonts as well as standalone SVG images.</span></span>

## <a name="supported-svg-elements-and-attributes"></a><span data-ttu-id="f5d78-109">支援的 SVG 元素和屬性</span><span class="sxs-lookup"><span data-stu-id="f5d78-109">Supported SVG elements and attributes</span></span>

<span data-ttu-id="f5d78-110">Direct2D 支援轉譯下列 SVG 元素，以及每個專案的相關屬性。</span><span class="sxs-lookup"><span data-stu-id="f5d78-110">Direct2D supports rendering the following SVG elements and the associated attributes for each element.</span></span> <span data-ttu-id="f5d78-111">系統會忽略其他元素和一般屬性。</span><span class="sxs-lookup"><span data-stu-id="f5d78-111">Other elements and regular attributes are ignored.</span></span>



| <span data-ttu-id="f5d78-112">元素</span><span class="sxs-lookup"><span data-stu-id="f5d78-112">Element</span></span>                                                                                  | <span data-ttu-id="f5d78-113">支援的一般屬性</span><span class="sxs-lookup"><span data-stu-id="f5d78-113">Supported regular attributes</span></span>                                                             |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f5d78-114">圈</span><span class="sxs-lookup"><span data-stu-id="f5d78-114">circle</span></span>](https://www.w3.org/TR/SVG11/shapes.mdl#circleelement)                           | <span data-ttu-id="f5d78-115">識別碼、樣式、轉換、cx、cy、r</span><span class="sxs-lookup"><span data-stu-id="f5d78-115">id, style, transform, cx, cy, r</span></span>                                                          |
| [<span data-ttu-id="f5d78-116">clipPath</span><span class="sxs-lookup"><span data-stu-id="f5d78-116">clipPath</span></span>](https://www.w3.org/TR/SVG11/masking.mdl#clippathelement)                      | <span data-ttu-id="f5d78-117">識別碼、樣式、轉換、clipPathUnits</span><span class="sxs-lookup"><span data-stu-id="f5d78-117">id, style, transform, clipPathUnits</span></span>                                                      |
| [<span data-ttu-id="f5d78-118">defs</span><span class="sxs-lookup"><span data-stu-id="f5d78-118">defs</span></span>](https://www.w3.org/TR/SVG11/struct.mdl#defselement)                               | <span data-ttu-id="f5d78-119">識別碼、樣式、轉換</span><span class="sxs-lookup"><span data-stu-id="f5d78-119">id, style, transform</span></span>                                                                     |
| <span data-ttu-id="f5d78-120">[desc](https://www.w3.org/TR/SVG11/struct.mdl#descriptionandtitleelements)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="f5d78-120">[desc](https://www.w3.org/TR/SVG11/struct.mdl#descriptionandtitleelements)<sup>\*</sup></span></span>  | <span data-ttu-id="f5d78-121">id</span><span class="sxs-lookup"><span data-stu-id="f5d78-121">id</span></span>                                                                                       |
| [<span data-ttu-id="f5d78-122">橢圓</span><span class="sxs-lookup"><span data-stu-id="f5d78-122">ellipse</span></span>](https://www.w3.org/TR/SVG11/shapes.mdl#ellipseelement)                         | <span data-ttu-id="f5d78-123">識別碼、樣式、轉換、cx、cy、rx、ry</span><span class="sxs-lookup"><span data-stu-id="f5d78-123">id, style, transform, cx, cy, rx, ry</span></span>                                                     |
| [<span data-ttu-id="f5d78-124">G</span><span class="sxs-lookup"><span data-stu-id="f5d78-124">g</span></span>](https://www.w3.org/TR/SVG11/struct.mdl#gelement)                                     | <span data-ttu-id="f5d78-125">識別碼、樣式、轉換</span><span class="sxs-lookup"><span data-stu-id="f5d78-125">id, style, transform</span></span>                                                                     |
| [<span data-ttu-id="f5d78-126">image</span><span class="sxs-lookup"><span data-stu-id="f5d78-126">image</span></span>](https://www.w3.org/TR/SVG11/struct.mdl#imageelement)                             | <span data-ttu-id="f5d78-127">識別碼、樣式、轉換、x、y、寬度、高度、preserveAspectRatio、xlink： href</span><span class="sxs-lookup"><span data-stu-id="f5d78-127">id, style, transform, x, y, width, height, preserveAspectRatio, xlink:href</span></span>               |
| [<span data-ttu-id="f5d78-128">line</span><span class="sxs-lookup"><span data-stu-id="f5d78-128">line</span></span>](https://www.w3.org/TR/SVG11/shapes.mdl#lineelement)                               | <span data-ttu-id="f5d78-129">id、style、transform、x1、y1、x2、y2</span><span class="sxs-lookup"><span data-stu-id="f5d78-129">id, style, transform, x1, y1, x2, y2</span></span>                                                     |
| [<span data-ttu-id="f5d78-130">linearGradient</span><span class="sxs-lookup"><span data-stu-id="f5d78-130">linearGradient</span></span>](https://www.w3.org/TR/SVG11/pservers.mdl#lineargradientelement)         | <span data-ttu-id="f5d78-131">id、style、x1、y1、x2、y2、gradientUnits、gradientTransform、spreadMethod、xlink： href</span><span class="sxs-lookup"><span data-stu-id="f5d78-131">id, style, x1, y1, x2, y2, gradientUnits, gradientTransform, spreadMethod, xlink:href</span></span>    |
| [<span data-ttu-id="f5d78-132">path</span><span class="sxs-lookup"><span data-stu-id="f5d78-132">path</span></span>](https://www.w3.org/TR/SVG11/paths.mdl#pathelement)                                | <span data-ttu-id="f5d78-133">識別碼、樣式、轉換、d</span><span class="sxs-lookup"><span data-stu-id="f5d78-133">id, style, transform, d</span></span>                                                                  |
| [<span data-ttu-id="f5d78-134">多邊形</span><span class="sxs-lookup"><span data-stu-id="f5d78-134">polygon</span></span>](https://www.w3.org/TR/SVG11/shapes.mdl#polygonelement)                         | <span data-ttu-id="f5d78-135">識別碼、樣式、轉換、點</span><span class="sxs-lookup"><span data-stu-id="f5d78-135">id, style, transform, points</span></span>                                                             |
| [<span data-ttu-id="f5d78-136">折線</span><span class="sxs-lookup"><span data-stu-id="f5d78-136">polyline</span></span>](https://www.w3.org/TR/SVG11/shapes.mdl#polylineelement)                       | <span data-ttu-id="f5d78-137">識別碼、樣式、轉換、點</span><span class="sxs-lookup"><span data-stu-id="f5d78-137">id, style, transform, points</span></span>                                                             |
| [<span data-ttu-id="f5d78-138">radialGradient</span><span class="sxs-lookup"><span data-stu-id="f5d78-138">radialGradient</span></span>](https://www.w3.org/TR/SVG11/pservers.mdl#radialgradientelement)         | <span data-ttu-id="f5d78-139">id、style、cx、cy、r、fx、2006、gradientUnits、gradientTransform、spreadMethod、xlink： href</span><span class="sxs-lookup"><span data-stu-id="f5d78-139">id, style, cx, cy, r, fx, fy, gradientUnits, gradientTransform, spreadMethod, xlink:href</span></span> |
| [<span data-ttu-id="f5d78-140">矩形</span><span class="sxs-lookup"><span data-stu-id="f5d78-140">rect</span></span>](https://www.w3.org/TR/SVG11/shapes.mdl#rectelement)                               | <span data-ttu-id="f5d78-141">識別碼、樣式、轉換、x、y、寬度、高度、rx、ry</span><span class="sxs-lookup"><span data-stu-id="f5d78-141">id, style, transform, x, y, width, height, rx, ry</span></span>                                        |
| [<span data-ttu-id="f5d78-142">停止</span><span class="sxs-lookup"><span data-stu-id="f5d78-142">stop</span></span>](https://www.w3.org/TR/SVG11/pservers.mdl#stopelement)                             | <span data-ttu-id="f5d78-143">id、style、offset</span><span class="sxs-lookup"><span data-stu-id="f5d78-143">id, style, offset</span></span>                                                                        |
| [<span data-ttu-id="f5d78-144">Svg</span><span class="sxs-lookup"><span data-stu-id="f5d78-144">svg</span></span>](https://www.w3.org/TR/SVG11/struct.mdl#svgelement)                                 | <span data-ttu-id="f5d78-145">id、style、x、y、width、height、viewBox、preserveAspectRatio</span><span class="sxs-lookup"><span data-stu-id="f5d78-145">id, style, x, y, width, height, viewBox, preserveAspectRatio</span></span>                             |
| <span data-ttu-id="f5d78-146">[標題](https://www.w3.org/TR/SVG11/struct.mdl#descriptionandtitleelements)<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="f5d78-146">[title](https://www.w3.org/TR/SVG11/struct.mdl#descriptionandtitleelements)<sup>\*</sup></span></span> | <span data-ttu-id="f5d78-147">id</span><span class="sxs-lookup"><span data-stu-id="f5d78-147">id</span></span>                                                                                       |
| [<span data-ttu-id="f5d78-148">use</span><span class="sxs-lookup"><span data-stu-id="f5d78-148">use</span></span>](https://www.w3.org/TR/SVG11/struct.mdl#useelement)                                 | <span data-ttu-id="f5d78-149">識別碼、樣式、轉換、x、y、寬度、高度、xlink： href</span><span class="sxs-lookup"><span data-stu-id="f5d78-149">id, style, transform, x, y, width, height, xlink:href</span></span>                                    |



 

<span data-ttu-id="f5d78-150"><sup>\*</sup> 只有 Windows 10 Creators Update 和更新版本才支援</span><span class="sxs-lookup"><span data-stu-id="f5d78-150"><sup>\*</sup> Only supported in Windows 10 Creators Update and newer</span></span>

## <a name="supported-svg-presentation-attributes"></a><span data-ttu-id="f5d78-151">支援的 SVG 呈現屬性</span><span class="sxs-lookup"><span data-stu-id="f5d78-151">Supported SVG presentation attributes</span></span>

<span data-ttu-id="f5d78-152">Direct2D 也支援下列展示屬性。</span><span class="sxs-lookup"><span data-stu-id="f5d78-152">Direct2D also supports the following presentation attributes.</span></span> <span data-ttu-id="f5d78-153">您可以在任何 SVG 元素上指定這些專案，但它們只會影響 SVG 規格中所述之特定專案的外觀 (查看 [呈現屬性](https://www.w3.org/TR/SVG11/attindex.mdl#presentationattributes)) 。</span><span class="sxs-lookup"><span data-stu-id="f5d78-153">These can be specified on any SVG elements, but they only affect the appearance of certain elements as described in the SVG specification (see [Presentation attributes](https://www.w3.org/TR/SVG11/attindex.mdl#presentationattributes)).</span></span>

-   <span data-ttu-id="f5d78-154">剪輯路徑</span><span class="sxs-lookup"><span data-stu-id="f5d78-154">clip-path</span></span>
-   <span data-ttu-id="f5d78-155">剪輯-規則</span><span class="sxs-lookup"><span data-stu-id="f5d78-155">clip-rule</span></span>
-   <span data-ttu-id="f5d78-156">color</span><span class="sxs-lookup"><span data-stu-id="f5d78-156">color</span></span>
-   <span data-ttu-id="f5d78-157">顯示<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="f5d78-157">display<sup>\*</sup></span></span>
-   <span data-ttu-id="f5d78-158">fill</span><span class="sxs-lookup"><span data-stu-id="f5d78-158">fill</span></span>
-   <span data-ttu-id="f5d78-159">填滿-不透明度</span><span class="sxs-lookup"><span data-stu-id="f5d78-159">fill-opacity</span></span>
-   <span data-ttu-id="f5d78-160">填滿規則</span><span class="sxs-lookup"><span data-stu-id="f5d78-160">fill-rule</span></span>
-   <span data-ttu-id="f5d78-161">不透明度</span><span class="sxs-lookup"><span data-stu-id="f5d78-161">opacity</span></span>
-   <span data-ttu-id="f5d78-162">Overflow - 溢位</span><span class="sxs-lookup"><span data-stu-id="f5d78-162">overflow</span></span>
-   <span data-ttu-id="f5d78-163">停止色彩</span><span class="sxs-lookup"><span data-stu-id="f5d78-163">stop-color</span></span>
-   <span data-ttu-id="f5d78-164">停止-不透明度</span><span class="sxs-lookup"><span data-stu-id="f5d78-164">stop-opacity</span></span>
-   <span data-ttu-id="f5d78-165">stroke (衝程)</span><span class="sxs-lookup"><span data-stu-id="f5d78-165">stroke</span></span>
-   <span data-ttu-id="f5d78-166">筆劃-dasharray</span><span class="sxs-lookup"><span data-stu-id="f5d78-166">stroke-dasharray</span></span>
-   <span data-ttu-id="f5d78-167">筆劃-dashoffset</span><span class="sxs-lookup"><span data-stu-id="f5d78-167">stroke-dashoffset</span></span>
-   <span data-ttu-id="f5d78-168">筆劃-linecap</span><span class="sxs-lookup"><span data-stu-id="f5d78-168">stroke-linecap</span></span>
-   <span data-ttu-id="f5d78-169">筆劃-linejoin</span><span class="sxs-lookup"><span data-stu-id="f5d78-169">stroke-linejoin</span></span>
-   <span data-ttu-id="f5d78-170">筆劃-miterlimit</span><span class="sxs-lookup"><span data-stu-id="f5d78-170">stroke-miterlimit</span></span>
-   <span data-ttu-id="f5d78-171">筆劃-不透明度</span><span class="sxs-lookup"><span data-stu-id="f5d78-171">stroke-opacity</span></span>
-   <span data-ttu-id="f5d78-172">筆劃寬度</span><span class="sxs-lookup"><span data-stu-id="f5d78-172">stroke-width</span></span>
-   <span data-ttu-id="f5d78-173">知名度<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="f5d78-173">visibility<sup>\*</sup></span></span>

<span data-ttu-id="f5d78-174"><sup>\*</sup> 只有 Windows 10 Creators Update 和更新版本才支援</span><span class="sxs-lookup"><span data-stu-id="f5d78-174"><sup>\*</sup> Only supported in Windows 10 Creators Update and newer</span></span>

## <a name="unsupported-svg-features"></a><span data-ttu-id="f5d78-175">不支援的 SVG 功能</span><span class="sxs-lookup"><span data-stu-id="f5d78-175">Unsupported SVG features</span></span>

### <a name="unsupported-elements-and-attributes"></a><span data-ttu-id="f5d78-176">不支援的元素和屬性</span><span class="sxs-lookup"><span data-stu-id="f5d78-176">Unsupported elements and attributes</span></span>

<span data-ttu-id="f5d78-177">Direct2D 不會將任何未包含在上述清單中的元素或屬性視為不受支援。</span><span class="sxs-lookup"><span data-stu-id="f5d78-177">Any element or attribute not included in the above lists is considered unsupported by Direct2D.</span></span> <span data-ttu-id="f5d78-178">剖析包含不支援之元素或屬性的 SVG 內容時，會忽略不支援的實體。</span><span class="sxs-lookup"><span data-stu-id="f5d78-178">When parsing SVG content that contains an unsupported element or attribute, the unsupported entity is ignored.</span></span> <span data-ttu-id="f5d78-179">其餘內容會盡可能地轉譯。</span><span class="sxs-lookup"><span data-stu-id="f5d78-179">The remainder of the content is rendered as faithfully as possible.</span></span>

### <a name="unsupported-length-units"></a><span data-ttu-id="f5d78-180">不支援的長度單位</span><span class="sxs-lookup"><span data-stu-id="f5d78-180">Unsupported length units</span></span>

<span data-ttu-id="f5d78-181">從 Windows 10 年度更新版，Direct2D 只支援使用者空間長度值和百分比長度值。</span><span class="sxs-lookup"><span data-stu-id="f5d78-181">As of Windows 10 Anniversary Update, Direct2D only supports user-space length values and percentage length values.</span></span> <span data-ttu-id="f5d78-182">不支援具有單位尾碼的長度（例如 "mm" 或 "em"）。</span><span class="sxs-lookup"><span data-stu-id="f5d78-182">Lengths with unit suffixes, like “mm” or “em,” are unsupported.</span></span>

<span data-ttu-id="f5d78-183">從 Windows 10 Fall Creators Update 開始，Direct2D 也支援絕對單位識別碼： px、pt、pc、cm、mm 和 in。</span><span class="sxs-lookup"><span data-stu-id="f5d78-183">Starting in Windows 10 Fall Creators Update, Direct2D also supports absolute unit identifiers: px, pt, pc, cm, mm, and in.</span></span> <span data-ttu-id="f5d78-184">不支援相對單位識別碼 (em，例如) 。</span><span class="sxs-lookup"><span data-stu-id="f5d78-184">Relative unit identifiers (em, ex) are not supported.</span></span>

### <a name="unsupported-image-sources"></a><span data-ttu-id="f5d78-185">不支援的影像來源</span><span class="sxs-lookup"><span data-stu-id="f5d78-185">Unsupported image sources</span></span>

<span data-ttu-id="f5d78-186">只有在 xlink： href 屬性設定為 base64 編碼的影像時，才支援 image 元素。</span><span class="sxs-lookup"><span data-stu-id="f5d78-186">The image element is only supported if its xlink:href attribute is set to a base64-encoded image.</span></span> <span data-ttu-id="f5d78-187">不支援遠端參考。</span><span class="sxs-lookup"><span data-stu-id="f5d78-187">Remote references are not supported.</span></span>

 

 