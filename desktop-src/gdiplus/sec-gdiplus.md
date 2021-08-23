---
description: 本主題提供使用 Windows GDI+ 進行程式設計相關安全性考慮的資訊。
ms.assetid: 411e16e4-ad8f-4567-8964-564f08283ba5
title: 安全性考慮： GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdc741911af403f079d16b4759431eaaa4b6cf55d5dad11826768033036aef75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035996"
---
# <a name="security-considerations-gdi"></a>安全性考慮： GDI+

本主題提供使用 Windows GDI+ 進行程式設計相關安全性考慮的資訊。 本主題並未提供安全性問題的相關資訊，而是將其作為此技術領域的起點和參考。

-   [驗證函式是否成功](#verifying-the-success-of-constructors)
-   [配置緩衝區](#allocating-buffers)
-   [錯誤檢查](#error-checking)
-   [執行緒同步處理](#thread-synchronization)
-   [相關主題](#related-topics)

## <a name="verifying-the-success-of-constructors"></a>驗證函式是否成功

許多 GDI+ 類別都提供 [**Image：： GetLastStatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus)方法，您可以呼叫這個方法來判斷在物件上叫用的方法是否成功。 您也可以呼叫 **Image：： GetLastStatus** 來判斷是否成功。

下列範例示範如何建立 [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 物件，並呼叫 [**Image：： GetLastStatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) 方法來判斷是否成功。 **Ok** 和 **InvalidParameter** 值是 [**Status**](/windows/desktop/api/Gdiplustypes/ne-gdiplustypes-status)列舉的元素。


```C++
Image myImage(L"Climber.jpg");
Status st = myImage.GetLastStatus();

if(Ok == st)
   // The constructor was successful. Use myImage.
else if(InvalidParameter == st)
   // The constructor failed because of an invalid parameter.
else
   // Compare st to other elements of the Status 
   // enumeration or do general error processing.
```



## <a name="allocating-buffers"></a>配置緩衝區

數個 GDI+ 方法會傳回呼叫端配置的緩衝區中的數值或字元資料。 這兩種方法都有提供所需緩衝區大小的伴隨方法。 例如， [**GraphicsPath：： GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) 方法會傳回 [**Point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) 物件的陣列。 在呼叫 **GraphicsPath：： GetPathPoints** 之前，您必須配置夠大的緩衝區來保存該陣列。 您可以藉由呼叫 [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath)物件的 [**GraphicsPath：： GetPointCount**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-getpointcount)方法，來判斷所需的緩衝區大小。

下列範例示範如何判斷 [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) 物件中的點數目、配置夠大的緩衝區以容納多個點，然後呼叫 [**GraphicsPath：： GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) 來填滿緩衝區。 在程式碼呼叫 **GraphicsPath：： GetPathPoints** 之前，它會先確認緩衝區指標不是 **Null**，藉以驗證緩衝區配置是否成功。


```C++
GraphicsPath path;
path.AddEllipse(10, 10, 200, 100);

INT count = path.GetPointCount();          // get the size
Point* pointArray = new Point[count];      // allocate the buffer

if(pointArray)  // Check for successful allocation.
{
   path.GetPathPoints(pointArray, count);  // get the data
   ...                                     // use pointArray
   delete[] pointArray;                    // release the buffer
   pointArray = NULL;
}
```



上述範例使用 new 運算子來配置緩衝區。 New 運算子很方便，因為緩衝區已填滿已知數目的 [**點**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) 物件。 在某些情況下，GDI+ 將更多寫入緩衝區，而不是 GDI+ 物件的陣列。 有時候緩衝區會填入 GDI+ 物件的陣列，以及這些物件的成員所指向的其他資料。 例如， [**image：： GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) 方法會傳回 [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) 物件的陣列，每一個屬性專案 (部分的中繼資料) 儲存在影像中。 但 **Image：： GetAllPropertyItems** 傳回的不只是 **PropertyItem** 物件的陣列;它會附加具有其他資料的陣列。

在您呼叫 [**Image：： GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems)之前，您必須配置夠大的緩衝區，以容納 [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) 物件的陣列以及額外的資料。 您可以呼叫影像物件的 [**image：： GetPropertySize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) 方法，以判斷所需緩衝區的總大小。

下列範例示範如何建立 [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image)物件，並在稍後呼叫該 **Image** 物件的 [**image：： GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems)方法，以抓取儲存在影像中 (中繼資料) 的所有屬性專案。 程式碼會根據 [**Image：： GetPropertySize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) 方法所傳回的大小值配置緩衝區。 **Image：： GetPropertySize** 也會傳回 count 值，以提供影像中屬性專案的數目。 請注意，程式碼不會將緩衝區大小計算為 `count*sizeof(PropertyItem)` 。 以該方式計算的緩衝區太小。


```C++
UINT count = 0;
UINT size = 0;
Image myImage(L"FakePhoto.jpg");
myImage.GetPropertySize(&size, &count);

// GetAllPropertyItems returns an array of PropertyItem objects
// along with additional data. Allocate a buffer large enough to 
// receive the array and the additional data.
PropertyItem* propBuffer =(PropertyItem*)malloc(size);

if(propBuffer)
{
   myImage.GetAllPropertyItems(size, count, propBuffer);
   ...
   free(propBuffer);
   propBuffer = NULL;
}
```



## <a name="error-checking"></a>錯誤檢查

GDI+ 檔中的大部分程式碼範例都不會顯示錯誤檢查。 完成錯誤檢查會讓程式碼範例變得更久，而且可能會遮蔽範例所說明的點。 您不應該將範例直接從檔貼入生產程式碼;相反地，您應該新增自己的錯誤檢查來增強範例。

下列範例示範如何使用 GDI+ 來執行錯誤檢查。 每次建立 GDI+ 物件時，程式碼都會檢查是否成功。 這項檢查對於需要讀取檔案的 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 檢查點而言特別重要。 如果所有四個 GDI+ 物件 ([**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)、 [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath)、**影像** 和 [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush)) 都已成功建立，則程式碼會在這些物件上呼叫方法。 系統會檢查每個方法呼叫是否成功，如果發生失敗，則會略過其餘的方法呼叫。


```C++
Status GdipExample(HDC hdc)
{
   Status status = GenericError;
   INT count = 0;
   Point* points = NULL;

   Graphics graphics(hdc);
   status = graphics.GetLastStatus();
   if(Ok != status)
      return status;

   GraphicsPath path;
   status = path.GetLastStatus();
   if(Ok != status)
      return status;

   Image image(L"MyTexture.bmp");
   status = image.GetLastStatus();
   if(Ok != status)
      return status;

   TextureBrush brush(&image);
   status = brush.GetLastStatus();
   if(Ok != status)
      return status;

   status = path.AddEllipse(10, 10, 200, 100);

   if(Ok == status)
   {
      status = path.AddBezier(40, 130, 200, 130, 200, 200, 60, 200);
   }
  
   if(Ok == status)
   {
      count = path.GetPointCount();
      status = path.GetLastStatus();
   }

   if(Ok == status)
   {
      points = new Point[count];

      if(NULL == points)
         status = OutOfMemory;
   }

   if(Ok == status)
   {
      status = path.GetPathPoints(points, count);  
   }
  
   if(Ok == status)
   {
      status = graphics.FillPath(&brush, &path);
   }
   
   if(Ok == status)
   {
      for(int j = 0; j < count; ++j)
      {
         status = graphics.FillEllipse(
         &brush, points[j].X - 5, points[j].Y - 5, 10, 10);
      }
   }

   if(points)
   {
      delete[] points;
      points = NULL;
   }

   return status;
}
```



## <a name="thread-synchronization"></a>執行緒同步處理

有一個以上的執行緒可以存取單一 GDI+ 物件。 不過，GDI+ 不會提供任何自動同步處理機制。 因此，如果您的應用程式中有兩個執行緒具有相同 GDI+ 物件的指標，則您必須負責同步處理該物件的存取權。

如果執行緒嘗試呼叫方法，而另一個執行緒在相同物件上執行方法，某些 GDI+ 方法會傳回 **ObjectBusy** 。 請勿嘗試根據 **ObjectBusy** 傳回值來同步處理對物件的存取。 相反地，每次您存取某個成員或呼叫物件的方法時，請將呼叫放在重要區段內，或使用其他標準同步處理技術。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[MSDN Security Developer Center](https://msdn.microsoft.com/security/)
</dt> <dt>

[安全性 How-To 資源](/previous-versions/msp-n-p/ff650055(v=pandp.10))
</dt> <dt>

[TechNet 安全性中心](https://technet.microsoft.com/security/)
</dt> </dl>

 

 
