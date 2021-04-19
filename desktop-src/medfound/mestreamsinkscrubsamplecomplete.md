---
description: 當資料流程接收完成清除要求時引發。
ms.assetid: 451c7e09-868e-4c05-b970-d222b97223f2
title: 'MEStreamSinkScrubSampleComplete 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81f29d478635d5a9ba7e7c5356c49ebd8da216f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983880"
---
# <a name="mestreamsinkscrubsamplecomplete-event"></a><span data-ttu-id="4c22b-103">MEStreamSinkScrubSampleComplete 事件</span><span class="sxs-lookup"><span data-stu-id="4c22b-103">MEStreamSinkScrubSampleComplete event</span></span>

<span data-ttu-id="4c22b-104">當資料流程接收完成清除要求時引發。</span><span class="sxs-lookup"><span data-stu-id="4c22b-104">Raised by a stream sink when it completes a scrubbing request.</span></span>

<span data-ttu-id="4c22b-105">當播放速率為零，且表示時鐘以指定的 srubbing 時間啟動時，就會進行清除。</span><span class="sxs-lookup"><span data-stu-id="4c22b-105">Scrubbing occurs when the playback rate is zero and the presentation clock is started with a specified srubbing time.</span></span> <span data-ttu-id="4c22b-106">如果媒體接收器支援清除，則每當呼叫 [**IMFClockStateSink：： OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) 方法，而播放速率為零時，每個資料流程上的每個資料流程都會引發此事件。</span><span class="sxs-lookup"><span data-stu-id="4c22b-106">If a media sink supports scrubbing, every stream on the sink raises this event whenever the [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) method is called while the playback rate is zero.</span></span>

<span data-ttu-id="4c22b-107">如果串流在清除時轉譯資料，它會在資料轉譯時立即傳送事件。</span><span class="sxs-lookup"><span data-stu-id="4c22b-107">If the stream renders data while scrubbing, it sends the event as soon as the data is rendered.</span></span> <span data-ttu-id="4c22b-108">如果資料流程未轉譯資料，它會在呼叫 [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) 之後立即傳送事件。</span><span class="sxs-lookup"><span data-stu-id="4c22b-108">If the stream does not render data, it sends the event immediately after [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) is called.</span></span>

## <a name="event-values"></a><span data-ttu-id="4c22b-109">事件值</span><span class="sxs-lookup"><span data-stu-id="4c22b-109">Event values</span></span>

<span data-ttu-id="4c22b-110">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="4c22b-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="4c22b-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="4c22b-111">VARTYPE</span></span>              | <span data-ttu-id="4c22b-112">Description</span><span class="sxs-lookup"><span data-stu-id="4c22b-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="4c22b-113">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="4c22b-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="4c22b-114">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="4c22b-114">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="4c22b-115">屬性</span><span class="sxs-lookup"><span data-stu-id="4c22b-115">Attributes</span></span>

<span data-ttu-id="4c22b-116">此事件會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="4c22b-116">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="4c22b-117">屬性</span><span class="sxs-lookup"><span data-stu-id="4c22b-117">Attribute</span></span>                                                                              | <span data-ttu-id="4c22b-118">描述</span><span class="sxs-lookup"><span data-stu-id="4c22b-118">Description</span></span>                                                                                                                                                   |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4c22b-119">**MF \_ 事件 \_ SCRUBSAMPLE \_ 時間**</span><span class="sxs-lookup"><span data-stu-id="4c22b-119">**MF\_EVENT\_SCRUBSAMPLE\_TIME**</span></span>](mf-event-scrubsample-time-attribute.md)<br/> | <span data-ttu-id="4c22b-120">轉譯資料的呈現時間。</span><span class="sxs-lookup"><span data-stu-id="4c22b-120">Presentation time for which data was rendered.</span></span> <span data-ttu-id="4c22b-121">如果媒體接收器未在清除時轉譯資料，則不會設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="4c22b-121">If the media sink does not render data while scrubbing, it does not set this attribute.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="4c22b-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c22b-122">Requirements</span></span>



| <span data-ttu-id="4c22b-123">需求</span><span class="sxs-lookup"><span data-stu-id="4c22b-123">Requirement</span></span> | <span data-ttu-id="4c22b-124">值</span><span class="sxs-lookup"><span data-stu-id="4c22b-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c22b-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4c22b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4c22b-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c22b-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4c22b-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4c22b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4c22b-128">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c22b-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4c22b-129">標頭</span><span class="sxs-lookup"><span data-stu-id="4c22b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c22b-130"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="4c22b-130"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c22b-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c22b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c22b-132">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="4c22b-132">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="4c22b-133">媒體接收器</span><span class="sxs-lookup"><span data-stu-id="4c22b-133">Media Sinks</span></span>](media-sinks.md)
</dt> <dt>

[<span data-ttu-id="4c22b-134">MESessionScrubSampleComplete</span><span class="sxs-lookup"><span data-stu-id="4c22b-134">MESessionScrubSampleComplete</span></span>](mesessionscrubsamplecomplete.md)
</dt> </dl>

 

 




