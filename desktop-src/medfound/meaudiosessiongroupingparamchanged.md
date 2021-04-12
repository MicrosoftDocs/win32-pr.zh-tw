---
description: 當音訊會話的群組參數變更時，由音訊轉譯器引發。
ms.assetid: d6f7757c-fd91-40bd-b2b5-a3e808445250
title: 'MEAudioSessionGroupingParamChanged 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ac115bb30a4c01247da537f3255e9bc40099e3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191584"
---
# <a name="meaudiosessiongroupingparamchanged-event"></a><span data-ttu-id="0cb48-103">MEAudioSessionGroupingParamChanged 事件</span><span class="sxs-lookup"><span data-stu-id="0cb48-103">MEAudioSessionGroupingParamChanged event</span></span>

<span data-ttu-id="0cb48-104">當音訊會話的群組參數變更時，由音訊轉譯器引發。</span><span class="sxs-lookup"><span data-stu-id="0cb48-104">Raised by the audio renderer when the grouping parameters change for the audio session.</span></span>

<span data-ttu-id="0cb48-105">媒體會話將此事件轉送到應用程式。</span><span class="sxs-lookup"><span data-stu-id="0cb48-105">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="0cb48-106">事件值</span><span class="sxs-lookup"><span data-stu-id="0cb48-106">Event values</span></span>

<span data-ttu-id="0cb48-107">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="0cb48-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="0cb48-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0cb48-108">VARTYPE</span></span>                | <span data-ttu-id="0cb48-109">Description</span><span class="sxs-lookup"><span data-stu-id="0cb48-109">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cb48-110">VT \_ 不明</span><span class="sxs-lookup"><span data-stu-id="0cb48-110">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="0cb48-111">[**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="0cb48-111">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0cb48-112">備註</span><span class="sxs-lookup"><span data-stu-id="0cb48-112">Remarks</span></span>

<span data-ttu-id="0cb48-113">此事件是由音訊轉譯器的資料流程接收所傳送。</span><span class="sxs-lookup"><span data-stu-id="0cb48-113">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="0cb48-114">當音訊轉譯器收到來自音訊會話的 [**IAudioSessionEvents：： OnGroupingParamChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ongroupingparamchanged) 事件時，就會觸發此事件。</span><span class="sxs-lookup"><span data-stu-id="0cb48-114">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnGroupingParamChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ongroupingparamchanged) event from the audio session.</span></span>

<span data-ttu-id="0cb48-115">若要取得新的群組參數，請呼叫 [**IMFAudioPolicy：： GetGroupingParam**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getgroupingparam)。</span><span class="sxs-lookup"><span data-stu-id="0cb48-115">To get the new grouping parameters, call [**IMFAudioPolicy::GetGroupingParam**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getgroupingparam).</span></span>

## <a name="requirements"></a><span data-ttu-id="0cb48-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="0cb48-116">Requirements</span></span>



| <span data-ttu-id="0cb48-117">需求</span><span class="sxs-lookup"><span data-stu-id="0cb48-117">Requirement</span></span> | <span data-ttu-id="0cb48-118">值</span><span class="sxs-lookup"><span data-stu-id="0cb48-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cb48-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0cb48-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0cb48-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0cb48-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0cb48-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0cb48-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0cb48-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0cb48-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0cb48-123">標頭</span><span class="sxs-lookup"><span data-stu-id="0cb48-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cb48-124"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="0cb48-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cb48-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0cb48-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cb48-126">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="0cb48-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="0cb48-127">**IMFAudioPolicy::GetGroupingParam**</span><span class="sxs-lookup"><span data-stu-id="0cb48-127">**IMFAudioPolicy::GetGroupingParam**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getgroupingparam)
</dt> <dt>

[<span data-ttu-id="0cb48-128">串流音訊轉譯器</span><span class="sxs-lookup"><span data-stu-id="0cb48-128">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
