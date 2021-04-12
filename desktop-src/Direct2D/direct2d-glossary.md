---
title: Direct2D 詞彙
description: 描述 Direct2D 檔一般使用的詞彙。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2e884390-56e4-45ae-b1c9-c58503d6f2dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd2fdaf284fee71724d7b9bb4ac4b5ad1100c82
ms.sourcegitcommit: fdd00b445ee88366e9cdd1eed0cb3e42e2a73eca
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2019
ms.locfileid: "104462672"
---
# <a name="direct2d-glossary"></a><span data-ttu-id="0148d-103">Direct2D 詞彙</span><span class="sxs-lookup"><span data-stu-id="0148d-103">Direct2D Glossary</span></span>

<dl> <dt>

<span data-ttu-id="0148d-104"><span id="direct2d.direct2d_glossary_a8_target"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_A8_TARGET"></span>**A8 目標**</span><span class="sxs-lookup"><span data-stu-id="0148d-104"><span id="direct2d.direct2d_glossary_a8_target"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_A8_TARGET"></span>**A8 target**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-105">轉譯目標，其使用像素格式來代表8位的 Alpha 色板。</span><span class="sxs-lookup"><span data-stu-id="0148d-105">A render target that uses a pixel format representing an alpha channel with eight bits.</span></span> <span data-ttu-id="0148d-106">A8 目標適用于將幾何繪製為遮罩。</span><span class="sxs-lookup"><span data-stu-id="0148d-106">A8 targets are useful for drawing geometries as masks.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-107"><span id="direct2d.direct2d_glossary_aliasing"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_ALIASING"></span>**混 疊**</span><span class="sxs-lookup"><span data-stu-id="0148d-107"><span id="direct2d.direct2d_glossary_aliasing"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_ALIASING"></span>**aliasing**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-108">在電腦圖形中，曲線或對角線線的不規則外觀。</span><span class="sxs-lookup"><span data-stu-id="0148d-108">In computer graphics, the jagged appearance of curves or diagonal lines.</span></span> <span data-ttu-id="0148d-109">較低的解析度最能看到別名。</span><span class="sxs-lookup"><span data-stu-id="0148d-109">Aliasing is most visible at lower resolutions.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-110"><span id="direct2d.direct2d_glossary_antialiasing"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_ANTIALIASING"></span>**消除鋸齒**</span><span class="sxs-lookup"><span data-stu-id="0148d-110"><span id="direct2d.direct2d_glossary_antialiasing"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_ANTIALIASING"></span>**antialiasing**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-111">將曲線或對角線的不規則外觀平滑化的技巧。</span><span class="sxs-lookup"><span data-stu-id="0148d-111">A technique for smoothing the jagged appearance of curved or diagonal lines.</span></span> <span data-ttu-id="0148d-112">消除鋸齒的方法包括使用中繼陰影的周圍圖元，以及操作圖元的大小和水準對齊。</span><span class="sxs-lookup"><span data-stu-id="0148d-112">Methods of antialiasing include surrounding pixels with intermediate shades and manipulating the size and horizontal alignment of the pixels.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-113"><span id="direct2d.direct2d_glossary_batch"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_BATCH"></span>**批**</span><span class="sxs-lookup"><span data-stu-id="0148d-113"><span id="direct2d.direct2d_glossary_batch"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_BATCH"></span>**batch**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-114">分組在一起的一組要求或交易。</span><span class="sxs-lookup"><span data-stu-id="0148d-114">A set of requests or transactions that have been grouped together.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-115"><span id="direct2d.direct2d_glossary_bitmap"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_BITMAP"></span>**點陣圖**</span><span class="sxs-lookup"><span data-stu-id="0148d-115"><span id="direct2d.direct2d_glossary_bitmap"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_BITMAP"></span>**bitmap**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-116">以個別圖元表示的字元或圖形。</span><span class="sxs-lookup"><span data-stu-id="0148d-116">A representation of characters or graphics by individual pixels.</span></span> <span data-ttu-id="0148d-117">您可以在資料行中水準、以資料列或垂直方式排列圖元。</span><span class="sxs-lookup"><span data-stu-id="0148d-117">The pixels can be arranged horizontally, in rows, or vertically, in columns.</span></span> <span data-ttu-id="0148d-118">每個圖元可以用一或多個位表示。</span><span class="sxs-lookup"><span data-stu-id="0148d-118">Each pixel can be represented by one or more bits.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-119"><span id="direct2d.direct2d_glossary_bits_per_pixel__bpp_"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_BITS_PER_PIXEL__BPP_"></span>**每圖元的位數 (bpp)**</span><span class="sxs-lookup"><span data-stu-id="0148d-119"><span id="direct2d.direct2d_glossary_bits_per_pixel__bpp_"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_BITS_PER_PIXEL__BPP_"></span>**bits per pixel (bpp)**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-120">用來儲存和顯示單一圖元色彩資料的位數。</span><span class="sxs-lookup"><span data-stu-id="0148d-120">The number of bits that are used to store and display the color data for a single pixel.</span></span> <span data-ttu-id="0148d-121">這是位深度的標準測量單位 (也稱為色彩深度) 。</span><span class="sxs-lookup"><span data-stu-id="0148d-121">This is the standard unit of measurement for bit depth (also called color depth).</span></span> <span data-ttu-id="0148d-122">常見的位深度包括8、16和32。</span><span class="sxs-lookup"><span data-stu-id="0148d-122">Common bit depths include 8, 16, and 32.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-123"><span id="direct2d.direct2d_glossary_brush"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_BRUSH"></span>**刷**</span><span class="sxs-lookup"><span data-stu-id="0148d-123"><span id="direct2d.direct2d_glossary_brush"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_BRUSH"></span>**brush**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-124">使用純色、漸層或點陣圖繪製無限平面的 Direct2D 資源。</span><span class="sxs-lookup"><span data-stu-id="0148d-124">A Direct2D resource that paints an infinite plane with a solid color, a gradient, or a bitmap.</span></span> <span data-ttu-id="0148d-125">筆刷通常用來對幾何進行筆觸和填滿。</span><span class="sxs-lookup"><span data-stu-id="0148d-125">A brush is typically used to stroke and fill a geometry.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-126"><span id="direct2d.direct2d_glossary_cleartype"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_CLEARTYPE"></span>**清晰**</span><span class="sxs-lookup"><span data-stu-id="0148d-126"><span id="direct2d.direct2d_glossary_cleartype"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_CLEARTYPE"></span>**ClearType**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-127">字型顯示技術可大幅改善字型顯示解析度，讓電腦螢幕上的字母看似平滑，而非不規則。</span><span class="sxs-lookup"><span data-stu-id="0148d-127">A font display technology that dramatically improves font display resolution, such that letters on the computer screen appear smooth, not jagged.</span></span> <span data-ttu-id="0148d-128">ClearType 改進了具有數位介面（例如膝上型電腦監視器和高品質平面桌面監視器）之 LCD 顯示器上的文字外觀。</span><span class="sxs-lookup"><span data-stu-id="0148d-128">ClearType improves text appearance on LCD monitors that have a digital interface, such as laptop monitors and high-quality flat-panel desktop monitors.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-129"><span id="direct2d.direct2d_glossary_dc"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_DC"></span>**直流**</span><span class="sxs-lookup"><span data-stu-id="0148d-129"><span id="direct2d.direct2d_glossary_dc"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_DC"></span>**DC**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-130">請參閱：裝置內容的定義。</span><span class="sxs-lookup"><span data-stu-id="0148d-130">See definition for: device context.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-131"><span id="direct2d.direct2d_glossary_device_context__dc_"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_DEVICE_CONTEXT__DC_"></span>**裝置內容 (DC)**</span><span class="sxs-lookup"><span data-stu-id="0148d-131"><span id="direct2d.direct2d_glossary_device_context__dc_"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_DEVICE_CONTEXT__DC_"></span>**device context (DC)**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-132">GDI 裝置內容。</span><span class="sxs-lookup"><span data-stu-id="0148d-132">A GDI device context.</span></span> <span data-ttu-id="0148d-133">另請參閱：圖形裝置介面。</span><span class="sxs-lookup"><span data-stu-id="0148d-133">See also: Graphics Device Interface.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-134"><span id="direct2d.direct2d_glossary_direct2d"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_DIRECT2D"></span>**Direct2D**</span><span class="sxs-lookup"><span data-stu-id="0148d-134"><span id="direct2d.direct2d_glossary_direct2d"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_DIRECT2D"></span>**Direct2D**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-135">硬體加速、立即模式的2-d 轉譯 API。</span><span class="sxs-lookup"><span data-stu-id="0148d-135">A hardware-accelerated, immediate-mode 2-D rendering API.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-136"><span id="direct2d.direct2d_glossary_direct3d"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_DIRECT3D"></span>**Direct3D**</span><span class="sxs-lookup"><span data-stu-id="0148d-136"><span id="direct2d.direct2d_glossary_direct3d"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_DIRECT3D"></span>**Direct3D**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-137">Windows 中3D 圖形的硬體加速平臺和執行時間。</span><span class="sxs-lookup"><span data-stu-id="0148d-137">The hardware acceleration platform and runtime for 3-D graphics in Windows.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-138"><span id="direct2d.direct2d_glossary_directwrite"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_DIRECTWRITE"></span>**DirectWrite**</span><span class="sxs-lookup"><span data-stu-id="0148d-138"><span id="direct2d.direct2d_glossary_directwrite"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_DIRECTWRITE"></span>**DirectWrite**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-139">提供文字轉譯、字型管理和文字版面配置支援的文字 API，與任何特定轉譯系統無關。</span><span class="sxs-lookup"><span data-stu-id="0148d-139">A text API that provides text rendering, font management, and text layout support that is independent of any specific rendering system.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-140"><span id="direct2d.direct2d_glossary_directx_graphics_infrastructure__dxgi_"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_DIRECTX_GRAPHICS_INFRASTRUCTURE__DXGI_"></span>**DirectX Graphic Infrastructure (DXGI)**</span><span class="sxs-lookup"><span data-stu-id="0148d-140"><span id="direct2d.direct2d_glossary_directx_graphics_infrastructure__dxgi_"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_DIRECTX_GRAPHICS_INFRASTRUCTURE__DXGI_"></span>**DirectX Graphics Infrastructure (DXGI)**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-141">管理與 DirectX 圖形執行時間無關之低層級圖形相關工作的基礎結構。</span><span class="sxs-lookup"><span data-stu-id="0148d-141">The infrastructure that manages the low-level graphics-related tasks that are independent of the DirectX graphics runtime.</span></span> <span data-ttu-id="0148d-142">DXGI 提供圖形元件的通用架構。</span><span class="sxs-lookup"><span data-stu-id="0148d-142">DXGI provides a common framework for graphics components.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-143"><span id="direct2d.direct2d_glossary_dxgi"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_DXGI"></span>**DXGI**</span><span class="sxs-lookup"><span data-stu-id="0148d-143"><span id="direct2d.direct2d_glossary_dxgi"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_DXGI"></span>**DXGI**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-144">請參閱： DirectX Graphic Infrastructure (DXGI) 的定義。</span><span class="sxs-lookup"><span data-stu-id="0148d-144">See definition for: DirectX Graphics Infrastructure (DXGI).</span></span>

</dd> <dt>

<span data-ttu-id="0148d-145"><span id="direct2d.direct2d_glossary_figure"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_FIGURE"></span>**圖**</span><span class="sxs-lookup"><span data-stu-id="0148d-145"><span id="direct2d.direct2d_glossary_figure"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_FIGURE"></span>**figure**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-146">由起始點和區段集合所定義的開啟或關閉圖形。</span><span class="sxs-lookup"><span data-stu-id="0148d-146">An open or closed shape defined by a start point and a collection of segments.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-147"><span id="direct2d.direct2d_glossary_flatten"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_FLATTEN"></span>**扁平 化**</span><span class="sxs-lookup"><span data-stu-id="0148d-147"><span id="direct2d.direct2d_glossary_flatten"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_FLATTEN"></span>**flatten**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-148">產生 (可能的弧形) 幾何的多邊形近似值。</span><span class="sxs-lookup"><span data-stu-id="0148d-148">To generate a polygonal approximation of a (potentially curved) geometry.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-149"><span id="direct2d.direct2d_glossary_gdi"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_GDI"></span>**Gdi**</span><span class="sxs-lookup"><span data-stu-id="0148d-149"><span id="direct2d.direct2d_glossary_gdi"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_GDI"></span>**GDI**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-150">請參閱：圖形裝置介面 (GDI) 的定義。</span><span class="sxs-lookup"><span data-stu-id="0148d-150">See definition for: Graphics Device Interface (GDI).</span></span>

</dd> <dt>

<span data-ttu-id="0148d-151"><span id="direct2d.direct2d_glossary_geometric_mask"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_GEOMETRIC_MASK"></span>**幾何遮罩**</span><span class="sxs-lookup"><span data-stu-id="0148d-151"><span id="direct2d.direct2d_glossary_geometric_mask"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_GEOMETRIC_MASK"></span>**geometric mask**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-152">ID2D1Geometry 物件所定義的剪輯或裁剪，會在轉譯目標繪製圖層時遮罩該圖層。</span><span class="sxs-lookup"><span data-stu-id="0148d-152">A clip or a cutout, defined by an ID2D1Geometry object, that masks a layer when it is drawn by a render target.</span></span> <span data-ttu-id="0148d-153">幾何遮罩可以是別名或有子圖元邊緣。</span><span class="sxs-lookup"><span data-stu-id="0148d-153">A geometric mask can be either aliased or have sub-pixel edges.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-154"><span id="direct2d.direct2d_glossary_geometry_transform"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_GEOMETRY_TRANSFORM"></span>**幾何轉換**</span><span class="sxs-lookup"><span data-stu-id="0148d-154"><span id="direct2d.direct2d_glossary_geometry_transform"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_GEOMETRY_TRANSFORM"></span>**geometry transform**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-155">在繪製或填滿幾何之前套用至幾何的轉換。</span><span class="sxs-lookup"><span data-stu-id="0148d-155">A transform that is applied to a geometry before it is stroked or filled.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-156"><span id="direct2d.direct2d_glossary_glyph"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_GLYPH"></span>**字形**</span><span class="sxs-lookup"><span data-stu-id="0148d-156"><span id="direct2d.direct2d_glossary_glyph"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_GLYPH"></span>**glyph**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-157">字元、字元的一部分或字元序列的圖形標記法。</span><span class="sxs-lookup"><span data-stu-id="0148d-157">A graphical representation of a character, part of a character, or sequence of characters.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-158"><span id="direct2d.direct2d_glossary_glyph_run"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_GLYPH_RUN"></span>**圖像執行**</span><span class="sxs-lookup"><span data-stu-id="0148d-158"><span id="direct2d.direct2d_glossary_glyph_run"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_GLYPH_RUN"></span>**glyph run**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-159">會連續執行共用通用格式的圖像。</span><span class="sxs-lookup"><span data-stu-id="0148d-159">A continuous run of glyphs that share a common format.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-160"><span id="direct2d.direct2d_glossary_gradient_brush"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_GRADIENT_BRUSH"></span>**漸層筆刷**</span><span class="sxs-lookup"><span data-stu-id="0148d-160"><span id="direct2d.direct2d_glossary_gradient_brush"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_GRADIENT_BRUSH"></span>**gradient brush**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-161">以漸進方式繪製區域的筆刷，從某種色彩到另一種色彩，或從某個陰影到相同色彩的另一個陰影。</span><span class="sxs-lookup"><span data-stu-id="0148d-161">A brush that paints an area in a gradual progression from one color to another or from one shade to another shade of the same color.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-162"><span id="direct2d.direct2d_glossary_gradient_stop"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_GRADIENT_STOP"></span>**漸層停駐點**</span><span class="sxs-lookup"><span data-stu-id="0148d-162"><span id="direct2d.direct2d_glossary_gradient_stop"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_GRADIENT_STOP"></span>**gradient stop**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-163">為漸層區域內的位置定義的特定色彩。</span><span class="sxs-lookup"><span data-stu-id="0148d-163">A specific color that is defined for a location within the gradient region.</span></span> <span data-ttu-id="0148d-164">漸層停駐點是用來定義沿著漸層路徑的特定位置的色彩。</span><span class="sxs-lookup"><span data-stu-id="0148d-164">Gradient stops are used to define the color at specific locations along the gradient path.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-165"><span id="direct2d.direct2d_glossary_grahics_primitive"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_GRAHICS_PRIMITIVE"></span>**grahics 基本**</span><span class="sxs-lookup"><span data-stu-id="0148d-165"><span id="direct2d.direct2d_glossary_grahics_primitive"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_GRAHICS_PRIMITIVE"></span>**grahics primitive**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-166">在電腦圖形中，圖形（例如線條、圓形、曲線或多邊形），圖形介面卡可以繪製、儲存和操作為離散實體。</span><span class="sxs-lookup"><span data-stu-id="0148d-166">In computer graphics, a shape such as a line, circle, curve, or polygon that a graphics adapter can draw, store, and manipulate as a discrete entity.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-167"><span id="direct2d.direct2d_glossary_graphics_device_interface__gdi_"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_GRAPHICS_DEVICE_INTERFACE__GDI_"></span>**圖形裝置介面 (GDI)**</span><span class="sxs-lookup"><span data-stu-id="0148d-167"><span id="direct2d.direct2d_glossary_graphics_device_interface__gdi_"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_GRAPHICS_DEVICE_INTERFACE__GDI_"></span>**Graphics Device Interface (GDI)**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-168">圖形 API，可讓應用程式傳送圖形命令至顯示器或列印裝置，通常不需要考慮其規格或功能。</span><span class="sxs-lookup"><span data-stu-id="0148d-168">A graphics API that enables applications to send graphics commands to a display or printing device, generally without consideration for its specifications or capabilities.</span></span> <span data-ttu-id="0148d-169">Microsoft Win32 GDI 會接收來自應用程式的轉譯要求，並將這些要求傳遞至核心模式 GDI。</span><span class="sxs-lookup"><span data-stu-id="0148d-169">A Microsoft Win32 GDI receives rendering requests from applications and passes those requests to the kernel-mode GDI.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-170"><span id="direct2d.direct2d_glossary_handle_to_a_device_context__hdc_"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_HANDLE_TO_A_DEVICE_CONTEXT__HDC_"></span>**(HDC) 的裝置內容控制碼**</span><span class="sxs-lookup"><span data-stu-id="0148d-170"><span id="direct2d.direct2d_glossary_handle_to_a_device_context__hdc_"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_HANDLE_TO_A_DEVICE_CONTEXT__HDC_"></span>**handle to a device context (HDC)**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-171">GDI 裝置內容的參考。</span><span class="sxs-lookup"><span data-stu-id="0148d-171">A reference to a GDI device context.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-172"><span id="direct2d.direct2d_glossary_hdc"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_HDC"></span>**HDC**</span><span class="sxs-lookup"><span data-stu-id="0148d-172"><span id="direct2d.direct2d_glossary_hdc"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_HDC"></span>**HDC**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-173">請參閱：對裝置內容之控制碼的定義。</span><span class="sxs-lookup"><span data-stu-id="0148d-173">See definition for: handle to a device context.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-174"><span id="direct2d.direct2d_glossary_mesh"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_MESH"></span>**網 格**</span><span class="sxs-lookup"><span data-stu-id="0148d-174"><span id="direct2d.direct2d_glossary_mesh"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_MESH"></span>**mesh**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-175">頂點的集合，定義構成圖形的一組三角形。</span><span class="sxs-lookup"><span data-stu-id="0148d-175">A collection of vertices that define a set of triangles that constitute a shape.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-176"><span id="direct2d.direct2d_glossary_multi-sample_anti-aliasing__msaa_"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_MULTI-SAMPLE_ANTI-ALIASING__MSAA_"></span>**多範例消除鋸齒 (MSAA)**</span><span class="sxs-lookup"><span data-stu-id="0148d-176"><span id="direct2d.direct2d_glossary_multi-sample_anti-aliasing__msaa_"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_MULTI-SAMPLE_ANTI-ALIASING__MSAA_"></span>**Multi-Sample Anti-Aliasing (MSAA)**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-177">處理整個場景的消除鋸齒技術。</span><span class="sxs-lookup"><span data-stu-id="0148d-177">An antialiasing technique that processes an entire scene.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-178"><span id="direct2d.direct2d_glossary_opacity_mask"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_OPACITY_MASK"></span>**不透明度遮罩**</span><span class="sxs-lookup"><span data-stu-id="0148d-178"><span id="direct2d.direct2d_glossary_opacity_mask"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_OPACITY_MASK"></span>**opacity mask**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-179">由筆刷或點陣圖描述的遮罩，會套用到另一個物件，使該物件部分或完全透明。</span><span class="sxs-lookup"><span data-stu-id="0148d-179">A mask, described by a brush or bitmap, that is applied to another object to make that object partially or completely transparent.</span></span> <span data-ttu-id="0148d-180">不透明度遮罩會使用 Alpha 色板資訊來指定如何將物件的來源圖元混合到最後的目的地目標。</span><span class="sxs-lookup"><span data-stu-id="0148d-180">An opacity mask uses alpha channel information to specify how the source pixels of the object are blended into the final destination target.</span></span> <span data-ttu-id="0148d-181">遮罩的透明部分表示隱藏基礎影像的區域，而遮罩的不透明部分則表示允許遮罩物件的位置。</span><span class="sxs-lookup"><span data-stu-id="0148d-181">The transparent portions of the mask indicate the areas where the underlying image is hidden, whereas the opaque portions of the mask indicate where the masked object is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-182"><span id="direct2d.direct2d_glossary_per_primitive_anti-aliasing__ppaa_"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_PER_PRIMITIVE_ANTI-ALIASING__PPAA_"></span>**每一基本的消除鋸齒 (PPAA)**</span><span class="sxs-lookup"><span data-stu-id="0148d-182"><span id="direct2d.direct2d_glossary_per_primitive_anti-aliasing__ppaa_"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_PER_PRIMITIVE_ANTI-ALIASING__PPAA_"></span>**Per Primitive Anti-Aliasing (PPAA)**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-183">適用于每個個別圖形基本型別的消除鋸齒技術，而不是整個場景。</span><span class="sxs-lookup"><span data-stu-id="0148d-183">An antialiasing technique that is applied to each individual graphics primitive rather than an entire scene.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-184"><span id="direct2d.direct2d_glossary_radial_gradient_brush"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_RADIAL_GRADIENT_BRUSH"></span>**放射狀漸層筆刷**</span><span class="sxs-lookup"><span data-stu-id="0148d-184"><span id="direct2d.direct2d_glossary_radial_gradient_brush"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_RADIAL_GRADIENT_BRUSH"></span>**radial gradient brush**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-185">漸層，其中的起點是由焦點定義，而結束點是由漸層定義。</span><span class="sxs-lookup"><span data-stu-id="0148d-185">A gradient where the start point is defined by a focal point and the end point is defined by a gradient.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-186"><span id="direct2d.direct2d_glossary_render_target"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_RENDER_TARGET"></span>**呈現目標**</span><span class="sxs-lookup"><span data-stu-id="0148d-186"><span id="direct2d.direct2d_glossary_render_target"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_RENDER_TARGET"></span>**render target**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-187">發出繪製命令的 Direct2D 資源。</span><span class="sxs-lookup"><span data-stu-id="0148d-187">A Direct2D resource that issues drawing commands.</span></span> <span data-ttu-id="0148d-188">轉譯目標有不同的類型，每個都呈現不同的目的地。</span><span class="sxs-lookup"><span data-stu-id="0148d-188">There are different types of render targets, each rendering to a different destination.</span></span> <span data-ttu-id="0148d-189">例如，ID2D1HwndRenderTarget 會呈現至視窗，而 ID2D1BitmapRenderTarget 會轉譯成點陣圖。</span><span class="sxs-lookup"><span data-stu-id="0148d-189">For example, an ID2D1HwndRenderTarget renders to a window, and an ID2D1BitmapRenderTarget renders to a bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-190"><span id="direct2d.direct2d_glossary_segment"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_SEGMENT"></span>**段**</span><span class="sxs-lookup"><span data-stu-id="0148d-190"><span id="direct2d.direct2d_glossary_segment"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_SEGMENT"></span>**segment**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-191">幾何路徑的一部分，由開始點和結束點定義。</span><span class="sxs-lookup"><span data-stu-id="0148d-191">A portion of a geometric path, defined by the start and end points.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-192"><span id="direct2d.direct2d_glossary_tessellate"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_TESSELLATE"></span>**tessellate**</span><span class="sxs-lookup"><span data-stu-id="0148d-192"><span id="direct2d.direct2d_glossary_tessellate"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_TESSELLATE"></span>**tessellate**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-193">將圖形分成三角形的集合。</span><span class="sxs-lookup"><span data-stu-id="0148d-193">To break a shape into a collection of triangles.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-194"><span id="direct2d.direct2d_glossary_transform"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_TRANSFORM"></span>**變換**</span><span class="sxs-lookup"><span data-stu-id="0148d-194"><span id="direct2d.direct2d_glossary_transform"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_TRANSFORM"></span>**transform**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-195">表示多維度中線性對應的矩陣。</span><span class="sxs-lookup"><span data-stu-id="0148d-195">A matrix that represents a linear mapping in a number of dimensions.</span></span> <span data-ttu-id="0148d-196">Direct2D 會使用由2到3的矩陣，將 API 限制為仿射的 deformations。</span><span class="sxs-lookup"><span data-stu-id="0148d-196">Direct2D uses a 2-by-3 matrix, which limits the API to those deformations that are affine.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-197"><span id="direct2d.direct2d_glossary_translation"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_TRANSLATION"></span>**翻譯**</span><span class="sxs-lookup"><span data-stu-id="0148d-197"><span id="direct2d.direct2d_glossary_translation"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_TRANSLATION"></span>**translation**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-198">使用轉換矩陣來移動物件的處理常式。</span><span class="sxs-lookup"><span data-stu-id="0148d-198">The process of using a transformation matrix to move an object.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-199"><span id="direct2d.direct2d_glossary_vertex"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_VERTEX"></span>**頂點**</span><span class="sxs-lookup"><span data-stu-id="0148d-199"><span id="direct2d.direct2d_glossary_vertex"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_VERTEX"></span>**vertex**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-200">曲線的最高點、曲線結束的點，或兩個區段在多邊形或自由路徑中符合的點。</span><span class="sxs-lookup"><span data-stu-id="0148d-200">The highest point of a curve, the point where a curve ends, or the point where two segments meet in a polygon or a freeform path.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-201"><span id="direct2d.direct2d_glossary_vertex_shader"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_VERTEX_SHADER"></span>**頂點著色器**</span><span class="sxs-lookup"><span data-stu-id="0148d-201"><span id="direct2d.direct2d_glossary_vertex_shader"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_VERTEX_SHADER"></span>**vertex shader**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-202">一種可程式化的著色器，其中包含一組在每個頂點的 GPU 上執行的組解碼指令，以及目前繪製呼叫的每個圖元。</span><span class="sxs-lookup"><span data-stu-id="0148d-202">A type of programmable shader that contains a set of assembly instructions that are run on the GPU per vertex and per pixel for the current draw call.</span></span> <span data-ttu-id="0148d-203">頂點著色器會將大量計算從 CPU 卸載至 GPU。</span><span class="sxs-lookup"><span data-stu-id="0148d-203">A vertex shader offloads intensive calculations from CPU to GPU.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-204"><span id="direct2d.direct2d_glossary_windows_imaging_component__wic_"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_WINDOWS_IMAGING_COMPONENT__WIC_"></span>**Windows 影像處理元件 (WIC)**</span><span class="sxs-lookup"><span data-stu-id="0148d-204"><span id="direct2d.direct2d_glossary_windows_imaging_component__wic_"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_WINDOWS_IMAGING_COMPONENT__WIC_"></span>**Windows Imaging Component (WIC)**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-205">此 API 可讓應用程式 (1) 顯示和編輯已安裝 WIC 相容編解碼器的任何影像格式，以及 (2) 讀取和寫入中繼資料或影像檔案。</span><span class="sxs-lookup"><span data-stu-id="0148d-205">An API that enables applications to (1) display and edit any image format for which a WIC-compliant CODEC is installed, and to (2) read and write metadata or image files.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-206"><span id="direct2d.direct2d_glossary_xml_paper_specification__xps_"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_XML_PAPER_SPECIFICATION__XPS_"></span>**XML 檔規格 (XPS)**</span><span class="sxs-lookup"><span data-stu-id="0148d-206"><span id="direct2d.direct2d_glossary_xml_paper_specification__xps_"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_XML_PAPER_SPECIFICATION__XPS_"></span>**XML Paper Specification (XPS)**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-207">XML 檔規格所描述的檔案格式，可用來儲存檔、處理檔以進行列印，以及列印檔案。</span><span class="sxs-lookup"><span data-stu-id="0148d-207">A document format, described by the XML Paper Specification, that can be used to store documents, to process them for printing, and to print them.</span></span>

</dd> <dt>

<span data-ttu-id="0148d-208"><span id="direct2d.direct2d_glossary_xps"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_XPS"></span>**Xps**</span><span class="sxs-lookup"><span data-stu-id="0148d-208"><span id="direct2d.direct2d_glossary_xps"></span><span id="DIRECT2D.DIRECT2D_GLOSSARY_XPS"></span>**XPS**</span></span>
</dt> <dd>

<span data-ttu-id="0148d-209">請參閱： XML 檔規格 (XPS) 的定義。</span><span class="sxs-lookup"><span data-stu-id="0148d-209">See definition for: XML Paper Specification (XPS).</span></span>

</dd> </dl>

 

 




