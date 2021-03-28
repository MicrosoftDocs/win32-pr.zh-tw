---
description: Image 類別提供 Image：： GetEncoderParameterList 方法，讓您可以判斷指定影像編碼器所支援的參數。
ms.assetid: 2e1a5279-dd9d-46de-822c-d356a344f340
title: 判斷編碼器所支援的參數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad9bd76abb0b9f01bf55fd738df77cd086bc757c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991363"
---
# <a name="determining-the-parameters-supported-by-an-encoder"></a><span data-ttu-id="d4205-103">判斷編碼器所支援的參數</span><span class="sxs-lookup"><span data-stu-id="d4205-103">Determining the Parameters Supported by an Encoder</span></span>

<span data-ttu-id="d4205-104">[**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image)類別提供 [**Image：： GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist)方法，讓您可以判斷指定影像編碼器所支援的參數。</span><span class="sxs-lookup"><span data-stu-id="d4205-104">The [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class provides the [**Image::GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist) method so that you can determine the parameters that are supported by a given image encoder.</span></span> <span data-ttu-id="d4205-105">**Image：： GetEncoderParameterList** 方法會傳回 [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter)物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="d4205-105">The **Image::GetEncoderParameterList** method returns an array of [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) objects.</span></span> <span data-ttu-id="d4205-106">您必須先配置緩衝區來接收該陣列，然後再呼叫 **Image：： GetEncoderParameterList**。</span><span class="sxs-lookup"><span data-stu-id="d4205-106">You must allocate a buffer to receive that array before you call **Image::GetEncoderParameterList**.</span></span> <span data-ttu-id="d4205-107">您可以呼叫 [**Image：： GetEncoderParameterListSize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlistsize) 來判斷所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="d4205-107">You can call [**Image::GetEncoderParameterListSize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlistsize) to determine the size of the required buffer.</span></span>

<span data-ttu-id="d4205-108">下列主控台應用程式會取得 JPEG 編碼器的參數清單。</span><span class="sxs-lookup"><span data-stu-id="d4205-108">The following console application obtains the parameter list for the JPEG encoder.</span></span> <span data-ttu-id="d4205-109">Main 函式依賴 helper 函式 GetEncoderClsid，其顯示于抓取 [編碼器的類別識別碼](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)。</span><span class="sxs-lookup"><span data-stu-id="d4205-109">The main function relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


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



<span data-ttu-id="d4205-110">當您執行上述的主控台應用程式時，您會取得如下所示的輸出：</span><span class="sxs-lookup"><span data-stu-id="d4205-110">When you run the preceding console application, you get an output similar to the following:</span></span>


```
The parameter list requires 172 bytes.
There are 4 EncoderParameter objects in the array.
```



<span data-ttu-id="d4205-111">陣列中的每個 [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) 物件都有下列四個公用資料成員：</span><span class="sxs-lookup"><span data-stu-id="d4205-111">Each of the [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) objects in the array has the following four public data members:</span></span>

<span data-ttu-id="d4205-112">下列程式碼是先前範例中所示的主控台應用程式接續。</span><span class="sxs-lookup"><span data-stu-id="d4205-112">The following code is a continuation of the console application shown in the preceding example.</span></span> <span data-ttu-id="d4205-113">程式碼會查看 [**Image：： GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist)所傳回之陣列中的第二個 [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter)物件。</span><span class="sxs-lookup"><span data-stu-id="d4205-113">The code looks at the second [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object in the array returned by [**Image::GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist).</span></span> <span data-ttu-id="d4205-114">程式碼會呼叫 [StringFromGUID2](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2)，這是在 Objbase 中宣告的系統函數，可將 **EncoderParameter** 物件的 **Guid** 成員轉換成字串。</span><span class="sxs-lookup"><span data-stu-id="d4205-114">The code calls [StringFromGUID2](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2), which is a system function declared in Objbase.h, to convert the **Guid** member of the **EncoderParameter** object to a string.</span></span>


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



<span data-ttu-id="d4205-115">前一個程式碼會產生下列輸出：</span><span class="sxs-lookup"><span data-stu-id="d4205-115">The preceding code produces the following output:</span></span>


```
Parameter[1]
   The GUID is {1D5BE4B5-FA4A-452D-9CDD-5DB35105E7EB}.
   The value type is 6.
   The number of values is 1.
```



<span data-ttu-id="d4205-116">您可以查詢 Gdiplusimaging 中的 GUID，並找出這個 [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) 物件的類別是 EncoderQuality。</span><span class="sxs-lookup"><span data-stu-id="d4205-116">You can look up the GUID in Gdiplusimaging.h and find out that the category of this [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object is EncoderQuality.</span></span> <span data-ttu-id="d4205-117">您可以使用此類別 (EncoderQuality) 的參數來設定 JPEG 影像的壓縮等級。</span><span class="sxs-lookup"><span data-stu-id="d4205-117">You can use this category (EncoderQuality) of parameter to set the compression level of a JPEG image.</span></span>

<span data-ttu-id="d4205-118">在 Gdiplusenums 中， [**2csystem.drawing.imaging.encoderparametervaluetype**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) 列舉表示資料類型6是 **ValueLongRange**。</span><span class="sxs-lookup"><span data-stu-id="d4205-118">In Gdiplusenums.h, the [**EncoderParameterValueType**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) enumeration indicates that data type 6 is **ValueLongRange**.</span></span> <span data-ttu-id="d4205-119">Long 範圍是一對 **ULONG** 值。</span><span class="sxs-lookup"><span data-stu-id="d4205-119">A long range is a pair of **ULONG** values.</span></span>

<span data-ttu-id="d4205-120">值的數目是一，因此我們知道 [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter)物件的 **值** 成員是具有一個元素之陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="d4205-120">The number of values is one, so we know that the **Value** member of the [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object is a pointer to an array that has one element.</span></span> <span data-ttu-id="d4205-121">其中一個元素是一對 **ULONG** 值。</span><span class="sxs-lookup"><span data-stu-id="d4205-121">That one element is a pair of **ULONG** values.</span></span>

<span data-ttu-id="d4205-122">下列程式碼是先前的兩個範例中所示的主控台應用程式接續。</span><span class="sxs-lookup"><span data-stu-id="d4205-122">The following code is a continuation of the console application that is shown in the preceding two examples.</span></span> <span data-ttu-id="d4205-123">此程式碼會定義名為 **PLONGRANGE** 的資料類型， (指向較長範圍) 的指標。</span><span class="sxs-lookup"><span data-stu-id="d4205-123">The code defines a data type called **PLONGRANGE** (pointer to a long range).</span></span> <span data-ttu-id="d4205-124">**PLONGRANGE** 型別的變數可用來將可當做品質設定傳遞的最小值和最大值解壓縮到 JPEG 編碼器。</span><span class="sxs-lookup"><span data-stu-id="d4205-124">A variable of type **PLONGRANGE** is used to extract the minimum and maximum values that can be passed as a quality setting to the JPEG encoder.</span></span>


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



<span data-ttu-id="d4205-125">前一個程式碼會產生下列輸出：</span><span class="sxs-lookup"><span data-stu-id="d4205-125">The preceding code produces the following output:</span></span>


```
The minimum possible quality value is 0.
The maximum possible quality value is 100.
```



<span data-ttu-id="d4205-126">在上述範例中， [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) 物件中傳回的值是一對 **ULONG** 值，指出 quality 參數的最小值和最大可能值。</span><span class="sxs-lookup"><span data-stu-id="d4205-126">In the preceding example, the value returned in the [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object is a pair of **ULONG** values that indicate the minimum and maximum possible values for the quality parameter.</span></span> <span data-ttu-id="d4205-127">在某些情況下， **EncoderParameter** 物件中傳回的值是 [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="d4205-127">In some cases, the values returned in an **EncoderParameter** object are members of the [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) enumeration.</span></span> <span data-ttu-id="d4205-128">下列主題討論 **EncoderValue** 列舉和方法，以更詳細地列出可能的參數值：</span><span class="sxs-lookup"><span data-stu-id="d4205-128">The following topics discuss the **EncoderValue** enumeration and methods for listing possible parameter values in more detail:</span></span>

-   [<span data-ttu-id="d4205-129">使用 EncoderValue 列舉</span><span class="sxs-lookup"><span data-stu-id="d4205-129">Using the EncoderValue Enumeration</span></span>](-gdiplus-using-the-encodervalue-enumeration-use.md)
-   [<span data-ttu-id="d4205-130">列出所有編碼器的參數和值</span><span class="sxs-lookup"><span data-stu-id="d4205-130">Listing Parameters and Values for All Encoders</span></span>](-gdiplus-listing-parameters-and-values-for-all-encoders-use.md)

 

 
