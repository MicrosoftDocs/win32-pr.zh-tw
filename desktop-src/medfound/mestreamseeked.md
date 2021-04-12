---
description: 在呼叫 IMFMediaSource：： Start 之後由媒體資料流程引發，會在資料流程中進行搜尋。 當媒體來源引發 MESourceSeeked 事件時，媒體資料流程會引發此事件。
ms.assetid: df06df16-711d-4262-b049-fb29f25934de
title: 'MEStreamSeeked 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7b66e2176b08c04b01fc487aac4b8218536b615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191903"
---
# <a name="mestreamseeked-event"></a><span data-ttu-id="cba52-104">MEStreamSeeked 事件</span><span class="sxs-lookup"><span data-stu-id="cba52-104">MEStreamSeeked event</span></span>

<span data-ttu-id="cba52-105">在呼叫 [**IMFMediaSource：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) 之後由媒體資料流程引發，會在資料流程中進行搜尋。</span><span class="sxs-lookup"><span data-stu-id="cba52-105">Raised by a media stream after a call to [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) causes a seek in the stream.</span></span> <span data-ttu-id="cba52-106">當媒體來源引發 [MESourceSeeked](mesourceseeked.md) 事件時，媒體資料流程會引發此事件。</span><span class="sxs-lookup"><span data-stu-id="cba52-106">A media stream raises this event when the media source raises the [MESourceSeeked](mesourceseeked.md) event.</span></span>

## <a name="event-values"></a><span data-ttu-id="cba52-107">事件值</span><span class="sxs-lookup"><span data-stu-id="cba52-107">Event values</span></span>

<span data-ttu-id="cba52-108">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="cba52-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="cba52-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cba52-109">VARTYPE</span></span>           | <span data-ttu-id="cba52-110">Description</span><span class="sxs-lookup"><span data-stu-id="cba52-110">Description</span></span>                                                        |
|-------------------|--------------------------------------------------------------------|
| <span data-ttu-id="cba52-111">VT \_ I8</span><span class="sxs-lookup"><span data-stu-id="cba52-111">VT\_I8</span></span><br/> | <span data-ttu-id="cba52-112">新的開始時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="cba52-112">New starting time, in 100-nanosecond units.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="cba52-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="cba52-113">Requirements</span></span>



| <span data-ttu-id="cba52-114">需求</span><span class="sxs-lookup"><span data-stu-id="cba52-114">Requirement</span></span> | <span data-ttu-id="cba52-115">值</span><span class="sxs-lookup"><span data-stu-id="cba52-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cba52-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cba52-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cba52-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cba52-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cba52-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cba52-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cba52-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cba52-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cba52-120">標頭</span><span class="sxs-lookup"><span data-stu-id="cba52-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="cba52-121"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="cba52-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cba52-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cba52-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cba52-123">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="cba52-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




