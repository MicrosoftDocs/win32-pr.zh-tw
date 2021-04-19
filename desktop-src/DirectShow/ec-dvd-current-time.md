---
description: 表示每個影片物件單位的開頭 (VOBU) ，其長度為0.4 到1.0 秒的影片區段。
ms.assetid: 1f2def2f-3a6b-458b-b564-09b6cf74543c
title: 'EC_DVD_CURRENT_TIME (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CURRENT_TIME
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 0f1bb2f5f31efa881917ac71ea381cc0a82e8744
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990192"
---
# <a name="ec_dvd_current_time"></a><span data-ttu-id="f1bae-103">EC \_ DVD \_ 目前 \_ 時間</span><span class="sxs-lookup"><span data-stu-id="f1bae-103">EC\_DVD\_CURRENT\_TIME</span></span>

<span data-ttu-id="f1bae-104">表示每個影片物件單位的開頭 (VOBU) ，其長度為0.4 到1.0 秒的影片區段。</span><span class="sxs-lookup"><span data-stu-id="f1bae-104">Signals the beginning of every video object unit (VOBU), a video segment which is 0.4 to 1.0 seconds in length.</span></span>

## <a name="parameters"></a><span data-ttu-id="f1bae-105">參數</span><span class="sxs-lookup"><span data-stu-id="f1bae-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1bae-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="f1bae-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="f1bae-107">**DWORD** 值，指出二進位編碼十進位 (BCD 中目前的播放時間碼，) 小時、分鐘、秒、框架 (HH： MM： SS： FF) 格式。</span><span class="sxs-lookup"><span data-stu-id="f1bae-107">**DWORD** value indicating the current playback timecode in a binary coded decimal (BCD) hours, minutes, seconds, frames (HH:MM:SS:FF) format.</span></span> <span data-ttu-id="f1bae-108">[**DVD 時間 \_ 碼**](/windows/win32/api/strmif/ns-strmif-dvd_timecode)結構的成員。</span><span class="sxs-lookup"><span data-stu-id="f1bae-108">Member of the [**DVD\_TIMECODE**](/windows/win32/api/strmif/ns-strmif-dvd_timecode) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f1bae-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="f1bae-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="f1bae-110">布林值 (**BOOL**) 指出時間碼的值。</span><span class="sxs-lookup"><span data-stu-id="f1bae-110">Boolean (**BOOL**) value indicating the timecode.</span></span> <span data-ttu-id="f1bae-111">零 (0) 表示每秒25個畫面格，1表示每秒30個畫面格 (nondropped) 。</span><span class="sxs-lookup"><span data-stu-id="f1bae-111">Zero (0) indicates 25 frames per second while 1 indicates 30 frames per second (nondropped).</span></span> <span data-ttu-id="f1bae-112">值為2表示無法判斷播放時間。</span><span class="sxs-lookup"><span data-stu-id="f1bae-112">A value of 2 indicates the playback time cannot be determined.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1bae-113">備註</span><span class="sxs-lookup"><span data-stu-id="f1bae-113">Remarks</span></span>

<span data-ttu-id="f1bae-114">只有簡單的線性電影會發出此事件的信號。</span><span class="sxs-lookup"><span data-stu-id="f1bae-114">Only simple linear movies signal this event.</span></span>

<span data-ttu-id="f1bae-115">此事件會在標題網域中引發。</span><span class="sxs-lookup"><span data-stu-id="f1bae-115">This event is raised in the title domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1bae-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1bae-116">Requirements</span></span>



| <span data-ttu-id="f1bae-117">需求</span><span class="sxs-lookup"><span data-stu-id="f1bae-117">Requirement</span></span> | <span data-ttu-id="f1bae-118">值</span><span class="sxs-lookup"><span data-stu-id="f1bae-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1bae-119">標頭</span><span class="sxs-lookup"><span data-stu-id="f1bae-119">Header</span></span><br/> | <dl> <span data-ttu-id="f1bae-120"><dt>Dvdevcode (包含 Dshow) </dt></span><span class="sxs-lookup"><span data-stu-id="f1bae-120"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1bae-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1bae-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1bae-122">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="f1bae-122">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="f1bae-123">DVD 事件通知碼</span><span class="sxs-lookup"><span data-stu-id="f1bae-123">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="f1bae-124">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="f1bae-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




