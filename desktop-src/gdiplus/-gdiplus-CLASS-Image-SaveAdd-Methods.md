---
description: 本主題列出 Image 類別的 SaveAdd 方法。 如需 Image 類別之方法的完整清單，請參閱影像方法。
ms.assetid: e597f6e6-6e07-4afb-8905-26e4af961685
title: 'SaveAdd 方法 (Gdiplusheaders .h) '
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: a2b65c6fe56507538f092edc7128497de5cb2f00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973029"
---
# <a name="imagesaveadd-methods"></a><span data-ttu-id="4dba8-104">SaveAdd 方法</span><span class="sxs-lookup"><span data-stu-id="4dba8-104">Image.SaveAdd methods</span></span>

<span data-ttu-id="4dba8-105">本主題列出 [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) 類別的 SaveAdd 方法。</span><span class="sxs-lookup"><span data-stu-id="4dba8-105">This topic lists the SaveAdd methods of the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class.</span></span> <span data-ttu-id="4dba8-106">如需 **image** 類別之方法的完整清單，請參閱 [影像方法](-gdiplus-class-image-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="4dba8-106">For a complete list of methods for the **Image** class, see [Image Methods](-gdiplus-class-image-methods.md).</span></span>

### <a name="overload-list"></a><span data-ttu-id="4dba8-107">多載清單</span><span class="sxs-lookup"><span data-stu-id="4dba8-107">Overload list</span></span>



| <span data-ttu-id="4dba8-108">方法</span><span class="sxs-lookup"><span data-stu-id="4dba8-108">Method</span></span>                                                                                               | <span data-ttu-id="4dba8-109">描述</span><span class="sxs-lookup"><span data-stu-id="4dba8-109">Description</span></span>                                                                                                                                                                                                                                                                            |
|:-----------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4dba8-110">[**SaveAdd (System.drawing.imaging.encoderparameters> \*)**](/previous-versions//ms535408(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4dba8-110">[**SaveAdd(EncoderParameters\*)**](/previous-versions//ms535408(v=vs.85))</span></span>                  | <span data-ttu-id="4dba8-111">[**Image：： SaveAdd**](/previous-versions//ms535408(v=vs.85))方法會將框架新增至 **儲存** 方法的前一個呼叫所指定的檔案或資料流程。</span><span class="sxs-lookup"><span data-stu-id="4dba8-111">The [**Image::SaveAdd**](/previous-versions//ms535408(v=vs.85)) method adds a frame to a file or stream specified in a previous call to the **Save** method.</span></span> <span data-ttu-id="4dba8-112">使用這個方法以從多重框架影像儲存選取框架至另一個多重框架影像。</span><span class="sxs-lookup"><span data-stu-id="4dba8-112">Use this method to save selected frames from a multiple-frame image to another multiple-frame image.</span></span><br/> |
| <span data-ttu-id="4dba8-113">[**SaveAdd (映射 \* ，system.drawing.imaging.encoderparameters> \*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))</span><span class="sxs-lookup"><span data-stu-id="4dba8-113">[**SaveAdd(Image\*,EncoderParameters\*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))</span></span> | <span data-ttu-id="4dba8-114">[**Image：： SaveAdd**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))方法會將框架新增至 **儲存** 方法的前一個呼叫所指定的檔案或資料流程。</span><span class="sxs-lookup"><span data-stu-id="4dba8-114">The [**Image::SaveAdd**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) method adds a frame to a file or stream specified in a previous call to the **Save** method.</span></span><br/>                                                                                             |



## <a name="requirements"></a><span data-ttu-id="4dba8-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="4dba8-115">Requirements</span></span>



| <span data-ttu-id="4dba8-116">需求</span><span class="sxs-lookup"><span data-stu-id="4dba8-116">Requirement</span></span> | <span data-ttu-id="4dba8-117">值</span><span class="sxs-lookup"><span data-stu-id="4dba8-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4dba8-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4dba8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4dba8-119">僅限 windows XP、Windows 2000 Professional \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4dba8-119">Windows XP, Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4dba8-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4dba8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4dba8-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4dba8-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="4dba8-122">產品</span><span class="sxs-lookup"><span data-stu-id="4dba8-122">Product</span></span><br/>                  | <span data-ttu-id="4dba8-123">GDI + 1。0</span><span class="sxs-lookup"><span data-stu-id="4dba8-123">GDI+ 1.0</span></span><br/>                                                                                             |
| <span data-ttu-id="4dba8-124">標頭</span><span class="sxs-lookup"><span data-stu-id="4dba8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4dba8-125"><dt>Gdiplusheaders (包含 Gdiplus.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="4dba8-125"><dt>Gdiplusheaders.h (include Gdiplus.h)</dt></span></span> </dl> |
| <span data-ttu-id="4dba8-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="4dba8-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="4dba8-127"><dt>Gdiplus.dll .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4dba8-127"><dt>Gdiplus.lib</dt></span></span> </dl>                          |



 

 
