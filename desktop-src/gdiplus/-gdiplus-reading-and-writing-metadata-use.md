---
description: 有些影像檔案包含可供您讀取的中繼資料，以判斷影像的功能。
ms.assetid: 2febea35-3fea-4a2d-baaf-7a4f935fc81f
title: 讀取和寫入中繼資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2f599c1134efc8768d0b6ed59deaae8adf9f6f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690335"
---
# <a name="reading-and-writing-metadata"></a>讀取和寫入中繼資料

有些影像檔案包含可供您讀取的中繼資料，以判斷影像的功能。 例如，數位相片可能包含您可以讀取的中繼資料，以判斷用來捕捉影像的相機製作和型號。 您可以使用 Windows GDI + 來讀取現有的中繼資料，也可以將新的中繼資料寫入影像檔案。

GDI + 提供統一的方式，可從影像檔案以各種格式儲存和抓取中繼資料。 在 GDI + 中，中繼資料的部分稱為 *屬性專案*。 您可以藉由呼叫 [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image)類別的 **SetPropertyItem** 和 **GetPropertyItem** 方法來儲存和取出中繼資料，而不需要擔心特定檔案格式儲存該中繼資料的詳細資料。

GDI + 目前支援 TIFF、JPEG、Exif 和 PNG 檔案格式的中繼資料。 此 Exif 格式可指定如何儲存數位攝影機所捕捉的影像，並以 TIFF 和 JPEG 格式為基礎。 Exif 針對未壓縮的圖元資料使用 TIFF 格式，並針對壓縮的圖元資料使用 JPEG 格式。

GDI + 會定義一組用來識別屬性專案的屬性標記。 某些標記為一般用途;亦即，上一段所述的所有檔案格式都支援它們。 其他標記是特殊用途，只適用于特定格式。 如果您嘗試將屬性專案儲存至不支援該屬性專案的檔案，GDI + 會忽略要求。 更具體來說， [**Image：： SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) 方法會傳回 PropertyNotSupported。

您可以藉由呼叫 [**image：： GetPropertyIdList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyidlist)，判斷儲存在影像檔案中的屬性專案。 如果您嘗試抓取不在檔案中的屬性專案，GDI + 會忽略要求。 更具體來說， [**Image：： GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) 方法會傳回 PropertyNotFound。

## <a name="reading-metadata-from-a-file"></a>從檔案讀取中繼資料

下列主控台應用程式會呼叫 [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image)物件的 **GetPropertySize** 方法，以判斷 FakePhoto.jpg 檔案中有多少部分的中繼資料。


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;
INT main()
{
   // Initialize <tla rid="tla_gdiplus"/>.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);
   UINT    size = 0;
   UINT    count = 0;
   Bitmap* bitmap = new Bitmap(L"FakePhoto.jpg");
   bitmap->GetPropertySize(&size, &count);
   printf("There are %d pieces of metadata in the file.\n", count);
   printf("The total size of the metadata is %d bytes.\n", size);
 
   delete bitmap;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



上述程式碼和特定檔案 FakePhoto.jpg，會產生下列輸出：


```
There are 7 pieces of metadata in the file.
The total size of the metadata is 436 bytes.
```



GDI + 會將個別的中繼資料儲存在 [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) 物件中。 您可以呼叫 [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image)類別的 **GetAllPropertyItems** 方法，從檔案取出所有中繼資料。 **GetAllPropertyItems** 方法會傳回 **PropertyItem** 物件的陣列。 在呼叫 **GetAllPropertyItems** 之前，您必須配置夠大的緩衝區來接收該陣列。 您可以呼叫 **Image** 類別的 **GetPropertySize** 方法，以取得所需緩衝區)  (位元組大小。

[**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem)物件具有下列四個公用成員：



|            |                                                                                                                                                                                                                                                                                                        |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **id**     | 識別中繼資料專案的標記。 可以指派給 **識別碼** 的值 (PropertyTagImageTitle、PropertyTagEquipMake、PropertyTagExifExposureTime 和 like) 都定義于 Gdiplusimaging 中。                                                                                           |
| **length** (長度) | **值** 資料成員所指向之值陣列的長度（以位元組為單位）。 請注意，如果 **類型** 資料成員設為 PropertyTagTypeASCII，則長度資料成員是以 null 結束的字元字串 **長度** ，包括 null 結束字元。                        |
| **type**   | 值資料成員所指向陣列中值的資料類型。 常數 (PropertyTagTypeByte、PropertyTagTypeASCII 和表示各種資料類型的 like) ，都是在 [**影像屬性標記類型常數**](-gdiplus-constant-image-property-tag-type-constants.md)中描述。 |
| **value**  | 值陣列的指標。                                                                                                                                                                                                                                                                       |



 

下列主控台應用程式會讀取並顯示檔案 FakePhoto.jpg 中的七個中繼資料片段。 Main 函式依賴 helper 函式 PropertyTypeFromWORD，它會在 main 函式之後顯示。


```
#include <windows.h>
#include <gdiplus.h>
#include <strsafe.h>
using namespace Gdiplus;

INT main()
{
   // Initialize GDI+
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   UINT  size = 0;
   UINT  count = 0;

   #define MAX_PROPTYPE_SIZE 30
   WCHAR strPropertyType[MAX_PROPTYPE_SIZE] = L"";

   Bitmap* bitmap = new Bitmap(L"FakePhoto.jpg");

   bitmap->GetPropertySize(&size, &count);
   printf("There are %d pieces of metadata in the file.\n\n", count);

   // GetAllPropertyItems returns an array of PropertyItem objects.
   // Allocate a buffer large enough to receive that array.
   PropertyItem* pPropBuffer =(PropertyItem*)malloc(size);

   // Get the array of PropertyItem objects.
   bitmap->GetAllPropertyItems(size, count, pPropBuffer);

   // For each PropertyItem in the array, display the id, type, and length.
   for(UINT j = 0; j < count; ++j)
   {
      // Convert the property type from a WORD to a string.
      PropertyTypeFromWORD(
         pPropBuffer[j].type, strPropertyType, MAX_PROPTYPE_SIZE);

      printf("Property Item %d\n", j);
      printf("  id: 0x%x\n", pPropBuffer[j].id);
      wprintf(L"  type: %s\n", strPropertyType);
      printf("  length: %d bytes\n\n", pPropBuffer[j].length);
   }

   free(pPropBuffer);
   delete bitmap;
   GdiplusShutdown(gdiplusToken);
   return 0;
} // main

// Helper function
HRESULT PropertyTypeFromWORD(WORD index, WCHAR* string, UINT maxChars)
{
   HRESULT hr = E_FAIL;

   WCHAR* propertyTypes[] = {
      L"Nothing",                   // 0
      L"PropertyTagTypeByte",       // 1
      L"PropertyTagTypeASCII",      // 2
      L"PropertyTagTypeShort",      // 3
      L"PropertyTagTypeLong",       // 4
      L"PropertyTagTypeRational",   // 5
      L"Nothing",                   // 6
      L"PropertyTagTypeUndefined",  // 7
      L"Nothing",                   // 8
      L"PropertyTagTypeSLONG",      // 9
      L"PropertyTagTypeSRational"}; // 10

   hr = StringCchCopyW(string, maxChars, propertyTypes[index]);
   return hr;
}
```



上述的主控台應用程式會產生下列輸出：


```
Property Item 0
  id: 0x320
  type: PropertyTagTypeASCII
  length: 16 bytes
Property Item 1
  id: 0x10f
  type: PropertyTagTypeASCII
  length: 17 bytes
Property Item 2
  id: 0x110
  type: PropertyTagTypeASCII
  length: 7 bytes
Property Item 3
  id: 0x9003
  type: PropertyTagTypeASCII
  length: 20 bytes
Property Item 4
  id: 0x829a
  type: PropertyTagTypeRational
  length: 8 bytes
Property Item 5
  id: 0x5090
  type: PropertyTagTypeShort
  length: 128 bytes
Property Item 6
  id: 0x5091
  type: PropertyTagTypeShort
  length: 128 bytes
```



上述輸出會顯示每個屬性專案的十六進位 ID 號碼。 您可以在 [影像屬性標記常數](-gdiplus-constant-image-property-tag-constants.md) 中查閱這些識別碼，並找出它們是否代表下列屬性標記。



| 十六進位值                                                                                                       | 屬性標記                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x0320 0x010f<br/>  0x0110<br/>  0x9003<br/>  0x829a<br/>  0x5090<br/>  0x5091<br/> | PropertyTagImageTitle PropertyTagEquipMake<br/>  PropertyTagEquipModel<br/>  PropertyTagExifDTOriginal<br/>  PropertyTagExifExposureTime<br/>  PropertyTagLuminanceTable<br/>  PropertyTagChrominanceTable<br/> |



 

清單中的第二個 (index 1) 屬性專案具有 **id** PropertyTagEquipMake 和 **類型** PropertyTagTypeASCII。 下列範例是前一個主控台應用程式的接續，會顯示該屬性專案的值：


```
printf("The equipment make is %s.\n", pPropBuffer[1].value);
```



上述程式程式碼會產生下列輸出：


```
The equipment make is Northwind Traders.
```



清單中的第五個 (index 4) 屬性專案具有 **id** PropertyTagExifExposureTime 和 **類型** PropertyTagTypeRational。 該資料類型 (PropertyTagTypeRational) 是一對 **LONG** s。 下列範例是前一個主控台應用程式的接續，會將這兩個 **長** 值顯示為分數。 該分數1/125 是以秒為單位的曝光時間。


```
long* ptrLong = (long*)(pPropBuffer[4].value);
printf("The exposure time is %d/%d.\n", ptrLong[0], ptrLong[1]);
```



前一個程式碼會產生下列輸出：


```
The exposure time is 1/125.
```



## <a name="writing-metadata-to-a-file"></a>將中繼資料寫入檔案

若要將中繼資料的專案寫入 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image)物件，請將 [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem)物件初始化，然後將該 **PropertyItem** 物件的位址傳遞至 **image** 物件的 **SetPropertyItem** 方法。

下列主控台應用程式會將 (影像標題) 的一個專案寫入 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 物件，然後將映射儲存在磁片檔案 FakePhoto2.jpg 中。 Main 函式依賴 helper 函式 GetEncoderClsid，它會在 [取得編碼器的類別識別碼](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)的主題中顯示。


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;
INT main()
{
   // Initialize <tla rid="tla_gdiplus"/>.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);
   Status stat;
   CLSID  clsid;
   char   propertyValue[] = "Fake Photograph";
   Bitmap* bitmap = new Bitmap(L"FakePhoto.jpg");
   PropertyItem* propertyItem = new PropertyItem;
   // Get the CLSID of the JPEG encoder.
   GetEncoderClsid(L"image/jpeg", &clsid);
   propertyItem->id = PropertyTagImageTitle;
   propertyItem->length = 16;  // string length including NULL terminator
   propertyItem->type = PropertyTagTypeASCII; 
   propertyItem->value = propertyValue;
   bitmap->SetPropertyItem(propertyItem);
   stat = bitmap->Save(L"FakePhoto2.jpg", &clsid, NULL);
   if(stat == Ok)
      printf("FakePhoto2.jpg saved successfully.\n");
   
   delete propertyItem;
   delete bitmap;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
