---
description: 移除裝置時，由音訊捕獲來源傳送。
ms.assetid: A249D8B4-15A8-4AD3-8316-2886E5C37825
title: 'MECaptureAudioSessionDeviceRemoved 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa0cf1b9a7536affed5a4665f6f2e364e1f872e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989018"
---
# <a name="mecaptureaudiosessiondeviceremoved-event"></a><span data-ttu-id="18456-103">MECaptureAudioSessionDeviceRemoved 事件</span><span class="sxs-lookup"><span data-stu-id="18456-103">MECaptureAudioSessionDeviceRemoved event</span></span>

<span data-ttu-id="18456-104">移除裝置時，由音訊捕獲來源傳送。</span><span class="sxs-lookup"><span data-stu-id="18456-104">Sent by an audio capture source when the device is removed.</span></span>

## <a name="event-values"></a><span data-ttu-id="18456-105">事件值</span><span class="sxs-lookup"><span data-stu-id="18456-105">Event values</span></span>

<span data-ttu-id="18456-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="18456-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="18456-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="18456-107">VARTYPE</span></span>               | <span data-ttu-id="18456-108">Description</span><span class="sxs-lookup"><span data-stu-id="18456-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="18456-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="18456-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="18456-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="18456-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="18456-111">備註</span><span class="sxs-lookup"><span data-stu-id="18456-111">Remarks</span></span>

<span data-ttu-id="18456-112">此事件是由音訊捕獲來源的媒體資料流程所傳送。</span><span class="sxs-lookup"><span data-stu-id="18456-112">This event is sent by the media stream of the audio capture source.</span></span>

<span data-ttu-id="18456-113">當捕捉來源收到來自音訊會話的 [**IAudioSessionEvents：： OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) 事件，且中斷連線原因等於 **DisconnectReasonDeviceRemoval** 時，會傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="18456-113">The capture source sends this event when it receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the audio session with the disconnection reason equal to **DisconnectReasonDeviceRemoval**.</span></span>

## <a name="requirements"></a><span data-ttu-id="18456-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="18456-114">Requirements</span></span>



| <span data-ttu-id="18456-115">需求</span><span class="sxs-lookup"><span data-stu-id="18456-115">Requirement</span></span> | <span data-ttu-id="18456-116">值</span><span class="sxs-lookup"><span data-stu-id="18456-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18456-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18456-117">Minimum supported client</span></span><br/> | <span data-ttu-id="18456-118">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18456-118">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="18456-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18456-119">Minimum supported server</span></span><br/> | <span data-ttu-id="18456-120">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18456-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="18456-121">標頭</span><span class="sxs-lookup"><span data-stu-id="18456-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="18456-122"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="18456-122"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18456-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18456-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18456-124">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="18456-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 
