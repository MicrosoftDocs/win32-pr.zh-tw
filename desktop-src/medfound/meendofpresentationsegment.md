---
description: 當區段已完成，且後面接著另一個區段時，由 sequencer 來源引發。 當最後一個區段完成時，sequencer 來源會引發 MEEndOfPresentation 事件。
ms.assetid: 1be13c9a-d454-4642-b26b-556f2461b705
title: 'MEEndOfPresentationSegment 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d3608f51f3ff66e21261cc40d1f8cf690c92c4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848542"
---
# <a name="meendofpresentationsegment-event"></a><span data-ttu-id="28a88-104">MEEndOfPresentationSegment 事件</span><span class="sxs-lookup"><span data-stu-id="28a88-104">MEEndOfPresentationSegment event</span></span>

<span data-ttu-id="28a88-105">當區段已完成，且後面接著另一個區段時，由 sequencer 來源引發。</span><span class="sxs-lookup"><span data-stu-id="28a88-105">Raised by the sequencer source when a segment is completed and is followed by another segment.</span></span> <span data-ttu-id="28a88-106">當最後一個區段完成時，sequencer 來源會引發 [MEEndOfPresentation](meendofpresentation.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="28a88-106">When the final segment is completed, the sequencer source raises an [MEEndOfPresentation](meendofpresentation.md) event.</span></span>

<span data-ttu-id="28a88-107">媒體會話將此事件轉送到應用程式。</span><span class="sxs-lookup"><span data-stu-id="28a88-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="28a88-108">事件值</span><span class="sxs-lookup"><span data-stu-id="28a88-108">Event values</span></span>

<span data-ttu-id="28a88-109">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="28a88-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="28a88-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="28a88-110">VARTYPE</span></span>              | <span data-ttu-id="28a88-111">Description</span><span class="sxs-lookup"><span data-stu-id="28a88-111">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="28a88-112">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="28a88-112">VT\_EMPTY</span></span><br/> | <span data-ttu-id="28a88-113">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="28a88-113">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="28a88-114">屬性</span><span class="sxs-lookup"><span data-stu-id="28a88-114">Attributes</span></span>

<span data-ttu-id="28a88-115">此事件會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="28a88-115">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="28a88-116">屬性</span><span class="sxs-lookup"><span data-stu-id="28a88-116">Attribute</span></span>                                                                                               | <span data-ttu-id="28a88-117">描述</span><span class="sxs-lookup"><span data-stu-id="28a88-117">Description</span></span>                                                                          |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="28a88-118">**\_已取消 MF 事件 \_ 來源 \_ 拓撲 \_**</span><span class="sxs-lookup"><span data-stu-id="28a88-118">**MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED**</span></span>](mf-event-source-topology-canceled-attribute.md)<br/> | <span data-ttu-id="28a88-119">指定 sequencer 來源是否取消此區段。</span><span class="sxs-lookup"><span data-stu-id="28a88-119">Specifies whether the sequencer source canceled this segment.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="28a88-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="28a88-120">Requirements</span></span>



| <span data-ttu-id="28a88-121">需求</span><span class="sxs-lookup"><span data-stu-id="28a88-121">Requirement</span></span> | <span data-ttu-id="28a88-122">值</span><span class="sxs-lookup"><span data-stu-id="28a88-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28a88-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="28a88-123">Minimum supported client</span></span><br/> | <span data-ttu-id="28a88-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="28a88-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="28a88-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="28a88-125">Minimum supported server</span></span><br/> | <span data-ttu-id="28a88-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="28a88-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="28a88-127">標頭</span><span class="sxs-lookup"><span data-stu-id="28a88-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="28a88-128"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="28a88-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28a88-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28a88-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28a88-130">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="28a88-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="28a88-131">關於 Sequencer 來源</span><span class="sxs-lookup"><span data-stu-id="28a88-131">About the Sequencer Source</span></span>](about-the-sequencer-source.md)
</dt> <dt>

[<span data-ttu-id="28a88-132">Sequencer 來源事件</span><span class="sxs-lookup"><span data-stu-id="28a88-132">Sequencer Source Events</span></span>](sequencer-source-events.md)
</dt> </dl>

 

 




