---
title: 從多框架影像複製個別的框架
description: 下列範例會從多框架 TIFF 檔案抓取個別的框架。
ms.assetid: dfed0b61-2230-4911-a642-0a6e4beb08d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8398df806ad56b65114b0cc9a986ea53061183fa4658872b65b7d08ef7e38a9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115098"
---
# <a name="copy-individual-frames-from-a-multiple-frame-image"></a>從多框架影像複製個別的框架

下列範例會從多框架 TIFF 檔案抓取個別的框架。 建立 TIFF 檔案時，會在頁面維度中加入個別的框架 (請參閱 [建立和儲存 Multiple-Frame 映射](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)) 。 此程式碼會顯示四個頁面中的每個頁面，並將每個頁面儲存至不同的 PNG 磁片檔案。

程式碼會從多框架 TIFF 檔案中建立 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 物件。 若要)  (頁面抓取個別的框架，程式碼會呼叫該 **影像** 物件的 [**Image：： SelectActiveFrame**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-selectactiveframe)方法。 傳遞至 **Image：： SelectActiveFrame** 方法的第一個引數是 GUID 的位址，這個 GUID 會指定框架先前加入至多框架 TIFF 檔案的維度。 GUID FrameDimensionPage 定義于 Gdiplusimaging 中。 在該標頭檔中定義的其他 Guid 為 FrameDimensionTime 和 FrameDimensionResolution。 傳遞至 **Image：： SelectActiveFrame** 方法的第二個引數是所需頁面的以零為基底的索引。

程式碼會依賴 helper 函式 GetEncoderClsid，它會顯示在抓取 [編碼器的類別識別碼](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)中。


```
GUID   pageGuid = FrameDimensionPage;
CLSID  encoderClsid;
Image  multi(L"Multiframe.tif");

// Get the CLSID of the PNG encoder.
GetEncoderClsid(L"image/png", &encoderClsid);

// Display and save the first page (index 0).
multi.SelectActiveFrame(&pageGuid, 0);
graphics.DrawImage(&multi, 10, 10);
multi.Save(L"Page0.png", &encoderClsid, NULL);

// Display and save the second page.
multi.SelectActiveFrame(&pageGuid, 1);
graphics.DrawImage(&multi, 200, 10);
multi.Save(L"Page1.png", &encoderClsid, NULL);

// Display and save the third page.
multi.SelectActiveFrame(&pageGuid, 2);
graphics.DrawImage(&multi, 10, 150);
multi.Save(L"Page2.png", &encoderClsid, NULL);

// Display and save the fourth page.
multi.SelectActiveFrame(&pageGuid, 3);
graphics.DrawImage(&multi, 200, 150);
multi.Save(L"Page3.png", &encoderClsid, NULL);
```



下圖顯示上述程式碼所顯示的個別頁面。

![顯示幾何圖形、彩色相片、單色相片和不同幾何形狀的圖例](images/multiframe1.png)

 

 



