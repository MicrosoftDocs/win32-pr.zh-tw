---
description: 使用特定檔案格式時，您可以將多個映射 (框架) 儲存至單一檔案。
ms.assetid: 9b61e01d-0a98-4ac3-865e-7570ed0c3cde
title: 建立和儲存多框架影像
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd99bc2d5f21c143b66ccc201f9a96a93f3437516a6fd1cdd03e521a00ceb59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115118"
---
# <a name="creating-and-saving-a-multiple-frame-image"></a>建立和儲存多框架影像

使用特定檔案格式時，您可以將多個映射 (框架) 儲存至單一檔案。 例如，您可以將數個頁面儲存至單一 TIFF 檔案。 若要儲存第一個頁面，請呼叫 [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image)類別的 [save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters))方法。 若要儲存後續頁面，請呼叫 **Image** 類別的 [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))方法。

> [!Note]  
> 您無法使用 [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) 將畫面格新增至動畫 gif 檔案。

 

下列主控台應用程式會建立具有四個頁面的 TIFF 檔案。 成為 TIFF 檔案頁面的影像來自四個磁片檔案： Shapes.bmp、Cereal.gif、Iron.jpg 和 House.png。 程式碼會先建立四個 [**影像**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) 物件： **多重**、 **page2**、 **page3** 和 **page4**。 一開始， **多重** 只包含 Shapes.bmp 中的影像，但最後會包含四個映射。 當個別頁面新增至 **多** 個 **映射** 物件時，也會將這些頁面新增至磁片檔案 Multiframe .tif。  

請注意，程式碼會呼叫 [save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) (not [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))) 來儲存第一個頁面。 傳遞至 Save 方法的第一個引數是最後將包含數個框架的磁片檔案名。 傳遞至 Save 方法的第二個引數會指定將用來將 **多** 個 [**影像**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image)物件中的資料轉換成格式的編碼器 (在此案例中，磁片檔案需要 TIFF) 。   所有後續呼叫 **多重**  **映射** 物件的 SaveAdd 方法時，會自動使用相同的編碼器。

傳遞至 [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) 方法的第三個引數是 [**system.drawing.imaging.encoderparameters>**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) 物件的位址。 **System.drawing.imaging.encoderparameters>** 物件具有包含單一 [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter)物件的陣列。 該 **EncoderParameter** 物件的 **Guid** 成員會設定為 EncoderSaveFlag。 **EncoderParameter** 物件的 **值** 成員指向包含值 EncoderValueMultiFrame 的 **ULONG** 。

程式碼會藉由呼叫 **多重**[**影像**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image)物件的 [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))方法，來儲存第二、第三和第四個頁面。   傳遞至 SaveAdd 方法的第一個引數是 **Image** 物件的位址。 該 **映射** 物件中的影像會新增至 **多** 個 **映射** 物件，並且也會新增至 Multiframe .tif 磁片檔。   傳遞至 SaveAdd 方法的第二個引數是 [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters))方法所使用之相同 [**system.drawing.imaging.encoderparameters>**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters)物件的位址。 差別在於 **值** 成員所指向的 **ULONG** 現在包含值 EncoderValueFrameDimensionPage。

Main 函式依賴 helper 函式 GetEncoderClsid，其顯示于抓取 [編碼器的類別識別碼](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)。


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

INT GetEncoderClsid(const WCHAR* format, CLSID* pClsid);  // helper function

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   EncoderParameters encoderParameters;
   ULONG             parameterValue;
   Status            stat;

   // An EncoderParameters object has an array of
   // EncoderParameter objects. In this case, there is only
   // one EncoderParameter object in the array.
   encoderParameters.Count = 1;

   // Initialize the one EncoderParameter object.
   encoderParameters.Parameter[0].Guid = EncoderSaveFlag;
   encoderParameters.Parameter[0].Type = EncoderParameterValueTypeLong;
   encoderParameters.Parameter[0].NumberOfValues = 1;
   encoderParameters.Parameter[0].Value = &parameterValue;

   // Get the CLSID of the TIFF encoder.
   CLSID encoderClsid;
   GetEncoderClsid(L"image/tiff", &encoderClsid);

   // Create four image objects.
   Image* multi = new Image(L"Shapes.bmp");
   Image* page2 = new Image(L"Cereal.gif");
   Image* page3 = new Image(L"Iron.jpg");
   Image* page4 = new Image(L"House.png");

   // Save the first page (frame).
   parameterValue = EncoderValueMultiFrame;
   stat = multi->Save(L"MultiFrame.tif", &encoderClsid, &encoderParameters);
   if(stat == Ok)
      printf("Page 1 saved successfully.\n");

   // Save the second page (frame).
   parameterValue = EncoderValueFrameDimensionPage;
   stat = multi->SaveAdd(page2, &encoderParameters);
   if(stat == Ok)
      printf("Page 2 saved successfully.\n");

   // Save the third page (frame).
   parameterValue = EncoderValueFrameDimensionPage;
   stat = multi->SaveAdd(page3, &encoderParameters);
   if(stat == Ok)
      printf("Page 3 saved successfully.\n");

   // Save the fourth page (frame).
   parameterValue = EncoderValueFrameDimensionPage;
   stat = multi->SaveAdd(page4, &encoderParameters);
   if(stat == Ok)
      printf("Page 4 saved successfully.\n");

   // Close the multiframe file.
   parameterValue = EncoderValueFlush;
   stat = multi->SaveAdd(&encoderParameters);
   if(stat == Ok)
      printf("File closed successfully.\n");

   delete multi;
   delete page2;
   delete page3;
   delete page4;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
