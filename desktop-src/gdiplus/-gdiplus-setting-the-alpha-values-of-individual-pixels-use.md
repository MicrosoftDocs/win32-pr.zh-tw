---
description: 使用色彩矩陣設定影像中的 Alpha 值的主題，會顯示變更影像 Alpha 值的非破壞性方法。
ms.assetid: 38c6254d-5191-4948-804a-1a4427aab7c6
title: 設定個別圖元的 Alpha 值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cd45bf32284ffc9a8cef13f368cff59e1e8a74f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511376"
---
# <a name="setting-the-alpha-values-of-individual-pixels"></a><span data-ttu-id="e8e0e-103">設定個別圖元的 Alpha 值</span><span class="sxs-lookup"><span data-stu-id="e8e0e-103">Setting the Alpha Values of Individual Pixels</span></span>

<span data-ttu-id="e8e0e-104">[使用色彩矩陣設定影像中的 Alpha 值](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md)的主題，會顯示變更影像 Alpha 值的非破壞性方法。</span><span class="sxs-lookup"><span data-stu-id="e8e0e-104">The topic [Using a Color Matrix to Set Alpha Values in Images](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md) shows a nondestructive method for changing the alpha values of an image.</span></span> <span data-ttu-id="e8e0e-105">該主題中的範例會轉譯影像 semitransparently，但是點陣圖中的圖元資料並不會變更。</span><span class="sxs-lookup"><span data-stu-id="e8e0e-105">The example in that topic renders an image semitransparently, but the pixel data in the bitmap is not changed.</span></span> <span data-ttu-id="e8e0e-106">Alpha 值只會在轉譯期間改變。</span><span class="sxs-lookup"><span data-stu-id="e8e0e-106">The alpha values are altered only during rendering.</span></span>

<span data-ttu-id="e8e0e-107">下列範例顯示如何變更個別圖元的 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="e8e0e-107">The following example shows how to change the alpha values of individual pixels.</span></span> <span data-ttu-id="e8e0e-108">範例中的程式碼實際上會變更 [**點陣圖**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) 物件中的 Alpha 資訊。</span><span class="sxs-lookup"><span data-stu-id="e8e0e-108">The code in the example actually changes the alpha information in a [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object.</span></span> <span data-ttu-id="e8e0e-109">這種方法比使用色矩陣和 [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) 物件慢很多，但可讓您控制點陣圖中的個別圖元。</span><span class="sxs-lookup"><span data-stu-id="e8e0e-109">The approach is much slower than using a color matrix and an [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) object but gives you control over the individual pixels in the bitmap.</span></span>


```
INT iWidth = bitmap.GetWidth();
INT iHeight = bitmap.GetHeight();
Color color, colorTemp;
for(INT iRow = 0; iRow < iHeight; iRow++)
{
   for(INT iColumn = 0; iColumn < iWidth; iColumn++)
   {
      bitmap.GetPixel(iColumn, iRow, &color);
      colorTemp.SetValue(color.MakeARGB(
         (BYTE)(255 * iColumn / iWidth), 
         color.GetRed(),
         color.GetGreen(),
         color.GetBlue()));
      bitmap.SetPixel(iColumn, iRow, colorTemp);
   }
}
// First draw a wide black line.
Pen pen(Color(255, 0, 0, 0), 25);
graphics.DrawLine(&pen, 10, 35, 200, 35);
// Now draw the modified bitmap.
graphics.DrawImage(&bitmap, 30, 0, iWidth, iHeight);
```



<span data-ttu-id="e8e0e-110">下圖顯示產生的影像。</span><span class="sxs-lookup"><span data-stu-id="e8e0e-110">The following illustration shows the resulting image.</span></span>

![圖例顯示在黑色矩形上從左至右取得較不透明的影像](images/image3.png)

<span data-ttu-id="e8e0e-112">上述程式碼範例會使用嵌套迴圈來變更點陣圖中每個圖元的 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="e8e0e-112">The preceding code example uses nested loops to change the alpha value of each pixel in the bitmap.</span></span> <span data-ttu-id="e8e0e-113">針對每個圖元， [**bitmap：： GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) 會取得現有的色彩， [**Color：： SetValue**](/windows/desktop/api/Gdipluscolor/nf-gdipluscolor-color-setvalue) 會建立包含新 Alpha 值的暫存色彩，然後 [**bitmap：： bitmap.setpixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) 會設定新的色彩。</span><span class="sxs-lookup"><span data-stu-id="e8e0e-113">For each pixel, [**Bitmap::GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) gets the existing color, [**Color::SetValue**](/windows/desktop/api/Gdipluscolor/nf-gdipluscolor-color-setvalue) creates a temporary color that contains the new alpha value, and then [**Bitmap::SetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) sets the new color.</span></span> <span data-ttu-id="e8e0e-114">Alpha 值是根據點陣圖的資料行來設定。</span><span class="sxs-lookup"><span data-stu-id="e8e0e-114">The alpha value is set based on the column of the bitmap.</span></span> <span data-ttu-id="e8e0e-115">在第一個資料行中，Alpha 設定為0。</span><span class="sxs-lookup"><span data-stu-id="e8e0e-115">In the first column, alpha is set to 0.</span></span> <span data-ttu-id="e8e0e-116">在最後一個資料行中，Alpha 設定為255。</span><span class="sxs-lookup"><span data-stu-id="e8e0e-116">In the last column, alpha is set to 255.</span></span> <span data-ttu-id="e8e0e-117">因此，產生的影像會從左邊緣的完全透明 () 到右邊邊緣) 的完全不透明 (。</span><span class="sxs-lookup"><span data-stu-id="e8e0e-117">So the resulting image goes from fully transparent (on the left edge) to fully opaque (on the right edge).</span></span>

<span data-ttu-id="e8e0e-118">[**Bitmap：： GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) 和 [**Bitmap：： bitmap.setpixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) 可讓您控制個別圖元值。</span><span class="sxs-lookup"><span data-stu-id="e8e0e-118">[**Bitmap::GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) and [**Bitmap::SetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) give you control of the individual pixel values.</span></span> <span data-ttu-id="e8e0e-119">不過，使用 **bitmap：： GetPixel** 和 **Bitmap：： bitmap.setpixel** 並不像使用 [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) 類別和 [**ColorMatrix**](/windows/desktop/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) 結構一樣快。</span><span class="sxs-lookup"><span data-stu-id="e8e0e-119">However, using **Bitmap::GetPixel** and **Bitmap::SetPixel** is not nearly as fast as using the [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) class and the [**ColorMatrix**](/windows/desktop/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) structure.</span></span>

 

 



