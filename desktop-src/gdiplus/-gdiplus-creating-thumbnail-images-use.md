---
description: 縮圖影像是小型的影像版本。 您可以藉由呼叫 Image 物件的 >getthumbnailimage 方法來建立縮圖影像。
ms.assetid: 96f95d00-6f96-4b8a-b84b-010203433d74
title: 建立縮圖影像
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ac737a49bad85ecc25eeeef1266a02cdeb408f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104555944"
---
# <a name="creating-thumbnail-images"></a><span data-ttu-id="5442b-104">建立縮圖影像</span><span class="sxs-lookup"><span data-stu-id="5442b-104">Creating Thumbnail Images</span></span>

<span data-ttu-id="5442b-105">縮圖影像是小型的影像版本。</span><span class="sxs-lookup"><span data-stu-id="5442b-105">A thumbnail image is a small version of an image.</span></span> <span data-ttu-id="5442b-106">您可以藉由呼叫 [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image)物件的 **>getthumbnailimage** 方法來建立縮圖影像。</span><span class="sxs-lookup"><span data-stu-id="5442b-106">You can create a thumbnail image by calling the **GetThumbnailImage** method of an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object.</span></span>

<span data-ttu-id="5442b-107">下列範例會從檔案 Compass.bmp 中，建立 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 物件。</span><span class="sxs-lookup"><span data-stu-id="5442b-107">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file Compass.bmp.</span></span> <span data-ttu-id="5442b-108">原始影像的寬度為640圖元，高度為479圖元。</span><span class="sxs-lookup"><span data-stu-id="5442b-108">The original image has a width of 640 pixels and a height of 479 pixels.</span></span> <span data-ttu-id="5442b-109">程式碼會建立寬度為100圖元且高度為100圖元的縮圖影像。</span><span class="sxs-lookup"><span data-stu-id="5442b-109">The code creates a thumbnail image that has a width of 100 pixels and a height of 100 pixels.</span></span>


```
Image image(L"Compass.bmp");
Image* pThumbnail = image.GetThumbnailImage(100, 100, NULL, NULL);
graphics.DrawImage(pThumbnail, 10, 10, 
   pThumbnail->GetWidth(), pThumbnail->GetHeight());
```



<span data-ttu-id="5442b-110">下圖顯示縮圖影像。</span><span class="sxs-lookup"><span data-stu-id="5442b-110">The following illustration shows the thumbnail image.</span></span>

![顯示羅盤的小型圖形圖例](images/thumbnail1.png)

 

 



