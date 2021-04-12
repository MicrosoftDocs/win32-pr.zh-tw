---
description: 當媒體接收變成無效時引發。
ms.assetid: fa75926e-7cef-44da-9efe-f2f86fd4fd45
title: 'MESinkInvalidated 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46807a45e907999b34190f9678bd3dc0051680ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191522"
---
# <a name="mesinkinvalidated-event"></a><span data-ttu-id="4b9b9-103">MESinkInvalidated 事件</span><span class="sxs-lookup"><span data-stu-id="4b9b9-103">MESinkInvalidated event</span></span>

<span data-ttu-id="4b9b9-104">當媒體接收變成無效時引發。</span><span class="sxs-lookup"><span data-stu-id="4b9b9-104">Raised when a media sink becomes invalid.</span></span>

## <a name="event-values"></a><span data-ttu-id="4b9b9-105">事件值</span><span class="sxs-lookup"><span data-stu-id="4b9b9-105">Event values</span></span>

<span data-ttu-id="4b9b9-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="4b9b9-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="4b9b9-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="4b9b9-107">VARTYPE</span></span>              | <span data-ttu-id="4b9b9-108">Description</span><span class="sxs-lookup"><span data-stu-id="4b9b9-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="4b9b9-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="4b9b9-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="4b9b9-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="4b9b9-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="4b9b9-111">屬性</span><span class="sxs-lookup"><span data-stu-id="4b9b9-111">Attributes</span></span>

<span data-ttu-id="4b9b9-112">此事件會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="4b9b9-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="4b9b9-113">屬性</span><span class="sxs-lookup"><span data-stu-id="4b9b9-113">Attribute</span></span>                                                                    | <span data-ttu-id="4b9b9-114">描述</span><span class="sxs-lookup"><span data-stu-id="4b9b9-114">Description</span></span>                                                              |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="4b9b9-115">**MF \_ 事件 \_ 輸出 \_ 節點**</span><span class="sxs-lookup"><span data-stu-id="4b9b9-115">**MF\_EVENT\_OUTPUT\_NODE**</span></span>](mf-event-output-node-attribute.md)<br/> | <span data-ttu-id="4b9b9-116">識別此媒體接收器的拓撲節點。</span><span class="sxs-lookup"><span data-stu-id="4b9b9-116">Identifies the topology node for this media sink.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="4b9b9-117">備註</span><span class="sxs-lookup"><span data-stu-id="4b9b9-117">Remarks</span></span>

<span data-ttu-id="4b9b9-118">如果媒體會話接收到來自媒體接收器的下列任何事件，就會引發這個事件：</span><span class="sxs-lookup"><span data-stu-id="4b9b9-118">The Media Session raises this event if it receives any of the following events from the media sink:</span></span>

-   [<span data-ttu-id="4b9b9-119">MEAudioSessionDeviceRemoved</span><span class="sxs-lookup"><span data-stu-id="4b9b9-119">MEAudioSessionDeviceRemoved</span></span>](meaudiosessiondeviceremoved.md)

-   [<span data-ttu-id="4b9b9-120">MEAudioSessionDisconnected</span><span class="sxs-lookup"><span data-stu-id="4b9b9-120">MEAudioSessionDisconnected</span></span>](meaudiosessiondisconnected.md)

-   [<span data-ttu-id="4b9b9-121">MEAudioSessionExclusiveModeOverride</span><span class="sxs-lookup"><span data-stu-id="4b9b9-121">MEAudioSessionExclusiveModeOverride</span></span>](meaudiosessionexclusivemodeoverride.md)

-   [<span data-ttu-id="4b9b9-122">MEAudioSessionFormatChanged</span><span class="sxs-lookup"><span data-stu-id="4b9b9-122">MEAudioSessionFormatChanged</span></span>](meaudiosessionformatchanged.md)

-   [<span data-ttu-id="4b9b9-123">MEAudioSessionServerShutdown</span><span class="sxs-lookup"><span data-stu-id="4b9b9-123">MEAudioSessionServerShutdown</span></span>](meaudiosessionservershutdown.md)

<span data-ttu-id="4b9b9-124">媒體接收器也可以引發這個事件，在這種情況下，媒體會話會設定事件的 [**MF \_ 事件 \_ 輸出 \_ 節點**](mf-event-output-node-attribute.md) 屬性，並將事件轉送到應用程式。</span><span class="sxs-lookup"><span data-stu-id="4b9b9-124">A media sink can also raise this event, in which case the Media Session sets the [**MF\_EVENT\_OUTPUT\_NODE**](mf-event-output-node-attribute.md) attribute on the event and forwards the event to the application.</span></span>

<span data-ttu-id="4b9b9-125">如果應用程式收到此事件，則必須重新建立媒體接收器，然後將拓撲重新排入佇列。</span><span class="sxs-lookup"><span data-stu-id="4b9b9-125">If the application receives this event, it needs to recreate the media sink and queue the topology again.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b9b9-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="4b9b9-126">Requirements</span></span>



| <span data-ttu-id="4b9b9-127">需求</span><span class="sxs-lookup"><span data-stu-id="4b9b9-127">Requirement</span></span> | <span data-ttu-id="4b9b9-128">值</span><span class="sxs-lookup"><span data-stu-id="4b9b9-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b9b9-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4b9b9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4b9b9-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4b9b9-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4b9b9-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4b9b9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4b9b9-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4b9b9-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4b9b9-133">標頭</span><span class="sxs-lookup"><span data-stu-id="4b9b9-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b9b9-134"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="4b9b9-134"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b9b9-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4b9b9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b9b9-136">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="4b9b9-136">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




