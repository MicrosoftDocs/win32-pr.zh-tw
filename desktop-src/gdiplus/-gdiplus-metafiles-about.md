---
description: Windows GDI + 提供了中繼檔類別，讓您可以記錄和顯示中繼檔。
ms.assetid: a9f9bac4-f3c7-44a1-9f0f-59ff1a27b077
title: " (GDI +) 的中繼檔"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae75c2185670563f9a9e624d868da5b0e299cbec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318339"
---
# <a name="metafiles-gdi"></a> (GDI +) 的中繼檔

Windows GDI + 提供了 [**中繼檔**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) 類別，讓您可以記錄和顯示中繼檔。 中繼檔（也稱為向量影像）是儲存為一系列繪製命令和設定的影像。 在 **中繼檔** 物件中記錄的命令和設定可以儲存在記憶體中，或儲存至檔案或資料流程。

GDI + 可以顯示以下列格式儲存的中繼檔：

-   Windows 中繼檔格式 (WMF) 
-   加強型中繼檔 (EMF) 
-   EMF +

GDI + 可以記錄 EMF 和 EMF + 格式的中繼檔，但不能以 WMF 格式記錄。

EMF + 是 EMF 的延伸模組，可讓您儲存 GDI + 記錄。 EMF + 格式有兩種變化： [僅限 EMF +] 和 [EMF + 雙重]。 僅限 EMF + 的中繼檔只包含 GDI + 記錄。 GDI + 可能會顯示這類中繼檔，但 Windows 圖形裝置介面 (GDI) 。 EMF + 雙重中繼檔包含 GDI + 和 GDI 記錄。 EMF + 雙重中繼檔中的每個 GDI + 記錄都會與替代的 GDI 記錄配對。 GDI + 或 GDI 可以顯示這類中繼檔。

下列範例會在磁片檔案中記錄一個設定和一個繪圖命令。 請注意，此範例會建立 [**graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件，而 **graphics** 物件的函式會接收 [**中繼檔**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) 物件的位址做為引數。


```
myMetafile = new Metafile(L"MyDiskFile.emf", hdc);
myGraphics = new Graphics(myMetafile);
   myPen = new Pen(Color(255, 0, 0, 200));
   myGraphics->SetSmoothingMode(SmoothingModeAntiAlias);
   myGraphics->DrawLine(myPen, 0, 0, 60, 40);
delete myGraphics;
delete myPen;
delete myMetafile;
```



如上一個範例所示， [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 類別是在 [**中繼檔**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) 物件中記錄指令和設定的關鍵。 對 **圖形** 物件的方法所做的任何呼叫都可以記錄在 **中繼檔** 物件中。 同樣地，您可以設定 **圖形** 物件的任何屬性，並將該設定記錄在 **中繼檔** 物件中。 當 **圖形** 物件被刪除或超出範圍時，就會結束錄製。

下列範例會顯示先前範例中所建立的中繼檔。 中繼檔的左上角會顯示 (100，100) 。


```
Graphics myGraphics(hdc);
Image myImage(L"MyDiskFile.emf");
myGraphics.DrawImage(&myImage, 100, 100);
```



下列範例會記錄 [**中繼檔**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) 物件中 (裁剪區域、世界轉換和平滑模式) 的數個屬性設定。 然後，程式碼會記錄數個繪圖指令。 指示和設定會儲存在磁片檔案中。


```
myMetafile = new Metafile(L"MyDiskFile2.emf", hdc); 
myGraphics = new Graphics(myMetafile);
   myGraphics->SetSmoothingMode(SmoothingModeAntiAlias);
   myGraphics->RotateTransform(30);

   // Create an elliptical clipping region.
   GraphicsPath myPath;
   myPath.AddEllipse(0, 0, 200, 100);
   Region myRegion(&myPath);
   myGraphics->SetClip(&myRegion);

   Pen myPen(Color(255, 0, 0, 255));
   myGraphics->DrawPath(&myPen, &myPath);

   for(INT j = 0; j <= 300; j += 10)
   {
      myGraphics->DrawLine(&myPen, 0, 0, 300 - j, j);
   }
delete myGraphics;
delete myMetafile;
```



下列範例會顯示先前範例中所建立的中繼檔映射。


```
myGraphics = new Graphics(hdc);
myMetafile = new Metafile(L"MyDiskFile.emf");
myGraphics->DrawImage(myMetafile, 10, 10);
```



下圖顯示上述程式碼的輸出。 請注意消除鋸齒、橢圓形裁剪區域和30度旋轉。

![視窗的螢幕擷取畫面，其中包含填滿繪製于橢圓形外面某個點之線條的橢圓形](images/aboutgdip05-art00.png)

 

 



