---
description: 有些影像檔案包含可供您讀取的中繼資料，以判斷影像的功能。
ms.assetid: 2febea35-3fea-4a2d-baaf-7a4f935fc81f
title: 讀取和寫入中繼資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e4ea0a8f389f31870b31a0b15480815bdd7cf1f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118293"
---
# <a name="reading-and-writing-metadata"></a><span data-ttu-id="66394-103">讀取和寫入中繼資料</span><span class="sxs-lookup"><span data-stu-id="66394-103">Reading and Writing Metadata</span></span>

<span data-ttu-id="66394-104">有些影像檔案包含可供您讀取的中繼資料，以判斷影像的功能。</span><span class="sxs-lookup"><span data-stu-id="66394-104">Some image files contain metadata that you can read to determine features of the image.</span></span> <span data-ttu-id="66394-105">例如，數位相片可能包含您可以讀取的中繼資料，以判斷用來捕捉影像的相機製作和型號。</span><span class="sxs-lookup"><span data-stu-id="66394-105">For example, a digital photograph might contain metadata that you can read to determine the make and model of the camera used to capture the image.</span></span> <span data-ttu-id="66394-106">您可以使用 Windows GDI + 來讀取現有的中繼資料，也可以將新的中繼資料寫入影像檔案。</span><span class="sxs-lookup"><span data-stu-id="66394-106">With Windows GDI+, you can read existing metadata, and you can also write new metadata to image files.</span></span>

<span data-ttu-id="66394-107">GDI + 提供統一的方式，可從影像檔案以各種格式儲存和抓取中繼資料。</span><span class="sxs-lookup"><span data-stu-id="66394-107">GDI+ provides a uniform way of storing and retrieving metadata from image files in various formats.</span></span> <span data-ttu-id="66394-108">在 GDI + 中，中繼資料的部分稱為 *屬性專案*。</span><span class="sxs-lookup"><span data-stu-id="66394-108">In GDI+, a piece of metadata is called a *property item*.</span></span> <span data-ttu-id="66394-109">您可以藉由呼叫 [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image)類別的 **SetPropertyItem** 和 **GetPropertyItem** 方法來儲存和取出中繼資料，而不需要擔心特定檔案格式儲存該中繼資料的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="66394-109">You can store and retrieve metadata by calling the **SetPropertyItem** and **GetPropertyItem** methods of the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class, and you don't have to be concerned about the details of how a particular file format stores that metadata.</span></span>

<span data-ttu-id="66394-110">GDI + 目前支援 TIFF、JPEG、Exif 和 PNG 檔案格式的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="66394-110">GDI+ currently supports metadata for the TIFF, JPEG, Exif, and PNG file formats.</span></span> <span data-ttu-id="66394-111">此 Exif 格式可指定如何儲存數位攝影機所捕捉的影像，並以 TIFF 和 JPEG 格式為基礎。</span><span class="sxs-lookup"><span data-stu-id="66394-111">The Exif format, which specifies how to store images captured by digital still cameras, is built on top of the TIFF and JPEG formats.</span></span> <span data-ttu-id="66394-112">Exif 針對未壓縮的圖元資料使用 TIFF 格式，並針對壓縮的圖元資料使用 JPEG 格式。</span><span class="sxs-lookup"><span data-stu-id="66394-112">Exif uses the TIFF format for uncompressed pixel data and the JPEG format for compressed pixel data.</span></span>

<span data-ttu-id="66394-113">GDI + 會定義一組用來識別屬性專案的屬性標記。</span><span class="sxs-lookup"><span data-stu-id="66394-113">GDI+ defines a set of property tags that identify property items.</span></span> <span data-ttu-id="66394-114">某些標記為一般用途;亦即，上一段所述的所有檔案格式都支援它們。</span><span class="sxs-lookup"><span data-stu-id="66394-114">Certain tags are general-purpose; that is, they are supported by all of the file formats mentioned in the preceding paragraph.</span></span> <span data-ttu-id="66394-115">其他標記是特殊用途，只適用于特定格式。</span><span class="sxs-lookup"><span data-stu-id="66394-115">Other tags are special-purpose and apply only to certain formats.</span></span> <span data-ttu-id="66394-116">如果您嘗試將屬性專案儲存至不支援該屬性專案的檔案，GDI + 會忽略要求。</span><span class="sxs-lookup"><span data-stu-id="66394-116">If you try to save a property item to a file that does not support that property item, GDI+ ignores the request.</span></span> <span data-ttu-id="66394-117">更具體來說， [**Image：： SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) 方法會傳回 PropertyNotSupported。</span><span class="sxs-lookup"><span data-stu-id="66394-117">More specifically, the [**Image::SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) method returns PropertyNotSupported.</span></span>

<span data-ttu-id="66394-118">您可以藉由呼叫 [**image：： GetPropertyIdList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyidlist)，判斷儲存在影像檔案中的屬性專案。</span><span class="sxs-lookup"><span data-stu-id="66394-118">You can determine the property items that are stored in an image file by calling [**Image::GetPropertyIdList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyidlist).</span></span> <span data-ttu-id="66394-119">如果您嘗試抓取不在檔案中的屬性專案，GDI + 會忽略要求。</span><span class="sxs-lookup"><span data-stu-id="66394-119">If you try to retrieve a property item that is not in the file, GDI+ ignores the request.</span></span> <span data-ttu-id="66394-120">更具體來說， [**Image：： GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) 方法會傳回 PropertyNotFound。</span><span class="sxs-lookup"><span data-stu-id="66394-120">More specifically, the [**Image::GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) method returns PropertyNotFound.</span></span>

## <a name="reading-metadata-from-a-file"></a><span data-ttu-id="66394-121">從檔案讀取中繼資料</span><span class="sxs-lookup"><span data-stu-id="66394-121">Reading Metadata from a File</span></span>

<span data-ttu-id="66394-122">下列主控台應用程式會呼叫 [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image)物件的 **GetPropertySize** 方法，以判斷 FakePhoto.jpg 檔案中有多少部分的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="66394-122">The following console application calls the **GetPropertySize** method of an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object to determine how many pieces of metadata are in the file FakePhoto.jpg.</span></span>


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



<span data-ttu-id="66394-123">上述程式碼和特定檔案 FakePhoto.jpg，會產生下列輸出：</span><span class="sxs-lookup"><span data-stu-id="66394-123">The preceding code, along with a particular file, FakePhoto.jpg, produced the following output:</span></span>


```
There are 7 pieces of metadata in the file.
The total size of the metadata is 436 bytes.
```



<span data-ttu-id="66394-124">GDI + 會將個別的中繼資料儲存在 [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) 物件中。</span><span class="sxs-lookup"><span data-stu-id="66394-124">GDI+ stores an individual piece of metadata in a [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) object.</span></span> <span data-ttu-id="66394-125">您可以呼叫 [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image)類別的 **GetAllPropertyItems** 方法，從檔案取出所有中繼資料。</span><span class="sxs-lookup"><span data-stu-id="66394-125">You can call the **GetAllPropertyItems** method of the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class to retrieve all the metadata from a file.</span></span> <span data-ttu-id="66394-126">**GetAllPropertyItems** 方法會傳回 **PropertyItem** 物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="66394-126">The **GetAllPropertyItems** method returns an array of **PropertyItem** objects.</span></span> <span data-ttu-id="66394-127">在呼叫 **GetAllPropertyItems** 之前，您必須配置夠大的緩衝區來接收該陣列。</span><span class="sxs-lookup"><span data-stu-id="66394-127">Before you call **GetAllPropertyItems**, you must allocate a buffer large enough to receive that array.</span></span> <span data-ttu-id="66394-128">您可以呼叫 **Image** 類別的 **GetPropertySize** 方法，以取得所需緩衝區)  (位元組大小。</span><span class="sxs-lookup"><span data-stu-id="66394-128">You can call the **GetPropertySize** method of the **Image** class to get the size (in bytes) of the required buffer.</span></span>

<span data-ttu-id="66394-129">[**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem)物件具有下列四個公用成員：</span><span class="sxs-lookup"><span data-stu-id="66394-129">A [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) object has the following four public members:</span></span>



|            | <span data-ttu-id="66394-130">描述</span><span class="sxs-lookup"><span data-stu-id="66394-130">Description</span></span>                                                                                                                                                                                                                                                                                                       |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66394-131">**id**</span><span class="sxs-lookup"><span data-stu-id="66394-131">**id**</span></span>     | <span data-ttu-id="66394-132">識別中繼資料專案的標記。</span><span class="sxs-lookup"><span data-stu-id="66394-132">A tag that identifies the metadata item.</span></span> <span data-ttu-id="66394-133">可以指派給 **識別碼** 的值 (PropertyTagImageTitle、PropertyTagEquipMake、PropertyTagExifExposureTime 和 like) 都定義于 Gdiplusimaging 中。</span><span class="sxs-lookup"><span data-stu-id="66394-133">The values that can be assigned to **id** (PropertyTagImageTitle, PropertyTagEquipMake, PropertyTagExifExposureTime, and the like) are defined in Gdiplusimaging.h.</span></span>                                                                                           |
| <span data-ttu-id="66394-134">**length** (長度)</span><span class="sxs-lookup"><span data-stu-id="66394-134">**length**</span></span> | <span data-ttu-id="66394-135">**值** 資料成員所指向之值陣列的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="66394-135">The length, in bytes, of the array of values pointed to by the **value** data member.</span></span> <span data-ttu-id="66394-136">請注意，如果 **類型** 資料成員設為 PropertyTagTypeASCII，則長度資料成員是以 null 結束的字元字串 **長度** ，包括 null 結束字元。</span><span class="sxs-lookup"><span data-stu-id="66394-136">Note that if the **type** data member is set to PropertyTagTypeASCII, then the length data member is the **length** of a null-terminated character string, including the NULL terminator.</span></span>                        |
| <span data-ttu-id="66394-137">**type**</span><span class="sxs-lookup"><span data-stu-id="66394-137">**type**</span></span>   | <span data-ttu-id="66394-138">值資料成員所指向陣列中值的資料類型。</span><span class="sxs-lookup"><span data-stu-id="66394-138">The data type of the values in the array pointed to by the value data member.</span></span> <span data-ttu-id="66394-139">常數 (PropertyTagTypeByte、PropertyTagTypeASCII 和表示各種資料類型的 like) ，都是在 [**影像屬性標記類型常數**](-gdiplus-constant-image-property-tag-type-constants.md)中描述。</span><span class="sxs-lookup"><span data-stu-id="66394-139">Constants (PropertyTagTypeByte, PropertyTagTypeASCII, and the like) that represent various data types are described in [**Image Property Tag Type Constants**](-gdiplus-constant-image-property-tag-type-constants.md).</span></span> |
| <span data-ttu-id="66394-140">**value**</span><span class="sxs-lookup"><span data-stu-id="66394-140">**value**</span></span>  | <span data-ttu-id="66394-141">值陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="66394-141">A pointer to an array of values.</span></span>                                                                                                                                                                                                                                                                       |



 

<span data-ttu-id="66394-142">下列主控台應用程式會讀取並顯示檔案 FakePhoto.jpg 中的七個中繼資料片段。</span><span class="sxs-lookup"><span data-stu-id="66394-142">The following console application reads and displays the seven pieces of metadata in the file FakePhoto.jpg.</span></span> <span data-ttu-id="66394-143">Main 函式依賴 helper 函式 PropertyTypeFromWORD，它會在 main 函式之後顯示。</span><span class="sxs-lookup"><span data-stu-id="66394-143">The main function relies on the helper function PropertyTypeFromWORD, which is shown following the main function.</span></span>


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



<span data-ttu-id="66394-144">上述的主控台應用程式會產生下列輸出：</span><span class="sxs-lookup"><span data-stu-id="66394-144">The preceding console application produces the following output:</span></span>


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



<span data-ttu-id="66394-145">上述輸出會顯示每個屬性專案的十六進位 ID 號碼。</span><span class="sxs-lookup"><span data-stu-id="66394-145">The preceding output shows a hexadecimal ID number for each property item.</span></span> <span data-ttu-id="66394-146">您可以在 [影像屬性標記常數](-gdiplus-constant-image-property-tag-constants.md) 中查閱這些識別碼，並找出它們是否代表下列屬性標記。</span><span class="sxs-lookup"><span data-stu-id="66394-146">You can look up those ID numbers in [Image Property Tag Constants](-gdiplus-constant-image-property-tag-constants.md) and find out that they represent the following property tags.</span></span>



| <span data-ttu-id="66394-147">十六進位值</span><span class="sxs-lookup"><span data-stu-id="66394-147">Hexadecimal value</span></span>                                                                                                       | <span data-ttu-id="66394-148">屬性標記</span><span class="sxs-lookup"><span data-stu-id="66394-148">Property tag</span></span>                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66394-149">0x0320 0x010f</span><span class="sxs-lookup"><span data-stu-id="66394-149">0x0320 0x010f</span></span><br/>  <span data-ttu-id="66394-150">0x0110</span><span class="sxs-lookup"><span data-stu-id="66394-150">0x0110</span></span><br/>  <span data-ttu-id="66394-151">0x9003</span><span class="sxs-lookup"><span data-stu-id="66394-151">0x9003</span></span><br/>  <span data-ttu-id="66394-152">0x829a</span><span class="sxs-lookup"><span data-stu-id="66394-152">0x829a</span></span><br/>  <span data-ttu-id="66394-153">0x5090</span><span class="sxs-lookup"><span data-stu-id="66394-153">0x5090</span></span><br/>  <span data-ttu-id="66394-154">0x5091</span><span class="sxs-lookup"><span data-stu-id="66394-154">0x5091</span></span><br/> | <span data-ttu-id="66394-155">PropertyTagImageTitle PropertyTagEquipMake</span><span class="sxs-lookup"><span data-stu-id="66394-155">PropertyTagImageTitle PropertyTagEquipMake</span></span><br/>  <span data-ttu-id="66394-156">PropertyTagEquipModel</span><span class="sxs-lookup"><span data-stu-id="66394-156">PropertyTagEquipModel</span></span><br/>  <span data-ttu-id="66394-157">PropertyTagExifDTOriginal</span><span class="sxs-lookup"><span data-stu-id="66394-157">PropertyTagExifDTOriginal</span></span><br/>  <span data-ttu-id="66394-158">PropertyTagExifExposureTime</span><span class="sxs-lookup"><span data-stu-id="66394-158">PropertyTagExifExposureTime</span></span><br/>  <span data-ttu-id="66394-159">PropertyTagLuminanceTable</span><span class="sxs-lookup"><span data-stu-id="66394-159">PropertyTagLuminanceTable</span></span><br/>  <span data-ttu-id="66394-160">PropertyTagChrominanceTable</span><span class="sxs-lookup"><span data-stu-id="66394-160">PropertyTagChrominanceTable</span></span><br/> |



 

<span data-ttu-id="66394-161">清單中的第二個 (index 1) 屬性專案具有 **id** PropertyTagEquipMake 和 **類型** PropertyTagTypeASCII。</span><span class="sxs-lookup"><span data-stu-id="66394-161">The second (index 1) property item in the list has **id** PropertyTagEquipMake and **type** PropertyTagTypeASCII.</span></span> <span data-ttu-id="66394-162">下列範例是前一個主控台應用程式的接續，會顯示該屬性專案的值：</span><span class="sxs-lookup"><span data-stu-id="66394-162">The following example, which is a continuation of the previous console application, displays the value of that property item:</span></span>


```
printf("The equipment make is %s.\n", pPropBuffer[1].value);
```



<span data-ttu-id="66394-163">上述程式程式碼會產生下列輸出：</span><span class="sxs-lookup"><span data-stu-id="66394-163">The preceding line of code produces the following output:</span></span>


```
The equipment make is Northwind Traders.
```



<span data-ttu-id="66394-164">清單中的第五個 (index 4) 屬性專案具有 **id** PropertyTagExifExposureTime 和 **類型** PropertyTagTypeRational。</span><span class="sxs-lookup"><span data-stu-id="66394-164">The fifth (index 4) property item in the list has **id** PropertyTagExifExposureTime and **type** PropertyTagTypeRational.</span></span> <span data-ttu-id="66394-165">該資料類型 (PropertyTagTypeRational) 是一對 **LONG** s。</span><span class="sxs-lookup"><span data-stu-id="66394-165">That data type (PropertyTagTypeRational) is a pair of **LONG** s.</span></span> <span data-ttu-id="66394-166">下列範例是前一個主控台應用程式的接續，會將這兩個 **長** 值顯示為分數。</span><span class="sxs-lookup"><span data-stu-id="66394-166">The following example, which is a continuation of the previous console application, displays those two **LONG** values as a fraction.</span></span> <span data-ttu-id="66394-167">該分數1/125 是以秒為單位的曝光時間。</span><span class="sxs-lookup"><span data-stu-id="66394-167">That fraction, 1/125, is the exposure time measured in seconds.</span></span>


```
long* ptrLong = (long*)(pPropBuffer[4].value);
printf("The exposure time is %d/%d.\n", ptrLong[0], ptrLong[1]);
```



<span data-ttu-id="66394-168">前一個程式碼會產生下列輸出：</span><span class="sxs-lookup"><span data-stu-id="66394-168">The preceding code produces the following output:</span></span>


```
The exposure time is 1/125.
```



## <a name="writing-metadata-to-a-file"></a><span data-ttu-id="66394-169">將中繼資料寫入檔案</span><span class="sxs-lookup"><span data-stu-id="66394-169">Writing Metadata to a File</span></span>

<span data-ttu-id="66394-170">若要將中繼資料的專案寫入 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image)物件，請將 [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem)物件初始化，然後將該 **PropertyItem** 物件的位址傳遞至 **image** 物件的 **SetPropertyItem** 方法。</span><span class="sxs-lookup"><span data-stu-id="66394-170">To write an item of metadata to an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object, initialize a [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) object and then pass the address of that **PropertyItem** object to the **SetPropertyItem** method of the **Image** object.</span></span>

<span data-ttu-id="66394-171">下列主控台應用程式會將 (影像標題) 的一個專案寫入 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 物件，然後將映射儲存在磁片檔案 FakePhoto2.jpg 中。</span><span class="sxs-lookup"><span data-stu-id="66394-171">The following console application writes one item (the image title) of metadata to an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and then saves the image in the disk file FakePhoto2.jpg.</span></span> <span data-ttu-id="66394-172">Main 函式依賴 helper 函式 GetEncoderClsid，它會在 [取得編碼器的類別識別碼](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)的主題中顯示。</span><span class="sxs-lookup"><span data-stu-id="66394-172">The main function relies on the helper function GetEncoderClsid, which is shown in the topic [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


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



 

 
