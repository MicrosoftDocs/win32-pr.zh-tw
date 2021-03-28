---
description: 中繼檔類別繼承自 Image 類別，可讓您記錄一系列的繪圖命令。
ms.assetid: 062de6c2-9f82-415d-860e-2d1afd2ac027
title: 錄製中繼檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 129b8fe810b1394921c60540488c93676341c562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972152"
---
# <a name="recording-metafiles"></a>錄製中繼檔

[**中繼檔**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile)類別繼承自 [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image)類別，可讓您記錄一系列的繪圖命令。 錄製的命令可以儲存在記憶體中、儲存至檔案，或儲存至資料流程。 中繼檔可以包含向量圖形、點陣影像和文字。

下列範例會建立 [**中繼檔**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) 物件。 程式碼會使用 **中繼檔** 物件來記錄圖形命令序列，然後將記錄的命令儲存在名為 SampleMetafile 的檔案中。 請注意， **中繼檔** 的函式會接收裝置內容控制碼，而 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 的函式會接收 **中繼檔** 物件的位址。 當 **圖形** 物件超出範圍時，會停止錄製 (，並將記錄的命令儲存至檔案) 。 最後兩行程式碼會藉由建立新的 **圖形** 物件，並將 **中繼檔** 物件的位址傳遞給該 **圖形** 物件的 **DrawImage** 方法，來顯示中繼檔。 請注意，程式碼會使用相同的 **中繼檔** 物件來記錄，並顯示 (播放中繼檔) 。


```
Metafile metafile(L"SampleMetafile.emf", hdc); 
{
   Graphics graphics(&metafile);
   Pen greenPen(Color(255, 0, 255, 0));
   SolidBrush solidBrush(Color(255, 0, 0, 255));

   // Add a rectangle and an ellipse to the metafile.
   graphics.DrawRectangle(&greenPen, Rect(50, 10, 25, 75));
   graphics.DrawEllipse(&greenPen, Rect(100, 10, 25, 75));

   // Add an ellipse (drawn with antialiasing) to the metafile.
   graphics.SetSmoothingMode(SmoothingModeHighQuality);
   graphics.DrawEllipse(&greenPen, Rect(150, 10, 25, 75));

   // Add some text (drawn with antialiasing) to the metafile.
   FontFamily fontFamily(L"Arial");
   Font font(&fontFamily, 24, FontStyleRegular, UnitPixel);
   
   graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
   graphics.RotateTransform(30.0f);
   graphics.DrawString(L"Smooth Text", 11, &font, 
      PointF(50.0f, 50.0f), &solidBrush);
} // End of recording metafile.

// Play back the metafile.
Graphics playbackGraphics(hdc);
playbackGraphics.DrawImage(&metafile, 200, 100);
```



> [!Note]  
> 若要記錄中繼檔，您必須根據 [**中繼檔**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile)物件來建立 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件。 當 **圖形** 物件被刪除或移出範圍時，中繼檔的錄製便會結束。

 

中繼檔包含自己的圖形狀態，此狀態是由用來記錄中繼檔的 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件所定義。 **圖形** 物件的任何屬性 (裁剪區域、世界轉換、平滑模式，以及您在錄製中繼檔時設定的類似) 都會儲存在中繼檔中。 當您顯示中繼檔時，將會根據這些儲存的屬性來完成繪圖。

在下列範例中，假設在錄製中繼檔期間已將平滑模式設定為 SmoothingModeNormal。 即使用於播放的 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件平滑模式設定為 SmoothingModeHighQuality，也會根據 SmoothingModeNormal 設定來播放中繼檔。 它是在錄製期間設定的平滑模式，而不是在播放之前設定的平滑模式。


```
graphics.SetSmoothingMode(SmoothingModeHighQuality);
graphics.DrawImage(&meta, 0, 0);
```



 

 



