---
description: 下列主控台應用程式會列出電腦上安裝的各種編碼器所支援的所有參數。
ms.assetid: c80ad013-0b92-461f-8714-4b6d0cb6de0d
title: 列出所有編碼器的參數和值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fdaf522193f1074a28fe9f5ebb8a7afc2bade0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991102"
---
# <a name="listing-parameters-and-values-for-all-encoders"></a><span data-ttu-id="31e0b-103">列出所有編碼器的參數和值</span><span class="sxs-lookup"><span data-stu-id="31e0b-103">Listing Parameters and Values for All Encoders</span></span>

<span data-ttu-id="31e0b-104">下列主控台應用程式會列出電腦上安裝的各種編碼器所支援的所有參數。</span><span class="sxs-lookup"><span data-stu-id="31e0b-104">The following console application lists all the parameters supported by the various encoders installed on the computer.</span></span> <span data-ttu-id="31e0b-105">Main 函式會呼叫 [**GetImageEncoders**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders) 來探索可用的編碼器。</span><span class="sxs-lookup"><span data-stu-id="31e0b-105">The main function calls [**GetImageEncoders**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders) to discover which encoders are available.</span></span> <span data-ttu-id="31e0b-106">針對每個可用的編碼器，主要函式會呼叫 helper 函數 ShowAllEncoderParameters。</span><span class="sxs-lookup"><span data-stu-id="31e0b-106">For each available encoder, the main function calls the helper function ShowAllEncoderParameters.</span></span>

<span data-ttu-id="31e0b-107">ShowAllEncoderParameters 函式會呼叫 [**Image：： GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist) 方法，以找出指定的編碼器支援哪些參數。</span><span class="sxs-lookup"><span data-stu-id="31e0b-107">The ShowAllEncoderParameters function calls the [**Image::GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist) method to discover which parameters are supported by a given encoder.</span></span> <span data-ttu-id="31e0b-108">針對每個支援的參數，此函式會列出類別、資料類型和值的數目。</span><span class="sxs-lookup"><span data-stu-id="31e0b-108">For each supported parameter, the function lists the category, data type, and number of values.</span></span> <span data-ttu-id="31e0b-109">ShowAllEncoderParameters 函式依賴兩個 helper 函數： EncoderParameterCategoryFromGUID 和 ValueTypeFromULONG。</span><span class="sxs-lookup"><span data-stu-id="31e0b-109">The ShowAllEncoderParameters function relies on two helper functions: EncoderParameterCategoryFromGUID and ValueTypeFromULONG.</span></span>


```
#include <windows.h>
#include <gdiplus.h>
#include <strsafe.h>
using namespace Gdiplus;

// Helper functions
void ShowAllEncoderParameters(ImageCodecInfo*);
HRESULT EncoderParameterCategoryFromGUID(GUID guid, WCHAR* category, UINT maxChars);
HRESULT ValueTypeFromULONG(ULONG index, WCHAR* strValueType, UINT maxChars);

INT main()
{
   // Initialize GDI+
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   UINT  num;        // Number of image encoders
   UINT  size;       // Size of the image encoder array in bytes

   ImageCodecInfo* pImageCodecInfo;

   // How many encoders are there?
   // How big (in bytes) is the array of all ImageCodecInfo objects?
   GetImageEncodersSize(&num, &size);

   // Create a buffer large enough to hold the array of ImageCodecInfo
   // objects that will be returned by GetImageEncoders.
   pImageCodecInfo = (ImageCodecInfo*)(malloc(size));

   // GetImageEncoders creates an array of ImageCodecInfo objects
   // and copies that array into a previously allocated buffer. 
   // The third argument, imageCodecInfos, is a pointer to that buffer. 
   GetImageEncoders(num, size, pImageCodecInfo);
    
   // For each ImageCodecInfo object in the array, show all parameters.
   for(UINT j = 0; j < num; ++j)
   { 
      ShowAllEncoderParameters(&(pImageCodecInfo[j]));
   }

   GdiplusShutdown(gdiplusToken);
   return 0;
}


/////////////////////////////////////////////////
// Helper functions

VOID ShowAllEncoderParameters(ImageCodecInfo* pImageCodecInfo)
{
   CONST MAX_CATEGORY_LENGTH = 50;
   CONST MAX_VALUE_TYPE_LENGTH = 50;
   WCHAR strParameterCategory[MAX_CATEGORY_LENGTH] = L"";
   WCHAR strValueType[MAX_VALUE_TYPE_LENGTH] = L"";

   wprintf(L"\n\n%s\n", pImageCodecInfo->MimeType);

   // Create a Bitmap (inherited from Image) object so that we can call
   // GetParameterListSize and GetParameterList.
   Bitmap bitmap(1, 1);

   // How big (in bytes) is the encoder's parameter list?
   UINT listSize = 0; 
   listSize = bitmap.GetEncoderParameterListSize(&pImageCodecInfo->Clsid);
   printf("  The parameter list requires %d bytes.\n", listSize);

   if(listSize == 0)
      return;

   // Allocate a buffer large enough to hold the parameter list.
   EncoderParameters* pEncoderParameters = NULL;
   pEncoderParameters = (EncoderParameters*)malloc(listSize);

   if(pEncoderParameters == NULL)
      return;

   // Get the parameter list for the encoder.
   bitmap.GetEncoderParameterList(
      &pImageCodecInfo->Clsid, listSize, pEncoderParameters);

   // pEncoderParameters points to an EncoderParameters object, which
   // has a Count member and an array of EncoderParameter objects.
   // How many EncoderParameter objects are in the array?
   printf("  There are %d EncoderParameter objects in the array.\n", 
      pEncoderParameters->Count);

   // For each EncoderParameter object in the array, list the
   // parameter category, data type, and number of values.
   for(UINT k = 0; k < pEncoderParameters->Count; ++k)
   {
      EncoderParameterCategoryFromGUID(
         pEncoderParameters->Parameter[k].Guid, strParameterCategory, MAX_CATEGORY_LENGTH);

      ValueTypeFromULONG(
         pEncoderParameters->Parameter[k].Type, strValueType, MAX_VALUE_TYPE_LENGTH);

      printf("    Parameter[%d]\n", k);
      wprintf(L"      The category is %s.\n", strParameterCategory);
      wprintf(L"      The data type is %s.\n", strValueType);

      printf("      The number of values is %d.\n",
      pEncoderParameters->Parameter[k].NumberOfValues); 
   } // for

   free(pEncoderParameters);
} // ShowAllEncoderParameters


HRESULT EncoderParameterCategoryFromGUID(GUID guid, WCHAR* category, UINT maxChars)
{
   HRESULT hr = E_FAIL;

   if(guid == EncoderCompression)
      hr = StringCchCopyW(category, maxChars, L"Compression");
   else if(guid == EncoderColorDepth)
      hr = StringCchCopyW(category, maxChars, L"ColorDepth");
   else if(guid == EncoderScanMethod)
      hr = StringCchCopyW(category, maxChars, L"ScanMethod");
   else if(guid == EncoderVersion)
      hr = StringCchCopyW(category, maxChars, L"Version");
   else if(guid == EncoderRenderMethod)
      hr = StringCchCopyW(category, maxChars, L"RenderMethod");
   else if(guid == EncoderQuality)
      hr = StringCchCopyW(category, maxChars, L"Quality");
   else if(guid == EncoderTransformation)
      hr = StringCchCopyW(category, maxChars, L"Transformation");
   else if(guid == EncoderLuminanceTable)
      hr = StringCchCopyW(category, maxChars, L"LuminanceTable");
   else if(guid == EncoderChrominanceTable)
      hr = StringCchCopyW(category, maxChars, L"ChrominanceTable");
   else if(guid == EncoderSaveFlag)
      hr = StringCchCopyW(category, maxChars, L"SaveFlag");
   else
      hr = StringCchCopyW(category, maxChars, L"Unknown category");

   return hr;
} // EncoderParameterCategoryFromGUID


HRESULT ValueTypeFromULONG(ULONG index, WCHAR* strValueType, UINT maxChars)
{
   HRESULT hr = E_FAIL;

   WCHAR* valueTypes[] = {
      L"Nothing",                  // 0
      L"ValueTypeByte",            // 1
      L"ValueTypeASCII",           // 2
      L"ValueTypeShort",           // 3
      L"ValueTypeLong",            // 4
      L"ValueTypeRational",        // 5
      L"ValueTypeLongRange",       // 6
      L"ValueTypeUndefined",       // 7
      L"ValueTypeRationalRange"};  // 8

   hr = StringCchCopyW(strValueType, maxChars, valueTypes[index]);
   return hr;

} // ValueTypeFromULONG
```



<span data-ttu-id="31e0b-110">當您執行上述的主控台應用程式時，您會取得如下所示的輸出：</span><span class="sxs-lookup"><span data-stu-id="31e0b-110">When you run the preceding console application, you get an output similar to the following:</span></span>


```
image/bmp
  The parameter list requires 0 bytes.

image/jpeg
  The parameter list requires 172 bytes.
  There are 4 EncoderParameter objects in the array.
    Parameter[0]
      The category is Transformation.
      The data type is Long.
      The number of values is 5.
    Parameter[1]
      The category is Quality.
      The data type is LongRange.
      The number of values is 1.
    Parameter[2]
      The category is LuminanceTable.
      The data type is Short.
      The number of values is 0.
    Parameter[3]
      The category is ChrominanceTable.
      The data type is Short.
      The number of values is 0.

image/gif
  The parameter list requires 0 bytes.

image/tiff
  The parameter list requires 160 bytes.
  There are 3 EncoderParameter objects in the array.
    Parameter[0]
      The category is Compression.
      The data type is Long.
      The number of values is 5.
    Parameter[1]
      The category is ColorDepth.
      The data type is Long.
      The number of values is 5.
    Parameter[2]
      The category is SaveFlag.
      The data type is Long.
      The number of values is 1.

image/png
  The parameter list requires 0 bytes.
```



<span data-ttu-id="31e0b-111">您可以藉由檢查上述的程式輸出來繪製下列結論：</span><span class="sxs-lookup"><span data-stu-id="31e0b-111">You can draw the following conclusions by examining the preceding program output:</span></span>

-   <span data-ttu-id="31e0b-112">JPEG 編碼器支援轉換、品質、LuminanceTable 和 ChrominanceTable 參數分類。</span><span class="sxs-lookup"><span data-stu-id="31e0b-112">The JPEG encoder supports the Transformation, Quality, LuminanceTable, and ChrominanceTable parameter categories.</span></span>
-   <span data-ttu-id="31e0b-113">TIFF 編碼器支援壓縮、ColorDepth 和 SaveFlag 參數分類。</span><span class="sxs-lookup"><span data-stu-id="31e0b-113">The TIFF encoder supports the Compression, ColorDepth, and SaveFlag parameter categories.</span></span>

<span data-ttu-id="31e0b-114">您也可以查看每個參數類別目錄的可接受值數目。</span><span class="sxs-lookup"><span data-stu-id="31e0b-114">You can also see the number of acceptable values for each parameter category.</span></span> <span data-ttu-id="31e0b-115">例如，您可以看到 ColorDepth 參數類別 (TIFF 編解碼器) 具有類型 **ULONG** 的五個值。</span><span class="sxs-lookup"><span data-stu-id="31e0b-115">For example, you can see that the ColorDepth parameter category (TIFF codec) has five values of type **ULONG**.</span></span> <span data-ttu-id="31e0b-116">下列程式碼會列出這五個值。</span><span class="sxs-lookup"><span data-stu-id="31e0b-116">The following code lists those five values.</span></span> <span data-ttu-id="31e0b-117">假設 **pEncoderParameters** 是代表 TIFF 編碼器之 [**system.drawing.imaging.encoderparameters>**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="31e0b-117">Assume that **pEncoderParameters** is a pointer to an [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) object that represents the TIFF encoder.</span></span>


```
ULONG* pUlong = (ULONG*)(pEncoderParameters->Parameter[1].Value);
ULONG numVals = pEncoderParameters->Parameter[1].NumberOfValues;
printf("\nThe allowable values for ColorDepth are\n");

for(ULONG k = 0; k < numVals; ++k)
{
   printf("  %u\n", pUlong[k]);
}
            
```



<span data-ttu-id="31e0b-118">前一個程式碼會產生下列輸出：</span><span class="sxs-lookup"><span data-stu-id="31e0b-118">The preceding code produces the following output:</span></span>


```
The allowable values for ColorDepth are
  1
  4
  8
  24
  32
            
```



> [!Note]  
> <span data-ttu-id="31e0b-119">在某些情況下， [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) 物件中的值是 [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) 列舉之元素的數值。</span><span class="sxs-lookup"><span data-stu-id="31e0b-119">In some cases, the values in an [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object are the numeric values of elements of the [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) enumeration.</span></span> <span data-ttu-id="31e0b-120">不過，上述清單中的數位與 **EncoderValue** 列舉沒有關聯。</span><span class="sxs-lookup"><span data-stu-id="31e0b-120">However, the numbers in the preceding list do not relate to the **EncoderValue** enumeration.</span></span> <span data-ttu-id="31e0b-121">數位表示每圖元1位、每圖元2位等等。</span><span class="sxs-lookup"><span data-stu-id="31e0b-121">The numbers mean 1 bit per pixel, 2 bits per pixel, and so on.</span></span>

 

<span data-ttu-id="31e0b-122">如果您撰寫類似上述範例的程式碼來調查其他參數類別目錄的允許值，您將會得到類似下面的結果。</span><span class="sxs-lookup"><span data-stu-id="31e0b-122">If you write code similar to the preceding example to investigate the allowable values for the other parameter categories, you will obtain a result similar to the following.</span></span>



| <span data-ttu-id="31e0b-123">JPEG 編碼器參數</span><span class="sxs-lookup"><span data-stu-id="31e0b-123">JPEG encoder parameter</span></span> | <span data-ttu-id="31e0b-124">允許的值</span><span class="sxs-lookup"><span data-stu-id="31e0b-124">Allowable values</span></span>                                                                                                                                                                                                 |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31e0b-125">轉換</span><span class="sxs-lookup"><span data-stu-id="31e0b-125">Transformation</span></span>         | <span data-ttu-id="31e0b-126">EncoderValueTransformRotate90 EncoderValueTransformRotate180</span><span class="sxs-lookup"><span data-stu-id="31e0b-126">EncoderValueTransformRotate90 EncoderValueTransformRotate180</span></span><br/>  <span data-ttu-id="31e0b-127">EncoderValueTransformRotate270</span><span class="sxs-lookup"><span data-stu-id="31e0b-127">EncoderValueTransformRotate270</span></span><br/>  <span data-ttu-id="31e0b-128">EncoderValueTransformFlipHorizontal</span><span class="sxs-lookup"><span data-stu-id="31e0b-128">EncoderValueTransformFlipHorizontal</span></span><br/>  <span data-ttu-id="31e0b-129">EncoderValueTransformFlipVertical</span><span class="sxs-lookup"><span data-stu-id="31e0b-129">EncoderValueTransformFlipVertical</span></span><br/> |
| <span data-ttu-id="31e0b-130">品質</span><span class="sxs-lookup"><span data-stu-id="31e0b-130">Quality</span></span>                | <span data-ttu-id="31e0b-131">0到100</span><span class="sxs-lookup"><span data-stu-id="31e0b-131">0 through 100</span></span>                                                                                                                                                                                                    |



 



| <span data-ttu-id="31e0b-132">TIFF 編碼器參數</span><span class="sxs-lookup"><span data-stu-id="31e0b-132">TIFF encoder parameter</span></span> | <span data-ttu-id="31e0b-133">允許的值</span><span class="sxs-lookup"><span data-stu-id="31e0b-133">Allowable values</span></span>                                                                                                                                                                             |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31e0b-134">壓縮</span><span class="sxs-lookup"><span data-stu-id="31e0b-134">Compression</span></span>            | <span data-ttu-id="31e0b-135">EncoderValueCompressionLZW EncoderValueCompressionCCITT3</span><span class="sxs-lookup"><span data-stu-id="31e0b-135">EncoderValueCompressionLZW EncoderValueCompressionCCITT3</span></span><br/>  <span data-ttu-id="31e0b-136">EncoderValueCompressionCCITT4</span><span class="sxs-lookup"><span data-stu-id="31e0b-136">EncoderValueCompressionCCITT4</span></span><br/>  <span data-ttu-id="31e0b-137">EncoderValueCompressionRle</span><span class="sxs-lookup"><span data-stu-id="31e0b-137">EncoderValueCompressionRle</span></span><br/>  <span data-ttu-id="31e0b-138">EncoderValueCompressionNone</span><span class="sxs-lookup"><span data-stu-id="31e0b-138">EncoderValueCompressionNone</span></span><br/> |
| <span data-ttu-id="31e0b-139">ColorDepth</span><span class="sxs-lookup"><span data-stu-id="31e0b-139">ColorDepth</span></span>             | <span data-ttu-id="31e0b-140">1、4、8、24、32</span><span class="sxs-lookup"><span data-stu-id="31e0b-140">1, 4, 8, 24, 32</span></span>                                                                                                                                                                              |
| <span data-ttu-id="31e0b-141">SaveFlag</span><span class="sxs-lookup"><span data-stu-id="31e0b-141">SaveFlag</span></span>               | <span data-ttu-id="31e0b-142">EncoderValueMultiFrame</span><span class="sxs-lookup"><span data-stu-id="31e0b-142">EncoderValueMultiFrame</span></span>                                                                                                                                                                       |



 

> [!Note]  
> <span data-ttu-id="31e0b-143">如果 JPEG 影像的寬度和高度為16的倍數，您可以套用 EncoderTransformation 參數類別所允許的任何轉換 (例如，90度旋轉) ，而不會遺失資訊。</span><span class="sxs-lookup"><span data-stu-id="31e0b-143">If the width and height of a JPEG image are multiples of 16, you can apply any of the transformations allowed by the EncoderTransformation parameter category (for example, 90-degree rotation) without loss of information.</span></span>

 

 

 
