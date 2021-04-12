---
description: 從呈現媒體資料的媒體接收器發出事件的信號。
ms.assetid: bb7db7c9-c39f-4bf4-9412-42525c4f2ea3
title: 'MERendererEvent 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c52e15bfbe97743e8af10a79cf3ef1d94626a877
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191910"
---
# <a name="merendererevent-event"></a><span data-ttu-id="c6d0f-103">MERendererEvent 事件</span><span class="sxs-lookup"><span data-stu-id="c6d0f-103">MERendererEvent event</span></span>

<span data-ttu-id="c6d0f-104">從呈現媒體資料的媒體接收器發出事件的信號。</span><span class="sxs-lookup"><span data-stu-id="c6d0f-104">Signals an event from a media sink that renders media data.</span></span>

<span data-ttu-id="c6d0f-105">[增強型影片](enhanced-video-renderer.md)轉譯器 (EVR) 會在收到來自 EVR 展示者的使用者事件時傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="c6d0f-105">The [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) sends this event when it receives a user event from the EVR presenter.</span></span>

## <a name="event-values"></a><span data-ttu-id="c6d0f-106">事件值</span><span class="sxs-lookup"><span data-stu-id="c6d0f-106">Event values</span></span>

<span data-ttu-id="c6d0f-107">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="c6d0f-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="c6d0f-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c6d0f-108">VARTYPE</span></span>           | <span data-ttu-id="c6d0f-109">Description</span><span class="sxs-lookup"><span data-stu-id="c6d0f-109">Description</span></span>                        |
|-------------------|------------------------------------|
| <span data-ttu-id="c6d0f-110">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="c6d0f-110">VT\_I4</span></span><br/> | <span data-ttu-id="c6d0f-111">事件代碼。</span><span class="sxs-lookup"><span data-stu-id="c6d0f-111">Event code.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="c6d0f-112">備註</span><span class="sxs-lookup"><span data-stu-id="c6d0f-112">Remarks</span></span>

<span data-ttu-id="c6d0f-113">如果展示者以 EC 使用者或更高範圍的事件代碼來呼叫 EVR 的 **IMediaEventSink：： Notify** 方法 \_ ，則 EVR 會傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="c6d0f-113">If the presenter calls the EVR's **IMediaEventSink::Notify** method with an event code in the range EC\_USER or higher, the EVR sends this event.</span></span> <span data-ttu-id="c6d0f-114">事件資料是傳遞給 **通知** 方法的事件程式碼。</span><span class="sxs-lookup"><span data-stu-id="c6d0f-114">The event data is the event code that was passed to the **Notify** method.</span></span>

<span data-ttu-id="c6d0f-115">*EventParam1* 和 *EventParam2* 在 **IMediaEventSink：： Notify**) 方法中 (的原始事件參數會被忽略，因此展示者應該將這些值設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c6d0f-115">The original event parameters (*EventParam1* and *EventParam2* in the **IMediaEventSink::Notify** method) are ignored, so the presenter should set these values to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6d0f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6d0f-116">Requirements</span></span>



| <span data-ttu-id="c6d0f-117">需求</span><span class="sxs-lookup"><span data-stu-id="c6d0f-117">Requirement</span></span> | <span data-ttu-id="c6d0f-118">值</span><span class="sxs-lookup"><span data-stu-id="c6d0f-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6d0f-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c6d0f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c6d0f-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6d0f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c6d0f-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c6d0f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c6d0f-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6d0f-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c6d0f-123">標頭</span><span class="sxs-lookup"><span data-stu-id="c6d0f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6d0f-124"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="c6d0f-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6d0f-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6d0f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6d0f-126">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="c6d0f-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




