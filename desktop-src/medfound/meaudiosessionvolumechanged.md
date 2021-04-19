---
description: 當音訊會話的音量或靜音狀態變更時，串流音訊轉譯器會 (SAR) 傳送。
ms.assetid: 63c37bd2-0289-407a-92f1-169eb5d2e02e
title: 'MEAudioSessionVolumeChanged 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429edd8a26ed7f4ca1e764c7fbea1c6930c4871c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991833"
---
# <a name="meaudiosessionvolumechanged-event"></a><span data-ttu-id="9436f-103">MEAudioSessionVolumeChanged 事件</span><span class="sxs-lookup"><span data-stu-id="9436f-103">MEAudioSessionVolumeChanged event</span></span>

<span data-ttu-id="9436f-104">當音訊會話的音量或靜音狀態變更時，串流音訊轉譯器會 (SAR) 傳送。</span><span class="sxs-lookup"><span data-stu-id="9436f-104">Sent by the streaming audio renderer (SAR) when the volume or mute state of the audio session changes.</span></span>

<span data-ttu-id="9436f-105">媒體會話將此事件轉送到應用程式。</span><span class="sxs-lookup"><span data-stu-id="9436f-105">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="9436f-106">事件值</span><span class="sxs-lookup"><span data-stu-id="9436f-106">Event values</span></span>

<span data-ttu-id="9436f-107">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="9436f-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="9436f-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="9436f-108">VARTYPE</span></span>                | <span data-ttu-id="9436f-109">Description</span><span class="sxs-lookup"><span data-stu-id="9436f-109">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9436f-110">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="9436f-110">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="9436f-111">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="9436f-111">No event data.</span></span><br/> <br/>                                                     |
| <span data-ttu-id="9436f-112">VT \_ 不明</span><span class="sxs-lookup"><span data-stu-id="9436f-112">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="9436f-113">[**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="9436f-113">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="9436f-114">備註</span><span class="sxs-lookup"><span data-stu-id="9436f-114">Remarks</span></span>

<span data-ttu-id="9436f-115">此事件是由 SAR 的資料流程接收所引發。</span><span class="sxs-lookup"><span data-stu-id="9436f-115">This event is raised by the stream sink of the SAR.</span></span> <span data-ttu-id="9436f-116">當 SAR 從音訊會話收到 [**IAudioSessionEvents：： OnSimpleVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) 事件時，就會觸發此事件。</span><span class="sxs-lookup"><span data-stu-id="9436f-116">The event is triggered when the SAR receives an [**IAudioSessionEvents::OnSimpleVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) event from the audio session.</span></span> <span data-ttu-id="9436f-117">若要取得新的磁片區層級和靜音狀態，請呼叫 [**IMFSimpleAudioVolume：： GetMasterVolume**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmastervolume) 和 [**IMFSimpleAudioVolume：： GetMute**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmute)。</span><span class="sxs-lookup"><span data-stu-id="9436f-117">To get the new volume level and mute state, call [**IMFSimpleAudioVolume::GetMasterVolume**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmastervolume) and [**IMFSimpleAudioVolume::GetMute**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmute).</span></span>

<span data-ttu-id="9436f-118">如果外部動作變更磁片區，則會傳送此事件（例如，如果使用者透過系統磁片區控制程式變更磁片區 (SndVol) 。</span><span class="sxs-lookup"><span data-stu-id="9436f-118">The SAR sends this event if an external action changes the volume—for example, if the user changes the volume through the system volume-control program (SndVol).</span></span> <span data-ttu-id="9436f-119">如果應用程式直接在 SAR 上變更磁片區，則 SAR 不會傳送事件。</span><span class="sxs-lookup"><span data-stu-id="9436f-119">The SAR does not send the event if the application changes the volume directly on the SAR.</span></span>

<span data-ttu-id="9436f-120">此外，當通道磁片區變更時，也不會傳送此事件 ([**IAudioSessionEvents：： OnChannelVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged)) 。</span><span class="sxs-lookup"><span data-stu-id="9436f-120">Also, the SAR does not send this event when the channel volume changes ([**IAudioSessionEvents::OnChannelVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged)).</span></span>

## <a name="requirements"></a><span data-ttu-id="9436f-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="9436f-121">Requirements</span></span>



| <span data-ttu-id="9436f-122">需求</span><span class="sxs-lookup"><span data-stu-id="9436f-122">Requirement</span></span> | <span data-ttu-id="9436f-123">值</span><span class="sxs-lookup"><span data-stu-id="9436f-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9436f-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9436f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9436f-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9436f-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9436f-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9436f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9436f-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9436f-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9436f-128">標頭</span><span class="sxs-lookup"><span data-stu-id="9436f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9436f-129"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="9436f-129"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9436f-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9436f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9436f-131">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="9436f-131">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="9436f-132">串流音訊轉譯器</span><span class="sxs-lookup"><span data-stu-id="9436f-132">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
