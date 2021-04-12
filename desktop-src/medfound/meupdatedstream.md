---
description: 當媒體來源重新開機或搜尋已在使用中的資料流程時引發。
ms.assetid: 2d91a267-e109-45f5-886b-11b883cc5509
title: 'MEUpdatedStream 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e3b2e6fdc5928a08306b344c02b5eaafc37e957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513729"
---
# <a name="meupdatedstream-event"></a><span data-ttu-id="67e8c-103">MEUpdatedStream 事件</span><span class="sxs-lookup"><span data-stu-id="67e8c-103">MEUpdatedStream event</span></span>

<span data-ttu-id="67e8c-104">當媒體來源重新開機或搜尋已在使用中的資料流程時引發。</span><span class="sxs-lookup"><span data-stu-id="67e8c-104">Raised by a media source when it restarts or seeks a stream that is already active.</span></span>

<span data-ttu-id="67e8c-105">在媒體來源上呼叫 [**IMFMediaSource：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) 方法時，媒體來源會為每個選取的資料流程傳送一個事件：</span><span class="sxs-lookup"><span data-stu-id="67e8c-105">When the [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method is called on a media source, the media source sends one event for each selected stream:</span></span>

-   <span data-ttu-id="67e8c-106">如果未在先前的 [**啟動**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)呼叫中選取資料流程，則來源會傳送 [MENewStream](menewstream.md)事件，或這是在此媒體來源上 **開始** 的第一次呼叫。</span><span class="sxs-lookup"><span data-stu-id="67e8c-106">The source sends the [MENewStream](menewstream.md) event if the stream was not selected in the previous call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), or this is the very first call to **Start** on this media source.</span></span>

-   <span data-ttu-id="67e8c-107">如果已在先前的 [**啟動**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)呼叫中選取資料流程，則來源會傳送 MEUpdatedStream 事件。</span><span class="sxs-lookup"><span data-stu-id="67e8c-107">The source sends the MEUpdatedStream event if the stream was already selected in the previous call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span></span>

<span data-ttu-id="67e8c-108">未選取的資料流程不會傳送任何事件。</span><span class="sxs-lookup"><span data-stu-id="67e8c-108">No events are sent for unselected streams.</span></span>

## <a name="event-values"></a><span data-ttu-id="67e8c-109">事件值</span><span class="sxs-lookup"><span data-stu-id="67e8c-109">Event values</span></span>

<span data-ttu-id="67e8c-110">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="67e8c-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="67e8c-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="67e8c-111">VARTYPE</span></span>                | <span data-ttu-id="67e8c-112">Description</span><span class="sxs-lookup"><span data-stu-id="67e8c-112">Description</span></span>                                                                                        |
|------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67e8c-113">VT \_ 不明</span><span class="sxs-lookup"><span data-stu-id="67e8c-113">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="67e8c-114">資料流程 [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="67e8c-114">Pointer to the stream's [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="67e8c-115">備註</span><span class="sxs-lookup"><span data-stu-id="67e8c-115">Remarks</span></span>

<span data-ttu-id="67e8c-116">在啟動資料流程的第一次呼叫 [**開始**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) 時，媒體來源會傳送資料流程的 [MENewStream](menewstream.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="67e8c-116">On the first call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) in which a stream becomes active, the media source sends an [MENewStream](menewstream.md) event for the stream.</span></span> <span data-ttu-id="67e8c-117">在後續呼叫 **開始** 時，媒體來源會傳送 MEUpdatedStream 事件，直到取消選取資料流程為止。</span><span class="sxs-lookup"><span data-stu-id="67e8c-117">On subsequent calls to **Start**, the media source sends an MEUpdatedStream event, until the stream is deselected.</span></span>

## <a name="requirements"></a><span data-ttu-id="67e8c-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="67e8c-118">Requirements</span></span>



| <span data-ttu-id="67e8c-119">需求</span><span class="sxs-lookup"><span data-stu-id="67e8c-119">Requirement</span></span> | <span data-ttu-id="67e8c-120">值</span><span class="sxs-lookup"><span data-stu-id="67e8c-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67e8c-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="67e8c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="67e8c-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67e8c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="67e8c-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="67e8c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="67e8c-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67e8c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="67e8c-125">標頭</span><span class="sxs-lookup"><span data-stu-id="67e8c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="67e8c-126"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="67e8c-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67e8c-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67e8c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67e8c-128">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="67e8c-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




