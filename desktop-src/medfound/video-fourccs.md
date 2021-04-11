---
description: 影片 FOURCCs
ms.assetid: bea4835d-fd7f-4ac3-8466-7f4e0d799a12
title: 影片 FOURCCs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b804962308d0ecc5bf32fcddf5176905d0e17fbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318916"
---
# <a name="video-fourccs"></a><span data-ttu-id="dd8d1-103">影片 FOURCCs</span><span class="sxs-lookup"><span data-stu-id="dd8d1-103">Video FOURCCs</span></span>

<span data-ttu-id="dd8d1-104">許多影片格式都有指派的 FOURCC 碼。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-104">Many video formats have FOURCC codes assigned to them.</span></span> <span data-ttu-id="dd8d1-105">FOURCC 程式碼是串連四個 ASCII 字元所建立的32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-105">A FOURCC code is a 32-bit unsigned integer that is created by concatenating four ASCII characters.</span></span> <span data-ttu-id="dd8d1-106">例如，YUY2 video 的 FOURCC 程式碼為 ' YUY2 '。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-106">For example, the FOURCC code for YUY2 video is 'YUY2'.</span></span>

<span data-ttu-id="dd8d1-107">定義各種 C/c + + 宏，以在原始程式碼中宣告 FOURCC 值。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-107">Various C/C++ macros are defined for declaring FOURCC values in source code.</span></span> <span data-ttu-id="dd8d1-108">**MAKEFOURCC** 宏是在 Mmsystem 中定義，而 **FCC** 宏則是在 Aviriff 和其他各種標頭檔中定義。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-108">The **MAKEFOURCC** macro is defined in Mmsystem.h, and the **FCC** macro is defined in Aviriff.h and various other header files.</span></span> <span data-ttu-id="dd8d1-109">您也可以藉由反轉字元順序，直接將 FOURCC 程式碼宣告為字串常值。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-109">You can also declare a FOURCC code directly as a string literal simply by reversing the order of the characters.</span></span> <span data-ttu-id="dd8d1-110">因此，下列語句是相等的：</span><span class="sxs-lookup"><span data-stu-id="dd8d1-110">Thus, the following statements are equivalent:</span></span>

``` syntax
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'.
```

<span data-ttu-id="dd8d1-111"> (在最後一個範例中，必須反轉位元組順序，因為 Windows 會使用位元組由大到小的架構。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-111">(In the last example, reversing the byte order is necessary because Windows uses a little-endian architecture.</span></span> <span data-ttu-id="dd8d1-112">' Y ' = 0x59，' U ' = 0x55，' 2 ' = 0x32，因此 ' 2YUY ' 為0x32595559。 ) </span><span class="sxs-lookup"><span data-stu-id="dd8d1-112">'Y' = 0x59, 'U' = 0x55, and '2' = 0x32, so '2YUY' is 0x32595559.)</span></span>

<span data-ttu-id="dd8d1-113">某些 [DirectX Video 加速 2.0](directx-video-acceleration-2-0.md) api 會使用 **D3DFORMAT** 值來描述影片格式。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-113">Some of the [DirectX Video Acceleration 2.0](directx-video-acceleration-2-0.md) APIs use a **D3DFORMAT** value to describe a video format.</span></span> <span data-ttu-id="dd8d1-114">您也可以在此內容中使用 FOURCC 程式碼：</span><span class="sxs-lookup"><span data-stu-id="dd8d1-114">A FOURCC code can be used in this context as well:</span></span>

``` syntax
D3DFORMAT fmt = (D3DFORMAT)MAKEFOURCC('Y','U','Y','2');
D3DFORMAT fmt = (D3DFORMAT)FCC('YUY2');
D3DFORMAT fmt = D3DFORMAT('2YUY'); // Coerce to D3DFORMAT type.
```

### <a name="fourcc-constants"></a><span data-ttu-id="dd8d1-115">FOURCC 常數</span><span class="sxs-lookup"><span data-stu-id="dd8d1-115">FOURCC Constants</span></span>

<span data-ttu-id="dd8d1-116">下表列出一些常見的 FOURCC 碼。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-116">The following table lists some common FOURCC codes.</span></span>



| <span data-ttu-id="dd8d1-117">FOURCC 值</span><span class="sxs-lookup"><span data-stu-id="dd8d1-117">FOURCC value</span></span> | <span data-ttu-id="dd8d1-118">Description</span><span class="sxs-lookup"><span data-stu-id="dd8d1-118">Description</span></span>                                                                                                           |
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd8d1-119">H264</span><span class="sxs-lookup"><span data-stu-id="dd8d1-119">'H264'</span></span>       | <span data-ttu-id="dd8d1-120">H.264 video。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-120">H.264 video.</span></span>                                                                                                          |
| <span data-ttu-id="dd8d1-121">'I420'</span><span class="sxs-lookup"><span data-stu-id="dd8d1-121">'I420'</span></span>       | <span data-ttu-id="dd8d1-122">YUV 以平面4:2:0 格式儲存的影片。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-122">YUV video stored in planar 4:2:0 format.</span></span>                                                                              |
| <span data-ttu-id="dd8d1-123">'IYUV'</span><span class="sxs-lookup"><span data-stu-id="dd8d1-123">'IYUV'</span></span>       | <span data-ttu-id="dd8d1-124">YUV 以平面4:2:0 格式儲存的影片。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-124">YUV video stored in planar 4:2:0 format.</span></span>                                                                              |
| <span data-ttu-id="dd8d1-125">4S2 '</span><span class="sxs-lookup"><span data-stu-id="dd8d1-125">'M4S2'</span></span>       | <span data-ttu-id="dd8d1-126">MPEG 4 第2部分影片。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-126">MPEG-4 part 2 video.</span></span>                                                                                                  |
| <span data-ttu-id="dd8d1-127">MP4</span><span class="sxs-lookup"><span data-stu-id="dd8d1-127">'MP4S'</span></span>       | <span data-ttu-id="dd8d1-128">Microsoft MPEG 4 編解碼器第3版。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-128">Microsoft MPEG 4 codec version 3.</span></span> <span data-ttu-id="dd8d1-129">不再支援此編解碼器。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-129">This codec is no longer supported.</span></span>                                                  |
| <span data-ttu-id="dd8d1-130">'MP4V'</span><span class="sxs-lookup"><span data-stu-id="dd8d1-130">'MP4V'</span></span>       | <span data-ttu-id="dd8d1-131">MPEG 4 第2部分影片。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-131">MPEG-4 part 2 video.</span></span>                                                                                                  |
| <span data-ttu-id="dd8d1-132">'MPG1'</span><span class="sxs-lookup"><span data-stu-id="dd8d1-132">'MPG1'</span></span>       | <span data-ttu-id="dd8d1-133">MPEG-2 影片。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-133">MPEG-1 video.</span></span>                                                                                                         |
| <span data-ttu-id="dd8d1-134">'MSS1'</span><span class="sxs-lookup"><span data-stu-id="dd8d1-134">'MSS1'</span></span>       | <span data-ttu-id="dd8d1-135">以 Windows Media 視訊7螢幕編解碼器編碼的內容。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-135">Content encoded with the Windows Media Video 7 screen codec.</span></span>                                                          |
| <span data-ttu-id="dd8d1-136">'MSS2'</span><span class="sxs-lookup"><span data-stu-id="dd8d1-136">'MSS2'</span></span>       | <span data-ttu-id="dd8d1-137">以 Windows Media 視訊9螢幕編解碼器編碼的內容。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-137">Content encoded with the Windows Media Video 9 screen codec.</span></span>                                                          |
| <span data-ttu-id="dd8d1-138">UYVY</span><span class="sxs-lookup"><span data-stu-id="dd8d1-138">'UYVY'</span></span>       | <span data-ttu-id="dd8d1-139">YUV 以壓縮的4:2:2 格式儲存的影片。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-139">YUV video stored in packed 4:2:2 format.</span></span> <span data-ttu-id="dd8d1-140">類似于 YUY2，但資料的順序不同。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-140">Similar to YUY2 but with different ordering of data.</span></span>                         |
| <span data-ttu-id="dd8d1-141">'WMV1'</span><span class="sxs-lookup"><span data-stu-id="dd8d1-141">'WMV1'</span></span>       | <span data-ttu-id="dd8d1-142">以 Windows Media 視訊7編解碼器編碼的內容。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-142">Content encoded with the Windows Media Video 7 codec.</span></span>                                                                 |
| <span data-ttu-id="dd8d1-143">'WMV2'</span><span class="sxs-lookup"><span data-stu-id="dd8d1-143">'WMV2'</span></span>       | <span data-ttu-id="dd8d1-144">以 Windows Media 視訊8編解碼器編碼的內容。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-144">Content encoded with the Windows Media Video 8 codec.</span></span>                                                                 |
| <span data-ttu-id="dd8d1-145">'WMV3'</span><span class="sxs-lookup"><span data-stu-id="dd8d1-145">'WMV3'</span></span>       | <span data-ttu-id="dd8d1-146">以 Windows Media 視訊9編解碼器編碼的內容。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-146">Content encoded with the Windows Media Video 9 codec.</span></span>                                                                 |
| <span data-ttu-id="dd8d1-147">'WMVA'</span><span class="sxs-lookup"><span data-stu-id="dd8d1-147">'WMVA'</span></span>       | <span data-ttu-id="dd8d1-148">以舊版、過時版本的 Windows Media 視訊 9 Advanced Profile 編解碼器編碼的內容。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-148">Content encoded with the older, obsolete version of the Windows Media Video 9 Advanced Profile codec.</span></span>                 |
| <span data-ttu-id="dd8d1-149">'WMVP'</span><span class="sxs-lookup"><span data-stu-id="dd8d1-149">'WMVP'</span></span>       | <span data-ttu-id="dd8d1-150">以 Windows Media 視訊9.1 影像編解碼器編碼的內容。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-150">Content encoded with the Windows Media Video 9.1 Image codec.</span></span>                                                         |
| <span data-ttu-id="dd8d1-151">'WVC1'</span><span class="sxs-lookup"><span data-stu-id="dd8d1-151">'WVC1'</span></span>       | <span data-ttu-id="dd8d1-152">SMPTE 421M ( "VC-1" ) 。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-152">SMPTE 421M ("VC-1").</span></span> <span data-ttu-id="dd8d1-153">使用 Windows Media 視訊 9 Advanced Profile 編碼的內容。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-153">Content encoded with Windows Media Video 9 Advanced Profile.</span></span>                                     |
| <span data-ttu-id="dd8d1-154">'WVP2'</span><span class="sxs-lookup"><span data-stu-id="dd8d1-154">'WVP2'</span></span>       | <span data-ttu-id="dd8d1-155">以 Windows Media 視訊9.1 影像 v2 編解碼器編碼的內容。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-155">Content encoded with the Windows Media Video 9.1 Image v2 codec.</span></span>                                                      |
| <span data-ttu-id="dd8d1-156">YUY2</span><span class="sxs-lookup"><span data-stu-id="dd8d1-156">'YUY2'</span></span>       | <span data-ttu-id="dd8d1-157">YUV 以壓縮的4:2:2 格式儲存的影片。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-157">YUV video stored in packed 4:2:2 format.</span></span>                                                                              |
| <span data-ttu-id="dd8d1-158">'YV12'</span><span class="sxs-lookup"><span data-stu-id="dd8d1-158">'YV12'</span></span>       | <span data-ttu-id="dd8d1-159">YUV 以平面4:2:0 或4:1:1 格式儲存的影片。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-159">YUV video stored in planar 4:2:0 or 4:1:1 format.</span></span> <span data-ttu-id="dd8d1-160">與 I420/IYUV 相同，不同之處在于您和 V 平面已切換。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-160">Identical to I420/IYUV except that the U and V planes are switched.</span></span> |
| <span data-ttu-id="dd8d1-161">YVU9</span><span class="sxs-lookup"><span data-stu-id="dd8d1-161">'YVU9'</span></span>       | <span data-ttu-id="dd8d1-162">YUV 以平面16:1:1 格式儲存的影片。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-162">YUV video stored in planar 16:1:1 format.</span></span>                                                                             |
| <span data-ttu-id="dd8d1-163">'YVYU'</span><span class="sxs-lookup"><span data-stu-id="dd8d1-163">'YVYU'</span></span>       | <span data-ttu-id="dd8d1-164">YUV 以壓縮的4:2:2 格式儲存的影片。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-164">YUV video stored in packed 4:2:2 format.</span></span> <span data-ttu-id="dd8d1-165">類似于 YUY2，但資料的順序不同。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-165">Similar to YUY2 but with different ordering of data.</span></span>                         |



 

## <a name="related-topics"></a><span data-ttu-id="dd8d1-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="dd8d1-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd8d1-167">影片媒體類型</span><span class="sxs-lookup"><span data-stu-id="dd8d1-167">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="dd8d1-168">影片子類型 Guid</span><span class="sxs-lookup"><span data-stu-id="dd8d1-168">Video Subtype GUIDs</span></span>](video-subtype-guids.md)
</dt> </dl>

 

 



