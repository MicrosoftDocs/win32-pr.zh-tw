---
description: 當來源特性變更時由媒體來源引發。
ms.assetid: df7bb9a3-5949-4a4a-8835-c5b1d01b5cb3
title: 'MESourceCharacteristicsChanged 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 659e9eea0352d131aac4959b2952e8426ae408a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976810"
---
# <a name="mesourcecharacteristicschanged-event"></a><span data-ttu-id="aac29-103">MESourceCharacteristicsChanged 事件</span><span class="sxs-lookup"><span data-stu-id="aac29-103">MESourceCharacteristicsChanged event</span></span>

<span data-ttu-id="aac29-104">當來源的特性變更時由媒體來源引發。</span><span class="sxs-lookup"><span data-stu-id="aac29-104">Raised by a media source when the source's characteristics change.</span></span>

## <a name="event-values"></a><span data-ttu-id="aac29-105">事件值</span><span class="sxs-lookup"><span data-stu-id="aac29-105">Event values</span></span>

<span data-ttu-id="aac29-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="aac29-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="aac29-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="aac29-107">VARTYPE</span></span>              | <span data-ttu-id="aac29-108">Description</span><span class="sxs-lookup"><span data-stu-id="aac29-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="aac29-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="aac29-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="aac29-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="aac29-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="aac29-111">屬性</span><span class="sxs-lookup"><span data-stu-id="aac29-111">Attributes</span></span>

<span data-ttu-id="aac29-112">此事件會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="aac29-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="aac29-113">屬性</span><span class="sxs-lookup"><span data-stu-id="aac29-113">Attribute</span></span>                                                                                                   | <span data-ttu-id="aac29-114">描述</span><span class="sxs-lookup"><span data-stu-id="aac29-114">Description</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="aac29-115">**MF \_ 事件 \_ 來源 \_ 特性**</span><span class="sxs-lookup"><span data-stu-id="aac29-115">**MF\_EVENT\_SOURCE\_CHARACTERISTICS**</span></span>](mf-event-source-characteristics-attribute.md)<br/>          | <span data-ttu-id="aac29-116">媒體來源的新特性。</span><span class="sxs-lookup"><span data-stu-id="aac29-116">New characteristics of the media source.</span></span><br/> <br/>      |
| [<span data-ttu-id="aac29-117">**MF \_ 事件 \_ 來源 \_ 特性 \_ 舊**</span><span class="sxs-lookup"><span data-stu-id="aac29-117">**MF\_EVENT\_SOURCE\_CHARACTERISTICS\_OLD**</span></span>](mf-event-source-characteristics-old-attribute.md)<br/> | <span data-ttu-id="aac29-118">媒體來源的先前特性。</span><span class="sxs-lookup"><span data-stu-id="aac29-118">Previous characteristics of the media source.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="aac29-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="aac29-119">Requirements</span></span>



| <span data-ttu-id="aac29-120">需求</span><span class="sxs-lookup"><span data-stu-id="aac29-120">Requirement</span></span> | <span data-ttu-id="aac29-121">值</span><span class="sxs-lookup"><span data-stu-id="aac29-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aac29-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aac29-122">Minimum supported client</span></span><br/> | <span data-ttu-id="aac29-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aac29-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="aac29-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aac29-124">Minimum supported server</span></span><br/> | <span data-ttu-id="aac29-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aac29-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="aac29-126">標頭</span><span class="sxs-lookup"><span data-stu-id="aac29-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="aac29-127"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="aac29-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aac29-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aac29-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aac29-129">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="aac29-129">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
</dt> <dt>

[<span data-ttu-id="aac29-130">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="aac29-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




