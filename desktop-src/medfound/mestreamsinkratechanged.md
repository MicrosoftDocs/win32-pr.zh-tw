---
description: 當速率變更時由資料流程接收器引發。
ms.assetid: c61c71de-fd3c-429b-a29f-f9d2bbfcb531
title: 'MEStreamSinkRateChanged 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a26adbdb64ffd5af0896d8aebe0cef474bee9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975366"
---
# <a name="mestreamsinkratechanged-event"></a><span data-ttu-id="cdff3-103">MEStreamSinkRateChanged 事件</span><span class="sxs-lookup"><span data-stu-id="cdff3-103">MEStreamSinkRateChanged event</span></span>

<span data-ttu-id="cdff3-104">當速率變更時由資料流程接收器引發。</span><span class="sxs-lookup"><span data-stu-id="cdff3-104">Raised by a stream sink when the rate has changed.</span></span>

## <a name="event-values"></a><span data-ttu-id="cdff3-105">事件值</span><span class="sxs-lookup"><span data-stu-id="cdff3-105">Event values</span></span>

<span data-ttu-id="cdff3-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="cdff3-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="cdff3-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cdff3-107">VARTYPE</span></span>              | <span data-ttu-id="cdff3-108">Description</span><span class="sxs-lookup"><span data-stu-id="cdff3-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="cdff3-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="cdff3-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="cdff3-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="cdff3-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="cdff3-111">備註</span><span class="sxs-lookup"><span data-stu-id="cdff3-111">Remarks</span></span>

<span data-ttu-id="cdff3-112">如果串流接收支援速率變更，它會在速率變更完成後傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="cdff3-112">If a stream sink supports rate changes, it sends this event after the rate change is complete.</span></span> <span data-ttu-id="cdff3-113">每次呼叫接收器的 [**IMFClockStateSink：： OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) 方法時，就會傳送一次此事件。</span><span class="sxs-lookup"><span data-stu-id="cdff3-113">The event is sent once for each call to the sink's [**IMFClockStateSink::OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) method.</span></span> <span data-ttu-id="cdff3-114">如果速率變更失敗，則事件狀態值為錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="cdff3-114">If the rate change is not successful, the event status value is an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdff3-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="cdff3-115">Requirements</span></span>



| <span data-ttu-id="cdff3-116">需求</span><span class="sxs-lookup"><span data-stu-id="cdff3-116">Requirement</span></span> | <span data-ttu-id="cdff3-117">值</span><span class="sxs-lookup"><span data-stu-id="cdff3-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdff3-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cdff3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cdff3-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cdff3-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cdff3-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cdff3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cdff3-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cdff3-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cdff3-122">標頭</span><span class="sxs-lookup"><span data-stu-id="cdff3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdff3-123"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="cdff3-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdff3-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cdff3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdff3-125">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="cdff3-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="cdff3-126">媒體接收器</span><span class="sxs-lookup"><span data-stu-id="cdff3-126">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




