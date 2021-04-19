---
description: 由封裝裝置的 IMFMediaSource 所傳送，以指出裝置已被佔用。
ms.assetid: 85EE663C-94B7-47EA-ABBA-A8371342EEB2
title: 'MEVideoCaptureDevicePreempted 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3968c0641d954741474b1d5ec7ffaa11dcad5f15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971710"
---
# <a name="mevideocapturedevicepreempted-event"></a><span data-ttu-id="7f88b-103">MEVideoCaptureDevicePreempted 事件</span><span class="sxs-lookup"><span data-stu-id="7f88b-103">MEVideoCaptureDevicePreempted event</span></span>

<span data-ttu-id="7f88b-104">由封裝裝置的 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) 所傳送，以指出裝置已被佔用。</span><span class="sxs-lookup"><span data-stu-id="7f88b-104">Sent by the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) that encapsulates the device to indicate that the device has been preempted.</span></span>

## <a name="event-values"></a><span data-ttu-id="7f88b-105">事件值</span><span class="sxs-lookup"><span data-stu-id="7f88b-105">Event values</span></span>

<span data-ttu-id="7f88b-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="7f88b-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="7f88b-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="7f88b-107">VARTYPE</span></span>               | <span data-ttu-id="7f88b-108">Description</span><span class="sxs-lookup"><span data-stu-id="7f88b-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="7f88b-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="7f88b-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="7f88b-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="7f88b-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="7f88b-111">備註</span><span class="sxs-lookup"><span data-stu-id="7f88b-111">Remarks</span></span>

<span data-ttu-id="7f88b-112">此事件是由封裝裝置的 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) 所傳送。</span><span class="sxs-lookup"><span data-stu-id="7f88b-112">This event is sent by the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) that encapsulates the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f88b-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f88b-113">Requirements</span></span>



| <span data-ttu-id="7f88b-114">需求</span><span class="sxs-lookup"><span data-stu-id="7f88b-114">Requirement</span></span> | <span data-ttu-id="7f88b-115">值</span><span class="sxs-lookup"><span data-stu-id="7f88b-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f88b-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7f88b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7f88b-117">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f88b-117">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="7f88b-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7f88b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7f88b-119">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f88b-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7f88b-120">標頭</span><span class="sxs-lookup"><span data-stu-id="7f88b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f88b-121"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="7f88b-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f88b-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f88b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f88b-123">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="7f88b-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




