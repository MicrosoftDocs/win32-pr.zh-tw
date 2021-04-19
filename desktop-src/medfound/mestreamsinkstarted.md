---
description: 當資料流程接收完成轉換到執行中狀態時引發。
ms.assetid: 95ac658b-bec0-442d-85ef-61966b40a2f2
title: 'MEStreamSinkStarted 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 407ab885da04746034b7126a8d9bb9389d2928f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978867"
---
# <a name="mestreamsinkstarted-event"></a><span data-ttu-id="5b460-103">MEStreamSinkStarted 事件</span><span class="sxs-lookup"><span data-stu-id="5b460-103">MEStreamSinkStarted event</span></span>

<span data-ttu-id="5b460-104">當資料流程接收完成轉換到執行中狀態時引發。</span><span class="sxs-lookup"><span data-stu-id="5b460-104">Raised by a stream sink when it completes the transition to the running state.</span></span> <span data-ttu-id="5b460-105">當針對接收器的簡報時鐘呼叫 [**IMFPresentationClock：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start) 方法時，會發生轉換成正在執行。</span><span class="sxs-lookup"><span data-stu-id="5b460-105">The transition to running occurs when the [**IMFPresentationClock::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start) method is called on the sink's presentation clock.</span></span> <span data-ttu-id="5b460-106">媒體接收器會透過其 [**IMFClockStateSink：： OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) 或 [**IMFClockStateSink：： OnClockRestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) 方法收到通知。</span><span class="sxs-lookup"><span data-stu-id="5b460-106">The media sink receives the notification through its [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) or [**IMFClockStateSink::OnClockRestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) method.</span></span>

## <a name="event-values"></a><span data-ttu-id="5b460-107">事件值</span><span class="sxs-lookup"><span data-stu-id="5b460-107">Event values</span></span>

<span data-ttu-id="5b460-108">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="5b460-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="5b460-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5b460-109">VARTYPE</span></span>              | <span data-ttu-id="5b460-110">Description</span><span class="sxs-lookup"><span data-stu-id="5b460-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="5b460-111">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="5b460-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="5b460-112">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="5b460-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="5b460-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b460-113">Requirements</span></span>



| <span data-ttu-id="5b460-114">需求</span><span class="sxs-lookup"><span data-stu-id="5b460-114">Requirement</span></span> | <span data-ttu-id="5b460-115">值</span><span class="sxs-lookup"><span data-stu-id="5b460-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b460-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5b460-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5b460-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b460-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5b460-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5b460-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5b460-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b460-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5b460-120">標頭</span><span class="sxs-lookup"><span data-stu-id="5b460-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b460-121"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="5b460-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b460-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b460-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b460-123">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="5b460-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="5b460-124">媒體接收器</span><span class="sxs-lookup"><span data-stu-id="5b460-124">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




