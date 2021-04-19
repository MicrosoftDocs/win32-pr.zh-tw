---
description: 表示媒體資料流程沒有可在指定時間提供資料的信號。
ms.assetid: 1a00fff1-c3ab-4965-a663-3c15bb48ea98
title: 'MEStreamTick 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27123569e991043a534883964ba94e4955d60a40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967165"
---
# <a name="mestreamtick-event"></a><span data-ttu-id="50fdb-103">MEStreamTick 事件</span><span class="sxs-lookup"><span data-stu-id="50fdb-103">MEStreamTick event</span></span>

<span data-ttu-id="50fdb-104">表示媒體資料流程沒有可在指定時間提供資料的信號。</span><span class="sxs-lookup"><span data-stu-id="50fdb-104">Signals that a media stream does not have data available at a specified time.</span></span>

## <a name="event-values"></a><span data-ttu-id="50fdb-105">事件值</span><span class="sxs-lookup"><span data-stu-id="50fdb-105">Event values</span></span>

<span data-ttu-id="50fdb-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="50fdb-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="50fdb-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="50fdb-107">VARTYPE</span></span>           | <span data-ttu-id="50fdb-108">Description</span><span class="sxs-lookup"><span data-stu-id="50fdb-108">Description</span></span>                                                                   |
|-------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="50fdb-109">VT \_ I8</span><span class="sxs-lookup"><span data-stu-id="50fdb-109">VT\_I8</span></span><br/> | <span data-ttu-id="50fdb-110">間隔發生的時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="50fdb-110">Time at which the gap occurs, in 100-nanosecond units.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="50fdb-111">備註</span><span class="sxs-lookup"><span data-stu-id="50fdb-111">Remarks</span></span>

<span data-ttu-id="50fdb-112">此事件表示資料中有間距。</span><span class="sxs-lookup"><span data-stu-id="50fdb-112">This event signals a gap in the data.</span></span> <span data-ttu-id="50fdb-113">事件會通知下游元件在指定時間不會預期任何資料。</span><span class="sxs-lookup"><span data-stu-id="50fdb-113">The event notifies downstream components not to expect any data at the specified time.</span></span>

<span data-ttu-id="50fdb-114">當物件產生串流中媒體範例的時間戳記時，應傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="50fdb-114">The event should be sent by whichever object generates the time stamps for the media samples in the stream.</span></span> <span data-ttu-id="50fdb-115">根據資料的格式而定，這可能是：</span><span class="sxs-lookup"><span data-stu-id="50fdb-115">Depending on the format of the data, this is either:</span></span>

-   <span data-ttu-id="50fdb-116">媒體來源上的媒體串流 ([**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) 介面) ，或</span><span class="sxs-lookup"><span data-stu-id="50fdb-116">The media stream on the media source ([**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) interface), or</span></span>
-   <span data-ttu-id="50fdb-117"> ([**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面) 的解碼器轉換。</span><span class="sxs-lookup"><span data-stu-id="50fdb-117">The decoder transform ([**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface).</span></span>

<span data-ttu-id="50fdb-118">在這段時間內，物件應該傳送的事件與通常會產生範例的頻率相同。</span><span class="sxs-lookup"><span data-stu-id="50fdb-118">During the gap, the object should send the event about as often as it would normally produce samples.</span></span> <span data-ttu-id="50fdb-119">針對影片，針對每個遺漏的框架傳送一個事件。</span><span class="sxs-lookup"><span data-stu-id="50fdb-119">For video, send one event for each missing frame.</span></span> <span data-ttu-id="50fdb-120">針對音訊，在間距期間每秒至少傳送一次事件。</span><span class="sxs-lookup"><span data-stu-id="50fdb-120">For audio, send the event at least once per second during the gap.</span></span> <span data-ttu-id="50fdb-121">事件的值為遺漏範例的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="50fdb-121">The value of the event is the time stamp of the missing sample.</span></span> <span data-ttu-id="50fdb-122">視需要傳送任意數量的 MEStreamTick 事件以填滿資料中的間距。</span><span class="sxs-lookup"><span data-stu-id="50fdb-122">Send as many MEStreamTick events as needed to fill the gap in the data.</span></span>

<span data-ttu-id="50fdb-123">如果媒體來源有多個資料流程，而且有一個以上的資料流程有間距，則每個資料流程都應該傳送 MEStreamTick 事件。</span><span class="sxs-lookup"><span data-stu-id="50fdb-123">If a media source has several streams and there is a gap in more than one stream, each stream should send MEStreamTick events.</span></span> <span data-ttu-id="50fdb-124">例如，如果音訊和影片資料中有間距，則這兩個數據流都會傳送事件。</span><span class="sxs-lookup"><span data-stu-id="50fdb-124">For example, if there is a gap in both audio and video data, then both streams send the event.</span></span>

<span data-ttu-id="50fdb-125">MEStreamTick 事件未完成 [**IMFMediaStream：： RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) 要求。</span><span class="sxs-lookup"><span data-stu-id="50fdb-125">The MEStreamTick event does not complete an [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) request.</span></span> <span data-ttu-id="50fdb-126">媒體來源仍然必須針對每個 **RequestSample** 呼叫傳送 [MEMediaSample](memediasample.md)事件。</span><span class="sxs-lookup"><span data-stu-id="50fdb-126">The media source must still send an [MEMediaSample](memediasample.md) event for each call to **RequestSample**.</span></span>

<span data-ttu-id="50fdb-127">媒體接收無法直接使用此事件。</span><span class="sxs-lookup"><span data-stu-id="50fdb-127">Media sinks cannot consume this event directly.</span></span> <span data-ttu-id="50fdb-128">若要對媒體接收器發出資料流程中的間隙，請使用 **MFSTREAMSINK \_ 標記 \_ 刻度** 標記來呼叫 [**IMFStreamSink：:P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) 。</span><span class="sxs-lookup"><span data-stu-id="50fdb-128">To signal a gap in the stream to a media sink, call [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) with an **MFSTREAMSINK\_MARKER\_TICK** marker.</span></span> <span data-ttu-id="50fdb-129">媒體基礎管線會在需要時，將 MEStreamTick 事件轉換成 **MFSTREAMSINK \_ 標記 \_ 刻度** 標記。</span><span class="sxs-lookup"><span data-stu-id="50fdb-129">The Media Foundation pipeline converts MEStreamTick events to **MFSTREAMSINK\_MARKER\_TICK** markers when needed.</span></span>

<span data-ttu-id="50fdb-130">請勿在 MEStreamTick 事件之後的下一個媒體範例中，設定 MFSampleExtension 不中斷屬性。 [**\_**](mfsampleextension-discontinuity-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="50fdb-130">Do not set the [**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute on the next media sample after an MEStreamTick event.</span></span> <span data-ttu-id="50fdb-131">**MFSampleExtension 中斷 \_** 屬性工作表示時間戳記與先前的時間戳記不連續，而 MEStreamTick 表示時間戳記是連續的，但遺漏了部分資料。</span><span class="sxs-lookup"><span data-stu-id="50fdb-131">The **MFSampleExtension\_Discontinuity** attribute implies that the time stamp is discontinuous with previous time stamps, whereas MEStreamTick implies that time stamps are continuous but some data is missing.</span></span>

> [!Note]  
> <span data-ttu-id="50fdb-132">較早版本的檔不正確地指出 MEStreamTick 事件之後的範例應該有 MFSampleExtension 不 [**連續 \_**](mfsampleextension-discontinuity-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="50fdb-132">An earlier version of the documentation incorrectly stated that the sample after an MEStreamTick event should have the [**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="50fdb-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="50fdb-133">Requirements</span></span>



| <span data-ttu-id="50fdb-134">需求</span><span class="sxs-lookup"><span data-stu-id="50fdb-134">Requirement</span></span> | <span data-ttu-id="50fdb-135">值</span><span class="sxs-lookup"><span data-stu-id="50fdb-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50fdb-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="50fdb-136">Minimum supported client</span></span><br/> | <span data-ttu-id="50fdb-137">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50fdb-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="50fdb-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="50fdb-138">Minimum supported server</span></span><br/> | <span data-ttu-id="50fdb-139">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50fdb-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="50fdb-140">標頭</span><span class="sxs-lookup"><span data-stu-id="50fdb-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="50fdb-141"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="50fdb-141"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50fdb-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50fdb-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50fdb-143">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="50fdb-143">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




