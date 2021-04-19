---
description: 當音訊會話與 Windows 終端機服務 (WTS) 會話中斷連線時，由音訊轉譯器引發。 音訊轉譯器現在無效。
ms.assetid: 08f9844c-f3b1-4d60-990e-9131f3312f6b
title: 'MEAudioSessionDisconnected 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db2d31349585d26c61cb2940cea70ddaf0617901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974321"
---
# <a name="meaudiosessiondisconnected-event"></a><span data-ttu-id="30ea3-104">MEAudioSessionDisconnected 事件</span><span class="sxs-lookup"><span data-stu-id="30ea3-104">MEAudioSessionDisconnected event</span></span>

<span data-ttu-id="30ea3-105">當音訊會話與 Windows 終端機服務 (WTS) 會話中斷連線時，由音訊轉譯器引發。</span><span class="sxs-lookup"><span data-stu-id="30ea3-105">Raised by the audio renderer when the audio session is disconnected from a Windows Terminal Services (WTS) session.</span></span> <span data-ttu-id="30ea3-106">音訊轉譯器現在無效。</span><span class="sxs-lookup"><span data-stu-id="30ea3-106">The audio renderer is now invalid.</span></span>

<span data-ttu-id="30ea3-107">媒體會話將此事件轉送到應用程式。</span><span class="sxs-lookup"><span data-stu-id="30ea3-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="30ea3-108">事件值</span><span class="sxs-lookup"><span data-stu-id="30ea3-108">Event values</span></span>

<span data-ttu-id="30ea3-109">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="30ea3-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="30ea3-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="30ea3-110">VARTYPE</span></span>                | <span data-ttu-id="30ea3-111">Description</span><span class="sxs-lookup"><span data-stu-id="30ea3-111">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="30ea3-112">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="30ea3-112">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="30ea3-113">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="30ea3-113">No event data.</span></span><br/> <br/>                                                     |
| <span data-ttu-id="30ea3-114">VT \_ 不明</span><span class="sxs-lookup"><span data-stu-id="30ea3-114">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="30ea3-115">[**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="30ea3-115">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="30ea3-116">備註</span><span class="sxs-lookup"><span data-stu-id="30ea3-116">Remarks</span></span>

<span data-ttu-id="30ea3-117">此事件是由音訊轉譯器的資料流程接收所傳送。</span><span class="sxs-lookup"><span data-stu-id="30ea3-117">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="30ea3-118">當音訊轉譯器從音訊會話接收 [**IAudioSessionEvents：： OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) 事件，而中斷連線原因等於 DisconnectReasonSessionDisconnected 時，就會觸發此事件。</span><span class="sxs-lookup"><span data-stu-id="30ea3-118">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the audio session with the disconnection reason equal to DisconnectReasonSessionDisconnected.</span></span>

<span data-ttu-id="30ea3-119">[**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)指標（如果設定的話）並不實用，因為音訊資料流程不再有效。</span><span class="sxs-lookup"><span data-stu-id="30ea3-119">The [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) pointer, if set, is not useful, because the audio stream is no longer valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="30ea3-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="30ea3-120">Requirements</span></span>



| <span data-ttu-id="30ea3-121">需求</span><span class="sxs-lookup"><span data-stu-id="30ea3-121">Requirement</span></span> | <span data-ttu-id="30ea3-122">值</span><span class="sxs-lookup"><span data-stu-id="30ea3-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30ea3-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="30ea3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="30ea3-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30ea3-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="30ea3-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="30ea3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="30ea3-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30ea3-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="30ea3-127">標頭</span><span class="sxs-lookup"><span data-stu-id="30ea3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="30ea3-128"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="30ea3-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30ea3-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30ea3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30ea3-130">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="30ea3-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="30ea3-131">串流音訊轉譯器</span><span class="sxs-lookup"><span data-stu-id="30ea3-131">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
