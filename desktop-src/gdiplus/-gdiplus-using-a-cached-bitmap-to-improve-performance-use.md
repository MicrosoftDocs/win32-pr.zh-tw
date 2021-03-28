---
description: 影像和點陣圖物件會以與裝置無關的格式來儲存影像。
ms.assetid: 42e2b664-197c-4c54-9220-b6231d6439d0
title: 使用快取點陣圖改善效能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a8e546460741342bcac8f1633e21d104984af9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991310"
---
# <a name="using-a-cached-bitmap-to-improve-performance"></a>使用快取點陣圖改善效能

[**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 和 [**點陣圖**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) 物件會以與裝置無關的格式來儲存影像。 [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap)物件會以目前顯示裝置的格式來儲存影像。 轉譯儲存在 **CachedBitmap** 物件中的影像很快速，因為不需要處理時間將影像轉換成顯示裝置所需的格式。

下列範例會從檔案 Texture.jpg 建立 [**點陣圖**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) 物件和 [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) 物件。 **點陣圖** 和 **CachedBitmap** 都會繪製30000次。 如果您執行程式碼，您會看到 **CachedBitmap** 影像的繪製速度明顯比 **點陣圖** 影像更快。


```
Bitmap        bitmap(L"Texture.jpg");
UINT          width = bitmap.GetWidth();
UINT          height = bitmap.GetHeight();
CachedBitmap  cBitmap(&bitmap, &graphics);
int           j, k;
for(j = 0; j < 300; j += 10)
   for(k = 0; k < 1000; ++k)
     graphics.DrawImage(&bitmap, j, j / 2, width, height);
for(j = 0; j < 300; j += 10)
   for(k = 0; k < 1000; ++k)
      graphics.DrawCachedBitmap(&cBitmap, j, 150 + j / 2 );
```



> [!Note]  
> [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap)物件符合在建立 **CachedBitmap** 物件時，顯示裝置的格式。 如果您程式的使用者變更了顯示設定，您的程式碼應該會建立新的 **CachedBitmap** 物件。 如果您傳遞的 **CachedBitmap** 物件是在變更顯示格式之前所建立的， **DrawImage** 方法將會失敗。

 

 

 



