---
description: 提供對品質管制員有關播放品質的意見反應。
ms.assetid: 1b4b6a2d-411e-42d1-a44b-bb1928e1c063
title: 'MEQualityNotify 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d8f486bfebfd137ba341176af0fdad257776df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512841"
---
# <a name="mequalitynotify-event"></a><span data-ttu-id="f122b-103">MEQualityNotify 事件</span><span class="sxs-lookup"><span data-stu-id="f122b-103">MEQualityNotify event</span></span>

<span data-ttu-id="f122b-104">提供對品質管制員有關播放品質的意見反應。</span><span class="sxs-lookup"><span data-stu-id="f122b-104">Provides feedback to the quality manager about playback quality.</span></span>

## <a name="event-values"></a><span data-ttu-id="f122b-105">事件值</span><span class="sxs-lookup"><span data-stu-id="f122b-105">Event values</span></span>

<span data-ttu-id="f122b-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="f122b-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="f122b-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="f122b-107">VARTYPE</span></span>           | <span data-ttu-id="f122b-108">Description</span><span class="sxs-lookup"><span data-stu-id="f122b-108">Description</span></span>                         |
|-------------------|-------------------------------------|
| <span data-ttu-id="f122b-109">VT \_ I8</span><span class="sxs-lookup"><span data-stu-id="f122b-109">VT\_I8</span></span><br/> | <span data-ttu-id="f122b-110">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="f122b-110">See Remarks.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="f122b-111">備註</span><span class="sxs-lookup"><span data-stu-id="f122b-111">Remarks</span></span>

<span data-ttu-id="f122b-112">某些管線元件會引發此事件。</span><span class="sxs-lookup"><span data-stu-id="f122b-112">This event is raised by some pipeline components.</span></span> <span data-ttu-id="f122b-113">媒體會話藉由呼叫 [**IMFQualityManager：： NotifyQualityEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyqualityevent) 方法，將事件轉寄給品質管制員。</span><span class="sxs-lookup"><span data-stu-id="f122b-113">The Media Session forwards the event to the quality manager by calling the [**IMFQualityManager::NotifyQualityEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyqualityevent) method.</span></span>

<span data-ttu-id="f122b-114">事件的擴充類型表示事件資料的意義。</span><span class="sxs-lookup"><span data-stu-id="f122b-114">The event's extended type indicates the meaning of the event data.</span></span>



| <span data-ttu-id="f122b-115">擴充類型</span><span class="sxs-lookup"><span data-stu-id="f122b-115">Extended type</span></span>                            | <span data-ttu-id="f122b-116">事件資料</span><span class="sxs-lookup"><span data-stu-id="f122b-116">Event data</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f122b-117">MF \_ 品質 \_ 通知 \_ 處理 \_ 延遲</span><span class="sxs-lookup"><span data-stu-id="f122b-117">MF\_QUALITY\_NOTIFY\_PROCESSING\_LATENCY</span></span> | <span data-ttu-id="f122b-118">元件所引進的大約處理延遲（100-毫微秒單位）。</span><span class="sxs-lookup"><span data-stu-id="f122b-118">Approximate processing latency introduced by the component, in 100-nanosecond units.</span></span><br/> <span data-ttu-id="f122b-119">處理延遲是元件透過處理範例導入管線中的延遲量。</span><span class="sxs-lookup"><span data-stu-id="f122b-119">Processing latency is the amount of latency that a component introduces into the pipeline by processing a sample.</span></span> <span data-ttu-id="f122b-120">在某些情況下，只需查看 [**IMFQualityManager：： NotifyProcessInput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput) 和 [**IMFQualityManager：： NotifyProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput)的呼叫，就無法衍生延遲。</span><span class="sxs-lookup"><span data-stu-id="f122b-120">In some cases, the latency cannot be derived simply by looking at the calls to [**IMFQualityManager::NotifyProcessInput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput) and [**IMFQualityManager::NotifyProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput).</span></span> <span data-ttu-id="f122b-121">例如，輸入範例和輸出範例之間可能不會有一對一的對應關係。</span><span class="sxs-lookup"><span data-stu-id="f122b-121">For example, there may not be a one-to-one correspondence between input samples and output samples.</span></span> <span data-ttu-id="f122b-122">在此情況下，元件可能會傳送具有處理延遲的 MEQualityNotify 事件。</span><span class="sxs-lookup"><span data-stu-id="f122b-122">In this case, the component might send an MEQualityNotify event with the processing latency.</span></span> <span data-ttu-id="f122b-123">如果處理延遲變更，元件可以在串流期間隨時傳送新的事件。</span><span class="sxs-lookup"><span data-stu-id="f122b-123">If the processing latency changes, the component can send a new event at any time during streaming.</span></span><br/> |
| <span data-ttu-id="f122b-124">MF \_ 品質 \_ 通知 \_ 範例 \_ 延遲</span><span class="sxs-lookup"><span data-stu-id="f122b-124">MF\_QUALITY\_NOTIFY\_SAMPLE\_LAG</span></span>         | <span data-ttu-id="f122b-125">範例的延遲時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="f122b-125">Lag time for the sample, in 100-nanosecond units.</span></span> <span data-ttu-id="f122b-126">如果值為正數，則表示此範例為晚期。</span><span class="sxs-lookup"><span data-stu-id="f122b-126">If the value is positive, the sample was late.</span></span> <span data-ttu-id="f122b-127">如果值為負數，則會提早範例。</span><span class="sxs-lookup"><span data-stu-id="f122b-127">If the value is negative, the sample was early.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="f122b-128">若要取得延伸型別，請呼叫 [**IMFMediaEvent：： GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype)。</span><span class="sxs-lookup"><span data-stu-id="f122b-128">To get the extended type, call [**IMFMediaEvent::GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype).</span></span>

<span data-ttu-id="f122b-129">傳送此事件時不需要管線元件。</span><span class="sxs-lookup"><span data-stu-id="f122b-129">Pipeline components are not required to send this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="f122b-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="f122b-130">Requirements</span></span>



| <span data-ttu-id="f122b-131">需求</span><span class="sxs-lookup"><span data-stu-id="f122b-131">Requirement</span></span> | <span data-ttu-id="f122b-132">值</span><span class="sxs-lookup"><span data-stu-id="f122b-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f122b-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f122b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f122b-134">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f122b-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f122b-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f122b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f122b-136">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f122b-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f122b-137">標頭</span><span class="sxs-lookup"><span data-stu-id="f122b-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f122b-138"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="f122b-138"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f122b-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f122b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f122b-140">**IMFQualityManager**</span><span class="sxs-lookup"><span data-stu-id="f122b-140">**IMFQualityManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)
</dt> <dt>

[<span data-ttu-id="f122b-141">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="f122b-141">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




