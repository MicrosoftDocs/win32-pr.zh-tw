---
description: 當媒體會話完成清除要求時引發。
ms.assetid: 1ae97022-3fb2-4c5e-9262-d5bdc2a62bee
title: 'MESessionScrubSampleComplete 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b076c2f2978831cc30521fcf49d71c04620c4dee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848537"
---
# <a name="mesessionscrubsamplecomplete-event"></a><span data-ttu-id="7fcda-103">MESessionScrubSampleComplete 事件</span><span class="sxs-lookup"><span data-stu-id="7fcda-103">MESessionScrubSampleComplete event</span></span>

<span data-ttu-id="7fcda-104">當媒體會話完成清除要求時引發。</span><span class="sxs-lookup"><span data-stu-id="7fcda-104">Raised by the Media Session when it completes a scrubbing request.</span></span>

<span data-ttu-id="7fcda-105">當播放速率為零時，應用程式呼叫 [**IMFMediaSession：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)時，就會進行清除。</span><span class="sxs-lookup"><span data-stu-id="7fcda-105">Scrubbing occurs when the playback rate is zero and the application calls [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span> <span data-ttu-id="7fcda-106">每個資料流程接收完成清除要求之後，就會引發此事件。</span><span class="sxs-lookup"><span data-stu-id="7fcda-106">This event is raised after every stream sink has completed the scrubbing request.</span></span>

## <a name="event-values"></a><span data-ttu-id="7fcda-107">事件值</span><span class="sxs-lookup"><span data-stu-id="7fcda-107">Event values</span></span>

<span data-ttu-id="7fcda-108">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="7fcda-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="7fcda-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="7fcda-109">VARTYPE</span></span>              | <span data-ttu-id="7fcda-110">Description</span><span class="sxs-lookup"><span data-stu-id="7fcda-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="7fcda-111">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="7fcda-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="7fcda-112">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="7fcda-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="7fcda-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="7fcda-113">Requirements</span></span>



| <span data-ttu-id="7fcda-114">需求</span><span class="sxs-lookup"><span data-stu-id="7fcda-114">Requirement</span></span> | <span data-ttu-id="7fcda-115">值</span><span class="sxs-lookup"><span data-stu-id="7fcda-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fcda-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7fcda-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7fcda-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7fcda-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7fcda-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7fcda-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7fcda-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7fcda-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7fcda-120">標頭</span><span class="sxs-lookup"><span data-stu-id="7fcda-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fcda-121"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="7fcda-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fcda-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7fcda-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fcda-123">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="7fcda-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="7fcda-124">MEStreamSinkScrubSampleComplete</span><span class="sxs-lookup"><span data-stu-id="7fcda-124">MEStreamSinkScrubSampleComplete</span></span>](mestreamsinkscrubsamplecomplete.md)
</dt> </dl>

 

 




