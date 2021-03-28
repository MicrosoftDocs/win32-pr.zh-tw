---
description: 您可以使用 Image 類別和 TextureBrush 類別，以紋理填滿封閉的圖形。
ms.assetid: 12e1e132-a93f-4438-8a1d-9036a43a8fd8
title: 使用影像材質填滿形狀
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3f1bf6ba04311310ab1985de1d1aaccd45db43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115225"
---
# <a name="filling-a-shape-with-an-image-texture"></a><span data-ttu-id="6efbe-103">使用影像材質填滿形狀</span><span class="sxs-lookup"><span data-stu-id="6efbe-103">Filling a Shape with an Image Texture</span></span>

<span data-ttu-id="6efbe-104">您可以使用 [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 類別和 [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) 類別，以紋理填滿封閉的圖形。</span><span class="sxs-lookup"><span data-stu-id="6efbe-104">You can fill a closed shape with a texture by using the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class and the [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) class.</span></span>

<span data-ttu-id="6efbe-105">下列範例會使用影像填滿橢圓形。</span><span class="sxs-lookup"><span data-stu-id="6efbe-105">The following example fills an ellipse with an image.</span></span> <span data-ttu-id="6efbe-106">程式碼會建立 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 物件，然後將該 **影像** 物件的位址當作引數傳遞給 [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) 的函式。</span><span class="sxs-lookup"><span data-stu-id="6efbe-106">The code constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object, and then passes the address of that **Image** object as an argument to a [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) constructor.</span></span> <span data-ttu-id="6efbe-107">第三個程式碼語句會調整影像，而第四個語句會使用縮放影像的重複複本來填滿橢圓形：</span><span class="sxs-lookup"><span data-stu-id="6efbe-107">The third code statement scales the image, and the fourth statement fills the ellipse with repeated copies of the scaled image:</span></span>


```
Image image(L"ImageFile.jpg");
TextureBrush tBrush(&image);
stat = tBrush.SetTransform(&Matrix(75.0/640.0, 0.0f, 0.0f,
   75.0/480.0, 0.0f, 0.0f));
stat = graphics.FillEllipse(&tBrush,Rect(0, 150, 150, 250));
```



<span data-ttu-id="6efbe-108">在上述程式碼範例中， [**TextureBrush：： SetTransform**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-texturebrush-settransform) 方法會設定在繪製之前套用至影像的轉換。</span><span class="sxs-lookup"><span data-stu-id="6efbe-108">In the preceding code example, the [**TextureBrush::SetTransform**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-texturebrush-settransform) method sets the transformation that is applied to the image before it is drawn.</span></span> <span data-ttu-id="6efbe-109">假設原始影像的寬度為640圖元，高度為480圖元。</span><span class="sxs-lookup"><span data-stu-id="6efbe-109">Assume that the original image has a width of 640 pixels and a height of 480 pixels.</span></span> <span data-ttu-id="6efbe-110">轉換會藉由設定水準和垂直縮放比例值，將影像縮減為75×75。</span><span class="sxs-lookup"><span data-stu-id="6efbe-110">The transform shrinks the image to 75 ×75, by setting the horizontal and vertical scaling values.</span></span>

> [!Note]  
> <span data-ttu-id="6efbe-111">在上述範例中，影像大小為75×75，而橢圓大小為150×250。</span><span class="sxs-lookup"><span data-stu-id="6efbe-111">In the preceding example, the image size is 75 ×75, and the ellipse size is 150 ×250.</span></span> <span data-ttu-id="6efbe-112">因為影像小於其填滿的橢圓，所以橢圓形會與影像並排顯示。</span><span class="sxs-lookup"><span data-stu-id="6efbe-112">Because the image is smaller than the ellipse it is filling, the ellipse is tiled with the image.</span></span> <span data-ttu-id="6efbe-113">圖格表示影像會以水準和垂直方式重複，直到達到圖形界限為止。</span><span class="sxs-lookup"><span data-stu-id="6efbe-113">Tiling means that the image is repeated horizontally and vertically until the boundary of the shape is reached.</span></span> <span data-ttu-id="6efbe-114">如需並排顯示的詳細資訊，請參閱 [使用影像將圖形平鋪](-gdiplus-tiling-a-shape-with-an-image-use.md)。</span><span class="sxs-lookup"><span data-stu-id="6efbe-114">For more information on tiling, see [Tiling a Shape with an Image](-gdiplus-tiling-a-shape-with-an-image-use.md).</span></span>

 

 

 



