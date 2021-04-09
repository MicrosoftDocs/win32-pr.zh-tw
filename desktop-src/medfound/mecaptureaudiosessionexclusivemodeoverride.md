---
description: 當另一個程式以獨佔模式開啟音訊裝置時，由音訊捕獲來源傳送。
ms.assetid: E9CC8507-38AB-4049-8DAC-767EC0ECE270
title: 'MECaptureAudioSessionExclusiveModeOverride 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2051e6073b06f62823b95c80d7d4cfaf21de2f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690316"
---
# <a name="mecaptureaudiosessionexclusivemodeoverride-event"></a><span data-ttu-id="36699-103">MECaptureAudioSessionExclusiveModeOverride 事件</span><span class="sxs-lookup"><span data-stu-id="36699-103">MECaptureAudioSessionExclusiveModeOverride event</span></span>

<span data-ttu-id="36699-104">當另一個程式以獨佔模式開啟音訊裝置時，由音訊捕獲來源傳送。</span><span class="sxs-lookup"><span data-stu-id="36699-104">Sent by an audio capture source when another program opens the audio device in exclusive mode.</span></span>

## <a name="event-values"></a><span data-ttu-id="36699-105">事件值</span><span class="sxs-lookup"><span data-stu-id="36699-105">Event values</span></span>

<span data-ttu-id="36699-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="36699-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="36699-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="36699-107">VARTYPE</span></span>               | <span data-ttu-id="36699-108">Description</span><span class="sxs-lookup"><span data-stu-id="36699-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="36699-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="36699-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="36699-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="36699-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="36699-111">備註</span><span class="sxs-lookup"><span data-stu-id="36699-111">Remarks</span></span>

<span data-ttu-id="36699-112">此事件是由音訊捕獲來源的媒體資料流程所傳送。</span><span class="sxs-lookup"><span data-stu-id="36699-112">This event is sent by the media stream of the audio capture source.</span></span>

<span data-ttu-id="36699-113">當捕捉來源收到來自音訊會話的 [**IAudioSessionEvents：： OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) 事件，且中斷連線原因等於 **DisconnectReasonExclusiveModeOverride** 時，會傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="36699-113">The capture source sends this event when it receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the audio session with the disconnection reason equal to **DisconnectReasonExclusiveModeOverride**.</span></span>

## <a name="requirements"></a><span data-ttu-id="36699-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="36699-114">Requirements</span></span>



| <span data-ttu-id="36699-115">需求</span><span class="sxs-lookup"><span data-stu-id="36699-115">Requirement</span></span> | <span data-ttu-id="36699-116">值</span><span class="sxs-lookup"><span data-stu-id="36699-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36699-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="36699-117">Minimum supported client</span></span><br/> | <span data-ttu-id="36699-118">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36699-118">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="36699-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="36699-119">Minimum supported server</span></span><br/> | <span data-ttu-id="36699-120">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36699-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="36699-121">標頭</span><span class="sxs-lookup"><span data-stu-id="36699-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="36699-122"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="36699-122"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36699-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36699-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36699-124">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="36699-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 
