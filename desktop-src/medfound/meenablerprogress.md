---
description: 通知內容啟用物件的進度。 公開 IMFContentEnabler 介面的物件可以引發這個事件，以通知應用程式有關內容執行程式執行動作的進度。
ms.assetid: ec14ba9b-cfb6-4e32-870e-2436e11c308b
title: 'MEEnablerProgress 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58303835113408a7fe09436967286d5ff988acdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191915"
---
# <a name="meenablerprogress-event"></a><span data-ttu-id="08039-104">MEEnablerProgress 事件</span><span class="sxs-lookup"><span data-stu-id="08039-104">MEEnablerProgress event</span></span>

<span data-ttu-id="08039-105">通知內容啟用物件的進度。</span><span class="sxs-lookup"><span data-stu-id="08039-105">Signals the progress of a content enabler object.</span></span> <span data-ttu-id="08039-106">公開 [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) 介面的物件可能會引發此事件，以通知應用程式有關內容啟用程式動作的進度。</span><span class="sxs-lookup"><span data-stu-id="08039-106">Objects that expose the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface can raise this event to notify the application about the progress of the content enabler's actions.</span></span>

## <a name="event-values"></a><span data-ttu-id="08039-107">事件值</span><span class="sxs-lookup"><span data-stu-id="08039-107">Event values</span></span>

<span data-ttu-id="08039-108">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="08039-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="08039-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="08039-109">VARTYPE</span></span>               | <span data-ttu-id="08039-110">Description</span><span class="sxs-lookup"><span data-stu-id="08039-110">Description</span></span>                                                               |
|-----------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="08039-111">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="08039-111">VT\_LPWSTR</span></span><br/> | <span data-ttu-id="08039-112">描述進度的寬字元字串。</span><span class="sxs-lookup"><span data-stu-id="08039-112">Wide-character string that describes the progress.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="08039-113">備註</span><span class="sxs-lookup"><span data-stu-id="08039-113">Remarks</span></span>

<span data-ttu-id="08039-114">若要接收此事件，請查詢 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)介面的 [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)介面。</span><span class="sxs-lookup"><span data-stu-id="08039-114">To receive this event, query the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface for the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="08039-115">然後呼叫 [**IMFMediaEventGenerator：： BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent)，如「 [媒體事件](media-event-generators.md)產生器」主題所述。</span><span class="sxs-lookup"><span data-stu-id="08039-115">Then call [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), as described in the topic [Media Event Generators](media-event-generators.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="08039-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="08039-116">Requirements</span></span>



| <span data-ttu-id="08039-117">需求</span><span class="sxs-lookup"><span data-stu-id="08039-117">Requirement</span></span> | <span data-ttu-id="08039-118">值</span><span class="sxs-lookup"><span data-stu-id="08039-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08039-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="08039-119">Minimum supported client</span></span><br/> | <span data-ttu-id="08039-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="08039-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="08039-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="08039-121">Minimum supported server</span></span><br/> | <span data-ttu-id="08039-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="08039-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="08039-123">標頭</span><span class="sxs-lookup"><span data-stu-id="08039-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="08039-124"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="08039-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08039-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08039-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08039-126">**IMFContentEnabler**</span><span class="sxs-lookup"><span data-stu-id="08039-126">**IMFContentEnabler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[<span data-ttu-id="08039-127">媒體事件產生器</span><span class="sxs-lookup"><span data-stu-id="08039-127">Media Event Generators</span></span>](media-event-generators.md)
</dt> <dt>

[<span data-ttu-id="08039-128">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="08039-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




