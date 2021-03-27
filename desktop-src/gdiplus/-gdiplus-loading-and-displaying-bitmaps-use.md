---
description: 若要在螢幕上顯示 (點陣圖) 的點陣影像，您需要影像物件和繪圖物件。
ms.assetid: 8c1a26d9-b640-4f38-8276-10c4464525f2
title: 載入和顯示點陣圖
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: ab2405462db5017215893d50d93dc0b228633cfb
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/20/2021
ms.locfileid: "104974793"
---
# <a name="loading-and-displaying-bitmaps"></a><span data-ttu-id="8cd5b-103">載入和顯示點陣圖</span><span class="sxs-lookup"><span data-stu-id="8cd5b-103">Loading and displaying bitmaps</span></span>

<span data-ttu-id="8cd5b-104">另請參閱 [WIC 檢視器 GDI + 範例應用程式](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus)。</span><span class="sxs-lookup"><span data-stu-id="8cd5b-104">Also see the [WIC Viewer GDI+ sample app](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus).</span></span>

<span data-ttu-id="8cd5b-105">若要在螢幕上顯示 (點陣圖) 的點陣影像，您需要 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 物件和 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件。</span><span class="sxs-lookup"><span data-stu-id="8cd5b-105">To display a raster image (bitmap) on the screen, you need an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="8cd5b-106">將檔案的名稱 (或) 的資料流程指標傳遞至 **影像** 的函式。</span><span class="sxs-lookup"><span data-stu-id="8cd5b-106">Pass the name of a file (or a pointer to a stream) to an **Image** constructor.</span></span> <span data-ttu-id="8cd5b-107">建立 **影像** 物件之後，將該 **影像** 物件的位址傳遞給 **圖形** 物件的 **DrawImage** 方法。</span><span class="sxs-lookup"><span data-stu-id="8cd5b-107">After you have created an **Image** object, pass the address of that **Image** object to the **DrawImage** method of a **Graphics** object.</span></span>

<span data-ttu-id="8cd5b-108">下列範例會從 JPEG 檔案建立 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 物件，然後在 (60，10) 的左上角繪製影像：</span><span class="sxs-lookup"><span data-stu-id="8cd5b-108">The following example creates an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from a JPEG file and then draws the image with its upper-left corner at (60, 10):</span></span>

```cpp
Image image(L"Grapes.jpg");
graphics.DrawImage(&image, 60, 10);
```

<span data-ttu-id="8cd5b-109">下圖顯示在指定位置繪製的影像。</span><span class="sxs-lookup"><span data-stu-id="8cd5b-109">The following illustration shows the image drawn at the specified location.</span></span>

![<span data-ttu-id="8cd5b-110">包含影像之視窗的螢幕擷取畫面，其中包含原始點的標注</span><span class="sxs-lookup"><span data-stu-id="8cd5b-110">screen shot of a window that contains an image, with a callout for the origin point</span></span> ](images/imageposition1.png)

<span data-ttu-id="8cd5b-111">[**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image)類別提供載入和顯示點陣影像和向量影像的基本方法。</span><span class="sxs-lookup"><span data-stu-id="8cd5b-111">The [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class provides basic methods for loading and displaying raster images and vector images.</span></span> <span data-ttu-id="8cd5b-112">[**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)類別是繼承自 **Image** 類別，可提供更特製化的方法來載入、顯示及操作點陣影像。</span><span class="sxs-lookup"><span data-stu-id="8cd5b-112">The [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) class, which inherits from the **Image** class, provides more specialized methods for loading, displaying, and manipulating raster images.</span></span> <span data-ttu-id="8cd5b-113">例如，您可以從圖示控制碼 (HICON) 來建立 **點陣圖** 物件。</span><span class="sxs-lookup"><span data-stu-id="8cd5b-113">For example, you can construct a **Bitmap** object from an icon handle (HICON).</span></span>

<span data-ttu-id="8cd5b-114">下列範例會取得圖示的控制碼，然後使用該控制碼來建立 [**點陣圖**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) 物件。</span><span class="sxs-lookup"><span data-stu-id="8cd5b-114">The following example obtains a handle to an icon and then uses that handle to construct a [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object.</span></span> <span data-ttu-id="8cd5b-115">程式碼會將 **Bitmap** 物件的位址傳遞至 [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件的 **DrawImage** 方法，以顯示圖示。</span><span class="sxs-lookup"><span data-stu-id="8cd5b-115">The code displays the icon by passing the address of the **Bitmap** object to the **DrawImage** method of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

```cpp
HICON hIcon = LoadIcon(NULL, IDI_APPLICATION);
Bitmap bitmap(hIcon);
graphics.DrawImage(&bitmap, 10, 10);
```

## <a name="see-also"></a><span data-ttu-id="8cd5b-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8cd5b-116">See also</span></span>

[<span data-ttu-id="8cd5b-117">WIC 檢視器 GDI + 範例應用程式</span><span class="sxs-lookup"><span data-stu-id="8cd5b-117">WIC Viewer GDI+ sample app</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus)
