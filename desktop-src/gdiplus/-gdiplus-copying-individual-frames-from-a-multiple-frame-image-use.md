---
title: 從多框架影像複製個別的框架
description: 下列範例會從多框架 TIFF 檔案抓取個別的框架。
ms.assetid: dfed0b61-2230-4911-a642-0a6e4beb08d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d6bdb5668bcebb9babcbcb7d07839694750aec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192336"
---
# <a name="copy-individual-frames-from-a-multiple-frame-image"></a><span data-ttu-id="4bd1a-103">從多框架影像複製個別的框架</span><span class="sxs-lookup"><span data-stu-id="4bd1a-103">Copy individual frames from a multiple-frame image</span></span>

<span data-ttu-id="4bd1a-104">下列範例會從多框架 TIFF 檔案抓取個別的框架。</span><span class="sxs-lookup"><span data-stu-id="4bd1a-104">The following example retrieves the individual frames from a multiple-frame TIFF file.</span></span> <span data-ttu-id="4bd1a-105">建立 TIFF 檔案時，會在頁面維度中加入個別的框架 (請參閱 [建立和儲存 Multiple-Frame 映射](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)) 。</span><span class="sxs-lookup"><span data-stu-id="4bd1a-105">When the TIFF file was created, the individual frames were added to the Page dimension (see [Creating and Saving a Multiple-Frame Image](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)).</span></span> <span data-ttu-id="4bd1a-106">此程式碼會顯示四個頁面中的每個頁面，並將每個頁面儲存至不同的 PNG 磁片檔案。</span><span class="sxs-lookup"><span data-stu-id="4bd1a-106">The code displays each of the four pages and saves each page to a separate PNG disk file.</span></span>

<span data-ttu-id="4bd1a-107">程式碼會從多框架 TIFF 檔案中建立 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 物件。</span><span class="sxs-lookup"><span data-stu-id="4bd1a-107">The code constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the multiple-frame TIFF file.</span></span> <span data-ttu-id="4bd1a-108">若要)  (頁面抓取個別的框架，程式碼會呼叫該 **影像** 物件的 [**Image：： SelectActiveFrame**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-selectactiveframe)方法。</span><span class="sxs-lookup"><span data-stu-id="4bd1a-108">To retrieve the individual frames (pages), the code calls the [**Image::SelectActiveFrame**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-selectactiveframe) method of that **Image** object.</span></span> <span data-ttu-id="4bd1a-109">傳遞至 **Image：： SelectActiveFrame** 方法的第一個引數是 GUID 的位址，這個 GUID 會指定框架先前加入至多框架 TIFF 檔案的維度。</span><span class="sxs-lookup"><span data-stu-id="4bd1a-109">The first argument passed to the **Image::SelectActiveFrame** method is the address of a GUID that specifies the dimension in which the frames were previously added to the multiple-frame TIFF file.</span></span> <span data-ttu-id="4bd1a-110">GUID FrameDimensionPage 定義于 Gdiplusimaging 中。</span><span class="sxs-lookup"><span data-stu-id="4bd1a-110">The GUID FrameDimensionPage is defined in Gdiplusimaging.h.</span></span> <span data-ttu-id="4bd1a-111">在該標頭檔中定義的其他 Guid 為 FrameDimensionTime 和 FrameDimensionResolution。</span><span class="sxs-lookup"><span data-stu-id="4bd1a-111">Other GUIDs defined in that header file are FrameDimensionTime and FrameDimensionResolution.</span></span> <span data-ttu-id="4bd1a-112">傳遞至 **Image：： SelectActiveFrame** 方法的第二個引數是所需頁面的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="4bd1a-112">The second argument passed to the **Image::SelectActiveFrame** method is the zero-based index of the desired page.</span></span>

<span data-ttu-id="4bd1a-113">程式碼會依賴 helper 函式 GetEncoderClsid，它會顯示在抓取 [編碼器的類別識別碼](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)中。</span><span class="sxs-lookup"><span data-stu-id="4bd1a-113">The code relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


```
GUID   pageGuid = FrameDimensionPage;
CLSID  encoderClsid;
Image  multi(L"Multiframe.tif");

// Get the CLSID of the PNG encoder.
GetEncoderClsid(L"image/png", &encoderClsid);

// Display and save the first page (index 0).
multi.SelectActiveFrame(&pageGuid, 0);
graphics.DrawImage(&multi, 10, 10);
multi.Save(L"Page0.png", &encoderClsid, NULL);

// Display and save the second page.
multi.SelectActiveFrame(&pageGuid, 1);
graphics.DrawImage(&multi, 200, 10);
multi.Save(L"Page1.png", &encoderClsid, NULL);

// Display and save the third page.
multi.SelectActiveFrame(&pageGuid, 2);
graphics.DrawImage(&multi, 10, 150);
multi.Save(L"Page2.png", &encoderClsid, NULL);

// Display and save the fourth page.
multi.SelectActiveFrame(&pageGuid, 3);
graphics.DrawImage(&multi, 200, 150);
multi.Save(L"Page3.png", &encoderClsid, NULL);
```



<span data-ttu-id="4bd1a-114">下圖顯示上述程式碼所顯示的個別頁面。</span><span class="sxs-lookup"><span data-stu-id="4bd1a-114">The following illustration shows the individual pages as displayed by the preceding code.</span></span>

![顯示幾何圖形、彩色相片、單色相片和不同幾何形狀的圖例](images/multiframe1.png)

 

 



