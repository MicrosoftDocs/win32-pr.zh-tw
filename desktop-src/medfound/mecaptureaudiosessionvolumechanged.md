---
description: 當磁片區變更時由音訊捕獲來源傳送。
ms.assetid: 4A525D5F-9226-4277-BDB7-174BF65FE320
title: 'MECaptureAudioSessionVolumeChanged 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a391c55e8fcebaef0f620430b12f7cdcc67364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974326"
---
# <a name="mecaptureaudiosessionvolumechanged-event"></a><span data-ttu-id="605ef-103">MECaptureAudioSessionVolumeChanged 事件</span><span class="sxs-lookup"><span data-stu-id="605ef-103">MECaptureAudioSessionVolumeChanged event</span></span>

<span data-ttu-id="605ef-104">當磁片區變更時由音訊捕獲來源傳送。</span><span class="sxs-lookup"><span data-stu-id="605ef-104">Sent by an audio capture source when the volume changes.</span></span>

## <a name="event-values"></a><span data-ttu-id="605ef-105">事件值</span><span class="sxs-lookup"><span data-stu-id="605ef-105">Event values</span></span>

<span data-ttu-id="605ef-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="605ef-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="605ef-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="605ef-107">VARTYPE</span></span>               | <span data-ttu-id="605ef-108">Description</span><span class="sxs-lookup"><span data-stu-id="605ef-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="605ef-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="605ef-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="605ef-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="605ef-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="605ef-111">備註</span><span class="sxs-lookup"><span data-stu-id="605ef-111">Remarks</span></span>

<span data-ttu-id="605ef-112">此事件是由音訊捕獲來源的媒體資料流程所傳送。</span><span class="sxs-lookup"><span data-stu-id="605ef-112">This event is sent by the media stream of the audio capture source.</span></span>

<span data-ttu-id="605ef-113">如果外部動作變更磁片區（例如，如果使用者透過主控台變更磁片區），音訊捕獲來源就會傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="605ef-113">The audio capture source sends this event if an external action changes the volume—for example, if the user changes the volume through the Control Panel.</span></span> <span data-ttu-id="605ef-114">如果應用程式直接在來源上變更磁片區，則捕捉來源不會傳送事件。</span><span class="sxs-lookup"><span data-stu-id="605ef-114">The capture source does not send the event if the application changes the volume directly on the source.</span></span>

## <a name="requirements"></a><span data-ttu-id="605ef-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="605ef-115">Requirements</span></span>



| <span data-ttu-id="605ef-116">需求</span><span class="sxs-lookup"><span data-stu-id="605ef-116">Requirement</span></span> | <span data-ttu-id="605ef-117">值</span><span class="sxs-lookup"><span data-stu-id="605ef-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="605ef-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="605ef-118">Minimum supported client</span></span><br/> | <span data-ttu-id="605ef-119">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="605ef-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="605ef-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="605ef-120">Minimum supported server</span></span><br/> | <span data-ttu-id="605ef-121">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="605ef-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="605ef-122">標頭</span><span class="sxs-lookup"><span data-stu-id="605ef-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="605ef-123"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="605ef-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="605ef-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="605ef-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="605ef-125">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="605ef-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




