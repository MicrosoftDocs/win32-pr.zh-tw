---
description: Windows 可攜式裝置支援下列影片內容。
ms.assetid: e6df5b2d-ceb8-4de0-b60b-9102c77143fe
title: '影片屬性 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Video
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1f44f32ab19c5ad10cc9c8dd5bdb8816ccc944f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984008"
---
# <a name="video-properties"></a><span data-ttu-id="ff9ae-103">影片屬性</span><span class="sxs-lookup"><span data-stu-id="ff9ae-103">Video Properties</span></span>

<span data-ttu-id="ff9ae-104">Windows 可攜式裝置支援下列影片內容。</span><span class="sxs-lookup"><span data-stu-id="ff9ae-104">Windows Portable Devices supports the following video properties.</span></span>



| <span data-ttu-id="ff9ae-105">屬性</span><span class="sxs-lookup"><span data-stu-id="ff9ae-105">Property</span></span>                                         | <span data-ttu-id="ff9ae-106">VarType</span><span class="sxs-lookup"><span data-stu-id="ff9ae-106">VarType</span></span>        | <span data-ttu-id="ff9ae-107">Description</span><span class="sxs-lookup"><span data-stu-id="ff9ae-107">Description</span></span>                                                                                                                                                                                                                                             |
|--------------------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff9ae-108">**WPD \_ 影片 \_ 作者**</span><span class="sxs-lookup"><span data-stu-id="ff9ae-108">**WPD\_VIDEO\_AUTHOR**</span></span>                           | <span data-ttu-id="ff9ae-109">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="ff9ae-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="ff9ae-110">影片檔案的作者。</span><span class="sxs-lookup"><span data-stu-id="ff9ae-110">The author of the video file.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="ff9ae-111">**WPD \_ 影片 \_ 位元速率**</span><span class="sxs-lookup"><span data-stu-id="ff9ae-111">**WPD\_VIDEO\_BITRATE**</span></span>                          | <span data-ttu-id="ff9ae-112">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="ff9ae-112">**VT\_UI4**</span></span>    | <span data-ttu-id="ff9ae-113">影片檔案的位元速率。</span><span class="sxs-lookup"><span data-stu-id="ff9ae-113">The bit rate of the video file.</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="ff9ae-114">**WPD \_ 影片 \_ 緩衝區 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="ff9ae-114">**WPD\_VIDEO\_BUFFER\_SIZE**</span></span>                     | <span data-ttu-id="ff9ae-115">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="ff9ae-115">**VT\_UI4**</span></span>    | <span data-ttu-id="ff9ae-116">值，指定轉譯此檔案所需的影片緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="ff9ae-116">A value that specifies the required video buffer size to render this file.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="ff9ae-117">**WPD \_ 影片 \_ 點數**</span><span class="sxs-lookup"><span data-stu-id="ff9ae-117">**WPD\_VIDEO\_CREDITS**</span></span>                          | <span data-ttu-id="ff9ae-118">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="ff9ae-118">**VT\_LPWSTR**</span></span> | <span data-ttu-id="ff9ae-119">列出影片轉換和小組的信用額度。</span><span class="sxs-lookup"><span data-stu-id="ff9ae-119">The credits listing the cast and crew for the video.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="ff9ae-120">**WPD \_ VIDEO \_ FOURCC 程式 \_ 代碼**</span><span class="sxs-lookup"><span data-stu-id="ff9ae-120">**WPD\_VIDEO\_FOURCC\_CODE**</span></span>                     | <span data-ttu-id="ff9ae-121">**VT \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="ff9ae-121">**VT\_DWORD**</span></span>  | <span data-ttu-id="ff9ae-122">註冊的 FourCC 程式碼，指出用於影片檔案的編解碼器。</span><span class="sxs-lookup"><span data-stu-id="ff9ae-122">The registered FourCC code that indicates the codec that was used for the video file.</span></span> <span data-ttu-id="ff9ae-123">如需 FourCC 格式的清單，請參閱 MSDN 網站上的 [註冊的 FourCC 碼和 WAVE 格式](https://msdn2.microsoft.com/library/ms867195.aspx) 文章。</span><span class="sxs-lookup"><span data-stu-id="ff9ae-123">For a listing of FourCC formats, see the article [Registered FOURCC Codes and WAVE Formats](https://msdn2.microsoft.com/library/ms867195.aspx) on the MSDN Web site.</span></span> |
| <span data-ttu-id="ff9ae-124">**WPD \_ 影片的 \_ 畫面播放速率**</span><span class="sxs-lookup"><span data-stu-id="ff9ae-124">**WPD\_VIDEO\_FRAMERATE**</span></span>                        | <span data-ttu-id="ff9ae-125">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="ff9ae-125">**VT\_UI4**</span></span>    | <span data-ttu-id="ff9ae-126">影片檔案的畫面播放速率，以框架/秒 x 1000 為限。</span><span class="sxs-lookup"><span data-stu-id="ff9ae-126">The frame rate of the video file, in frames/second x 1,000.</span></span> <span data-ttu-id="ff9ae-127">例如，畫面播放速率29.97 表示為29970。</span><span class="sxs-lookup"><span data-stu-id="ff9ae-127">For example, a frame rate of 29.97 is represented as 29970.</span></span>                                                                                                                                 |
| <span data-ttu-id="ff9ae-128">**WPD \_ 影片內容類型 \_**</span><span class="sxs-lookup"><span data-stu-id="ff9ae-128">**WPD\_VIDEO\_GENRE**</span></span>                            | <span data-ttu-id="ff9ae-129">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="ff9ae-129">**VT\_LPWSTR**</span></span> | <span data-ttu-id="ff9ae-130">此影片檔案的類型。</span><span class="sxs-lookup"><span data-stu-id="ff9ae-130">The genre of this video file.</span></span> <span data-ttu-id="ff9ae-131">沒有標準的內容類型定義。</span><span class="sxs-lookup"><span data-stu-id="ff9ae-131">There are no standard genre definitions.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="ff9ae-132">**WPD \_ 影片 \_ 主要 \_ 畫面 \_ 距離**</span><span class="sxs-lookup"><span data-stu-id="ff9ae-132">**WPD\_VIDEO\_KEY\_FRAME\_DISTANCE**</span></span>             | <span data-ttu-id="ff9ae-133">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="ff9ae-133">**VT\_UI4**</span></span>    | <span data-ttu-id="ff9ae-134">主要畫面格之間的間隔（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ff9ae-134">The interval between key frames, in milliseconds.</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="ff9ae-135">**WPD \_ 視頻 \_ 品質 \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="ff9ae-135">**WPD\_VIDEO\_QUALITY\_SETTING**</span></span>                 | <span data-ttu-id="ff9ae-136">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="ff9ae-136">**VT\_UI4**</span></span>    | <span data-ttu-id="ff9ae-137">影片檔案的品質設定。</span><span class="sxs-lookup"><span data-stu-id="ff9ae-137">The quality setting for the video file.</span></span> <span data-ttu-id="ff9ae-138">這與編解碼器相依。</span><span class="sxs-lookup"><span data-stu-id="ff9ae-138">This is codec-dependent.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="ff9ae-139">**WPD \_ VIDEO \_ RECORDEDTV \_ CHANNEL \_ NUMBER**</span><span class="sxs-lookup"><span data-stu-id="ff9ae-139">**WPD\_VIDEO\_RECORDEDTV\_CHANNEL\_NUMBER**</span></span>      | <span data-ttu-id="ff9ae-140">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="ff9ae-140">**VT\_UI4**</span></span>    | <span data-ttu-id="ff9ae-141">錄製影片的電視頻道號碼。</span><span class="sxs-lookup"><span data-stu-id="ff9ae-141">The television channel number the video was recorded from.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="ff9ae-142">**WPD \_ VIDEO \_ RECORDEDTV \_ 節目 \_ 說明**</span><span class="sxs-lookup"><span data-stu-id="ff9ae-142">**WPD\_VIDEO\_RECORDEDTV\_PROGRAM\_DESCRIPTION**</span></span> | <span data-ttu-id="ff9ae-143">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="ff9ae-143">**VT\_LPWSTR**</span></span> | <span data-ttu-id="ff9ae-144">錄製的電視節目描述。</span><span class="sxs-lookup"><span data-stu-id="ff9ae-144">A description of the recorded television program.</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="ff9ae-145">**WPD \_ VIDEO \_ RECORDEDTV \_ REPEAT**</span><span class="sxs-lookup"><span data-stu-id="ff9ae-145">**WPD\_VIDEO\_RECORDEDTV\_REPEAT**</span></span>               | <span data-ttu-id="ff9ae-146">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="ff9ae-146">**VT\_BOOL**</span></span>   | <span data-ttu-id="ff9ae-147">指定電視節目是否重複顯示的布林值。</span><span class="sxs-lookup"><span data-stu-id="ff9ae-147">A Boolean value that specifies whether the television program was a repeat showing.</span></span>                                                                                                                                                                     |
| <span data-ttu-id="ff9ae-148">**WPD \_ VIDEO \_ RECORDEDTV \_ 站 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="ff9ae-148">**WPD\_VIDEO\_RECORDEDTV\_STATION\_NAME**</span></span>        | <span data-ttu-id="ff9ae-149">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="ff9ae-149">**VT\_LPWSTR**</span></span> | <span data-ttu-id="ff9ae-150">影片錄製來源的電視電臺。</span><span class="sxs-lookup"><span data-stu-id="ff9ae-150">The television station that the video was recorded from.</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="ff9ae-151">**WPD \_ 影片 \_ 掃描 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="ff9ae-151">**WPD\_VIDEO\_SCAN\_TYPE**</span></span>                       | <span data-ttu-id="ff9ae-152">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="ff9ae-152">**VT\_UI4**</span></span>    | <span data-ttu-id="ff9ae-153">[**WPD \_ 影片 \_ 掃描 \_ 類型**](wpd-video-scan-types.md)列舉值，指定影片檔案的交錯。</span><span class="sxs-lookup"><span data-stu-id="ff9ae-153">A [**WPD\_VIDEO\_SCAN\_TYPES**](wpd-video-scan-types.md) enumerator that specifies the interlacing of the video file.</span></span>                                                                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="ff9ae-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff9ae-154">Requirements</span></span>



| <span data-ttu-id="ff9ae-155">需求</span><span class="sxs-lookup"><span data-stu-id="ff9ae-155">Requirement</span></span> | <span data-ttu-id="ff9ae-156">值</span><span class="sxs-lookup"><span data-stu-id="ff9ae-156">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff9ae-157">標頭</span><span class="sxs-lookup"><span data-stu-id="ff9ae-157">Header</span></span><br/> | <dl> <span data-ttu-id="ff9ae-158"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="ff9ae-158"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff9ae-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff9ae-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff9ae-160">**WPD 屬性和屬性**</span><span class="sxs-lookup"><span data-stu-id="ff9ae-160">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




