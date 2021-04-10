---
description: 當 IMFMediaSession：： Start 方法以非同步方式完成時引發。
ms.assetid: 28ed32f0-9b23-4da1-9587-15f490da7bf9
title: 'MESessionStarted 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9510fb5f5dda3d14b916ed40dcba4ca05800b52b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026452"
---
# <a name="mesessionstarted-event"></a><span data-ttu-id="7e65d-103">MESessionStarted 事件</span><span class="sxs-lookup"><span data-stu-id="7e65d-103">MESessionStarted event</span></span>

<span data-ttu-id="7e65d-104">當 [**IMFMediaSession：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) 方法以非同步方式完成時引發。</span><span class="sxs-lookup"><span data-stu-id="7e65d-104">Raised when the [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="7e65d-105">事件值</span><span class="sxs-lookup"><span data-stu-id="7e65d-105">Event values</span></span>

<span data-ttu-id="7e65d-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="7e65d-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="7e65d-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="7e65d-107">VARTYPE</span></span>              | <span data-ttu-id="7e65d-108">Description</span><span class="sxs-lookup"><span data-stu-id="7e65d-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="7e65d-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="7e65d-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="7e65d-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="7e65d-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="7e65d-111">屬性</span><span class="sxs-lookup"><span data-stu-id="7e65d-111">Attributes</span></span>

<span data-ttu-id="7e65d-112">此事件會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="7e65d-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="7e65d-113">屬性</span><span class="sxs-lookup"><span data-stu-id="7e65d-113">Attribute</span></span>                                                                                               | <span data-ttu-id="7e65d-114">描述</span><span class="sxs-lookup"><span data-stu-id="7e65d-114">Description</span></span>                                                                                     |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e65d-115">**MF \_ 事件 \_ 呈現 \_ 時間 \_ 位移**</span><span class="sxs-lookup"><span data-stu-id="7e65d-115">**MF\_EVENT\_PRESENTATION\_TIME\_OFFSET**</span></span>](mf-event-presentation-time-offset-attribute.md)<br/> | <span data-ttu-id="7e65d-116">呈現時間與媒體來源時間戳記之間的位移。</span><span class="sxs-lookup"><span data-stu-id="7e65d-116">Offset between the presentation time and the media source's time stamps.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="7e65d-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="7e65d-117">Requirements</span></span>



| <span data-ttu-id="7e65d-118">需求</span><span class="sxs-lookup"><span data-stu-id="7e65d-118">Requirement</span></span> | <span data-ttu-id="7e65d-119">值</span><span class="sxs-lookup"><span data-stu-id="7e65d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e65d-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7e65d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7e65d-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e65d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7e65d-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7e65d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7e65d-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e65d-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7e65d-124">標頭</span><span class="sxs-lookup"><span data-stu-id="7e65d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e65d-125"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="7e65d-125"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e65d-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7e65d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e65d-127">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="7e65d-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




