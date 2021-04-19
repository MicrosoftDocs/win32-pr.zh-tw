---
description: 已開始新的區段。
ms.assetid: 9742436a-e233-4641-a0d5-aa240cde5f28
title: 'EC_SEGMENT_STARTED (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7e7df85bddb78fe2687a017b481e6db62ba37c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991549"
---
# <a name="ec_segment_started"></a><span data-ttu-id="b4c51-103">\_ \_ 已開始 EC 區段</span><span class="sxs-lookup"><span data-stu-id="b4c51-103">EC\_SEGMENT\_STARTED</span></span>

<span data-ttu-id="b4c51-104">已開始新的區段。</span><span class="sxs-lookup"><span data-stu-id="b4c51-104">A new segment has started.</span></span>

## <a name="parameters"></a><span data-ttu-id="b4c51-105">參數</span><span class="sxs-lookup"><span data-stu-id="b4c51-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4c51-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="b4c51-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="b4c51-107"> (**常\數\*\*\**參考 \_ 時間** \*) **參考 \_ 時間** 值的指標，此值會指定自區段開始以來累積的資料流程時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="b4c51-107">(**const** **REFERENCE\_TIME**\*) Pointer to a **REFERENCE\_TIME** value that specifies the accumulated stream time since the start of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="b4c51-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="b4c51-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="b4c51-109"> (**DWORD**) 區段號碼 (以零為基礎的) 。</span><span class="sxs-lookup"><span data-stu-id="b4c51-109">(**DWORD**) Segment number (zero-based).</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="b4c51-110">預設動作</span><span class="sxs-lookup"><span data-stu-id="b4c51-110">Default Action</span></span>

<span data-ttu-id="b4c51-111">此事件不會傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="b4c51-111">This event is not sent to the application.</span></span> <span data-ttu-id="b4c51-112">應用程式無法覆寫此事件的預設動作。</span><span class="sxs-lookup"><span data-stu-id="b4c51-112">Applications cannot override the default action for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4c51-113">備註</span><span class="sxs-lookup"><span data-stu-id="b4c51-113">Remarks</span></span>

<span data-ttu-id="b4c51-114">如果篩選準則會在區段結尾傳送 [**EC \_ 結尾 \_ 的 \_ 區段**](ec-end-of-segment.md) ，則會在區段的開頭傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="b4c51-114">If a filter will send an [**EC\_END\_OF\_SEGMENT**](ec-end-of-segment.md) at the end of a segment, it sends this event at the start of the segment.</span></span> <span data-ttu-id="b4c51-115">篩選圖形管理員會使用此事件通知來計算在 \_ \_ \_ 區段結束時應預期的 EC 區段通知數目。</span><span class="sxs-lookup"><span data-stu-id="b4c51-115">The filter graph manager uses this event notification to compute how many EC\_END\_OF\_SEGMENT notifications it should expect at the end of the segment.</span></span>

<span data-ttu-id="b4c51-116">根據預設，篩選不會在區段結尾傳送 $ [**\_ end \_ 的 \_ 區段**](ec-end-of-segment.md) 事件，因此不應該傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="b4c51-116">By default, filters do not send [**EC\_END\_OF\_SEGMENT**](ec-end-of-segment.md) events at the end of segments, and therefore should not send this event.</span></span> <span data-ttu-id="b4c51-117">如需詳細資訊，請參閱 [**IMediaSeeking：： SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions)。</span><span class="sxs-lookup"><span data-stu-id="b4c51-117">For more information, see [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4c51-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="b4c51-118">Requirements</span></span>



| <span data-ttu-id="b4c51-119">需求</span><span class="sxs-lookup"><span data-stu-id="b4c51-119">Requirement</span></span> | <span data-ttu-id="b4c51-120">值</span><span class="sxs-lookup"><span data-stu-id="b4c51-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b4c51-121">標頭</span><span class="sxs-lookup"><span data-stu-id="b4c51-121">Header</span></span><br/> | <dl> <span data-ttu-id="b4c51-122"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="b4c51-122"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4c51-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b4c51-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4c51-124">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="b4c51-124">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="b4c51-125">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="b4c51-125">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




