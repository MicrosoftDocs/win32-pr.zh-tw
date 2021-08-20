---
description: Image 類別提供 Image：： GetEncoderParameterList 方法，讓您可以判斷指定影像編碼器所支援的參數。
ms.assetid: 2e1a5279-dd9d-46de-822c-d356a344f340
title: 判斷編碼器所支援的參數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c842b14a2d14af578eede428e79018a2d266ea6133ed61a9bd0736e8dadc97e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977568"
---
# <a name="determining-the-parameters-supported-by-an-encoder"></a>判斷編碼器所支援的參數

[**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image)類別提供 [**Image：： GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist)方法，讓您可以判斷指定影像編碼器所支援的參數。 **Image：： GetEncoderParameterList** 方法會傳回 [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter)物件的陣列。 您必須先配置緩衝區來接收該陣列，然後再呼叫 **Image：： GetEncoderParameterList**。 您可以呼叫 [**Image：： GetEncoderParameterListSize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlistsize) 來判斷所需的緩衝區大小。

下列主控台應用程式會取得 JPEG 編碼器的參數清單。 Main 函式依賴 helper 函式 GetEncoderClsid，其顯示于抓取 [編碼器的類別識別碼](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)。


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

   // Create Bitmap (inherited from Image) object so that we can call
   // GetParameterListSize and GetParameterList.
   Bitmap* bitmap = new Bitmap(1, 1);

   // Get the JPEG encoder CLSID.
   CLSID encoderClsid;
   GetEncoderClsid(L"image/jpeg", &encoderClsid);

   // How big (in bytes) is the JPEG encoder's parameter list?
   UINT listSize = 0; 
   listSize = bitmap->GetEncoderParameterListSize(&encoderClsid);
   printf("The parameter list requires %d bytes.\n", listSize);

   // Allocate a buffer large enough to hold the parameter list.
   EncoderParameters* pEncoderParameters = NULL;
   pEncoderParameters = (EncoderParameters*)malloc(listSize);

   // Get the parameter list for the JPEG encoder.
   bitmap->GetEncoderParameterList(
      &encoderClsid, listSize, pEncoderParameters);

   // pEncoderParameters points to an EncoderParameters object, which
   // has a Count member and an array of EncoderParameter objects.
   // How many EncoderParameter objects are in the array?
   printf("There are %d EncoderParameter objects in the array.\n", 
      pEncoderParameters->Count);

   free(pEncoderParameters);
   delete(bitmap);
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



當您執行上述的主控台應用程式時，您會取得如下所示的輸出：


```
The parameter list requires 172 bytes.
There are 4 EncoderParameter objects in the array.
```



陣列中的每個 [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) 物件都有下列四個公用資料成員：

下列程式碼是先前範例中所示的主控台應用程式接續。 程式碼會查看 [**Image：： GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist)所傳回之陣列中的第二個 [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter)物件。 程式碼會呼叫 [StringFromGUID2](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2)，這是在 Objbase 中宣告的系統函數，可將 **EncoderParameter** 物件的 **Guid** 成員轉換成字串。


```
// Look at the second (index 1) EncoderParameter object in the array.
printf("Parameter[1]\n");

WCHAR strGuid[39];
StringFromGUID2(pEncoderParameters->Parameter[1].Guid, strGuid, 39);
wprintf(L"   The GUID is %s.\n", strGuid);

printf("   The value type is %d.\n", 
   pEncoderParameters->Parameter[1].Type);

printf("   The number of values is %d.\n",
   pEncoderParameters->Parameter[1].NumberOfValues);
```



前一個程式碼會產生下列輸出：


```
Parameter[1]
   The GUID is {1D5BE4B5-FA4A-452D-9CDD-5DB35105E7EB}.
   The value type is 6.
   The number of values is 1.
```



您可以查詢 Gdiplusimaging 中的 GUID，並找出這個 [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) 物件的類別是 EncoderQuality。 您可以使用此類別 (EncoderQuality) 的參數來設定 JPEG 影像的壓縮等級。

在 Gdiplusenums 中， [**2csystem.drawing.imaging.encoderparametervaluetype**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) 列舉表示資料類型6是 **ValueLongRange**。 Long 範圍是一對 **ULONG** 值。

值的數目是一，因此我們知道 [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter)物件的 **值** 成員是具有一個元素之陣列的指標。 其中一個元素是一對 **ULONG** 值。

下列程式碼是先前的兩個範例中所示的主控台應用程式接續。 此程式碼會定義名為 **PLONGRANGE** 的資料類型， (指向較長範圍) 的指標。 **PLONGRANGE** 型別的變數可用來將可當做品質設定傳遞的最小值和最大值解壓縮到 JPEG 編碼器。


```
typedef struct
   {
      long min;
      long max;
   }* PLONGRANGE;

   PLONGRANGE pLongRange = 
      (PLONGRANGE)(pEncoderParameters->Parameter[1].Value);

   printf("   The minimum possible quality value is %d.\n",
      pLongRange->min);

   printf("   The maximum possible quality value is %d.\n",
      pLongRange->max);
```



前一個程式碼會產生下列輸出：


```
The minimum possible quality value is 0.
The maximum possible quality value is 100.
```



在上述範例中， [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) 物件中傳回的值是一對 **ULONG** 值，指出 quality 參數的最小值和最大可能值。 在某些情況下， **EncoderParameter** 物件中傳回的值是 [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) 列舉的成員。 下列主題討論 **EncoderValue** 列舉和方法，以更詳細地列出可能的參數值：

-   [使用 EncoderValue 列舉](-gdiplus-using-the-encodervalue-enumeration-use.md)
-   [列出所有編碼器的參數和值](-gdiplus-listing-parameters-and-values-for-all-encoders-use.md)

 

 
