---
title: 關於裁剪和縮放 GDI+ 影像
description: 您可以使用 Graphics 類別的 DrawImage 方法來繪製和放置影像。
ms.assetid: 81d20adc-0481-4b1b-80aa-ae218fdecd84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b44a13b5cee632e6ceafe327f94eca48edd93dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115237"
---
# <a name="about-cropping-and-scaling-gdi-images"></a><span data-ttu-id="8c3ae-103">關於裁剪和縮放 GDI+ 影像</span><span class="sxs-lookup"><span data-stu-id="8c3ae-103">About cropping and scaling GDI+ images</span></span>

<span data-ttu-id="8c3ae-104">您可以使用 [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別的 [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_))方法來繪製和放置影像。</span><span class="sxs-lookup"><span data-stu-id="8c3ae-104">You can use the [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to draw and position images.</span></span> <span data-ttu-id="8c3ae-105">DrawImage 是一種多載的方法，因此您可以透過數種方式提供引數給它。</span><span class="sxs-lookup"><span data-stu-id="8c3ae-105">DrawImage is an overloaded method, so there are several ways you can supply it with arguments.</span></span> <span data-ttu-id="8c3ae-106">圖形的一個變化 [**：:D rawimage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) 方法會接收 [**影像**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) 物件的位址和 [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) 物件的參考。</span><span class="sxs-lookup"><span data-stu-id="8c3ae-106">One variation of the [**Graphics::DrawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) method receives the address of an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object and a reference to a [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) object.</span></span> <span data-ttu-id="8c3ae-107">矩形會指定繪圖作業的目的地;也就是說，它會指定要在其中繪製影像的矩形。</span><span class="sxs-lookup"><span data-stu-id="8c3ae-107">The rectangle specifies the destination for the drawing operation; that is, it specifies the rectangle in which the image will be drawn.</span></span> <span data-ttu-id="8c3ae-108">如果目的地矩形的大小與原始影像的大小不同，則影像會縮放以符合目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="8c3ae-108">If the size of the destination rectangle is different from the size of the original image, the image is scaled to fit the destination rectangle.</span></span> <span data-ttu-id="8c3ae-109">下列範例會繪製相同的影像三次：一次沒有調整、一次展開，以及一次壓縮。</span><span class="sxs-lookup"><span data-stu-id="8c3ae-109">The following example draws the same image three times: once with no scaling, once with an expansion, and once with a compression.</span></span>


```
Bitmap myBitmap(L"Spiral.png");
Rect expansionRect(80, 10, 2 * myBitmap.GetWidth(), myBitmap.GetHeight());
Rect compressionRect(210, 10, myBitmap.GetWidth() / 2, 
   myBitmap.GetHeight() / 2);

myGraphics.DrawImage(&myBitmap, 10, 10);
myGraphics.DrawImage(&myBitmap, expansionRect);
myGraphics.DrawImage(&myBitmap, compressionRect);
```



<span data-ttu-id="8c3ae-110">上述程式碼和特定檔案 Spiral.png，會產生下列輸出。</span><span class="sxs-lookup"><span data-stu-id="8c3ae-110">The preceding code, along with a particular file, Spiral.png, produced the following output.</span></span>

![顯示影像的三個版本的圖例：標準、延伸寬，以及壓縮成原始大小的一半](images/aboutgdip03-art06.png)

<span data-ttu-id="8c3ae-112">圖形的部分變化 [**：:D rawimage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) 方法具有來源矩形參數，以及目的地矩形參數。</span><span class="sxs-lookup"><span data-stu-id="8c3ae-112">Some variations of the [**Graphics::DrawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) method have a source-rectangle parameter as well as a destination-rectangle parameter.</span></span> <span data-ttu-id="8c3ae-113">來源矩形會指定將繪製的原始影像部分。</span><span class="sxs-lookup"><span data-stu-id="8c3ae-113">The source rectangle specifies the portion of the original image that will be drawn.</span></span> <span data-ttu-id="8c3ae-114">目的地矩形會指定將繪製影像部分的位置。</span><span class="sxs-lookup"><span data-stu-id="8c3ae-114">The destination rectangle specifies where that portion of the image will be drawn.</span></span> <span data-ttu-id="8c3ae-115">如果目的地矩形的大小與來源矩形的大小不同，則影像會縮放以符合目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="8c3ae-115">If the size of the destination rectangle is different from the size of the source rectangle, the image is scaled to fit the destination rectangle.</span></span>

<span data-ttu-id="8c3ae-116">下列範例會從檔案 Runner.jpg 中，建立 [**點陣圖**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) 物件。</span><span class="sxs-lookup"><span data-stu-id="8c3ae-116">The following example constructs a [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object from the file Runner.jpg.</span></span> <span data-ttu-id="8c3ae-117">在 (0、0) 的情況下繪製整個影像，而不會進行縮放。</span><span class="sxs-lookup"><span data-stu-id="8c3ae-117">The entire image is drawn with no scaling at (0, 0).</span></span> <span data-ttu-id="8c3ae-118">然後，影像的一小部分會繪製兩次：一次使用壓縮，一次進行擴充。</span><span class="sxs-lookup"><span data-stu-id="8c3ae-118">Then a small portion of the image is drawn twice: once with a compression and once with an expansion.</span></span>


```
Bitmap myBitmap(L"Runner.jpg"); 

// The rectangle (in myBitmap) with upper-left corner (80, 70), 
// width 80, and height 45, encloses one of the runner's hands.

// Small destination rectangle for compressed hand.
Rect destRect1(200, 10, 20, 16);

// Large destination rectangle for expanded hand.
Rect destRect2(200, 40, 200, 160);

// Draw the original image at (0, 0).
myGraphics.DrawImage(&myBitmap, 0, 0);

// Draw the compressed hand.
myGraphics.DrawImage(
   &myBitmap, destRect1, 80, 70, 80, 45, UnitPixel);

// Draw the expanded hand. 
myGraphics.DrawImage(
   &myBitmap, destRect2, 80, 70, 80, 45, UnitPixel);
```



<span data-ttu-id="8c3ae-119">下圖顯示未縮放的影像，以及壓縮和展開的影像部分。</span><span class="sxs-lookup"><span data-stu-id="8c3ae-119">The following illustration shows the unscaled image, and the compressed and expanded image portions.</span></span>

![顯示影像的螢幕擷取畫面，其中已壓縮影像的一部分，然後展開相同部分](images/aboutgdip03-art07.png)

 

 



