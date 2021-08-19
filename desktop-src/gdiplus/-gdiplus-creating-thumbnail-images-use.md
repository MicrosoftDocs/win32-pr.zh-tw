---
description: 縮圖影像是小型的影像版本。 您可以藉由呼叫 Image 物件的 >getthumbnailimage 方法來建立縮圖影像。
ms.assetid: 96f95d00-6f96-4b8a-b84b-010203433d74
title: 建立縮圖影像
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5d44fec3220bef7a6691d3852d16f90e9cf43635c99f69bba16f3b569ebabc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117696309"
---
# <a name="creating-thumbnail-images"></a>建立縮圖影像

縮圖影像是小型的影像版本。 您可以藉由呼叫 [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image)物件的 **>getthumbnailimage** 方法來建立縮圖影像。

下列範例會從檔案 Compass.bmp 中，建立 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 物件。 原始影像的寬度為640圖元，高度為479圖元。 程式碼會建立寬度為100圖元且高度為100圖元的縮圖影像。


```
Image image(L"Compass.bmp");
Image* pThumbnail = image.GetThumbnailImage(100, 100, NULL, NULL);
graphics.DrawImage(pThumbnail, 10, 10, 
   pThumbnail->GetWidth(), pThumbnail->GetHeight());
```



下圖顯示縮圖影像。

![顯示羅盤的小型圖形圖例](images/thumbnail1.png)

 

 



