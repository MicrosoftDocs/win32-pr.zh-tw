---
description: 點陣圖是可以選取到裝置內容 (DC) 的其中一個 GDI 物件。
ms.assetid: 36afaabc-1334-42d1-8004-7952ce3c119e
title: 關於點陣圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53dbba516734dc255ce33005a7a9073865765785
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512465"
---
# <a name="about-bitmaps"></a><span data-ttu-id="76812-103">關於點陣圖</span><span class="sxs-lookup"><span data-stu-id="76812-103">About Bitmaps</span></span>

<span data-ttu-id="76812-104">點陣圖是可以選取到 *裝置內容* (DC) 的其中一個 GDI 物件。</span><span class="sxs-lookup"><span data-stu-id="76812-104">A bitmap is one of the GDI objects that can be selected into a *device context* (DC).</span></span> <span data-ttu-id="76812-105">[裝置](device-contexts.md) 內容是定義一組繪圖物件與其相關聯屬性的結構，以及影響輸出的圖形模式。</span><span class="sxs-lookup"><span data-stu-id="76812-105">[Device contexts](device-contexts.md) are structures that define a set of graphic objects and their associated attributes, and graphic modes that affect output.</span></span> <span data-ttu-id="76812-106">下表說明可在裝置內容中選取的 GDI 物件。</span><span class="sxs-lookup"><span data-stu-id="76812-106">The table below describes the GDI objects that can be selected into a device context.</span></span>



| <span data-ttu-id="76812-107">繪圖物件</span><span class="sxs-lookup"><span data-stu-id="76812-107">Graphic object</span></span>                         | <span data-ttu-id="76812-108">Description</span><span class="sxs-lookup"><span data-stu-id="76812-108">Description</span></span>                                                                                                                                                                                          |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="76812-109">點陣圖</span><span class="sxs-lookup"><span data-stu-id="76812-109">Bitmaps</span></span>](bitmaps.md)                 | <span data-ttu-id="76812-110">建立、操控 (縮放、滾動、旋轉和繪製) ，並將影像儲存為磁片上的檔案。</span><span class="sxs-lookup"><span data-stu-id="76812-110">Creates, manipulates (scale, scroll, rotate, and paint), and stores images as files on a disk.</span></span>                                                                                                       |
| [<span data-ttu-id="76812-111">筆刷</span><span class="sxs-lookup"><span data-stu-id="76812-111">Brushes</span></span>](brushes.md)                 | <span data-ttu-id="76812-112">繪製多邊形、橢圓形和路徑的內部。</span><span class="sxs-lookup"><span data-stu-id="76812-112">Paints the interior of polygons, ellipses, and paths.</span></span>                                                                                                                                                |
| [<span data-ttu-id="76812-113">字型</span><span class="sxs-lookup"><span data-stu-id="76812-113">Fonts</span></span>](fonts-and-text.md)            | <span data-ttu-id="76812-114">在影片顯示器和其他輸出裝置上繪製文字。</span><span class="sxs-lookup"><span data-stu-id="76812-114">Draws text on video displays and other output devices.</span></span>                                                                                                                                               |
| [<span data-ttu-id="76812-115">邏輯調色板</span><span class="sxs-lookup"><span data-stu-id="76812-115">Logical Palette</span></span>](logical-palette.md) | <span data-ttu-id="76812-116">由應用程式建立並與指定的裝置內容相關聯的調色板。</span><span class="sxs-lookup"><span data-stu-id="76812-116">A color palette created by an application and associated with a given device context.</span></span>                                                                                                                |
| [<span data-ttu-id="76812-117">路徑</span><span class="sxs-lookup"><span data-stu-id="76812-117">Paths</span></span>](paths.md)                     | <span data-ttu-id="76812-118">一或多個圖形 (或圖形) 填滿及/或勾勒出。</span><span class="sxs-lookup"><span data-stu-id="76812-118">One or more figures (or shapes) that are filled and/or outlined.</span></span>                                                                                                                                     |
| [<span data-ttu-id="76812-119">手寫筆</span><span class="sxs-lookup"><span data-stu-id="76812-119">Pens</span></span>](pens.md)                       | <span data-ttu-id="76812-120">應用程式用來繪製線條和曲線的圖形工具。</span><span class="sxs-lookup"><span data-stu-id="76812-120">A graphics tool that an application uses to draw lines and curves.</span></span>                                                                                                                                   |
| [<span data-ttu-id="76812-121">區域</span><span class="sxs-lookup"><span data-stu-id="76812-121">Regions</span></span>](regions.md)                 | <span data-ttu-id="76812-122">矩形、多邊形或橢圓形 (或兩個或多個圖形的組合) 可進行填滿、繪製、反轉、框住，以及用來執行點擊測試 (測試資料指標位置) 。</span><span class="sxs-lookup"><span data-stu-id="76812-122">A rectangle, polygon, or ellipse (or a combination of two or more of these shapes) that can be filled, painted, inverted, framed, and used to perform hit testing (testing for the cursor location).</span></span> |



 

<span data-ttu-id="76812-123">從開發人員的觀點來看，點陣圖是由指定或包含下列元素的結構集合所組成：</span><span class="sxs-lookup"><span data-stu-id="76812-123">From a developer's perspective, a bitmap consists of a collection of structures that specify or contain the following elements:</span></span>

-   <span data-ttu-id="76812-124">描述建立圖元矩形的裝置解析度、矩形的維度、位陣列的大小等等的標頭（標頭）。</span><span class="sxs-lookup"><span data-stu-id="76812-124">A header that describes the resolution of the device on which the rectangle of pixels was created, the dimensions of the rectangle, the size of the array of bits, and so on.</span></span>
-   <span data-ttu-id="76812-125">邏輯調色板。</span><span class="sxs-lookup"><span data-stu-id="76812-125">A logical palette.</span></span>
-   <span data-ttu-id="76812-126">位的陣列，定義點陣圖影像中的圖元與邏輯調色板中的專案之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="76812-126">An array of bits that defines the relationship between pixels in the bitmapped image and entries in the logical palette.</span></span>

<span data-ttu-id="76812-127">點陣圖大小與它所包含之影像的類型有關。</span><span class="sxs-lookup"><span data-stu-id="76812-127">A bitmap size is related to the type of image it contains.</span></span> <span data-ttu-id="76812-128">點陣圖影像可以是單色或彩色。</span><span class="sxs-lookup"><span data-stu-id="76812-128">Bitmap images can be either monochrome or color.</span></span> <span data-ttu-id="76812-129">在影像中，每個圖元都對應到點陣圖中的一個或多個位。</span><span class="sxs-lookup"><span data-stu-id="76812-129">In an image, each pixel corresponds to one or more bits in a bitmap.</span></span> <span data-ttu-id="76812-130">單色影像的比率為每圖元1位， (bpp) 。</span><span class="sxs-lookup"><span data-stu-id="76812-130">Monochrome images have a ratio of 1 bit per pixel (bpp).</span></span> <span data-ttu-id="76812-131">色彩影像處理更為複雜。</span><span class="sxs-lookup"><span data-stu-id="76812-131">Color imaging is more complex.</span></span> <span data-ttu-id="76812-132">點陣圖可顯示的色彩數目等於兩個值，每圖元的位數。</span><span class="sxs-lookup"><span data-stu-id="76812-132">The number of colors that can be displayed by a bitmap is equal to two raised to the number of bits per pixel.</span></span> <span data-ttu-id="76812-133">因此，256色點陣圖需要 8 bpp (2 ^ 8 = 256) 。</span><span class="sxs-lookup"><span data-stu-id="76812-133">Thus, a 256-color bitmap requires 8 bpp (2^8 = 256).</span></span>

<span data-ttu-id="76812-134">主控台應用程式是使用點陣圖的應用程式範例。</span><span class="sxs-lookup"><span data-stu-id="76812-134">Control Panel applications are examples of applications that use bitmaps.</span></span> <span data-ttu-id="76812-135">當您選取桌面的背景 (或壁紙) 時，您實際上是選取一個點陣圖，系統會使用該點陣圖來繪製桌面背景。</span><span class="sxs-lookup"><span data-stu-id="76812-135">When you select a background (or wallpaper) for your desktop, you actually select a bitmap, which the system uses to paint the desktop background.</span></span> <span data-ttu-id="76812-136">系統會在桌面上重複繪製 32 32 圖元模式，藉此建立選取的背景模式。</span><span class="sxs-lookup"><span data-stu-id="76812-136">The system creates the selected background pattern by repeatedly drawing a 32-by-32 pixel pattern on the desktop.</span></span>

<span data-ttu-id="76812-137">下圖顯示開發人員在檔案 Redbrick.bmp 中找到之點陣圖的觀點。</span><span class="sxs-lookup"><span data-stu-id="76812-137">The following illustration shows the developer's perspective of the bitmap found in the file Redbrick.bmp.</span></span> <span data-ttu-id="76812-138">它會顯示一個調色板陣列、一個32到32圖元的矩形，以及將色彩從調色板對應至矩形中圖元的索引陣列。</span><span class="sxs-lookup"><span data-stu-id="76812-138">It shows a palette array, a 32-by-32 pixel rectangle, and the index array that maps colors from the palette to pixels in the rectangle.</span></span>

![redbrick.bmp 的圖元矩形、調色板陣列和索引陣列的圖例](images/csbmp-01.png)

<span data-ttu-id="76812-140">在上述範例中，圖元的矩形是在使用16個色彩之調色板的 VGA 顯示裝置上建立的。</span><span class="sxs-lookup"><span data-stu-id="76812-140">In the preceding example, the rectangle of pixels was created on a VGA display device using a palette of 16 colors.</span></span> <span data-ttu-id="76812-141">16色調色板需要4位的索引;因此，將調色板色彩對應到圖元色彩的陣列也是由4位索引所組成。</span><span class="sxs-lookup"><span data-stu-id="76812-141">A 16-color palette requires 4-bit indexes; therefore, the array that maps palette colors to pixel colors is composed of 4-bit indexes as well.</span></span> <span data-ttu-id="76812-142"> (如需有關邏輯調色板的詳細資訊，請參閱 [色彩](colors.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="76812-142">(For more information about logical color-palettes, see [Colors](colors.md).)</span></span>

> [!Note]
>
> <span data-ttu-id="76812-143">在上述的點陣圖中，系統會將索引從矩形區域的底部掃描行開始對應到圖元，並以最上層的掃描行結尾。</span><span class="sxs-lookup"><span data-stu-id="76812-143">In the above bitmap, the system maps indexes to pixels beginning with the bottom scan line of the rectangular region and ending with the top scan line.</span></span> <span data-ttu-id="76812-144">*掃描行* 是影片顯示器上相鄰圖元的單一資料列。</span><span class="sxs-lookup"><span data-stu-id="76812-144">A *scan line* is a single row of adjacent pixels on a video display.</span></span> <span data-ttu-id="76812-145">例如，陣列的第一個資料列 (資料列 0) 對應至底部資料列（掃描第31行）。</span><span class="sxs-lookup"><span data-stu-id="76812-145">For example, the first row of the array (row 0) corresponds to the bottom row of pixels, scan line 31.</span></span> <span data-ttu-id="76812-146">這是因為上述點陣圖是 (DIB) （一般點陣圖類型）的最底層裝置獨立點陣圖。</span><span class="sxs-lookup"><span data-stu-id="76812-146">This is because the above bitmap is a bottom-up device-independent bitmap (DIB), a common type of bitmap.</span></span> <span data-ttu-id="76812-147">在由上而下的 Dib，以及與裝置相關的點陣圖 (DDB) 中，系統會將索引對應到從最上層掃描行開始的圖元。</span><span class="sxs-lookup"><span data-stu-id="76812-147">In top-down DIBs and in device-dependent bitmaps (DDB), the system maps indexes to pixels beginning with the top scan line.</span></span>

 

<span data-ttu-id="76812-148">下列主題描述不同的點陣圖區域。</span><span class="sxs-lookup"><span data-stu-id="76812-148">The following topics describe different areas of bitmaps.</span></span>

-   [<span data-ttu-id="76812-149">點陣圖分類</span><span class="sxs-lookup"><span data-stu-id="76812-149">Bitmap Classifications</span></span>](bitmap-classifications.md)
-   [<span data-ttu-id="76812-150">點陣圖標頭類型</span><span class="sxs-lookup"><span data-stu-id="76812-150">Bitmap Header Types</span></span>](bitmap-header-types.md)
-   [<span data-ttu-id="76812-151">特定點陣圖函式和結構的 JPEG 和 PNG 擴充功能</span><span class="sxs-lookup"><span data-stu-id="76812-151">JPEG and PNG Extensions for Specific Bitmap Functions and Structures</span></span>](jpeg-and-png-extensions-for-specific-bitmap-functions-and-structures.md)
-   [<span data-ttu-id="76812-152">點陣圖、裝置內容和繪圖表面</span><span class="sxs-lookup"><span data-stu-id="76812-152">Bitmaps, Device Contexts, and Drawing Surfaces</span></span>](bitmaps--device-contexts--and-drawing-surfaces.md)
-   [<span data-ttu-id="76812-153">點陣圖建立</span><span class="sxs-lookup"><span data-stu-id="76812-153">Bitmap Creation</span></span>](bitmap-creation.md)
-   [<span data-ttu-id="76812-154">點陣圖旋轉</span><span class="sxs-lookup"><span data-stu-id="76812-154">Bitmap Rotation</span></span>](bitmap-rotation.md)
-   [<span data-ttu-id="76812-155">點陣圖縮放比例</span><span class="sxs-lookup"><span data-stu-id="76812-155">Bitmap Scaling</span></span>](bitmap-scaling.md)
-   [<span data-ttu-id="76812-156">點陣圖作為筆刷</span><span class="sxs-lookup"><span data-stu-id="76812-156">Bitmaps as Brushes</span></span>](bitmaps-as-brushes.md)
-   [<span data-ttu-id="76812-157">點陣圖儲存體</span><span class="sxs-lookup"><span data-stu-id="76812-157">Bitmap Storage</span></span>](bitmap-storage.md)
-   [<span data-ttu-id="76812-158">點陣圖壓縮</span><span class="sxs-lookup"><span data-stu-id="76812-158">Bitmap Compression</span></span>](bitmap-compression.md)
-   [<span data-ttu-id="76812-159">Alpha 混色</span><span class="sxs-lookup"><span data-stu-id="76812-159">Alpha Blending</span></span>](alpha-blending.md)
-   [<span data-ttu-id="76812-160">平滑陰影</span><span class="sxs-lookup"><span data-stu-id="76812-160">Smooth Shading</span></span>](smooth-shading.md)
-   [<span data-ttu-id="76812-161">具備 ICM 功能的點陣圖函式</span><span class="sxs-lookup"><span data-stu-id="76812-161">ICM-Enabled Bitmap Functions</span></span>](icm-enabled-bitmap-functions.md)

 

 



