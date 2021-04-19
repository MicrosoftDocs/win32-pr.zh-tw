---
description: 下列全域唯一識別碼 (Guid) 定義不同的時間格式。
ms.assetid: 510c7146-ff3c-4812-a7ad-b4051aa82ef3
title: '時間格式 Guid (Uuid .h) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac144a2a631602848286864c4bac10a81edc918
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990566"
---
# <a name="time-format-guids"></a><span data-ttu-id="2a911-103">時間格式 Guid</span><span class="sxs-lookup"><span data-stu-id="2a911-103">Time Format GUIDs</span></span>

<span data-ttu-id="2a911-104">下列全域唯一識別碼 (Guid) 定義不同的時間格式。</span><span class="sxs-lookup"><span data-stu-id="2a911-104">The following globally unique identifiers (GUIDs) define different time formats.</span></span>



| <span data-ttu-id="2a911-105">GUID</span><span class="sxs-lookup"><span data-stu-id="2a911-105">GUID</span></span>                                                                                                                                                                                       | <span data-ttu-id="2a911-106">Description</span><span class="sxs-lookup"><span data-stu-id="2a911-106">Description</span></span>                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------|
| <span id="TIME_FORMAT_NONE"></span><span id="time_format_none"></span><dl> <span data-ttu-id="2a911-107"><dt>**時間 \_ 格式 \_ 無**</dt></span><span class="sxs-lookup"><span data-stu-id="2a911-107"><dt>**TIME\_FORMAT\_NONE**</dt></span></span> </dl>                    | <span data-ttu-id="2a911-108">沒有格式。</span><span class="sxs-lookup"><span data-stu-id="2a911-108">No format.</span></span><br/>                             |
| <span id="TIME_FORMAT_FRAME"></span><span id="time_format_frame"></span><dl> <span data-ttu-id="2a911-109"><dt>**時間 \_ 格式 \_ 框架**</dt></span><span class="sxs-lookup"><span data-stu-id="2a911-109"><dt>**TIME\_FORMAT\_FRAME**</dt></span></span> </dl>                 | <span data-ttu-id="2a911-110">影片畫面。</span><span class="sxs-lookup"><span data-stu-id="2a911-110">Video frames.</span></span><br/>                          |
| <span id="TIME_FORMAT_SAMPLE"></span><span id="time_format_sample"></span><dl> <span data-ttu-id="2a911-111"><dt>**時間 \_ 格式 \_ 範例**</dt></span><span class="sxs-lookup"><span data-stu-id="2a911-111"><dt>**TIME\_FORMAT\_SAMPLE**</dt></span></span> </dl>              | <span data-ttu-id="2a911-112">資料流程中的範例。</span><span class="sxs-lookup"><span data-stu-id="2a911-112">Samples in the stream.</span></span><br/>                 |
| <span id="TIME_FORMAT_FIELD"></span><span id="time_format_field"></span><dl> <span data-ttu-id="2a911-113"><dt>**時間 \_ 格式 \_ 欄位**</dt></span><span class="sxs-lookup"><span data-stu-id="2a911-113"><dt>**TIME\_FORMAT\_FIELD**</dt></span></span> </dl>                 | <span data-ttu-id="2a911-114">交錯式影片欄位。</span><span class="sxs-lookup"><span data-stu-id="2a911-114">Interlaced video fields.</span></span><br/>               |
| <span id="TIME_FORMAT_BYTE"></span><span id="time_format_byte"></span><dl> <span data-ttu-id="2a911-115"><dt>**時間 \_ 格式 \_ 位元組**</dt></span><span class="sxs-lookup"><span data-stu-id="2a911-115"><dt>**TIME\_FORMAT\_BYTE**</dt></span></span> </dl>                    | <span data-ttu-id="2a911-116">資料流程內的位元組位移。</span><span class="sxs-lookup"><span data-stu-id="2a911-116">Byte offset within the stream.</span></span><br/>         |
| <span id="TIME_FORMAT_MEDIA_TIME"></span><span id="time_format_media_time"></span><dl> <span data-ttu-id="2a911-117"><dt>**時間 \_ 格式 \_ 媒體 \_ 時間**</dt></span><span class="sxs-lookup"><span data-stu-id="2a911-117"><dt>**TIME\_FORMAT\_MEDIA\_TIME**</dt></span></span> </dl> | <span data-ttu-id="2a911-118">參考時間 (100-納秒單位) 。</span><span class="sxs-lookup"><span data-stu-id="2a911-118">Reference time (100-nanosecond units).</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="2a911-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a911-119">Requirements</span></span>



| <span data-ttu-id="2a911-120">需求</span><span class="sxs-lookup"><span data-stu-id="2a911-120">Requirement</span></span> | <span data-ttu-id="2a911-121">值</span><span class="sxs-lookup"><span data-stu-id="2a911-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a911-122">標頭</span><span class="sxs-lookup"><span data-stu-id="2a911-122">Header</span></span><br/> | <dl> <span data-ttu-id="2a911-123"><dt>Uuid (包含 Dshow .h) </dt></span><span class="sxs-lookup"><span data-stu-id="2a911-123"><dt>Uuids.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a911-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a911-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a911-125">常數和 Guid</span><span class="sxs-lookup"><span data-stu-id="2a911-125">Constants and GUIDs</span></span>](constants-and-guids.md)
</dt> <dt>

[<span data-ttu-id="2a911-126">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="2a911-126">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)
</dt> </dl>

 

 




