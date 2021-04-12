---
description: 由媒體來源引發，以要求新的播放速率。 應用程式應該以要求的速率呼叫 IMFRateControl：： SetRate。 如果媒體來源無法以目前的速率繼續播放，可能會引發此事件。
ms.assetid: 705e5a79-836b-417b-a7ed-c733572f6905
title: 'MESourceRateChangeRequested 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9973a509541f3ec3d4f6a235b8f1277a20f7ed1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191905"
---
# <a name="mesourceratechangerequested-event"></a><span data-ttu-id="ea088-105">MESourceRateChangeRequested 事件</span><span class="sxs-lookup"><span data-stu-id="ea088-105">MESourceRateChangeRequested event</span></span>

<span data-ttu-id="ea088-106">由媒體來源引發，以要求新的播放速率。</span><span class="sxs-lookup"><span data-stu-id="ea088-106">Raised by a media source to request a new playback rate.</span></span> <span data-ttu-id="ea088-107">應用程式應該以要求的速率呼叫 [**IMFRateControl：： SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) 。</span><span class="sxs-lookup"><span data-stu-id="ea088-107">The application should call [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) with the requested rate.</span></span> <span data-ttu-id="ea088-108">如果媒體來源無法以目前的速率繼續播放，可能會引發此事件。</span><span class="sxs-lookup"><span data-stu-id="ea088-108">A media source might raise this event if it cannot continue playback at the current rate.</span></span>

## <a name="event-values"></a><span data-ttu-id="ea088-109">事件值</span><span class="sxs-lookup"><span data-stu-id="ea088-109">Event values</span></span>

<span data-ttu-id="ea088-110">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="ea088-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="ea088-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ea088-111">VARTYPE</span></span>           | <span data-ttu-id="ea088-112">Description</span><span class="sxs-lookup"><span data-stu-id="ea088-112">Description</span></span>                                             |
|-------------------|---------------------------------------------------------|
| <span data-ttu-id="ea088-113">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="ea088-113">VT\_R4</span></span><br/> | <span data-ttu-id="ea088-114">要求的新播放速率。</span><span class="sxs-lookup"><span data-stu-id="ea088-114">The requested new playback rate.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="ea088-115">屬性</span><span class="sxs-lookup"><span data-stu-id="ea088-115">Attributes</span></span>

<span data-ttu-id="ea088-116">此事件會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="ea088-116">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="ea088-117">屬性</span><span class="sxs-lookup"><span data-stu-id="ea088-117">Attribute</span></span>                                                                    | <span data-ttu-id="ea088-118">描述</span><span class="sxs-lookup"><span data-stu-id="ea088-118">Description</span></span>                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="ea088-119">**MF \_ 事件 \_ DO \_ THINNING**</span><span class="sxs-lookup"><span data-stu-id="ea088-119">**MF\_EVENT\_DO\_THINNING**</span></span>](mf-event-do-thinning-attribute.md)<br/> | <span data-ttu-id="ea088-120">指定媒體來源是否也要求 thinning。</span><span class="sxs-lookup"><span data-stu-id="ea088-120">Specifies whether the media source also requests thinning.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="ea088-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="ea088-121">Requirements</span></span>



| <span data-ttu-id="ea088-122">需求</span><span class="sxs-lookup"><span data-stu-id="ea088-122">Requirement</span></span> | <span data-ttu-id="ea088-123">值</span><span class="sxs-lookup"><span data-stu-id="ea088-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea088-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ea088-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ea088-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ea088-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ea088-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ea088-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ea088-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ea088-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ea088-128">標頭</span><span class="sxs-lookup"><span data-stu-id="ea088-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea088-129"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="ea088-129"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea088-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ea088-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea088-131">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="ea088-131">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




