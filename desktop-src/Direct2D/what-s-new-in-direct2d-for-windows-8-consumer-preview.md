---
title: Direct2D 的新功能
description: 以下是一些 Direct2D 新增專案。
ms.assetid: BA459FF0-9457-4652-A97C-BD4EC57EC8E2
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 9208ded926bda197baf41d9195c13cacd8f7079b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315652"
---
# <a name="whats-new-in-direct2d"></a><span data-ttu-id="9b96a-103">Direct2D 的新功能</span><span class="sxs-lookup"><span data-stu-id="9b96a-103">What's new in Direct2D</span></span>

<span data-ttu-id="9b96a-104">以下是一些 Direct2D 新增專案。</span><span class="sxs-lookup"><span data-stu-id="9b96a-104">Here are some of the new additions to Direct2D.</span></span>

## <a name="whats-new-for-windows-10-creators-update"></a><span data-ttu-id="9b96a-105">Windows 10 Creators Update 的新功能</span><span class="sxs-lookup"><span data-stu-id="9b96a-105">What’s new for Windows 10 Creators Update</span></span>

<span data-ttu-id="9b96a-106">已針對 Windows 10 Creators Update 新增或更新下列功能和 Api。</span><span class="sxs-lookup"><span data-stu-id="9b96a-106">The following features and APIs were added or updated for Windows 10 Creators Update.</span></span>

### <a name="support-for-svg-image-rendering"></a><span data-ttu-id="9b96a-107">SVG 影像轉譯的支援</span><span class="sxs-lookup"><span data-stu-id="9b96a-107">Support for SVG image rendering</span></span>

<span data-ttu-id="9b96a-108">從 Windows 10 Creators Update 開始，Direct2D 提供剖析和繪製 SVG 影像的支援，可讓開發人員轉譯其最愛的向量藝術工具所產生的資產，而不需要先將它們轉換成「光柵影像」。</span><span class="sxs-lookup"><span data-stu-id="9b96a-108">Starting in Windows 10 Creators Update, Direct2D provides support for parsing and drawing SVG images, allowing developers to render assets produced in their favorite vector art tools without converting them to raster images first.</span></span> <span data-ttu-id="9b96a-109">您可以使用這項功能來改善應用程式內圖示的磁片使用量和規模調整行為，並使用 Direct2d 新的 SVG 物件模型 Api，以程式設計方式變更您的應用程式 SVG。</span><span class="sxs-lookup"><span data-stu-id="9b96a-109">Use this feature to improve the disk footprint and scaling behavior of your in-app iconography, and use Direct2D’s new SVG object model APIs to make programmatic changes to your app’s SVG.</span></span> <span data-ttu-id="9b96a-110">請注意，Direct2D 僅支援適用于影像的有限 SVG 子集，且不支援所有 SVG 繪圖功能。</span><span class="sxs-lookup"><span data-stu-id="9b96a-110">Note that Direct2D only supports a limited subset of SVG suitable for images and does not support all SVG drawing features.</span></span> <span data-ttu-id="9b96a-111">如果您需要瀏覽器級 SVG 相容性或 SVG 的 web 導向功能，請考慮改為使用 XAML web 導向 [控制項](/uwp/api/Windows.UI.Xaml.Controls.WebView) 。</span><span class="sxs-lookup"><span data-stu-id="9b96a-111">If you need browser-grade SVG compatibility or SVG’s web-oriented features, consider using the [XAML WebView control](/uwp/api/Windows.UI.Xaml.Controls.WebView) instead.</span></span> <span data-ttu-id="9b96a-112">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="9b96a-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="9b96a-113">Direct2D SVG 影像呈現範例</span><span class="sxs-lookup"><span data-stu-id="9b96a-113">Direct2D SVG image rendering sample</span></span>](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DSvgImage)
-   [<span data-ttu-id="9b96a-114">SVG 支援</span><span class="sxs-lookup"><span data-stu-id="9b96a-114">SVG Support</span></span>](svg-support.md)
-   <span data-ttu-id="9b96a-115">[**ID2D1DeviceCoNtext5：： CreateSvgDocument**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createsvgdocument) 方法</span><span class="sxs-lookup"><span data-stu-id="9b96a-115">[**ID2D1DeviceContext5::CreateSvgDocument**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createsvgdocument) method</span></span>
-   <span data-ttu-id="9b96a-116">[**ID2D1DeviceCoNtext5：:D rawsvgdocument**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-drawsvgdocument) 方法</span><span class="sxs-lookup"><span data-stu-id="9b96a-116">[**ID2D1DeviceContext5::DrawSvgDocument**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-drawsvgdocument) method</span></span>
-   <span data-ttu-id="9b96a-117">[**ID2D1SvgElement**](/windows/win32/api/d2d1svg/nn-d2d1svg-id2d1svgelement) 介面</span><span class="sxs-lookup"><span data-stu-id="9b96a-117">[**ID2D1SvgElement**](/windows/win32/api/d2d1svg/nn-d2d1svg-id2d1svgelement) interface</span></span>

### <a name="improved-support-for-color-management"></a><span data-ttu-id="9b96a-118">改善對色彩管理的支援</span><span class="sxs-lookup"><span data-stu-id="9b96a-118">Improved support for color management</span></span>

<span data-ttu-id="9b96a-119">從 Windows 10 Creators Update 開始，Direct2D 提供改良的色彩管理功能。</span><span class="sxs-lookup"><span data-stu-id="9b96a-119">Starting in Windows 10 Creators Update, Direct2D provides improved color management capabilities.</span></span> <span data-ttu-id="9b96a-120">開發人員不再需要使用 Direct2d 色彩管理效果的 ICC 設定檔;他們現在可以使用 DXGI 色彩空間，或建立自己的參數化色彩空間定義。</span><span class="sxs-lookup"><span data-stu-id="9b96a-120">Developers no longer need an ICC profile to use Direct2D’s color management effect; they can now use DXGI color spaces or construct their own parameterized color space definition.</span></span> <span data-ttu-id="9b96a-121">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="9b96a-121">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="9b96a-122">色彩管理效果</span><span class="sxs-lookup"><span data-stu-id="9b96a-122">Color management effect</span></span>](color-management.md)
-   [<span data-ttu-id="9b96a-123">**ID2D1DeviceCoNtext5::CreateColorCoNtextFromDxgiColorSpace**</span><span class="sxs-lookup"><span data-stu-id="9b96a-123">**ID2D1DeviceContext5::CreateColorContextFromDxgiColorSpace**</span></span>](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace)
-   <span data-ttu-id="9b96a-124">[**ID2D1DeviceCoNtext5::CreateColorCoNtextFromSimpleColorProfile**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile_id2d1colorcontext1))</span><span class="sxs-lookup"><span data-stu-id="9b96a-124">[**ID2D1DeviceContext5::CreateColorContextFromSimpleColorProfile**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile_id2d1colorcontext1))</span></span>

## <a name="whats-new-for-windows-10-anniversary-update"></a><span data-ttu-id="9b96a-125">Windows 10 年度更新版的新功能</span><span class="sxs-lookup"><span data-stu-id="9b96a-125">What's new for Windows 10 Anniversary Update</span></span>

<span data-ttu-id="9b96a-126">已針對 Windows 10 年度更新版新增或更新下列功能和 Api。</span><span class="sxs-lookup"><span data-stu-id="9b96a-126">The following features and APIs were added or updated for Windows 10 Anniversary Update.</span></span>

### <a name="improved-support-for-color-fonts"></a><span data-ttu-id="9b96a-127">改善的色彩字型支援</span><span class="sxs-lookup"><span data-stu-id="9b96a-127">Improved support for color fonts</span></span>

<span data-ttu-id="9b96a-128">從 Windows 10 年度更新版開始，Direct2D 現在支援轉譯各式各樣的色彩字型格式，可讓開發人員在其 Direct2D 的應用程式中使用比以往更多的字型類型。</span><span class="sxs-lookup"><span data-stu-id="9b96a-128">Starting in Windows 10 Anniversary Update, Direct2D now supports rendering a wider variety of color font formats, allowing developers to use more types of fonts in their Direct2D-powered apps than ever before.</span></span> <span data-ttu-id="9b96a-129">這包括下列項目的支援：</span><span class="sxs-lookup"><span data-stu-id="9b96a-129">This includes support for:</span></span>

-   <span data-ttu-id="9b96a-130">' COLR ' OpenType 資料表，可在字型中啟用精簡向量內容。</span><span class="sxs-lookup"><span data-stu-id="9b96a-130">The ‘COLR’ OpenType table, which enables compact vector content in fonts.</span></span> <span data-ttu-id="9b96a-131">自 Windows 8.1 之後 (支援。 ) </span><span class="sxs-lookup"><span data-stu-id="9b96a-131">(Supported since Windows 8.1.)</span></span>
-   <span data-ttu-id="9b96a-132">「SVG」 OpenType 資料表，可在字型中啟用 SVG 內容。</span><span class="sxs-lookup"><span data-stu-id="9b96a-132">The ‘SVG ’ OpenType table, which enables SVG content in fonts.</span></span>
-   <span data-ttu-id="9b96a-133">' CBDT ' OpenType 資料表，可在字型中啟用色彩點陣圖內容。</span><span class="sxs-lookup"><span data-stu-id="9b96a-133">The ‘CBDT’ OpenType table, which enables color bitmap content in fonts.</span></span>
-   <span data-ttu-id="9b96a-134">' Sbix ' OpenType 資料表，可在字型中啟用色彩點陣圖內容。</span><span class="sxs-lookup"><span data-stu-id="9b96a-134">The ‘sbix’ OpenType table, which enables color bitmap content in fonts.</span></span>

<span data-ttu-id="9b96a-135">啟用 [ [**D2D1 \_ 繪圖 \_ 文字 \_ 選項 \_ 啟用 \_ 色彩 \_ 字型**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_draw_text_options) ] 旗標時，Direct2D 會自動支援這些色彩字型格式。</span><span class="sxs-lookup"><span data-stu-id="9b96a-135">Direct2D supports these color font formats automatically when the [**D2D1\_DRAW\_TEXT\_OPTIONS\_ENABLE\_COLOR\_FONT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_draw_text_options) flag is enabled.</span></span> <span data-ttu-id="9b96a-136">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="9b96a-136">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="9b96a-137">色彩字型</span><span class="sxs-lookup"><span data-stu-id="9b96a-137">Color Fonts</span></span>](/windows/desktop/DirectWrite/color-fonts)
-   [<span data-ttu-id="9b96a-138">DirectWrite 色彩圖像範例</span><span class="sxs-lookup"><span data-stu-id="9b96a-138">DirectWrite color glyph sample</span></span>](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)

### <a name="new-image-effects"></a><span data-ttu-id="9b96a-139">新影像效果</span><span class="sxs-lookup"><span data-stu-id="9b96a-139">New image effects</span></span>

<span data-ttu-id="9b96a-140">從 Windows 10 年度更新版開始，Direct2D 包含 AlphaMask、CrossFade、不透明度和色調效果。</span><span class="sxs-lookup"><span data-stu-id="9b96a-140">Starting in Windows 10 Anniversary Update, Direct2D includes the AlphaMask, CrossFade, Opacity, and Tint effects.</span></span> <span data-ttu-id="9b96a-141">這項功能先前是由複合、ArithmeticComposite 和 ColorMatrix 效果的特定設定所提供，但新的內建效果可讓您更輕鬆地執行這些一般作業。</span><span class="sxs-lookup"><span data-stu-id="9b96a-141">This functionality was previously available from specific configurations of Composite, ArithmeticComposite, and ColorMatrix effects, but the new built-in effects make it easier to do these common operations.</span></span>

## <a name="whats-new-for-windows-10"></a><span data-ttu-id="9b96a-142">Windows 10 的新功能</span><span class="sxs-lookup"><span data-stu-id="9b96a-142">What's new for Windows 10</span></span>

<span data-ttu-id="9b96a-143">已針對 Windows 10 新增或更新下列功能和 Api。</span><span class="sxs-lookup"><span data-stu-id="9b96a-143">The following features and APIs were added or updated for Windows 10.</span></span>

### <a name="sprite-batches"></a><span data-ttu-id="9b96a-144">Sprite 批次</span><span class="sxs-lookup"><span data-stu-id="9b96a-144">Sprite batches</span></span>

<span data-ttu-id="9b96a-145">從 Windows 10 開始，Direct2D 會提供建立和呈現 sprite 批次的支援。</span><span class="sxs-lookup"><span data-stu-id="9b96a-145">Starting in Windows 10, Direct2D provides support for creating and rendering sprite batches.</span></span> <span data-ttu-id="9b96a-146">相較于一般用途的 [**DrawImage**](id2d1devicecontext-drawimage-overload.md) 方法，sprite 批次批次產生的每個映射 CPU 額外負荷極少。</span><span class="sxs-lookup"><span data-stu-id="9b96a-146">Compared to the general-purpose [**DrawImage**](id2d1devicecontext-drawimage-overload.md) method, sprite batches incur dramatically less per-image CPU overhead.</span></span> <span data-ttu-id="9b96a-147">這讓它們適合涉及數百或數千個並行影像的案例，例如遊戲 sprite 或物件系統。</span><span class="sxs-lookup"><span data-stu-id="9b96a-147">This makes them ideal for scenarios involving hundreds or thousands of concurrent images, such as game sprites or particle systems.</span></span> <span data-ttu-id="9b96a-148">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="9b96a-148">For more information, see the following topics:</span></span>

-   <span data-ttu-id="9b96a-149">[**ID2D1DeviceCoNtext3：： CreateSpriteBatch**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext3-createspritebatch) 方法</span><span class="sxs-lookup"><span data-stu-id="9b96a-149">[**ID2D1DeviceContext3::CreateSpriteBatch**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext3-createspritebatch) method</span></span>
-   <span data-ttu-id="9b96a-150">[**ID2D1DeviceCoNtext3：:D rawspritebatch**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext3-drawspritebatch(id2d1spritebatch_id2d1bitmap_d2d1_bitmap_interpolation_mode_d2d1_sprite_options)) 方法</span><span class="sxs-lookup"><span data-stu-id="9b96a-150">[**ID2D1DeviceContext3::DrawSpriteBatch**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext3-drawspritebatch(id2d1spritebatch_id2d1bitmap_d2d1_bitmap_interpolation_mode_d2d1_sprite_options)) methods</span></span>
-   <span data-ttu-id="9b96a-151">[**ID2D1SpriteBatch**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1spritebatch) 介面</span><span class="sxs-lookup"><span data-stu-id="9b96a-151">[**ID2D1SpriteBatch**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1spritebatch) interface</span></span>

### <a name="gradient-meshes"></a><span data-ttu-id="9b96a-152">漸層網格</span><span class="sxs-lookup"><span data-stu-id="9b96a-152">Gradient meshes</span></span>

<span data-ttu-id="9b96a-153">從 Windows 10 開始，Direct2D 會為漸層網格提供新的基本。</span><span class="sxs-lookup"><span data-stu-id="9b96a-153">Starting in Windows 10, Direct2D provides a new primitive for gradient meshes.</span></span> <span data-ttu-id="9b96a-154">漸層網格通常是由圖形設計軟體中的專業 illustrators 所使用，而且可讓演出者轉譯複雜的 (甚至是相片真實的) 彩色圖形，以及向量的所有記憶體和擴充性優點。</span><span class="sxs-lookup"><span data-stu-id="9b96a-154">Gradient meshes are often used by professional illustrators in graphic design software, and they allow artists to render complex (even photo-realistic) multicolored shapes with all the memory and scalability benefits of vectors.</span></span> <span data-ttu-id="9b96a-155">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="9b96a-155">For more information, see the follow topics:</span></span>

-   [<span data-ttu-id="9b96a-156">Direct2D 漸層網格範例</span><span class="sxs-lookup"><span data-stu-id="9b96a-156">Direct2D gradient mesh sample</span></span>](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DGradientMesh)
-   <span data-ttu-id="9b96a-157">[**D2D1 \_梯度 \_ 網格 \_ 修補程式**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_gradient_mesh_patch) 結構</span><span class="sxs-lookup"><span data-stu-id="9b96a-157">[**D2D1\_GRADIENT\_MESH\_PATCH**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_gradient_mesh_patch) structure</span></span>
-   <span data-ttu-id="9b96a-158">[**ID2D1DeviceCoNtext2：:D rawgradientmesh**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-drawgradientmesh) 方法</span><span class="sxs-lookup"><span data-stu-id="9b96a-158">[**ID2D1DeviceContext2::DrawGradientMesh**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-drawgradientmesh) method</span></span>

### <a name="improved-image-loading-apis"></a><span data-ttu-id="9b96a-159">改良的影像載入 Api</span><span class="sxs-lookup"><span data-stu-id="9b96a-159">Improved image loading APIs</span></span>

<span data-ttu-id="9b96a-160">從 Windows 10 開始，Direct2D 提供了新的 API，可用於載入影像 ID2D1ImageSource。</span><span class="sxs-lookup"><span data-stu-id="9b96a-160">Starting with Windows 10, Direct2D offers a new API for loading images, ID2D1ImageSource.</span></span> <span data-ttu-id="9b96a-161">映射來源可在現有的映射載入 Api （包括 CreateBitmapFromWicBitmap、點陣圖來源效果和 YCbCr 效果）時改善。</span><span class="sxs-lookup"><span data-stu-id="9b96a-161">The image source improves upon existing image loading APIs including CreateBitmapFromWicBitmap, the Bitmap Source effect, and the YCbCr effect.</span></span> <span data-ttu-id="9b96a-162">Direct2D 映射來源結合了這些 Api 的功能，可支援任意大型影像、輕鬆整合列印和效果，以及許多優化，包括 YCbCr JPEG 和編制索引的 JPEG。</span><span class="sxs-lookup"><span data-stu-id="9b96a-162">The Direct2D image source combines the capabilities of these APIs with support for arbitrarily large images, easy integration with printing and effects, and numerous optimizations including YCbCr JPEG and indexed JPEG.</span></span> <span data-ttu-id="9b96a-163">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="9b96a-163">For more information, see these topics:</span></span>

-   [<span data-ttu-id="9b96a-164">Direct2D 相片調整 SDK 範例</span><span class="sxs-lookup"><span data-stu-id="9b96a-164">Direct2D Photo Adjustment SDK sample</span></span>](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)
-   [<span data-ttu-id="9b96a-165">**ID2D1ImageSource**</span><span class="sxs-lookup"><span data-stu-id="9b96a-165">**ID2D1ImageSource**</span></span>](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource)
-   [<span data-ttu-id="9b96a-166">**ID2D1ImageSourceFromWic**</span><span class="sxs-lookup"><span data-stu-id="9b96a-166">**ID2D1ImageSourceFromWic**</span></span>](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic)
-   [<span data-ttu-id="9b96a-167">IWICJpegFrameDecode::SetIndexing</span><span class="sxs-lookup"><span data-stu-id="9b96a-167">IWICJpegFrameDecode::SetIndexing</span></span>](/windows/desktop/api/wincodec/nf-wincodec-iwicjpegframedecode-setindexing)

### <a name="improved-support-for-ink-rendering"></a><span data-ttu-id="9b96a-168">改進筆墨轉譯的支援</span><span class="sxs-lookup"><span data-stu-id="9b96a-168">Improved support for ink rendering</span></span>

<span data-ttu-id="9b96a-169">從 Windows 10 開始，Direct2D 會提供新的基本型別來代表筆墨筆劃。</span><span class="sxs-lookup"><span data-stu-id="9b96a-169">Starting in Windows 10, Direct2D provides a new primitive to represent ink strokes.</span></span> <span data-ttu-id="9b96a-170">Direct2D 筆墨筆觸是由貝茲曲線定義、支援不同的鋼筆圖案和轉換，而且可能具有固定或變動的粗細。</span><span class="sxs-lookup"><span data-stu-id="9b96a-170">Direct2D ink strokes are defined by Bezier curves, support different nib shapes and transforms, and may have fixed or variable thickness.</span></span> <span data-ttu-id="9b96a-171">Direct2d 筆墨筆觸的內建支援，可讓應用程式輕鬆地轉譯比先前的方法更快、更美觀的筆墨，通常需要應用程式來管理筆墨本身，作為一系列的省略號和 quadrilaterals。</span><span class="sxs-lookup"><span data-stu-id="9b96a-171">Direct2D’s built-in support for ink strokes allows apps to easily render faster, more beautiful ink than previous approaches, which typically required apps to manage ink themselves, as a series of ellipses and quadrilaterals.</span></span> <span data-ttu-id="9b96a-172">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="9b96a-172">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="9b96a-173">**ID2D1Ink 介面**</span><span class="sxs-lookup"><span data-stu-id="9b96a-173">**ID2D1Ink interface**</span></span>](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1ink)
-   [<span data-ttu-id="9b96a-174">**ID2D1DeviceCoNtext2：:D rawInk 方法**</span><span class="sxs-lookup"><span data-stu-id="9b96a-174">**ID2D1DeviceContext2::DrawInk method**</span></span>](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-drawink)
-   [<span data-ttu-id="9b96a-175">**ID2D1InkStyle 介面**</span><span class="sxs-lookup"><span data-stu-id="9b96a-175">**ID2D1InkStyle interface**</span></span>](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1inkstyle)

### <a name="effect-shader-linking"></a><span data-ttu-id="9b96a-176">效果著色器連結</span><span class="sxs-lookup"><span data-stu-id="9b96a-176">Effect shader linking</span></span>

<span data-ttu-id="9b96a-177">Direct2D 效果會使用 HLSL 圖元、頂點和/或計算著色器來執行。</span><span class="sxs-lookup"><span data-stu-id="9b96a-177">Direct2D effects are implemented using HLSL pixel, vertex, and/or compute shaders.</span></span> <span data-ttu-id="9b96a-178">從 Windows 10 開始，Direct2D 現在會自動分析效果圖形，讓您有機會結合和執行個別著色器。</span><span class="sxs-lookup"><span data-stu-id="9b96a-178">Starting with Windows 10, Direct2D now automatically analyzes effect graphs for opportunities to combine and execute individual shaders together.</span></span> <span data-ttu-id="9b96a-179">這可能會大幅增加效果輸送量。</span><span class="sxs-lookup"><span data-stu-id="9b96a-179">This can provide a significant increase in effect throughput.</span></span> <span data-ttu-id="9b96a-180">內建效果的取用者不需要執行任何動作來受益于效果著色器連結，但是建立自己自訂效果的開發人員應該遵循可利用效果著色器連結的更新最佳作法。</span><span class="sxs-lookup"><span data-stu-id="9b96a-180">Consumers of built-in effects do not need to do anything to benefit from effect shader linking, but developers who build their own custom effects should follow updated best practices for leveraging effect shader linking.</span></span> <span data-ttu-id="9b96a-181">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="9b96a-181">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="9b96a-182">效果著色器連結</span><span class="sxs-lookup"><span data-stu-id="9b96a-182">Effect Shader Linking</span></span>](effect-shader-linking.md)
-   [<span data-ttu-id="9b96a-183">Direct2D HLSL 協助程式</span><span class="sxs-lookup"><span data-stu-id="9b96a-183">Direct2D HLSL Helpers</span></span>](hlsl-helpers.md)
-   [<span data-ttu-id="9b96a-184">Direct2D 自訂效果 SDK 範例</span><span class="sxs-lookup"><span data-stu-id="9b96a-184">Direct2D custom effects SDK sample</span></span>](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)

<span data-ttu-id="9b96a-185">效果著色器連結的設計目的是不影響視覺效果的視覺效果輸出。</span><span class="sxs-lookup"><span data-stu-id="9b96a-185">Effect shader linking is designed to not affect the visual output of effects.</span></span> <span data-ttu-id="9b96a-186">不過，這不一定是因為效果有效位數和數位裁剪的特定行為。</span><span class="sxs-lookup"><span data-stu-id="9b96a-186">However, this is not always possible due to specific behavior around effect precision and numerical clipping.</span></span> <span data-ttu-id="9b96a-187">如需如何控制這些行為的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="9b96a-187">For more information on how to control for these behaviors, see:</span></span>

-   [<span data-ttu-id="9b96a-188">控制效果圖形中的有效位數和數位裁剪</span><span class="sxs-lookup"><span data-stu-id="9b96a-188">Controlling Precision and Numerical Clipping in Effect Graphs</span></span>](precision-and-clipping-in-effect-graphs.md)

### <a name="new-built-in-effects"></a><span data-ttu-id="9b96a-189">新的內建效果</span><span class="sxs-lookup"><span data-stu-id="9b96a-189">New built-in effects</span></span>

<span data-ttu-id="9b96a-190">從 Windows 10 開始，Direct2D 包含一組豐富的新內建效果，可解決頂尖的開發人員要求，並啟用新的視覺案例類型。</span><span class="sxs-lookup"><span data-stu-id="9b96a-190">Starting with Windows 10, Direct2D includes a rich set of new built-in effects which address top developer requests and enable new kinds of visual scenarios.</span></span> <span data-ttu-id="9b96a-191">新的效果如下：</span><span class="sxs-lookup"><span data-stu-id="9b96a-191">The new effects are:</span></span>

### <a name="color"></a><span data-ttu-id="9b96a-192">色彩：</span><span class="sxs-lookup"><span data-stu-id="9b96a-192">Color:</span></span>

-   [<span data-ttu-id="9b96a-193">RGB 到色調效果</span><span class="sxs-lookup"><span data-stu-id="9b96a-193">RGB to Hue effect</span></span>](rgb-to-hue-effect.md)
-   [<span data-ttu-id="9b96a-194">色調至 RGB 效果</span><span class="sxs-lookup"><span data-stu-id="9b96a-194">Hue to RGB effect</span></span>](hue-to-rgb-effect.md)
-   [<span data-ttu-id="9b96a-195">3D 查閱資料表效果</span><span class="sxs-lookup"><span data-stu-id="9b96a-195">3D lookup table effect</span></span>](3d-lookup-table-effect.md)

### <a name="photo"></a><span data-ttu-id="9b96a-196">照片：</span><span class="sxs-lookup"><span data-stu-id="9b96a-196">Photo:</span></span>

-   [<span data-ttu-id="9b96a-197">對比效果</span><span class="sxs-lookup"><span data-stu-id="9b96a-197">Contrast effect</span></span>](contrast-effect.md)
-   [<span data-ttu-id="9b96a-198">曝光效果</span><span class="sxs-lookup"><span data-stu-id="9b96a-198">Exposure effect</span></span>](exposure-effect.md)
-   [<span data-ttu-id="9b96a-199">灰階效果</span><span class="sxs-lookup"><span data-stu-id="9b96a-199">Grayscale effect</span></span>](grayscale-effect.md)
-   [<span data-ttu-id="9b96a-200">醒目顯示和陰影效果</span><span class="sxs-lookup"><span data-stu-id="9b96a-200">Highlights and shadows effect</span></span>](highlights-and-shadows-effect.md)
-   [<span data-ttu-id="9b96a-201">反轉效果</span><span class="sxs-lookup"><span data-stu-id="9b96a-201">Invert effect</span></span>](invert-effect.md)
-   [<span data-ttu-id="9b96a-202">棕褐色效果</span><span class="sxs-lookup"><span data-stu-id="9b96a-202">Sepia effect</span></span>](sepia-effect.md)
-   [<span data-ttu-id="9b96a-203">銳化效果</span><span class="sxs-lookup"><span data-stu-id="9b96a-203">Sharpen effect</span></span>](sharpen-effect.md)
-   [<span data-ttu-id="9b96a-204">伸直效果</span><span class="sxs-lookup"><span data-stu-id="9b96a-204">Straighten effect</span></span>](straighten-effect.md)
-   [<span data-ttu-id="9b96a-205">溫度和色調效果</span><span class="sxs-lookup"><span data-stu-id="9b96a-205">Temperature and tint effect</span></span>](temperature-and-tint-effect.md)
-   [<span data-ttu-id="9b96a-206">Vignette 效果</span><span class="sxs-lookup"><span data-stu-id="9b96a-206">Vignette effect</span></span>](vignette-effect.md)

### <a name="filter"></a><span data-ttu-id="9b96a-207">篩選：</span><span class="sxs-lookup"><span data-stu-id="9b96a-207">Filter:</span></span>

-   [<span data-ttu-id="9b96a-208">Edge 偵測效果</span><span class="sxs-lookup"><span data-stu-id="9b96a-208">Edge detection effect</span></span>](edge-detection-effect.md)

### <a name="stylize"></a><span data-ttu-id="9b96a-209">風格</span><span class="sxs-lookup"><span data-stu-id="9b96a-209">Stylize:</span></span>

-   [<span data-ttu-id="9b96a-210">浮凸效果</span><span class="sxs-lookup"><span data-stu-id="9b96a-210">Emboss effect</span></span>](emboss-effect.md)
-   [<span data-ttu-id="9b96a-211">色調影響</span><span class="sxs-lookup"><span data-stu-id="9b96a-211">Posterize effect</span></span>](posterize-effect.md)

### <a name="transparency"></a><span data-ttu-id="9b96a-212">透明度：</span><span class="sxs-lookup"><span data-stu-id="9b96a-212">Transparency:</span></span>

-   [<span data-ttu-id="9b96a-213">色度鍵效果</span><span class="sxs-lookup"><span data-stu-id="9b96a-213">Chroma-key effect</span></span>](chromakey-effect.md)

<span data-ttu-id="9b96a-214">[Direct2D 相片調整 SDK 範例](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)中示範了伸直、飽和度、對比、反白顯示和遮蔽，以及溫度和色調效果。</span><span class="sxs-lookup"><span data-stu-id="9b96a-214">The straighten, saturation, contrast, highlights and shadows, and temperature and tint effects are demonstrated in the [Direct2D Photo Adjustment SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment).</span></span>

## <a name="whats-new-for-windows-81"></a><span data-ttu-id="9b96a-215">Windows 8.1 的新功能</span><span class="sxs-lookup"><span data-stu-id="9b96a-215">What's new for Windows 8.1</span></span>

<span data-ttu-id="9b96a-216">已針對 Windows 8.1 新增或更新下列功能和 Api。</span><span class="sxs-lookup"><span data-stu-id="9b96a-216">The following features and APIs were added or updated for Windows 8.1.</span></span>

<span data-ttu-id="9b96a-217">從 Windows 8.1 開始，Direct2D 是建置於 Direct3D 11.2 之上。</span><span class="sxs-lookup"><span data-stu-id="9b96a-217">Starting with Windows 8.1, Direct2D is built on top of Direct3D 11.2.</span></span>

### <a name="geometry-realizations"></a><span data-ttu-id="9b96a-218">幾何實踐</span><span class="sxs-lookup"><span data-stu-id="9b96a-218">Geometry realizations</span></span>

<span data-ttu-id="9b96a-219">從 Windows 8.1 開始，Direct2D 提供 geometry 實踐。</span><span class="sxs-lookup"><span data-stu-id="9b96a-219">Starting in Windows 8.1, Direct2D offers geometry realizations.</span></span> <span data-ttu-id="9b96a-220">幾何實踐可讓應用程式在某些情況下改善幾何轉譯效能，而不會有一些將幾何柵格化到點陣圖的缺點。</span><span class="sxs-lookup"><span data-stu-id="9b96a-220">Geometry realizations allow applications to improve geometry rendering performance in certain situations, without some of the drawbacks of rasterizing geometry to a bitmap.</span></span> <span data-ttu-id="9b96a-221">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="9b96a-221">For more information, see the following topics:</span></span>

-   <span data-ttu-id="9b96a-222">[**ID2D1Device1**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1device1) 介面</span><span class="sxs-lookup"><span data-stu-id="9b96a-222">[**ID2D1Device1**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1device1) interface</span></span>
-   <span data-ttu-id="9b96a-223">[**ID2D1DeviceCoNtext1：:D rawgeometryrealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-drawgeometryrealization) 方法</span><span class="sxs-lookup"><span data-stu-id="9b96a-223">[**ID2D1DeviceContext1::DrawGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-drawgeometryrealization) method</span></span>

### <a name="support-for-jpeg-ycbcr-images"></a><span data-ttu-id="9b96a-224">支援 JPEG YCbCr 影像</span><span class="sxs-lookup"><span data-stu-id="9b96a-224">Support for JPEG YCbCr images</span></span>

<span data-ttu-id="9b96a-225">從 Windows 8.1 開始，Direct2D 提供以 JPEG Y'CbCr 格式轉譯影像資料的支援。</span><span class="sxs-lookup"><span data-stu-id="9b96a-225">Starting in Windows 8.1, Direct2D provides support for rendering image data in the JPEG Y’CbCr format.</span></span> <span data-ttu-id="9b96a-226">應用程式可以在其原生 Y'CbCr 標記法中轉譯 JPEG 內容，而不是解壓縮至 BGRA。</span><span class="sxs-lookup"><span data-stu-id="9b96a-226">Apps can render JPEG content in its native Y’CbCr representation instead of decompressing to BGRA.</span></span> <span data-ttu-id="9b96a-227">這可大幅減少圖形記憶體耗用量和資源建立時間。</span><span class="sxs-lookup"><span data-stu-id="9b96a-227">This can significantly reduce graphics memory consumption and resource creation time.</span></span> <span data-ttu-id="9b96a-228">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="9b96a-228">For more information, see the following topics:</span></span>

-   <span data-ttu-id="9b96a-229">Direct2D [YCbCr 效果](ycbcr-effect.md)</span><span class="sxs-lookup"><span data-stu-id="9b96a-229">Direct2D [YCbCr effect](ycbcr-effect.md)</span></span>
-   <span data-ttu-id="9b96a-230">[**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/wincodec/nn-wincodec-iwicplanarbitmapsourcetransform) 介面</span><span class="sxs-lookup"><span data-stu-id="9b96a-230">[**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/wincodec/nn-wincodec-iwicplanarbitmapsourcetransform) interface</span></span>

### <a name="support-for-block-compressed-formats-dds-files"></a><span data-ttu-id="9b96a-231">支援 (DDS 檔案的區塊壓縮格式) </span><span class="sxs-lookup"><span data-stu-id="9b96a-231">Support for block compressed formats (DDS files)</span></span>

<span data-ttu-id="9b96a-232">從 Windows 8.1 開始，Direct2D 支援包含 DXGI 格式的點陣圖 \_ \_ BC1 \_ UNORM、dxgi \_ 格式 \_ BC2 \_ UNORM 和 dxgi \_ 格式 \_ BC3 \_ UNORM 圖元資料。</span><span class="sxs-lookup"><span data-stu-id="9b96a-232">Starting in Windows 8.1, Direct2D provides support for bitmaps that contain DXGI\_FORMAT\_BC1\_UNORM, DXGI\_FORMAT\_BC2\_UNORM, and DXGI\_FORMAT\_BC3\_UNORM pixel data.</span></span> <span data-ttu-id="9b96a-233">應用程式可將其影像資產取代為區塊壓縮的 DDS 映射。</span><span class="sxs-lookup"><span data-stu-id="9b96a-233">Apps can replace their image assets with block compressed DDS images.</span></span> <span data-ttu-id="9b96a-234">這可大幅減少圖形記憶體耗用量和資源建立時間。</span><span class="sxs-lookup"><span data-stu-id="9b96a-234">This can significantly reduce graphics memory consumption and resource creation time.</span></span> <span data-ttu-id="9b96a-235">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="9b96a-235">For more information, see the following topics:</span></span>

-   <span data-ttu-id="9b96a-236">[**ID2D1DeviceCoNtext：： CreateBitmapFromWicBitmap**](id2d1devicecontext-createbitmapfromwicbitmap-overload.md) 方法</span><span class="sxs-lookup"><span data-stu-id="9b96a-236">[**ID2D1DeviceContext::CreateBitmapFromWicBitmap**](id2d1devicecontext-createbitmapfromwicbitmap-overload.md) method</span></span>
-   <span data-ttu-id="9b96a-237">[**IWICDdsFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsframedecode) 介面</span><span class="sxs-lookup"><span data-stu-id="9b96a-237">[**IWICDdsFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsframedecode) interface</span></span>

### <a name="rendering-priority"></a><span data-ttu-id="9b96a-238">轉譯優先權</span><span class="sxs-lookup"><span data-stu-id="9b96a-238">Rendering priority</span></span>

<span data-ttu-id="9b96a-239">從 Windows 8.1 開始，Direct2D 會提供對每個裝置轉譯優先權的支援。</span><span class="sxs-lookup"><span data-stu-id="9b96a-239">Starting in Windows 8.1, Direct2D provides support for per-device rendering priority.</span></span> <span data-ttu-id="9b96a-240">這項新功能可讓應用程式在一般轉譯優先順序之間切換裝置 (預設) 和低轉譯優先順序 (，裝置將不會在系統) 上封鎖其他轉譯工作。</span><span class="sxs-lookup"><span data-stu-id="9b96a-240">This new feature allows apps to switch a device between normal rendering priority (the default) and low rendering priority (in which the device will not block other rendering tasks on the system).</span></span> <span data-ttu-id="9b96a-241">建議應用程式對使用者回應性不重要的工作使用低轉譯優先順序，例如預先轉譯的內容、最小化的轉譯，以及通常在背景中執行的其他作業。</span><span class="sxs-lookup"><span data-stu-id="9b96a-241">It is recommended that apps use low rendering priority for tasks that are not critical to user-responsiveness, such as pre-rendering content, rendering while minimized, and other operations that are typically performed in the background.</span></span> <span data-ttu-id="9b96a-242">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="9b96a-242">For more information, see the following topics:</span></span>

-   <span data-ttu-id="9b96a-243">[**ID2D1Device1：： SetRenderingPriority**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1device1-setrenderingpriority) 方法</span><span class="sxs-lookup"><span data-stu-id="9b96a-243">[**ID2D1Device1::SetRenderingPriority**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1device1-setrenderingpriority) method</span></span>
-   <span data-ttu-id="9b96a-244">[**D2D1 \_轉譯 \_ 優先權**](/windows/desktop/api/D2D1_2/ne-d2d1_2-d2d1_rendering_priority) 列舉</span><span class="sxs-lookup"><span data-stu-id="9b96a-244">[**D2D1\_RENDERING\_PRIORITY**](/windows/desktop/api/D2D1_2/ne-d2d1_2-d2d1_rendering_priority) enumeration</span></span>

## <a name="whats-new-for-windows-8"></a><span data-ttu-id="9b96a-245">Windows 8 的新功能</span><span class="sxs-lookup"><span data-stu-id="9b96a-245">What's new for Windows 8</span></span>

<span data-ttu-id="9b96a-246">已針對 Windows 8 新增或更新下列功能和 Api。</span><span class="sxs-lookup"><span data-stu-id="9b96a-246">The following features and APIs were added or updated for Windows 8.</span></span>

<span data-ttu-id="9b96a-247">已安裝 [適用于 windows 7 的 Platform Update](/windows/desktop/direct3darticles/platform-update-for-windows-7) 的 windows 7 上支援新的 Direct2D 介面。</span><span class="sxs-lookup"><span data-stu-id="9b96a-247">The new Direct2D interfaces are supported on Windows 7 with the [Platform Update for Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7) installed.</span></span>

<span data-ttu-id="9b96a-248">裝置和裝置內容的 Direct2d 語義已更新為更接近 Direct3D 所使用的語法，以及在 Windows Store 應用程式上提供精確的操作。</span><span class="sxs-lookup"><span data-stu-id="9b96a-248">Direct2D's semantics for devices and device contexts have been updated to more closely resemble the semantics used by Direct3D, and to provide concise operation on Windows Store apps.</span></span> <span data-ttu-id="9b96a-249">如需詳細資訊，請參閱 [裝置和裝置](devices-and-device-contexts.md) 內容。</span><span class="sxs-lookup"><span data-stu-id="9b96a-249">See [Devices and device contexts](devices-and-device-contexts.md) for more info.</span></span>

<span data-ttu-id="9b96a-250">選取的相關 Api：</span><span class="sxs-lookup"><span data-stu-id="9b96a-250">Selected related APIs:</span></span>

-   [<span data-ttu-id="9b96a-251">**ID2D1Device**</span><span class="sxs-lookup"><span data-stu-id="9b96a-251">**ID2D1Device**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device)
-   [<span data-ttu-id="9b96a-252">**ID2D1DeviceCoNtext**</span><span class="sxs-lookup"><span data-stu-id="9b96a-252">**ID2D1DeviceContext**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)

<span data-ttu-id="9b96a-253">命令清單 API 可讓您在螢幕轉譯和列印時共用轉譯路徑。</span><span class="sxs-lookup"><span data-stu-id="9b96a-253">The command list API allows you to share the rendering path for on screen rendering and printing.</span></span> <span data-ttu-id="9b96a-254">它也可讓您使用基本專案來建立用來填滿基本專案的影像筆刷。</span><span class="sxs-lookup"><span data-stu-id="9b96a-254">It also allows you to use primitives to create an image brush for filling primitives.</span></span>

<span data-ttu-id="9b96a-255">選取的相關 Api：</span><span class="sxs-lookup"><span data-stu-id="9b96a-255">Selected related APIs:</span></span>

-   [<span data-ttu-id="9b96a-256">**ID2D1CommandList**</span><span class="sxs-lookup"><span data-stu-id="9b96a-256">**ID2D1CommandList**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist)
-   [<span data-ttu-id="9b96a-257">**ID2D1PrintControl**</span><span class="sxs-lookup"><span data-stu-id="9b96a-257">**ID2D1PrintControl**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol)
-   [<span data-ttu-id="9b96a-258">**ID2D1ImageBrush**</span><span class="sxs-lookup"><span data-stu-id="9b96a-258">**ID2D1ImageBrush**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush)

<span data-ttu-id="9b96a-259">[Direct2D 效果](effects-overview.md) 是一組 api，Windows 8 的新功能，可將高品質效果套用至影像。</span><span class="sxs-lookup"><span data-stu-id="9b96a-259">[Direct2D effects](effects-overview.md) is a set of APIs, new in Windows 8, for applying high quality effects to images.</span></span> <span data-ttu-id="9b96a-260">它也包含可讓您自行自訂效果的 Api。</span><span class="sxs-lookup"><span data-stu-id="9b96a-260">It also includes APIs that allow you to make your own custom effects.</span></span>

<span data-ttu-id="9b96a-261">選取的相關 Api：</span><span class="sxs-lookup"><span data-stu-id="9b96a-261">Selected related APIs:</span></span>

-   [<span data-ttu-id="9b96a-262">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="9b96a-262">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
-   [<span data-ttu-id="9b96a-263">**ID2D1EffectImpl**</span><span class="sxs-lookup"><span data-stu-id="9b96a-263">**ID2D1EffectImpl**</span></span>](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl)
-   [<span data-ttu-id="9b96a-264">**ID2D1EffectCoNtext**</span><span class="sxs-lookup"><span data-stu-id="9b96a-264">**ID2D1EffectContext**</span></span>](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext)

<span data-ttu-id="9b96a-265">從 Windows 8 開始，Direct2D 包含用於建立多執行緒應用程式的其他 Api。</span><span class="sxs-lookup"><span data-stu-id="9b96a-265">Starting with Windows 8, Direct2D includes additional APIs for building multithreaded apps.</span></span> <span data-ttu-id="9b96a-266">如需詳細資訊，請參閱多 [執行緒 Direct2D 應用程式](multi-threaded-direct2d-apps.md) 。</span><span class="sxs-lookup"><span data-stu-id="9b96a-266">See [Multithreaded Direct2D Apps](multi-threaded-direct2d-apps.md) for more info.</span></span>

<span data-ttu-id="9b96a-267">選取的相關 Api：</span><span class="sxs-lookup"><span data-stu-id="9b96a-267">Selected related APIs:</span></span>

-   [<span data-ttu-id="9b96a-268">**ID2D1MultiThread**</span><span class="sxs-lookup"><span data-stu-id="9b96a-268">**ID2D1MultiThread**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1multithread)
-   [<span data-ttu-id="9b96a-269">**D2D1 \_ FACTORY \_ 類型 \_ 多 \_ 執行緒**</span><span class="sxs-lookup"><span data-stu-id="9b96a-269">**D2D1\_FACTORY\_TYPE\_MULTI\_THREADED**</span></span>](/windows/desktop/api/d2d1/ne-d2d1-d2d1_factory_type)

 

 