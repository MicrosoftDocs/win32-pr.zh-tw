---
description: 當媒體來源啟動新的資料流程時引發。
ms.assetid: 1bc8b265-b7a1-4068-89f7-c0da03dfb874
title: 'MENewStream 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60394d442b24dcdc234ada2dd3fd418e6ab7b54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980760"
---
# <a name="menewstream-event"></a><span data-ttu-id="df0cb-103">MENewStream 事件</span><span class="sxs-lookup"><span data-stu-id="df0cb-103">MENewStream event</span></span>

<span data-ttu-id="df0cb-104">當媒體來源啟動新的資料流程時引發。</span><span class="sxs-lookup"><span data-stu-id="df0cb-104">Raised by a media source when it starts a new stream.</span></span>

<span data-ttu-id="df0cb-105">在媒體來源上呼叫 [**IMFMediaSource：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) 方法時，媒體來源會為每個選取的資料流程傳送一個事件：</span><span class="sxs-lookup"><span data-stu-id="df0cb-105">When the [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method is called on a media source, the media source sends one event for each selected stream:</span></span>

-   <span data-ttu-id="df0cb-106">如果未在先前的 [**啟動**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)呼叫中選取資料流程，則來源會傳送 MENewStream 事件，或這是在此媒體來源上 **開始** 的第一次呼叫。</span><span class="sxs-lookup"><span data-stu-id="df0cb-106">The source sends the MENewStream event if the stream was not selected in the previous call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), or this is the very first call to **Start** on this media source.</span></span>

-   <span data-ttu-id="df0cb-107">如果已在先前的 [**啟動**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)呼叫中選取資料流程，則來源會傳送 [MEUpdatedStream](meupdatedstream.md)事件。</span><span class="sxs-lookup"><span data-stu-id="df0cb-107">The source sends the [MEUpdatedStream](meupdatedstream.md) event if the stream was already selected in the previous call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span></span>

<span data-ttu-id="df0cb-108">未選取的資料流程不會傳送任何事件。</span><span class="sxs-lookup"><span data-stu-id="df0cb-108">No events are sent for unselected streams.</span></span>

## <a name="event-values"></a><span data-ttu-id="df0cb-109">事件值</span><span class="sxs-lookup"><span data-stu-id="df0cb-109">Event values</span></span>

<span data-ttu-id="df0cb-110">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="df0cb-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="df0cb-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="df0cb-111">VARTYPE</span></span>                | <span data-ttu-id="df0cb-112">Description</span><span class="sxs-lookup"><span data-stu-id="df0cb-112">Description</span></span>                                                                                                   |
|------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df0cb-113">VT \_ 不明</span><span class="sxs-lookup"><span data-stu-id="df0cb-113">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="df0cb-114">包含資料流程 [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="df0cb-114">Contains a pointer to the stream's [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) interface.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="df0cb-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="df0cb-115">Requirements</span></span>



| <span data-ttu-id="df0cb-116">需求</span><span class="sxs-lookup"><span data-stu-id="df0cb-116">Requirement</span></span> | <span data-ttu-id="df0cb-117">值</span><span class="sxs-lookup"><span data-stu-id="df0cb-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df0cb-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="df0cb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="df0cb-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="df0cb-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="df0cb-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="df0cb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="df0cb-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="df0cb-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="df0cb-122">標頭</span><span class="sxs-lookup"><span data-stu-id="df0cb-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="df0cb-123"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="df0cb-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df0cb-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df0cb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df0cb-125">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="df0cb-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




