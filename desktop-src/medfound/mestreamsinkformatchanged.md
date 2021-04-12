---
description: 當接收媒體類型不再有效時，由資料流程接收器引發。
ms.assetid: 9eeb4262-1593-4c5f-9341-ebd328b586e7
title: 'MEStreamSinkFormatChanged 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e04c62072f69425079753ef4d0a56edcf8d65d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191902"
---
# <a name="mestreamsinkformatchanged-event"></a><span data-ttu-id="7a336-103">MEStreamSinkFormatChanged 事件</span><span class="sxs-lookup"><span data-stu-id="7a336-103">MEStreamSinkFormatChanged event</span></span>

<span data-ttu-id="7a336-104">當接收的媒體類型不再有效時，由資料流程接收器引發。</span><span class="sxs-lookup"><span data-stu-id="7a336-104">Raised by a stream sink when the sink's media type is no longer valid.</span></span>

## <a name="event-values"></a><span data-ttu-id="7a336-105">事件值</span><span class="sxs-lookup"><span data-stu-id="7a336-105">Event values</span></span>

<span data-ttu-id="7a336-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="7a336-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="7a336-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="7a336-107">VARTYPE</span></span>              | <span data-ttu-id="7a336-108">Description</span><span class="sxs-lookup"><span data-stu-id="7a336-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="7a336-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="7a336-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="7a336-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="7a336-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="7a336-111">備註</span><span class="sxs-lookup"><span data-stu-id="7a336-111">Remarks</span></span>

<span data-ttu-id="7a336-112">即使發生會使資料流程接收的媒體類型失效的情況，資料流程接收也可以引發此問題。</span><span class="sxs-lookup"><span data-stu-id="7a336-112">A stream sink can raise this even if something happens that invalidates the stream sink's media type.</span></span> <span data-ttu-id="7a336-113">例如，增強型影片轉譯器 (EVR) 會在顯示變更時傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="7a336-113">For example, the enhanced video renderer (EVR) sends this event when the display changes.</span></span>

<span data-ttu-id="7a336-114">[**IMFMediaEvent：： GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus)所抓取的 **HRESULT** 值可能指出媒體類型不再有效的原因。</span><span class="sxs-lookup"><span data-stu-id="7a336-114">The **HRESULT** value retrieved by [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) might indicate why the media type is no longer valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a336-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a336-115">Requirements</span></span>



| <span data-ttu-id="7a336-116">需求</span><span class="sxs-lookup"><span data-stu-id="7a336-116">Requirement</span></span> | <span data-ttu-id="7a336-117">值</span><span class="sxs-lookup"><span data-stu-id="7a336-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a336-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7a336-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7a336-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7a336-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7a336-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7a336-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7a336-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7a336-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7a336-122">標頭</span><span class="sxs-lookup"><span data-stu-id="7a336-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a336-123"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="7a336-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a336-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7a336-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a336-125">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="7a336-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="7a336-126">媒體接收器</span><span class="sxs-lookup"><span data-stu-id="7a336-126">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




