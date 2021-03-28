---
description: 下列函式可用於點陣圖。
ms.assetid: ef3abc8a-5d95-41d0-8eb6-47719d472414
title: " (Windows GDI) 的點陣圖函數"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e61ef02f5065d746f0d82a7b3352c3445ebf61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991290"
---
# <a name="bitmap-functions-windows-gdi"></a><span data-ttu-id="420af-103"> (Windows GDI) 的點陣圖函數</span><span class="sxs-lookup"><span data-stu-id="420af-103">Bitmap Functions (Windows GDI)</span></span>

<span data-ttu-id="420af-104">下列函式可用於點陣圖。</span><span class="sxs-lookup"><span data-stu-id="420af-104">The following functions are used with bitmaps.</span></span>



| <span data-ttu-id="420af-105">函式</span><span class="sxs-lookup"><span data-stu-id="420af-105">Function</span></span>                                                 | <span data-ttu-id="420af-106">描述</span><span class="sxs-lookup"><span data-stu-id="420af-106">Description</span></span>                                                    |
|----------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="420af-107">**AlphaBlend**</span><span class="sxs-lookup"><span data-stu-id="420af-107">**AlphaBlend**</span></span>](/windows/desktop/api/WinGdi/nf-wingdi-alphablend)                         | <span data-ttu-id="420af-108">顯示具有透明或半透明圖元的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="420af-108">Displays a bitmap with transparent or semitransparent pixels.</span></span>  |
| [<span data-ttu-id="420af-109">**BitBlt**</span><span class="sxs-lookup"><span data-stu-id="420af-109">**BitBlt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-bitblt)                                 | <span data-ttu-id="420af-110">執行位區區塊轉送。</span><span class="sxs-lookup"><span data-stu-id="420af-110">Performs a bit-block transfer.</span></span>                                 |
| [<span data-ttu-id="420af-111">**CreateBitmap**</span><span class="sxs-lookup"><span data-stu-id="420af-111">**CreateBitmap**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap)                     | <span data-ttu-id="420af-112">建立點陣圖。</span><span class="sxs-lookup"><span data-stu-id="420af-112">Creates a bitmap.</span></span>                                              |
| [<span data-ttu-id="420af-113">**CreateBitmapIndirect**</span><span class="sxs-lookup"><span data-stu-id="420af-113">**CreateBitmapIndirect**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)     | <span data-ttu-id="420af-114">建立點陣圖。</span><span class="sxs-lookup"><span data-stu-id="420af-114">Creates a bitmap.</span></span>                                              |
| [<span data-ttu-id="420af-115">**CreateCompatibleBitmap**</span><span class="sxs-lookup"><span data-stu-id="420af-115">**CreateCompatibleBitmap**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) | <span data-ttu-id="420af-116">建立與裝置相容的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="420af-116">Creates a bitmap compatible with a device.</span></span>                     |
| [<span data-ttu-id="420af-117">**CreateDIBitmap**</span><span class="sxs-lookup"><span data-stu-id="420af-117">**CreateDIBitmap**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)                 | <span data-ttu-id="420af-118">從 DIB 建立裝置相依點陣圖 (DDB) 。</span><span class="sxs-lookup"><span data-stu-id="420af-118">Creates a device-dependent bitmap (DDB) from a DIB.</span></span>            |
| [<span data-ttu-id="420af-119">**CreateDIBSection**</span><span class="sxs-lookup"><span data-stu-id="420af-119">**CreateDIBSection**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdibsection)             | <span data-ttu-id="420af-120">建立應用程式可直接寫入的 DIB。</span><span class="sxs-lookup"><span data-stu-id="420af-120">Creates a DIB that applications can write to directly.</span></span>         |
| [<span data-ttu-id="420af-121">**ExtFloodFill**</span><span class="sxs-lookup"><span data-stu-id="420af-121">**ExtFloodFill**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extfloodfill)                     | <span data-ttu-id="420af-122">使用目前的筆刷來填滿顯示介面的區域。</span><span class="sxs-lookup"><span data-stu-id="420af-122">Fills an area of the display surface with the current brush.</span></span>   |
| [<span data-ttu-id="420af-123">**GetBitmapDimensionEx**</span><span class="sxs-lookup"><span data-stu-id="420af-123">**GetBitmapDimensionEx**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getbitmapdimensionex)     | <span data-ttu-id="420af-124">取得點陣圖的維度。</span><span class="sxs-lookup"><span data-stu-id="420af-124">Gets the dimensions of a bitmap.</span></span>                               |
| [<span data-ttu-id="420af-125">**GetDIBColorTable**</span><span class="sxs-lookup"><span data-stu-id="420af-125">**GetDIBColorTable**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getdibcolortable)             | <span data-ttu-id="420af-126">從 DIB 區段點陣圖取出 RGB 色彩值。</span><span class="sxs-lookup"><span data-stu-id="420af-126">Retrieves RGB color values from a DIB section bitmap.</span></span>          |
| [<span data-ttu-id="420af-127">**GetDIBits**</span><span class="sxs-lookup"><span data-stu-id="420af-127">**GetDIBits**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getdibits)                           | <span data-ttu-id="420af-128">將點陣圖複製到緩衝區。</span><span class="sxs-lookup"><span data-stu-id="420af-128">Copies a bitmap into a buffer.</span></span>                                 |
| [<span data-ttu-id="420af-129">**GetPixel**</span><span class="sxs-lookup"><span data-stu-id="420af-129">**GetPixel**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getpixel)                             | <span data-ttu-id="420af-130">取得指定座標之圖元的 RGB 色彩值。</span><span class="sxs-lookup"><span data-stu-id="420af-130">Gets the RGB color value of the pixel at a given coordinate.</span></span>   |
| [<span data-ttu-id="420af-131">**GetStretchBltMode**</span><span class="sxs-lookup"><span data-stu-id="420af-131">**GetStretchBltMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getstretchbltmode)           | <span data-ttu-id="420af-132">取得目前的延展模式。</span><span class="sxs-lookup"><span data-stu-id="420af-132">Gets the current stretching mode.</span></span>                              |
| [<span data-ttu-id="420af-133">**GradientFill**</span><span class="sxs-lookup"><span data-stu-id="420af-133">**GradientFill**</span></span>](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill)                     | <span data-ttu-id="420af-134">填滿矩形和三角形結構。</span><span class="sxs-lookup"><span data-stu-id="420af-134">Fills rectangle and triangle structures.</span></span>                       |
| [<span data-ttu-id="420af-135">**LoadBitmap**</span><span class="sxs-lookup"><span data-stu-id="420af-135">**LoadBitmap**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadbitmapa)                         | <span data-ttu-id="420af-136">從模組的可執行檔載入點陣圖。</span><span class="sxs-lookup"><span data-stu-id="420af-136">Loads a bitmap from a module's executable file.</span></span>                |
| [<span data-ttu-id="420af-137">**MaskBlt**</span><span class="sxs-lookup"><span data-stu-id="420af-137">**MaskBlt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-maskblt)                               | <span data-ttu-id="420af-138">結合來源和目的點陣圖中的色彩資料。</span><span class="sxs-lookup"><span data-stu-id="420af-138">Combines the color data in the source and destination bitmaps.</span></span> |
| [<span data-ttu-id="420af-139">**PlgBlt**</span><span class="sxs-lookup"><span data-stu-id="420af-139">**PlgBlt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-plgblt)                                 | <span data-ttu-id="420af-140">執行位區區塊轉送。</span><span class="sxs-lookup"><span data-stu-id="420af-140">Performs a bit-block transfer.</span></span>                                 |
| [<span data-ttu-id="420af-141">**SetBitmapDimensionEx**</span><span class="sxs-lookup"><span data-stu-id="420af-141">**SetBitmapDimensionEx**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setbitmapdimensionex)     | <span data-ttu-id="420af-142">將慣用的維度設定為點陣圖。</span><span class="sxs-lookup"><span data-stu-id="420af-142">Sets the preferred dimensions to a bitmap.</span></span>                     |
| [<span data-ttu-id="420af-143">**SetDIBColorTable**</span><span class="sxs-lookup"><span data-stu-id="420af-143">**SetDIBColorTable**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdibcolortable)             | <span data-ttu-id="420af-144">在 DIB 中設定 RGB 值。</span><span class="sxs-lookup"><span data-stu-id="420af-144">Sets RGB values in a DIB.</span></span>                                      |
| [<span data-ttu-id="420af-145">**SetDIBits**</span><span class="sxs-lookup"><span data-stu-id="420af-145">**SetDIBits**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdibits)                           | <span data-ttu-id="420af-146">使用 DIB 中的色彩資料，設定點陣圖中的圖元。</span><span class="sxs-lookup"><span data-stu-id="420af-146">Sets the pixels in a bitmap using color data from a DIB.</span></span>       |
| [<span data-ttu-id="420af-147">**SetDIBitsToDevice**</span><span class="sxs-lookup"><span data-stu-id="420af-147">**SetDIBitsToDevice**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice)           | <span data-ttu-id="420af-148">使用 DIB 中的色彩資料，設定矩形中的圖元。</span><span class="sxs-lookup"><span data-stu-id="420af-148">Sets the pixels in a rectangle using color data from a DIB.</span></span>    |
| [<span data-ttu-id="420af-149">**Bitmap.setpixel**</span><span class="sxs-lookup"><span data-stu-id="420af-149">**SetPixel**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setpixel)                             | <span data-ttu-id="420af-150">設定圖元的色彩。</span><span class="sxs-lookup"><span data-stu-id="420af-150">Sets the color for a pixel.</span></span>                                    |
| [<span data-ttu-id="420af-151">**SetPixelV**</span><span class="sxs-lookup"><span data-stu-id="420af-151">**SetPixelV**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setpixelv)                           | <span data-ttu-id="420af-152">將圖元設定為色彩的最佳近似。</span><span class="sxs-lookup"><span data-stu-id="420af-152">Sets a pixel to the best approximation of a color.</span></span>             |
| [<span data-ttu-id="420af-153">**SetStretchBltMode**</span><span class="sxs-lookup"><span data-stu-id="420af-153">**SetStretchBltMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode)           | <span data-ttu-id="420af-154">設定點陣圖延展模式。</span><span class="sxs-lookup"><span data-stu-id="420af-154">Sets the bitmap stretching mode.</span></span>                               |
| [<span data-ttu-id="420af-155">**StretchBlt**</span><span class="sxs-lookup"><span data-stu-id="420af-155">**StretchBlt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)                         | <span data-ttu-id="420af-156">複製並伸展或壓縮點陣圖。</span><span class="sxs-lookup"><span data-stu-id="420af-156">Copies a bitmap and stretches or compresses it.</span></span>                |
| [<span data-ttu-id="420af-157">**StretchDIBits**</span><span class="sxs-lookup"><span data-stu-id="420af-157">**StretchDIBits**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits)                   | <span data-ttu-id="420af-158">複製 DIB 中的色彩資料。</span><span class="sxs-lookup"><span data-stu-id="420af-158">Copies the color data in a DIB.</span></span>                                |
| [<span data-ttu-id="420af-159">**TransparentBlt**</span><span class="sxs-lookup"><span data-stu-id="420af-159">**TransparentBlt**</span></span>](/windows/desktop/api/WinGdi/nf-wingdi-transparentblt)                 | <span data-ttu-id="420af-160">執行色彩資料的位區塊傳輸。</span><span class="sxs-lookup"><span data-stu-id="420af-160">Performs a bit-block transfer of color data.</span></span>                   |



 

## <a name="obsolete-functions"></a><span data-ttu-id="420af-161">過時的函式</span><span class="sxs-lookup"><span data-stu-id="420af-161">Obsolete Functions</span></span>

<span data-ttu-id="420af-162">下列函式僅提供給與16位版本的 Microsoft Windows 相容：</span><span class="sxs-lookup"><span data-stu-id="420af-162">The following functions are provided only for compatibility with 16-bit versions of Microsoft Windows:</span></span>

-   [<span data-ttu-id="420af-163">**CreateDiscardableBitmap**</span><span class="sxs-lookup"><span data-stu-id="420af-163">**CreateDiscardableBitmap**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap)
-   [<span data-ttu-id="420af-164">**FloodFill**</span><span class="sxs-lookup"><span data-stu-id="420af-164">**FloodFill**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-floodfill)
-   [<span data-ttu-id="420af-165">**GetBitmapBits**</span><span class="sxs-lookup"><span data-stu-id="420af-165">**GetBitmapBits**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getbitmapbits)
-   [<span data-ttu-id="420af-166">**SetBitmapBits**</span><span class="sxs-lookup"><span data-stu-id="420af-166">**SetBitmapBits**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setbitmapbits)

 

 



