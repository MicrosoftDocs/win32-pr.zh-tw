---
description: 媒體來源啟動但未搜尋時引發。
ms.assetid: a52d8ee1-cb46-487d-a744-fca6db7c2353
title: 'MESourceStarted 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c17ba7898a8bf33df4a3508afee9b7c0c9bc81c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512836"
---
# <a name="mesourcestarted-event"></a><span data-ttu-id="f022f-103">MESourceStarted 事件</span><span class="sxs-lookup"><span data-stu-id="f022f-103">MESourceStarted event</span></span>

<span data-ttu-id="f022f-104">媒體來源啟動但未搜尋時引發。</span><span class="sxs-lookup"><span data-stu-id="f022f-104">Raised when a media source starts without seeking.</span></span>

## <a name="event-values"></a><span data-ttu-id="f022f-105">事件值</span><span class="sxs-lookup"><span data-stu-id="f022f-105">Event values</span></span>

<span data-ttu-id="f022f-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="f022f-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="f022f-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="f022f-107">VARTYPE</span></span>              | <span data-ttu-id="f022f-108">Description</span><span class="sxs-lookup"><span data-stu-id="f022f-108">Description</span></span>                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f022f-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="f022f-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="f022f-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="f022f-110">No event data.</span></span> <span data-ttu-id="f022f-111">開始時間是從目前的位置開始。</span><span class="sxs-lookup"><span data-stu-id="f022f-111">The start time was from the current position.</span></span><br/> <br/>                            |
| <span data-ttu-id="f022f-112">VT \_ I8</span><span class="sxs-lookup"><span data-stu-id="f022f-112">VT\_I8</span></span><br/>    | <span data-ttu-id="f022f-113">相對於樣本上時間戳記的開始時間，以 100-毫微秒單位為單位。</span><span class="sxs-lookup"><span data-stu-id="f022f-113">The starting time, in 100-nanosecond units, relative to the time stamps on the samples.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="f022f-114">屬性</span><span class="sxs-lookup"><span data-stu-id="f022f-114">Attributes</span></span>

<span data-ttu-id="f022f-115">此事件會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="f022f-115">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="f022f-116">屬性</span><span class="sxs-lookup"><span data-stu-id="f022f-116">Attribute</span></span>                                                                                     | <span data-ttu-id="f022f-117">描述</span><span class="sxs-lookup"><span data-stu-id="f022f-117">Description</span></span>                                                                                                                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f022f-118">**MF \_ 事件 \_ 來源 \_ 實際 \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="f022f-118">**MF\_EVENT\_SOURCE\_ACTUAL\_START**</span></span>](mf-event-source-actual-start-attribute.md)<br/> | <span data-ttu-id="f022f-119">開始時間。</span><span class="sxs-lookup"><span data-stu-id="f022f-119">Start time.</span></span> <span data-ttu-id="f022f-120">媒體來源會設定這個屬性（如果它目前的位置重新開機的話）。</span><span class="sxs-lookup"><span data-stu-id="f022f-120">The media source sets this attribute if it restarts from its current position.</span></span><br/> <br/>                     |
| [<span data-ttu-id="f022f-121">**MF \_ 事件 \_ 來源 \_ 假 \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="f022f-121">**MF\_EVENT\_SOURCE\_FAKE\_START**</span></span>](mf-event-source-fake-start-attribute.md)<br/>     | <span data-ttu-id="f022f-122">指定目前區段拓撲是否為空白。</span><span class="sxs-lookup"><span data-stu-id="f022f-122">Specifies whether the current segment topology is empty.</span></span> <span data-ttu-id="f022f-123">Sequencer 來源會設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="f022f-123">The sequencer source sets this attribute.</span></span><br/> <br/>             |
| [<span data-ttu-id="f022f-124">**MF \_ 事件 \_ 來源 \_ PROJECTSTART**</span><span class="sxs-lookup"><span data-stu-id="f022f-124">**MF\_EVENT\_SOURCE\_PROJECTSTART**</span></span>](mf-event-source-projectstart-attribute.md)<br/>  | <span data-ttu-id="f022f-125">區段的開始時間，相對於簡報的開始時間。</span><span class="sxs-lookup"><span data-stu-id="f022f-125">Start time for a segment, relative to the start of the presentation.</span></span> <span data-ttu-id="f022f-126">Sequencer 來源會設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="f022f-126">The sequencer source sets this attribute.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="f022f-127">備註</span><span class="sxs-lookup"><span data-stu-id="f022f-127">Remarks</span></span>

<span data-ttu-id="f022f-128">當媒體來源從停止狀態開始，或從來源中相同位置的暫停狀態開始時，就會引發此事件。</span><span class="sxs-lookup"><span data-stu-id="f022f-128">A media source raises this event when it starts from a stopped state, or starts from a paused state at the same position in the source.</span></span> <span data-ttu-id="f022f-129">如果 [**IMFMediaSource：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) 方法傳回 S OK，就會引發事件 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f022f-129">The event is raised if the [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method returns S\_OK.</span></span>

<span data-ttu-id="f022f-130">如果媒體來源從目前位置開始，且來源的先前狀態為 [執行中] 或 [已暫停]，則事件資料可以空白 (VT \_ 空白) 。</span><span class="sxs-lookup"><span data-stu-id="f022f-130">If the media source starts from the current position and the source's previous state was running or paused, the event data can empty (VT\_EMPTY).</span></span> <span data-ttu-id="f022f-131">如果事件資料是 VT \_ 空白，則媒體來源可能會以實際的開始時間設定 [**MF \_ 事件 \_ 來源 \_ 實際 \_ 開始**](mf-event-source-actual-start-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="f022f-131">If the event data is VT\_EMPTY, the media source might set the [**MF\_EVENT\_SOURCE\_ACTUAL\_START**](mf-event-source-actual-start-attribute.md) attribute with the actual starting time.</span></span>

<span data-ttu-id="f022f-132">如果媒體來源從新位置開始，或來源的先前狀態為 [已停止]，則事件資料必須是 (VT I8) 的開始時間 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f022f-132">If the media source starts from a new position, or the source's previous state was stopped, the event data must be the starting time (VT\_I8).</span></span>

<span data-ttu-id="f022f-133">如果 [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) 方法導致搜尋，媒體來源會傳送 [MESourceSeeked](mesourceseeked.md) 事件，而不是 MESourceStarted。</span><span class="sxs-lookup"><span data-stu-id="f022f-133">If the [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method causes a seek, the media source sends the [MESourceSeeked](mesourceseeked.md) event instead of MESourceStarted.</span></span>

## <a name="requirements"></a><span data-ttu-id="f022f-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="f022f-134">Requirements</span></span>



| <span data-ttu-id="f022f-135">需求</span><span class="sxs-lookup"><span data-stu-id="f022f-135">Requirement</span></span> | <span data-ttu-id="f022f-136">值</span><span class="sxs-lookup"><span data-stu-id="f022f-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f022f-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f022f-137">Minimum supported client</span></span><br/> | <span data-ttu-id="f022f-138">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f022f-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f022f-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f022f-139">Minimum supported server</span></span><br/> | <span data-ttu-id="f022f-140">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f022f-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f022f-141">標頭</span><span class="sxs-lookup"><span data-stu-id="f022f-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="f022f-142"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="f022f-142"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f022f-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f022f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f022f-144">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="f022f-144">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




