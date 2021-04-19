---
description: 到達區段的結尾。
ms.assetid: 07f141b1-2e96-49e2-9cf7-581690e245b5
title: 'EC_END_OF_SEGMENT (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a779b0f46a031ad694bd3fed3fe29536424a3a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983029"
---
# <a name="ec_end_of_segment"></a><span data-ttu-id="b2331-103">EC \_ 結尾 \_ 的 \_ 區段</span><span class="sxs-lookup"><span data-stu-id="b2331-103">EC\_END\_OF\_SEGMENT</span></span>

<span data-ttu-id="b2331-104">到達區段的結尾。</span><span class="sxs-lookup"><span data-stu-id="b2331-104">The end of a segment was reached.</span></span>

## <a name="parameters"></a><span data-ttu-id="b2331-105">參數</span><span class="sxs-lookup"><span data-stu-id="b2331-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2331-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="b2331-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="b2331-107"> (**常\數\*\*\**參考 \_ 時間** \*) **參考 \_ 時間** 值的指標，此值會指定自區段開始以來累積的資料流程時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="b2331-107">(**const** **REFERENCE\_TIME**\*) Pointer to a **REFERENCE\_TIME** value that specifies the accumulated stream time since the start of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="b2331-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="b2331-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="b2331-109"> (**DWORD**) 區段號碼 (以零為基礎的) 。</span><span class="sxs-lookup"><span data-stu-id="b2331-109">(**DWORD**) Segment number (zero-based).</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="b2331-110">預設動作</span><span class="sxs-lookup"><span data-stu-id="b2331-110">Default Action</span></span>

<span data-ttu-id="b2331-111">篩選圖形管理員會根據 [**ec \_ 區段 \_ 開始**](ec-segment-started.md)事件的數目，來檢查 **\_ \_ \_ 區段事件的 EC 結束** 次數。</span><span class="sxs-lookup"><span data-stu-id="b2331-111">The filter graph manager checks the number of **EC\_END\_OF\_SEGMENT** events against the number of [**EC\_SEGMENT\_STARTED**](ec-segment-started.md) events.</span></span> <span data-ttu-id="b2331-112">如果兩者相符，就會將 [ **EC] \_ \_ \_ 區段** 事件轉送到應用程式。</span><span class="sxs-lookup"><span data-stu-id="b2331-112">If they match, it forwards the **EC\_END\_OF\_SEGMENT** event to the application.</span></span> <span data-ttu-id="b2331-113">應用程式無法覆寫此事件的預設動作。</span><span class="sxs-lookup"><span data-stu-id="b2331-113">Applications cannot override the default action for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2331-114">備註</span><span class="sxs-lookup"><span data-stu-id="b2331-114">Remarks</span></span>

<span data-ttu-id="b2331-115">此事件程式碼支援無縫迴圈。</span><span class="sxs-lookup"><span data-stu-id="b2331-115">This event code supports seamless looping.</span></span> <span data-ttu-id="b2331-116">當呼叫 [**IMediaSeeking：： SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) 方法包含 AM \_ 搜尋區段旗標時 \_ ，來源篩選會傳送此事件程式碼，而不是呼叫 [**IPin：： EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)。</span><span class="sxs-lookup"><span data-stu-id="b2331-116">When a call to the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method includes the AM\_SEEKING\_Segment flag, the source filter sends this event code instead of calling [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream).</span></span>

## <a name="requirements"></a><span data-ttu-id="b2331-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2331-117">Requirements</span></span>



| <span data-ttu-id="b2331-118">需求</span><span class="sxs-lookup"><span data-stu-id="b2331-118">Requirement</span></span> | <span data-ttu-id="b2331-119">值</span><span class="sxs-lookup"><span data-stu-id="b2331-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b2331-120">標頭</span><span class="sxs-lookup"><span data-stu-id="b2331-120">Header</span></span><br/> | <dl> <span data-ttu-id="b2331-121"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="b2331-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2331-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2331-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2331-123">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="b2331-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="b2331-124">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="b2331-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




