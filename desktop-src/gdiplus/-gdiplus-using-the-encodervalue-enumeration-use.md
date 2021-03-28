---
description: 指定的編碼器支援特定的參數分類，而針對每個類別，該編碼器會允許特定的值。
ms.assetid: cb9552e9-e807-4b07-b315-4550762e7026
title: 使用 EncoderValue 列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d755248150e81f963ea1c5c597ab04649c342944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972824"
---
# <a name="using-the-encodervalue-enumeration"></a><span data-ttu-id="88507-103">使用 EncoderValue 列舉</span><span class="sxs-lookup"><span data-stu-id="88507-103">Using the EncoderValue Enumeration</span></span>

<span data-ttu-id="88507-104">指定的編碼器支援特定的參數分類，而針對每個類別，該編碼器會允許特定的值。</span><span class="sxs-lookup"><span data-stu-id="88507-104">A given encoder supports certain parameter categories, and for each of those categories, that encoder allows certain values.</span></span> <span data-ttu-id="88507-105">例如，JPEG 編碼器支援 EncoderValueQuality 參數分類，而允許的參數值為0到100的整數。</span><span class="sxs-lookup"><span data-stu-id="88507-105">For example, the JPEG encoder supports the EncoderValueQuality parameter category, and the allowable parameter values are the integers 0 through 100.</span></span> <span data-ttu-id="88507-106">部分允許的參數值在數個編碼器中都相同。</span><span class="sxs-lookup"><span data-stu-id="88507-106">Some of the allowable parameter values are the same across several encoders.</span></span> <span data-ttu-id="88507-107">這些標準值定義于 Gdiplusenums 中的 [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) 列舉：</span><span class="sxs-lookup"><span data-stu-id="88507-107">These standard values are defined in the [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) enumeration in Gdiplusenums.h:</span></span>


```
enum EncoderValue
{
   EncoderValueColorTypeCMYK,             // 0
   EncoderValueColorTypeYCCK,             // 1
   EncoderValueCompressionLZW,            // 2
   EncoderValueCompressionCCITT3,         // 3
   EncoderValueCompressionCCITT4,         // 4
   EncoderValueCompressionRle,            // 5
   EncoderValueCompressionNone,           // 6
   EncoderValueScanMethodInterlaced,      // 7
   EncoderValueScanMethodNonInterlaced,   // 8
   EncoderValueVersionGif87,              // 9
   EncoderValueVersionGif89,              // 10
   EncoderValueRenderProgressive,         // 11
   EncoderValueRenderNonProgressive,      // 12
   EncoderValueTransformRotate90,         // 13
   EncoderValueTransformRotate180,        // 14
   EncoderValueTransformRotate270,        // 15
   EncoderValueTransformFlipHorizontal,   // 16
   EncoderValueTransformFlipVertical,     // 17
   EncoderValueMultiFrame,                // 18
   EncoderValueLastFrame,                 // 19
   EncoderValueFlush,                     // 20
   EncoderValueFrameDimensionTime,        // 21
   EncoderValueFrameDimensionResolution,  // 22
   EncoderValueFrameDimensionPage         // 23
};
```



<span data-ttu-id="88507-108">JPEG 編碼器所支援的其中一個參數分類是 EncoderTransformation 類別。</span><span class="sxs-lookup"><span data-stu-id="88507-108">One of the parameter categories supported by the JPEG encoder is the EncoderTransformation category.</span></span> <span data-ttu-id="88507-109">藉由檢查 [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) 列舉，您可能會 speculate (，且您會正確) EncoderTransformation 類別目錄允許下列五個值：</span><span class="sxs-lookup"><span data-stu-id="88507-109">By examining the [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) enumeration, you might speculate (and you would be correct) that the EncoderTransformation category allows the following five values:</span></span>


```
EncoderValueTransformRotate90,          // 13
EncoderValueTransformRotate180,         // 14
EncoderValueTransformRotate270,         // 15
EncoderValueTransformFlipHorizontal,    // 16
EncoderValueTransformFlipVertical,      // 17
```



<span data-ttu-id="88507-110">下列主控台應用程式會驗證 JPEG 編碼器是否支援 EncoderTransformation 參數類別目錄，以及這類參數是否有五個可允許的值。</span><span class="sxs-lookup"><span data-stu-id="88507-110">The following console application verifies that the JPEG encoder supports the EncoderTransformation parameter category and that there are five allowable values for such a parameter.</span></span> <span data-ttu-id="88507-111">Main 函式依賴 helper 函式 GetEncoderClsid，其顯示于抓取 [編碼器的類別識別碼](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)。</span><span class="sxs-lookup"><span data-stu-id="88507-111">The main function relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;
INT GetEncoderClsid(const WCHAR* format, CLSID* pClsid);
INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);
   // Create a Bitmap (inherited from Image) object so that we can call
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
   // Look at the first (index 0) EncoderParameter object in the array.
   printf("Parameter[0]\n");
   WCHAR strGuid[39];
   StringFromGUID2(pEncoderParameters->Parameter[0].Guid, strGuid, 39);
   wprintf(L"   The guid is %s.\n", strGuid);
   printf("   The data type is %d.\n", 
      pEncoderParameters->Parameter[0].Type);
   printf("   The number of values is %d.\n",
      pEncoderParameters->Parameter[0].NumberOfValues);
   free(pEncoderParameters);
   delete bitmap;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



<span data-ttu-id="88507-112">當您執行上述的主控台應用程式時，您會取得如下所示的輸出：</span><span class="sxs-lookup"><span data-stu-id="88507-112">When you run the preceding console application, you get an output similar to the following:</span></span>


```
The parameter list requires 172 bytes.
There are 4 EncoderParameter objects in the array.
Parameter[0]
   The GUID is {8D0EB2D1-A58E-4EA8-AA14-108074B7B6F9}.
   The value type is 4.
   The number of values is 5.
```



<span data-ttu-id="88507-113">您可以查詢 Gdiplusimaging 中的 GUID，並找出這個 [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) 物件的類別是 EncoderTransformation。</span><span class="sxs-lookup"><span data-stu-id="88507-113">You can look up the GUID in Gdiplusimaging.h and find out that the category of this [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object is EncoderTransformation.</span></span> <span data-ttu-id="88507-114">在 Gdiplusenums 中， [**2csystem.drawing.imaging.encoderparametervaluetype**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) 列舉表示資料類型4是 ValueLong (32 位不帶正負號整數) 。</span><span class="sxs-lookup"><span data-stu-id="88507-114">In Gdiplusenums.h, the [**EncoderParameterValueType**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) enumeration indicates that data type 4 is ValueLong (32-bit unsigned integer).</span></span> <span data-ttu-id="88507-115">值的數目為5，因此我們知道 **EncoderParameter** 物件的 **值** 成員是指向五個 **ULONG** 值陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="88507-115">The number of values is five, so we know that the **Value** member of the **EncoderParameter** object is a pointer to an array of five **ULONG** values.</span></span>

<span data-ttu-id="88507-116">下列程式碼是先前範例中所示的主控台應用程式接續。</span><span class="sxs-lookup"><span data-stu-id="88507-116">The following code is a continuation of the console application that is shown in the preceding example.</span></span> <span data-ttu-id="88507-117">程式碼會列出 EncoderTransformation 參數允許的值：</span><span class="sxs-lookup"><span data-stu-id="88507-117">The code lists the allowable values for an EncoderTransformation parameter:</span></span>


```
ULONG* pUlong = (ULONG*)(pEncoderParameters->Parameter[0].Value);
ULONG numVals = pEncoderParameters->Parameter[0].NumberOfValues;
printf("%s", "   The allowable values are");
for(ULONG j = 0; j < numVals; ++j)
{
   printf("  %d", pUlong[j]);
}
```



<span data-ttu-id="88507-118">前一個程式碼會產生下列輸出：</span><span class="sxs-lookup"><span data-stu-id="88507-118">The preceding code produces the following output:</span></span>


```
The allowable values are  13  14  15  16  17
```



<span data-ttu-id="88507-119">可允許的值 (13、14、15、16和 17) 對應至 [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) 列舉的下列成員：</span><span class="sxs-lookup"><span data-stu-id="88507-119">The allowable values (13, 14, 15, 16, and 17) correspond to the following members of the [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) enumeration:</span></span>


```
EncoderValueTransformRotate90,        // 13
EncoderValueTransformRotate180,       // 14
EncoderValueTransformRotate270,       // 15
EncoderValueTransformFlipHorizontal,  // 16
EncoderValueTransformFlipVertical,    // 17
```



 

 
