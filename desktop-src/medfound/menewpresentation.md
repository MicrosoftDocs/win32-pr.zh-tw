---
description: 由媒體來源引發，該媒體來源透過 IMFMediaSourceTopologyProvider 介面（例如 sequencer 來源）提供拓撲。 來源會在有新的簡報時引發事件。 媒體會話將此事件轉送到應用程式。
ms.assetid: c669b2c9-5ece-4045-b691-8a71bbf491e1
title: 'MENewPresentation 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70265a84cc7724fc6f5b6a77be2181149bd82176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191912"
---
# <a name="menewpresentation-event"></a><span data-ttu-id="cd3e9-105">MENewPresentation 事件</span><span class="sxs-lookup"><span data-stu-id="cd3e9-105">MENewPresentation event</span></span>

<span data-ttu-id="cd3e9-106">由媒體來源引發，該媒體來源透過 [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) 介面（例如 sequencer 來源）提供拓撲。</span><span class="sxs-lookup"><span data-stu-id="cd3e9-106">Raised by a media source that provides topologies through the [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) interface, such as the sequencer source.</span></span> <span data-ttu-id="cd3e9-107">來源會在有新的簡報時引發事件。</span><span class="sxs-lookup"><span data-stu-id="cd3e9-107">The source raises the event when it has a new presentation.</span></span> <span data-ttu-id="cd3e9-108">媒體會話將此事件轉送到應用程式。</span><span class="sxs-lookup"><span data-stu-id="cd3e9-108">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="cd3e9-109">事件值</span><span class="sxs-lookup"><span data-stu-id="cd3e9-109">Event values</span></span>

<span data-ttu-id="cd3e9-110">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="cd3e9-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="cd3e9-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cd3e9-111">VARTYPE</span></span>                | <span data-ttu-id="cd3e9-112">Description</span><span class="sxs-lookup"><span data-stu-id="cd3e9-112">Description</span></span>                                                                                                                                                             |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd3e9-113">VT \_ 不明</span><span class="sxs-lookup"><span data-stu-id="cd3e9-113">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="cd3e9-114">新簡報之呈現描述項的 [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="cd3e9-114">Pointer to the [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface of the presentation descriptor for the new presentation.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="cd3e9-115">備註</span><span class="sxs-lookup"><span data-stu-id="cd3e9-115">Remarks</span></span>

<span data-ttu-id="cd3e9-116">應用程式可以藉由呼叫媒體來源上的 [**IMFMediaSourceTopologyProvider：： GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) ，取得對應至展示描述項的拓撲。</span><span class="sxs-lookup"><span data-stu-id="cd3e9-116">The application can get the topology that corresponds to the presentation descriptor by calling [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) on the media source.</span></span> <span data-ttu-id="cd3e9-117">然後，應用程式可以藉由呼叫 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)，在媒體會話上將新的拓撲排入佇列。</span><span class="sxs-lookup"><span data-stu-id="cd3e9-117">The application can then queue the new topology on the Media Session by calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd3e9-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd3e9-118">Requirements</span></span>



| <span data-ttu-id="cd3e9-119">需求</span><span class="sxs-lookup"><span data-stu-id="cd3e9-119">Requirement</span></span> | <span data-ttu-id="cd3e9-120">值</span><span class="sxs-lookup"><span data-stu-id="cd3e9-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd3e9-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cd3e9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cd3e9-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd3e9-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cd3e9-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cd3e9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cd3e9-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd3e9-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cd3e9-125">標頭</span><span class="sxs-lookup"><span data-stu-id="cd3e9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd3e9-126"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="cd3e9-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd3e9-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cd3e9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd3e9-128">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="cd3e9-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="cd3e9-129">Sequencer 來源</span><span class="sxs-lookup"><span data-stu-id="cd3e9-129">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 




