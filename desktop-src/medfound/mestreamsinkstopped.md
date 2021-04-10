---
description: 當資料流程接收完成轉換至已停止狀態時引發。 在接收呈現時鐘上呼叫 IMFPresentationClock Stop 方法時，會發生轉換為已停止。
ms.assetid: 1a8c7faa-4d4a-4458-ad08-a760a15dc347
title: 'MEStreamSinkStopped 事件 (Mfobjects) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e35313ab3d43c950184a82e403fa6ad0eb5b4ab4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027068"
---
# <a name="mestreamsinkstopped-event"></a><span data-ttu-id="3de7b-104">MEStreamSinkStopped 事件</span><span class="sxs-lookup"><span data-stu-id="3de7b-104">MEStreamSinkStopped event</span></span>

<span data-ttu-id="3de7b-105">當資料流程接收完成轉換至已停止狀態時引發。</span><span class="sxs-lookup"><span data-stu-id="3de7b-105">Raised by a stream sink when it completes the transition to the stopped state.</span></span> <span data-ttu-id="3de7b-106">當對接收器的呈現時鐘呼叫 [**IMFPresentationClock：： Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-stop) 方法時，就會發生轉換為已停止。</span><span class="sxs-lookup"><span data-stu-id="3de7b-106">The transition to stopped occurs when the [**IMFPresentationClock::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-stop) method is called on the sink's presentation clock.</span></span>

## <a name="event-values"></a><span data-ttu-id="3de7b-107">事件值</span><span class="sxs-lookup"><span data-stu-id="3de7b-107">Event values</span></span>

<span data-ttu-id="3de7b-108">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="3de7b-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="3de7b-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="3de7b-109">VARTYPE</span></span>              | <span data-ttu-id="3de7b-110">Description</span><span class="sxs-lookup"><span data-stu-id="3de7b-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="3de7b-111">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="3de7b-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="3de7b-112">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="3de7b-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="3de7b-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="3de7b-113">Requirements</span></span>



| <span data-ttu-id="3de7b-114">需求</span><span class="sxs-lookup"><span data-stu-id="3de7b-114">Requirement</span></span> | <span data-ttu-id="3de7b-115">值</span><span class="sxs-lookup"><span data-stu-id="3de7b-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3de7b-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3de7b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3de7b-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3de7b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3de7b-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3de7b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3de7b-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3de7b-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3de7b-120">標頭</span><span class="sxs-lookup"><span data-stu-id="3de7b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3de7b-121"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="3de7b-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3de7b-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3de7b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3de7b-123">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="3de7b-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="3de7b-124">媒體接收器</span><span class="sxs-lookup"><span data-stu-id="3de7b-124">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




