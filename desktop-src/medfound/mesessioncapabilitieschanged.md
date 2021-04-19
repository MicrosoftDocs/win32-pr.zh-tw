---
description: 當會話功能變更時由媒體會話引發。
ms.assetid: d59fd3a0-29db-434c-b6ba-d9beb33bd965
title: 'MESessionCapabilitiesChanged 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0612b705571c50a6adcbde4afe93b42a524a950
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998474"
---
# <a name="mesessioncapabilitieschanged-event"></a><span data-ttu-id="a6621-103">MESessionCapabilitiesChanged 事件</span><span class="sxs-lookup"><span data-stu-id="a6621-103">MESessionCapabilitiesChanged event</span></span>

<span data-ttu-id="a6621-104">當會話功能變更時由媒體會話引發。</span><span class="sxs-lookup"><span data-stu-id="a6621-104">Raised by the Media Session when the session capabilities change.</span></span>

## <a name="event-values"></a><span data-ttu-id="a6621-105">事件值</span><span class="sxs-lookup"><span data-stu-id="a6621-105">Event values</span></span>

<span data-ttu-id="a6621-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="a6621-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="a6621-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="a6621-107">VARTYPE</span></span>              | <span data-ttu-id="a6621-108">Description</span><span class="sxs-lookup"><span data-stu-id="a6621-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="a6621-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="a6621-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="a6621-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="a6621-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="a6621-111">備註</span><span class="sxs-lookup"><span data-stu-id="a6621-111">Remarks</span></span>

<span data-ttu-id="a6621-112">此事件包含下列屬性。</span><span class="sxs-lookup"><span data-stu-id="a6621-112">The event contains the following attributes.</span></span>



| <span data-ttu-id="a6621-113">屬性</span><span class="sxs-lookup"><span data-stu-id="a6621-113">Attribute</span></span>                                                                     | <span data-ttu-id="a6621-114">描述</span><span class="sxs-lookup"><span data-stu-id="a6621-114">Description</span></span>                                      |
|-------------------------------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="a6621-115">**MF \_ 事件 \_ SESSIONCAPS**</span><span class="sxs-lookup"><span data-stu-id="a6621-115">**MF\_EVENT\_SESSIONCAPS**</span></span>](mf-event-sessioncaps-attribute.md)              | <span data-ttu-id="a6621-116">新的會話功能旗標。</span><span class="sxs-lookup"><span data-stu-id="a6621-116">New session capabilities flags.</span></span>                  |
| [<span data-ttu-id="a6621-117">**MF \_ 事件 \_ SESSIONCAPS \_ 差異**</span><span class="sxs-lookup"><span data-stu-id="a6621-117">**MF\_EVENT\_SESSIONCAPS\_DELTA**</span></span>](mf-event-sessioncaps-delta-attribute.md) | <span data-ttu-id="a6621-118">指出哪些功能旗標已變更。</span><span class="sxs-lookup"><span data-stu-id="a6621-118">Indicates which capabilities flags have changed.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="a6621-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="a6621-119">Requirements</span></span>



| <span data-ttu-id="a6621-120">需求</span><span class="sxs-lookup"><span data-stu-id="a6621-120">Requirement</span></span> | <span data-ttu-id="a6621-121">值</span><span class="sxs-lookup"><span data-stu-id="a6621-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6621-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a6621-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a6621-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a6621-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a6621-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a6621-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a6621-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a6621-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a6621-126">標頭</span><span class="sxs-lookup"><span data-stu-id="a6621-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6621-127"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="a6621-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6621-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a6621-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6621-129">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="a6621-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




