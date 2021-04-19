---
description: 在簡報結束時由媒體來源引發。 此事件表示簡報中的所有串流都已完成。 媒體會話將此事件轉送到應用程式。
ms.assetid: 259b00ae-a91b-461b-a12f-f7291ecc04ff
title: 'MEEndOfPresentation 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5e3a904725908d83afd54bbd64012420075037a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993043"
---
# <a name="meendofpresentation-event"></a><span data-ttu-id="bdcd2-105">MEEndOfPresentation 事件</span><span class="sxs-lookup"><span data-stu-id="bdcd2-105">MEEndOfPresentation event</span></span>

<span data-ttu-id="bdcd2-106">在簡報結束時由媒體來源引發。</span><span class="sxs-lookup"><span data-stu-id="bdcd2-106">Raised by a media source when a presentation ends.</span></span> <span data-ttu-id="bdcd2-107">此事件表示簡報中的所有串流都已完成。</span><span class="sxs-lookup"><span data-stu-id="bdcd2-107">This event signals that all streams in the presentation are complete.</span></span> <span data-ttu-id="bdcd2-108">媒體會話將此事件轉送到應用程式。</span><span class="sxs-lookup"><span data-stu-id="bdcd2-108">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="bdcd2-109">事件值</span><span class="sxs-lookup"><span data-stu-id="bdcd2-109">Event values</span></span>

<span data-ttu-id="bdcd2-110">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="bdcd2-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="bdcd2-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="bdcd2-111">VARTYPE</span></span>              | <span data-ttu-id="bdcd2-112">Description</span><span class="sxs-lookup"><span data-stu-id="bdcd2-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="bdcd2-113">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="bdcd2-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="bdcd2-114">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="bdcd2-114">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="bdcd2-115">屬性</span><span class="sxs-lookup"><span data-stu-id="bdcd2-115">Attributes</span></span>

<span data-ttu-id="bdcd2-116">此事件會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="bdcd2-116">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="bdcd2-117">屬性</span><span class="sxs-lookup"><span data-stu-id="bdcd2-117">Attribute</span></span>                                                                                               | <span data-ttu-id="bdcd2-118">描述</span><span class="sxs-lookup"><span data-stu-id="bdcd2-118">Description</span></span>                                                                               |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bdcd2-119">**\_已取消 MF 事件 \_ 來源 \_ 拓撲 \_**</span><span class="sxs-lookup"><span data-stu-id="bdcd2-119">**MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED**</span></span>](mf-event-source-topology-canceled-attribute.md)<br/> | <span data-ttu-id="bdcd2-120">指定 sequencer 來源是否取消此展示。</span><span class="sxs-lookup"><span data-stu-id="bdcd2-120">Specifies whether the sequencer source canceled this presentation.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="bdcd2-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="bdcd2-121">Requirements</span></span>



| <span data-ttu-id="bdcd2-122">需求</span><span class="sxs-lookup"><span data-stu-id="bdcd2-122">Requirement</span></span> | <span data-ttu-id="bdcd2-123">值</span><span class="sxs-lookup"><span data-stu-id="bdcd2-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdcd2-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bdcd2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bdcd2-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bdcd2-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bdcd2-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bdcd2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bdcd2-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bdcd2-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bdcd2-128">標頭</span><span class="sxs-lookup"><span data-stu-id="bdcd2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdcd2-129"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="bdcd2-129"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdcd2-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bdcd2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdcd2-131">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="bdcd2-131">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




