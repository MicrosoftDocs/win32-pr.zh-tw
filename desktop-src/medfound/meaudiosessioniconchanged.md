---
description: 當音訊會話圖示變更時，由音訊轉譯器引發。
ms.assetid: 72aae901-e5fe-481d-babb-459038abd629
title: 'MEAudioSessionIconChanged 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba7a12a4e82585c270206d595d32ba82c4e9e594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971044"
---
# <a name="meaudiosessioniconchanged-event"></a><span data-ttu-id="5f8ad-103">MEAudioSessionIconChanged 事件</span><span class="sxs-lookup"><span data-stu-id="5f8ad-103">MEAudioSessionIconChanged event</span></span>

<span data-ttu-id="5f8ad-104">當音訊會話圖示變更時，由音訊轉譯器引發。</span><span class="sxs-lookup"><span data-stu-id="5f8ad-104">Raised by the audio renderer when the audio session icon changes.</span></span>

<span data-ttu-id="5f8ad-105">媒體會話將此事件轉送到應用程式。</span><span class="sxs-lookup"><span data-stu-id="5f8ad-105">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="5f8ad-106">事件值</span><span class="sxs-lookup"><span data-stu-id="5f8ad-106">Event values</span></span>

<span data-ttu-id="5f8ad-107">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="5f8ad-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="5f8ad-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5f8ad-108">VARTYPE</span></span>                | <span data-ttu-id="5f8ad-109">Description</span><span class="sxs-lookup"><span data-stu-id="5f8ad-109">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f8ad-110">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="5f8ad-110">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="5f8ad-111">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="5f8ad-111">No event data.</span></span><br/> <br/>                                                     |
| <span data-ttu-id="5f8ad-112">VT \_ 不明</span><span class="sxs-lookup"><span data-stu-id="5f8ad-112">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="5f8ad-113">[**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="5f8ad-113">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="5f8ad-114">備註</span><span class="sxs-lookup"><span data-stu-id="5f8ad-114">Remarks</span></span>

<span data-ttu-id="5f8ad-115">此事件是由音訊轉譯器的資料流程接收所傳送。</span><span class="sxs-lookup"><span data-stu-id="5f8ad-115">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="5f8ad-116">當音訊轉譯器收到來自音訊會話的 [**IAudioSessionEvents：： OnIconPathChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-oniconpathchanged) 事件時，就會觸發此事件。</span><span class="sxs-lookup"><span data-stu-id="5f8ad-116">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnIconPathChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-oniconpathchanged) event from the audio session.</span></span>

<span data-ttu-id="5f8ad-117">若要取得新的圖示，請呼叫 [**IMFAudioPolicy：： GetIconPath**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath)。</span><span class="sxs-lookup"><span data-stu-id="5f8ad-117">To get the new icon, call [**IMFAudioPolicy::GetIconPath**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath).</span></span>

## <a name="requirements"></a><span data-ttu-id="5f8ad-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f8ad-118">Requirements</span></span>



| <span data-ttu-id="5f8ad-119">需求</span><span class="sxs-lookup"><span data-stu-id="5f8ad-119">Requirement</span></span> | <span data-ttu-id="5f8ad-120">值</span><span class="sxs-lookup"><span data-stu-id="5f8ad-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f8ad-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5f8ad-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5f8ad-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f8ad-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5f8ad-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5f8ad-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5f8ad-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f8ad-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5f8ad-125">標頭</span><span class="sxs-lookup"><span data-stu-id="5f8ad-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f8ad-126"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="5f8ad-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f8ad-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f8ad-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f8ad-128">**IMFAudioPolicy::GetIconPath**</span><span class="sxs-lookup"><span data-stu-id="5f8ad-128">**IMFAudioPolicy::GetIconPath**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath)
</dt> <dt>

[<span data-ttu-id="5f8ad-129">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="5f8ad-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="5f8ad-130">串流音訊轉譯器</span><span class="sxs-lookup"><span data-stu-id="5f8ad-130">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
