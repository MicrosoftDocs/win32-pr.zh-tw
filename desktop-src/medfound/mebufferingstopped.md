---
description: 表示媒體來源已停止緩衝處理資料。
ms.assetid: 11b1290d-d462-4aa0-a358-b3f6447c99d8
title: 'MEBufferingStopped 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e996ec160f57ec598196b388170741705adb9a8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318696"
---
# <a name="mebufferingstopped-event"></a><span data-ttu-id="88375-103">MEBufferingStopped 事件</span><span class="sxs-lookup"><span data-stu-id="88375-103">MEBufferingStopped event</span></span>

<span data-ttu-id="88375-104">表示媒體來源已停止緩衝處理資料。</span><span class="sxs-lookup"><span data-stu-id="88375-104">Signals that a media source has stopped buffering data.</span></span>

<span data-ttu-id="88375-105">媒體來源會在傳送 [MEBufferingStarted](mebufferingstarted.md) 事件之後停止緩衝資料時傳送。</span><span class="sxs-lookup"><span data-stu-id="88375-105">A media source sends this when it stops buffering data after sending the [MEBufferingStarted](mebufferingstarted.md) event.</span></span>

<span data-ttu-id="88375-106">執行 [**IMFByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) 介面的位元組資料流程也會傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="88375-106">Byte streams that implement the [**IMFByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) interface also send this event.</span></span>

## <a name="event-values"></a><span data-ttu-id="88375-107">事件值</span><span class="sxs-lookup"><span data-stu-id="88375-107">Event values</span></span>

<span data-ttu-id="88375-108">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="88375-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="88375-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="88375-109">VARTYPE</span></span>              | <span data-ttu-id="88375-110">Description</span><span class="sxs-lookup"><span data-stu-id="88375-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="88375-111">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="88375-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="88375-112">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="88375-112">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="88375-113">備註</span><span class="sxs-lookup"><span data-stu-id="88375-113">Remarks</span></span>

<span data-ttu-id="88375-114">當媒體會話收到此事件時，它會重新開機表示時鐘。</span><span class="sxs-lookup"><span data-stu-id="88375-114">When the Media Session receives this event, it restarts the presentation clock.</span></span> <span data-ttu-id="88375-115">媒體會話也會將事件轉送到應用程式。</span><span class="sxs-lookup"><span data-stu-id="88375-115">The Media Session also forwards the event to the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="88375-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="88375-116">Requirements</span></span>



| <span data-ttu-id="88375-117">需求</span><span class="sxs-lookup"><span data-stu-id="88375-117">Requirement</span></span> | <span data-ttu-id="88375-118">值</span><span class="sxs-lookup"><span data-stu-id="88375-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88375-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="88375-119">Minimum supported client</span></span><br/> | <span data-ttu-id="88375-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="88375-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="88375-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="88375-121">Minimum supported server</span></span><br/> | <span data-ttu-id="88375-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="88375-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="88375-123">標頭</span><span class="sxs-lookup"><span data-stu-id="88375-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="88375-124"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="88375-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88375-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88375-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88375-126">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="88375-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




