---
description: 下列各節說明 Windows GDI + 中的數個新功能。
ms.assetid: 0257a23c-560e-472e-863a-6ab5881dc156
title: 新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca79ddb4cabd14cc2eaa2493033a78cc7377f8e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690347"
---
# <a name="new-features"></a><span data-ttu-id="b9d04-103">新功能</span><span class="sxs-lookup"><span data-stu-id="b9d04-103">New Features</span></span>

<span data-ttu-id="b9d04-104">下列各節說明 Windows GDI + 中的數個新功能。</span><span class="sxs-lookup"><span data-stu-id="b9d04-104">The following sections describe several of the new features in Windows GDI+.</span></span>

-   [<span data-ttu-id="b9d04-105">漸層筆刷</span><span class="sxs-lookup"><span data-stu-id="b9d04-105">Gradient Brushes</span></span>](#gradient-brushes)
-   [<span data-ttu-id="b9d04-106">基本曲線</span><span class="sxs-lookup"><span data-stu-id="b9d04-106">Cardinal Splines</span></span>](#cardinal-splines)
-   [<span data-ttu-id="b9d04-107">獨立路徑物件</span><span class="sxs-lookup"><span data-stu-id="b9d04-107">Independent Path Objects</span></span>](#independent-path-objects)
-   [<span data-ttu-id="b9d04-108">轉換和矩陣物件</span><span class="sxs-lookup"><span data-stu-id="b9d04-108">Transformations and the Matrix Object</span></span>](#transformations-and-the-matrix-object)
-   [<span data-ttu-id="b9d04-109">可擴充的區域</span><span class="sxs-lookup"><span data-stu-id="b9d04-109">Scalable Regions</span></span>](#scalable-regions)
-   [<span data-ttu-id="b9d04-110">Alpha 混色</span><span class="sxs-lookup"><span data-stu-id="b9d04-110">Alpha Blending</span></span>](#alpha-blending)
-   [<span data-ttu-id="b9d04-111">支援多種影像格式</span><span class="sxs-lookup"><span data-stu-id="b9d04-111">Support for Multiple Image Formats</span></span>](#support-for-multiple-image-formats)

## <a name="gradient-brushes"></a><span data-ttu-id="b9d04-112">漸層筆刷</span><span class="sxs-lookup"><span data-stu-id="b9d04-112">Gradient Brushes</span></span>

<span data-ttu-id="b9d04-113">GDI + 藉由提供線性漸層和軌跡漸層筆刷來填滿形狀、路徑和區域，來展開 Windows 圖形裝置介面 (GDI) 。</span><span class="sxs-lookup"><span data-stu-id="b9d04-113">GDI+ expands on Windows Graphics Device Interface (GDI) by providing linear gradient and path gradient brushes for filling shapes, paths, and regions.</span></span> <span data-ttu-id="b9d04-114">漸層筆刷也可以用來繪製線條、曲線和路徑。</span><span class="sxs-lookup"><span data-stu-id="b9d04-114">Gradient brushes can also be used to draw lines, curves, and paths.</span></span> <span data-ttu-id="b9d04-115">當您以線性漸層筆刷填滿圖形時，色彩會在您移動整個圖形時逐漸變更。</span><span class="sxs-lookup"><span data-stu-id="b9d04-115">When you fill a shape with a linear gradient brush, the color gradually changes as you move across the shape.</span></span> <span data-ttu-id="b9d04-116">例如，假設您在圖形的左邊緣指定藍色，在右邊緣指定綠色來建立水準漸層筆刷。</span><span class="sxs-lookup"><span data-stu-id="b9d04-116">For example, suppose you create a horizontal gradient brush by specifying blue at the left edge of a shape and green at the right edge.</span></span> <span data-ttu-id="b9d04-117">當您使用水準漸層筆刷來填滿該圖形時，當您從左邊緣移至其右邊緣時，它會逐漸從藍色變更為綠色。</span><span class="sxs-lookup"><span data-stu-id="b9d04-117">When you fill that shape with the horizontal gradient brush, it will gradually change from blue to green as you move from its left edge to its right edge.</span></span> <span data-ttu-id="b9d04-118">同樣地，以垂直漸層筆刷填滿的形狀，會隨著您從上往下移動而改變色彩。</span><span class="sxs-lookup"><span data-stu-id="b9d04-118">Similarly, a shape filled with a vertical gradient brush will change color as you move from top to bottom.</span></span> <span data-ttu-id="b9d04-119">下圖顯示填滿水準漸層筆刷的橢圓形，以及以對角漸層筆刷填滿的區域。</span><span class="sxs-lookup"><span data-stu-id="b9d04-119">The following illustration shows an ellipse filled with a horizontal gradient brush and a region filled with a diagonal gradient brush.</span></span>

![以水準漸層填滿，且由對角線漸層所組成的圖形圖例](images/aboutgdip01-art01.png)

<span data-ttu-id="b9d04-121">當您使用路徑漸層筆刷填滿圖形時，您可以使用各種選項來指定當您從圖形的某個部分移至另一個部分時，色彩如何變更。</span><span class="sxs-lookup"><span data-stu-id="b9d04-121">When you fill a shape with a path gradient brush, you have a variety of options for specifying how the colors change as you move from one portion of the shape to another.</span></span> <span data-ttu-id="b9d04-122">其中一個選項是使用中間色彩和界限色彩，讓圖元從形狀的中間移到外部邊緣時，從某種色彩逐漸變更為另一種色彩。</span><span class="sxs-lookup"><span data-stu-id="b9d04-122">One option is to have a center color and a boundary color so that the pixels change gradually from one color to the other as you move from the middle of the shape towards the outer edges.</span></span> <span data-ttu-id="b9d04-123">下圖顯示 (從一對貝茲曲線建立的路徑，) 填滿路徑漸層筆刷。</span><span class="sxs-lookup"><span data-stu-id="b9d04-123">The following illustration shows a path (created from a pair of Bézier splines) filled with a path gradient brush.</span></span>

![類似無限大符號的圖形圖例，填滿藍色，其中一半符合邊緣的綠色](images/aboutgdip01-art02.png)

## <a name="cardinal-splines"></a><span data-ttu-id="b9d04-125">基本曲線</span><span class="sxs-lookup"><span data-stu-id="b9d04-125">Cardinal Splines</span></span>

<span data-ttu-id="b9d04-126">GDI + 支援在 GDI 中不支援的基線曲線。</span><span class="sxs-lookup"><span data-stu-id="b9d04-126">GDI+ supports cardinal splines, which are not supported in GDI.</span></span> <span data-ttu-id="b9d04-127">基本曲線是一條聯結的個別曲線，形成較大的曲線。</span><span class="sxs-lookup"><span data-stu-id="b9d04-127">A cardinal spline is a sequence of individual curves joined to form a larger curve.</span></span> <span data-ttu-id="b9d04-128">曲線是由點陣列所指定，並傳遞該陣列中的每個點。</span><span class="sxs-lookup"><span data-stu-id="b9d04-128">The spline is specified by an array of points and passes through each point in that array.</span></span> <span data-ttu-id="b9d04-129">基線曲線會順暢地通過 (沒有任何尖角) 整個陣列中的每個點，因此比連接直線所建立的路徑更精簡。</span><span class="sxs-lookup"><span data-stu-id="b9d04-129">A cardinal spline passes smoothly (no sharp corners) through each point in the array and thus is more refined than a path created by connecting straight lines.</span></span> <span data-ttu-id="b9d04-130">下圖顯示兩個路徑，其中一個是連接直線，另一個建立為基線曲線。</span><span class="sxs-lookup"><span data-stu-id="b9d04-130">The following illustration shows two paths, one created by connecting straight lines and one created as a cardinal spline.</span></span>

![圖例顯示相同的五個點兩次：透過基線曲線連接後，另一個則是依線段](images/aboutgdip01-art03.png)

## <a name="independent-path-objects"></a><span data-ttu-id="b9d04-132">獨立路徑物件</span><span class="sxs-lookup"><span data-stu-id="b9d04-132">Independent Path Objects</span></span>

<span data-ttu-id="b9d04-133">在 GDI 中，路徑屬於裝置內容，而且路徑會在繪製時損毀。</span><span class="sxs-lookup"><span data-stu-id="b9d04-133">In GDI, a path belongs to a device context, and the path is destroyed as it is drawn.</span></span> <span data-ttu-id="b9d04-134">使用 GDI + 時，繪圖是由 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件執行，而且您可以建立和維護數個與 **圖形** 物件不同的 [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath)物件。</span><span class="sxs-lookup"><span data-stu-id="b9d04-134">With GDI+, drawing is performed by a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, and you can create and maintain several [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) objects that are separate from the **Graphics** object.</span></span> <span data-ttu-id="b9d04-135">繪圖動作不會終結 **GraphicsPath** 物件，因此您可以使用相同的 **GraphicsPath** 物件來繪製路徑數次。</span><span class="sxs-lookup"><span data-stu-id="b9d04-135">A **GraphicsPath** object is not destroyed by the drawing action, so you can use the same **GraphicsPath** object to draw a path several times.</span></span>

## <a name="transformations-and-the-matrix-object"></a><span data-ttu-id="b9d04-136">轉換和矩陣物件</span><span class="sxs-lookup"><span data-stu-id="b9d04-136">Transformations and the Matrix Object</span></span>

<span data-ttu-id="b9d04-137">GDI + 提供 [**矩陣**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) 物件，這是一種功能強大的工具，可讓轉換 (旋轉、轉譯等) 輕鬆且彈性。</span><span class="sxs-lookup"><span data-stu-id="b9d04-137">GDI+ provides the [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) object, a powerful tool that makes transformations (rotations, translations, and so on) easy and flexible.</span></span> <span data-ttu-id="b9d04-138">矩陣物件與轉換的物件搭配運作。</span><span class="sxs-lookup"><span data-stu-id="b9d04-138">A matrix object works in conjunction with the objects that are transformed.</span></span> <span data-ttu-id="b9d04-139">例如， [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) 物件有一個 [**GraphicsPath：： Transform**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-transform) 方法，它會以引數的形式接收 **矩陣** 物件的位址。</span><span class="sxs-lookup"><span data-stu-id="b9d04-139">For example, a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object has a [**GraphicsPath::Transform**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-transform) method that receives the address of a **Matrix** object as an argument.</span></span> <span data-ttu-id="b9d04-140">單一的3×3矩陣可以儲存一個轉換或一連串的轉換。</span><span class="sxs-lookup"><span data-stu-id="b9d04-140">A single 3×3 matrix can store one transformation or a sequence of transformations.</span></span> <span data-ttu-id="b9d04-141">下圖顯示兩個轉換順序之前和之後的路徑 (首次調整，然後旋轉) 。</span><span class="sxs-lookup"><span data-stu-id="b9d04-141">The following illustration shows a path before and after a sequence of two transformations (first scale, then rotate).</span></span>

![圖例顯示圖案的外框，然後是相同的外框，但較窄和旋轉](images/aboutgdip01-art04.png)

## <a name="scalable-regions"></a><span data-ttu-id="b9d04-143">可擴充的區域</span><span class="sxs-lookup"><span data-stu-id="b9d04-143">Scalable Regions</span></span>

<span data-ttu-id="b9d04-144">GDI + 會大幅擴充 GDI 的支援區域。</span><span class="sxs-lookup"><span data-stu-id="b9d04-144">GDI+ expands greatly on GDI with its support for regions.</span></span> <span data-ttu-id="b9d04-145">在 GDI 中，區域會儲存在裝置座標中，而唯一可套用至區域的轉換是轉譯。</span><span class="sxs-lookup"><span data-stu-id="b9d04-145">In GDI, regions are stored in device coordinates, and the only transformation that can be applied to a region is a translation.</span></span> <span data-ttu-id="b9d04-146">GDI + 會以全局座標儲存區域，並允許區域進行任何轉換 (調整，例如可儲存在轉換矩陣中的) 。</span><span class="sxs-lookup"><span data-stu-id="b9d04-146">GDI+ stores regions in world coordinates and allows a region to undergo any transformation (scaling, for example) that can be stored in a transformation matrix.</span></span> <span data-ttu-id="b9d04-147">下圖顯示三個轉換順序之前和之後的區域：調整、旋轉和轉譯。</span><span class="sxs-lookup"><span data-stu-id="b9d04-147">The following illustration shows a region before and after a sequence of three transformations: scale, rotate, and translate.</span></span>

![圖例顯示以座標軸為中心的形狀，然後是相同的形狀，但較大、旋轉和轉譯為右邊](images/aboutgdip01-art05.png)

## <a name="alpha-blending"></a><span data-ttu-id="b9d04-149">Alpha 混色</span><span class="sxs-lookup"><span data-stu-id="b9d04-149">Alpha Blending</span></span>

<span data-ttu-id="b9d04-150">請注意，在上圖中，您可以看到未轉換區域 (透過已轉換的區域填滿紅色)  (填滿了影線筆刷) 。</span><span class="sxs-lookup"><span data-stu-id="b9d04-150">Note that in the previous figure, you can see the untransformed region (filled with red) through the transformed region (filled with a hatch brush).</span></span> <span data-ttu-id="b9d04-151">這是由 GDI + 支援的 Alpha 混色所達成。</span><span class="sxs-lookup"><span data-stu-id="b9d04-151">This is made possible by alpha blending, which is supported by GDI+.</span></span> <span data-ttu-id="b9d04-152">使用 Alpha 混色時，您可以指定填滿色彩的透明度。</span><span class="sxs-lookup"><span data-stu-id="b9d04-152">With alpha blending, you can specify the transparency of a fill color.</span></span> <span data-ttu-id="b9d04-153">透明色彩會與背景色彩混合使用，您可以使用填滿色彩的透明色彩，讓背景顯示的越多。</span><span class="sxs-lookup"><span data-stu-id="b9d04-153">A transparent color is blended with the background color — the more transparent you make a fill color, the more the background shows through.</span></span> <span data-ttu-id="b9d04-154">下圖顯示四個在不同透明度層級 (紅色) 填滿色彩的省略號。</span><span class="sxs-lookup"><span data-stu-id="b9d04-154">The following illustration shows four ellipses that are filled with the same color (red) at different transparency levels.</span></span>

![顯示與半透明矩形重迭的四個不同透明度橢圓形的圖例](images/aboutgdip01-art06.png)

## <a name="support-for-multiple-image-formats"></a><span data-ttu-id="b9d04-156">支援多種影像格式</span><span class="sxs-lookup"><span data-stu-id="b9d04-156">Support for Multiple Image Formats</span></span>

<span data-ttu-id="b9d04-157">GDI + 提供 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image)、 [**點陣圖**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)和 [**中繼檔**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) 類別，可讓您以各種不同的格式載入、儲存和操作影像。</span><span class="sxs-lookup"><span data-stu-id="b9d04-157">GDI+ provides the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image), [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap), and [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) classes, which allow you to load, save and manipulate images in a variety of formats.</span></span> <span data-ttu-id="b9d04-158">下列為支援的格式：</span><span class="sxs-lookup"><span data-stu-id="b9d04-158">The following formats are supported:</span></span>

-   <span data-ttu-id="b9d04-159">BMP</span><span class="sxs-lookup"><span data-stu-id="b9d04-159">BMP</span></span>
-   <span data-ttu-id="b9d04-160">圖形交換格式 (GIF)</span><span class="sxs-lookup"><span data-stu-id="b9d04-160">Graphics Interchange Format (GIF)</span></span>
-   <span data-ttu-id="b9d04-161">JPEG</span><span class="sxs-lookup"><span data-stu-id="b9d04-161">JPEG</span></span>
-   <span data-ttu-id="b9d04-162">Exif</span><span class="sxs-lookup"><span data-stu-id="b9d04-162">Exif</span></span>
-   <span data-ttu-id="b9d04-163">PNG</span><span class="sxs-lookup"><span data-stu-id="b9d04-163">PNG</span></span>
-   <span data-ttu-id="b9d04-164">TIFF</span><span class="sxs-lookup"><span data-stu-id="b9d04-164">TIFF</span></span>
-   <span data-ttu-id="b9d04-165">圖示</span><span class="sxs-lookup"><span data-stu-id="b9d04-165">ICON</span></span>
-   <span data-ttu-id="b9d04-166">WMF</span><span class="sxs-lookup"><span data-stu-id="b9d04-166">WMF</span></span>
-   <span data-ttu-id="b9d04-167">EMF</span><span class="sxs-lookup"><span data-stu-id="b9d04-167">EMF</span></span>

 

 



