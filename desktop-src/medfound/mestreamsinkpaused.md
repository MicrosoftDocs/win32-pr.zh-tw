---
description: 當資料流程接收完成轉換為暫停狀態時引發。
ms.assetid: 84ab62fc-1525-433c-8af5-70659122703c
title: 'MEStreamSinkPaused 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17016285f2b88a1fc266b79f5eee45fea31f824c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984983"
---
# <a name="mestreamsinkpaused-event"></a><span data-ttu-id="0b57d-103">MEStreamSinkPaused 事件</span><span class="sxs-lookup"><span data-stu-id="0b57d-103">MEStreamSinkPaused event</span></span>

<span data-ttu-id="0b57d-104">當資料流程接收完成轉換為暫停狀態時引發。</span><span class="sxs-lookup"><span data-stu-id="0b57d-104">Raised by a stream sink when it completes the transition to the paused state.</span></span> <span data-ttu-id="0b57d-105">當呼叫 [**IMFPresentationClock：:P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-pause) 方法時，會在接收器的簡報時鐘上進行轉換。</span><span class="sxs-lookup"><span data-stu-id="0b57d-105">The transition to paused occurs when the [**IMFPresentationClock::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-pause) method is called on the sink's presentation clock.</span></span>

## <a name="event-values"></a><span data-ttu-id="0b57d-106">事件值</span><span class="sxs-lookup"><span data-stu-id="0b57d-106">Event values</span></span>

<span data-ttu-id="0b57d-107">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="0b57d-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="0b57d-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0b57d-108">VARTYPE</span></span>              | <span data-ttu-id="0b57d-109">Description</span><span class="sxs-lookup"><span data-stu-id="0b57d-109">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="0b57d-110">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="0b57d-110">VT\_EMPTY</span></span><br/> | <span data-ttu-id="0b57d-111">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="0b57d-111">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="0b57d-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b57d-112">Requirements</span></span>



| <span data-ttu-id="0b57d-113">需求</span><span class="sxs-lookup"><span data-stu-id="0b57d-113">Requirement</span></span> | <span data-ttu-id="0b57d-114">值</span><span class="sxs-lookup"><span data-stu-id="0b57d-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b57d-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0b57d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0b57d-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0b57d-116">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0b57d-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0b57d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0b57d-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0b57d-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0b57d-119">標頭</span><span class="sxs-lookup"><span data-stu-id="0b57d-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b57d-120"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="0b57d-120"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b57d-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0b57d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b57d-122">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="0b57d-122">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="0b57d-123">媒體接收器</span><span class="sxs-lookup"><span data-stu-id="0b57d-123">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




