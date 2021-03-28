---
description: 使用特定檔案格式時，您可以將多個映射 (框架) 儲存至單一檔案。
ms.assetid: 9b61e01d-0a98-4ac3-865e-7570ed0c3cde
title: 建立和儲存多框架影像
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 532a8fc8f8fc7e8742651f3d3853e001d493609b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115240"
---
# <a name="creating-and-saving-a-multiple-frame-image"></a><span data-ttu-id="6868e-103">建立和儲存多框架影像</span><span class="sxs-lookup"><span data-stu-id="6868e-103">Creating and Saving a Multiple-Frame Image</span></span>

<span data-ttu-id="6868e-104">使用特定檔案格式時，您可以將多個映射 (框架) 儲存至單一檔案。</span><span class="sxs-lookup"><span data-stu-id="6868e-104">With certain file formats, you can save multiple images (frames) to a single file.</span></span> <span data-ttu-id="6868e-105">例如，您可以將數個頁面儲存至單一 TIFF 檔案。</span><span class="sxs-lookup"><span data-stu-id="6868e-105">For example, you can save several pages to a single TIFF file.</span></span> <span data-ttu-id="6868e-106">若要儲存第一個頁面，請呼叫 [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image)類別的 [save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters))方法。</span><span class="sxs-lookup"><span data-stu-id="6868e-106">To save the first page, call the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method of the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class.</span></span> <span data-ttu-id="6868e-107">若要儲存後續頁面，請呼叫 **Image** 類別的 [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))方法。</span><span class="sxs-lookup"><span data-stu-id="6868e-107">To save subsequent pages, call the [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) method of the **Image** class.</span></span>

> [!Note]  
> <span data-ttu-id="6868e-108">您無法使用 [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) 將畫面格新增至動畫 gif 檔案。</span><span class="sxs-lookup"><span data-stu-id="6868e-108">You cannot use [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) to add frames to an animated gif file.</span></span>

 

<span data-ttu-id="6868e-109">下列主控台應用程式會建立具有四個頁面的 TIFF 檔案。</span><span class="sxs-lookup"><span data-stu-id="6868e-109">The following console application creates a TIFF file with four pages.</span></span> <span data-ttu-id="6868e-110">成為 TIFF 檔案頁面的影像來自四個磁片檔案： Shapes.bmp、Cereal.gif、Iron.jpg 和 House.png。</span><span class="sxs-lookup"><span data-stu-id="6868e-110">The images that become the pages of the TIFF file come from four disk files: Shapes.bmp, Cereal.gif, Iron.jpg, and House.png.</span></span> <span data-ttu-id="6868e-111">程式碼會先建立四個 [**影像**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) 物件： **多重**、 **page2**、 **page3** 和 **page4**。</span><span class="sxs-lookup"><span data-stu-id="6868e-111">The code first constructs four [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) objects: **multi**, **page2**, **page3**, and **page4**.</span></span> <span data-ttu-id="6868e-112">一開始， **多重** 只包含 Shapes.bmp 中的影像，但最後會包含四個映射。</span><span class="sxs-lookup"><span data-stu-id="6868e-112">At first, **multi** contains only the image from Shapes.bmp, but eventually it contains all four images.</span></span> <span data-ttu-id="6868e-113">當個別頁面新增至 **多** 個 **映射** 物件時，也會將這些頁面新增至磁片檔案 Multiframe .tif。  </span><span class="sxs-lookup"><span data-stu-id="6868e-113">As the individual pages are added to the **multi**  **Image** object, they are also added to the disk file Multiframe.tif.</span></span>

<span data-ttu-id="6868e-114">請注意，程式碼會呼叫 [save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) (not [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))) 來儲存第一個頁面。</span><span class="sxs-lookup"><span data-stu-id="6868e-114">Note that the code calls [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) (not [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))) to save the first page.</span></span> <span data-ttu-id="6868e-115">傳遞至 Save 方法的第一個引數是最後將包含數個框架的磁片檔案名。</span><span class="sxs-lookup"><span data-stu-id="6868e-115">The first argument passed to the Save method is the name of the disk file that will eventually contain several frames.</span></span> <span data-ttu-id="6868e-116">傳遞至 Save 方法的第二個引數會指定將用來將 **多** 個 [**影像**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image)物件中的資料轉換成格式的編碼器 (在此案例中，磁片檔案需要 TIFF) 。  </span><span class="sxs-lookup"><span data-stu-id="6868e-116">The second argument passed to the Save method specifies the encoder that will be used to convert the data in the **multi**  [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object to the format (in this case TIFF) required by the disk file.</span></span> <span data-ttu-id="6868e-117">所有後續呼叫 **多重**  **映射** 物件的 SaveAdd 方法時，會自動使用相同的編碼器。</span><span class="sxs-lookup"><span data-stu-id="6868e-117">That same encoder is used automatically by all subsequent calls to the SaveAdd method of the **multi**  **Image** object.</span></span>

<span data-ttu-id="6868e-118">傳遞至 [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) 方法的第三個引數是 [**system.drawing.imaging.encoderparameters>**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) 物件的位址。</span><span class="sxs-lookup"><span data-stu-id="6868e-118">The third argument passed to the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method is the address of an [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) object.</span></span> <span data-ttu-id="6868e-119">**System.drawing.imaging.encoderparameters>** 物件具有包含單一 [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter)物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="6868e-119">The **EncoderParameters** object has an array that contains a single [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object.</span></span> <span data-ttu-id="6868e-120">該 **EncoderParameter** 物件的 **Guid** 成員會設定為 EncoderSaveFlag。</span><span class="sxs-lookup"><span data-stu-id="6868e-120">The **Guid** member of that **EncoderParameter** object is set to EncoderSaveFlag.</span></span> <span data-ttu-id="6868e-121">**EncoderParameter** 物件的 **值** 成員指向包含值 EncoderValueMultiFrame 的 **ULONG** 。</span><span class="sxs-lookup"><span data-stu-id="6868e-121">The **Value** member of the **EncoderParameter** object points to a **ULONG** that contains the value EncoderValueMultiFrame.</span></span>

<span data-ttu-id="6868e-122">程式碼會藉由呼叫 **多重**[**影像**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image)物件的 [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))方法，來儲存第二、第三和第四個頁面。  </span><span class="sxs-lookup"><span data-stu-id="6868e-122">The code saves the second, third, and fourth pages by calling the [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) method of the **multi**  [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object.</span></span> <span data-ttu-id="6868e-123">傳遞至 SaveAdd 方法的第一個引數是 **Image** 物件的位址。</span><span class="sxs-lookup"><span data-stu-id="6868e-123">The first argument passed to the SaveAdd method is the address of an **Image** object.</span></span> <span data-ttu-id="6868e-124">該 **映射** 物件中的影像會新增至 **多** 個 **映射** 物件，並且也會新增至 Multiframe .tif 磁片檔。  </span><span class="sxs-lookup"><span data-stu-id="6868e-124">The image in that **Image** object is added to the **multi**  **Image** object and is also added to the Multiframe.tif disk file.</span></span> <span data-ttu-id="6868e-125">傳遞至 SaveAdd 方法的第二個引數是 [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters))方法所使用之相同 [**system.drawing.imaging.encoderparameters>**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters)物件的位址。</span><span class="sxs-lookup"><span data-stu-id="6868e-125">The second argument passed to the SaveAdd method is the address of the same [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) object that was used by the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method.</span></span> <span data-ttu-id="6868e-126">差別在於 **值** 成員所指向的 **ULONG** 現在包含值 EncoderValueFrameDimensionPage。</span><span class="sxs-lookup"><span data-stu-id="6868e-126">The difference is that the **ULONG** pointed to by the **Value** member now contains the value EncoderValueFrameDimensionPage.</span></span>

<span data-ttu-id="6868e-127">Main 函式依賴 helper 函式 GetEncoderClsid，其顯示于抓取 [編碼器的類別識別碼](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)。</span><span class="sxs-lookup"><span data-stu-id="6868e-127">The main function relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


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



 

 
