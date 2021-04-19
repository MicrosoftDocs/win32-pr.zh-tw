---
description: 當新的簡報開始時，由媒體會話引發。 此事件表示簡報開始的時間，以及呈現時間與來源時間之間的位移。
ms.assetid: 67c7d5f3-ffaf-4359-a59c-bb26b992b6cd
title: 'MESessionNotifyPresentationTime 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7b0cd8811d98094ab58ddcf844ec73e1470d120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993041"
---
# <a name="mesessionnotifypresentationtime-event"></a><span data-ttu-id="a1d01-104">MESessionNotifyPresentationTime 事件</span><span class="sxs-lookup"><span data-stu-id="a1d01-104">MESessionNotifyPresentationTime event</span></span>

<span data-ttu-id="a1d01-105">當新的簡報開始時，由媒體會話引發。</span><span class="sxs-lookup"><span data-stu-id="a1d01-105">Raised by the Media Session when a new presentation starts.</span></span> <span data-ttu-id="a1d01-106">此事件表示簡報開始的時間，以及呈現時間與來源時間之間的位移。</span><span class="sxs-lookup"><span data-stu-id="a1d01-106">This event indicates when the presentation will start and the offset between the presentation time and the source time.</span></span>

## <a name="event-values"></a><span data-ttu-id="a1d01-107">事件值</span><span class="sxs-lookup"><span data-stu-id="a1d01-107">Event values</span></span>

<span data-ttu-id="a1d01-108">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="a1d01-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="a1d01-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="a1d01-109">VARTYPE</span></span>              | <span data-ttu-id="a1d01-110">Description</span><span class="sxs-lookup"><span data-stu-id="a1d01-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="a1d01-111">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="a1d01-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="a1d01-112">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="a1d01-112">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="a1d01-113">屬性</span><span class="sxs-lookup"><span data-stu-id="a1d01-113">Attributes</span></span>

<span data-ttu-id="a1d01-114">此事件會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="a1d01-114">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="a1d01-115">屬性</span><span class="sxs-lookup"><span data-stu-id="a1d01-115">Attribute</span></span>                                                                                                                   | <span data-ttu-id="a1d01-116">描述</span><span class="sxs-lookup"><span data-stu-id="a1d01-116">Description</span></span>                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a1d01-117">**MF \_ 事件 \_ 開始 \_ 簡報 \_ 時間**</span><span class="sxs-lookup"><span data-stu-id="a1d01-117">**MF\_EVENT\_START\_PRESENTATION\_TIME**</span></span>](mf-event-start-presentation-time-attribute.md)<br/>                       | <span data-ttu-id="a1d01-118">簡報的開始時間。</span><span class="sxs-lookup"><span data-stu-id="a1d01-118">Starting time for the presentation.</span></span><br/> <br/>                                                      |
| [<span data-ttu-id="a1d01-119">**MF \_ 事件 \_ 呈現 \_ 時間 \_ 位移**</span><span class="sxs-lookup"><span data-stu-id="a1d01-119">**MF\_EVENT\_PRESENTATION\_TIME\_OFFSET**</span></span>](mf-event-presentation-time-offset-attribute.md)<br/>                     | <span data-ttu-id="a1d01-120">呈現時間與媒體來源時間戳記之間的位移。</span><span class="sxs-lookup"><span data-stu-id="a1d01-120">Offset between the presentation time and the media source's time stamps.</span></span><br/> <br/>                 |
| [<span data-ttu-id="a1d01-121">**MF \_ 事件 \_ \_ \_ \_ 在輸出時開始展示時間 \_**</span><span class="sxs-lookup"><span data-stu-id="a1d01-121">**MF\_EVENT\_START\_PRESENTATION\_TIME\_AT\_OUTPUT**</span></span>](mf-event-start-presentation-time-at-output-attribute.md)<br/> | <span data-ttu-id="a1d01-122">當媒體接收器轉譯新拓撲的第一個範例時的呈現時間。</span><span class="sxs-lookup"><span data-stu-id="a1d01-122">Presentation time when the media sinks will render the first sample of the new topology.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="a1d01-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1d01-123">Requirements</span></span>



| <span data-ttu-id="a1d01-124">需求</span><span class="sxs-lookup"><span data-stu-id="a1d01-124">Requirement</span></span> | <span data-ttu-id="a1d01-125">值</span><span class="sxs-lookup"><span data-stu-id="a1d01-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1d01-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a1d01-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a1d01-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a1d01-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a1d01-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a1d01-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a1d01-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a1d01-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a1d01-130">標頭</span><span class="sxs-lookup"><span data-stu-id="a1d01-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1d01-131"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="a1d01-131"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1d01-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1d01-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1d01-133">**IMFMediaSession**</span><span class="sxs-lookup"><span data-stu-id="a1d01-133">**IMFMediaSession**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
</dt> <dt>

[<span data-ttu-id="a1d01-134">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="a1d01-134">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




