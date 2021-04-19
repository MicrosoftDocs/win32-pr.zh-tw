---
description: 當下游格式變成失效且必須重新協商時，由資料流程接收器傳送。
ms.assetid: 732B3BDD-F394-430F-B895-AF18ED61114D
title: 'MEStreamSinkFormatInvalidated 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39c4453c0d5720ffb57f1277946f9cf891ed443
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970638"
---
# <a name="mestreamsinkformatinvalidated-event"></a><span data-ttu-id="f31f4-103">MEStreamSinkFormatInvalidated 事件</span><span class="sxs-lookup"><span data-stu-id="f31f4-103">MEStreamSinkFormatInvalidated event</span></span>

<span data-ttu-id="f31f4-104">當下游格式變成失效且必須重新協商時，由資料流程接收器傳送。</span><span class="sxs-lookup"><span data-stu-id="f31f4-104">Sent by a stream sink when the downstream format has become invalidated and it needs to be renegotiated.</span></span>

## <a name="event-values"></a><span data-ttu-id="f31f4-105">事件值</span><span class="sxs-lookup"><span data-stu-id="f31f4-105">Event values</span></span>

<span data-ttu-id="f31f4-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="f31f4-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="f31f4-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="f31f4-107">VARTYPE</span></span>              | <span data-ttu-id="f31f4-108">Description</span><span class="sxs-lookup"><span data-stu-id="f31f4-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="f31f4-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="f31f4-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="f31f4-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="f31f4-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="f31f4-111">備註</span><span class="sxs-lookup"><span data-stu-id="f31f4-111">Remarks</span></span>

<span data-ttu-id="f31f4-112">若資料已排入目前播放位置之前的接收，則應該重新傳送。</span><span class="sxs-lookup"><span data-stu-id="f31f4-112">Data that was queued to the sink, past the current playback position, should be resent.</span></span>

## <a name="requirements"></a><span data-ttu-id="f31f4-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="f31f4-113">Requirements</span></span>



| <span data-ttu-id="f31f4-114">需求</span><span class="sxs-lookup"><span data-stu-id="f31f4-114">Requirement</span></span> | <span data-ttu-id="f31f4-115">值</span><span class="sxs-lookup"><span data-stu-id="f31f4-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f31f4-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f31f4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f31f4-117">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f31f4-117">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                                      |
| <span data-ttu-id="f31f4-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f31f4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f31f4-119">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f31f4-119">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                                           |
| <span data-ttu-id="f31f4-120">標頭</span><span class="sxs-lookup"><span data-stu-id="f31f4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f31f4-121"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="f31f4-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f31f4-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f31f4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f31f4-123">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="f31f4-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




