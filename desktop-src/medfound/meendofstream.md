---
description: 當資料流程結束時由媒體資料流程引發。
ms.assetid: e793131a-f737-411f-a9fc-03b5b3d09aea
title: 'MEEndOfStream 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eb70af021c1a35af829df9b3c80c0c2b71aa120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848541"
---
# <a name="meendofstream-event"></a><span data-ttu-id="ae9ab-103">MEEndOfStream 事件</span><span class="sxs-lookup"><span data-stu-id="ae9ab-103">MEEndOfStream event</span></span>

<span data-ttu-id="ae9ab-104">當資料流程結束時由媒體資料流程引發。</span><span class="sxs-lookup"><span data-stu-id="ae9ab-104">Raised by a media stream when the stream ends.</span></span>

## <a name="event-values"></a><span data-ttu-id="ae9ab-105">事件值</span><span class="sxs-lookup"><span data-stu-id="ae9ab-105">Event values</span></span>

<span data-ttu-id="ae9ab-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="ae9ab-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="ae9ab-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ae9ab-107">VARTYPE</span></span>              | <span data-ttu-id="ae9ab-108">Description</span><span class="sxs-lookup"><span data-stu-id="ae9ab-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="ae9ab-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="ae9ab-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="ae9ab-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="ae9ab-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="ae9ab-111">備註</span><span class="sxs-lookup"><span data-stu-id="ae9ab-111">Remarks</span></span>

<span data-ttu-id="ae9ab-112">當 [媒體會話](media-session.md) 收到 MEEndOfStream 事件時，它會在對應的媒體接收上呼叫 [**IMFStreamSink：:P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) ，並以 **MFSTREAMSINK \_ 標記 \_ ENDOFSEGMENT** 標記類型來呼叫。</span><span class="sxs-lookup"><span data-stu-id="ae9ab-112">When the [Media Session](media-session.md) receives the MEEndOfStream event, it calls [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) on the corresponding media sink, with the **MFSTREAMSINK\_MARKER\_ENDOFSEGMENT** marker type.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae9ab-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae9ab-113">Requirements</span></span>



| <span data-ttu-id="ae9ab-114">需求</span><span class="sxs-lookup"><span data-stu-id="ae9ab-114">Requirement</span></span> | <span data-ttu-id="ae9ab-115">值</span><span class="sxs-lookup"><span data-stu-id="ae9ab-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae9ab-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ae9ab-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ae9ab-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae9ab-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ae9ab-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ae9ab-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ae9ab-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae9ab-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ae9ab-120">標頭</span><span class="sxs-lookup"><span data-stu-id="ae9ab-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae9ab-121"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="ae9ab-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae9ab-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ae9ab-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae9ab-123">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="ae9ab-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




