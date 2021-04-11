---
description: 當播放速率變更時由媒體來源引發。 此事件會在 IMFRateControl：： SetRate 方法以非同步方式完成之後傳送。
ms.assetid: 68a7fe64-e28a-4c20-830c-9402e1fb57f8
title: 'MESourceRateChanged 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2af1ca671e09fc8a236ba79b36c1610635989ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113693"
---
# <a name="mesourceratechanged-event"></a><span data-ttu-id="f122a-104">MESourceRateChanged 事件</span><span class="sxs-lookup"><span data-stu-id="f122a-104">MESourceRateChanged event</span></span>

<span data-ttu-id="f122a-105">當播放速率變更時由媒體來源引發。</span><span class="sxs-lookup"><span data-stu-id="f122a-105">Raised by a media source when the playback rate changes.</span></span> <span data-ttu-id="f122a-106">此事件會在 [**IMFRateControl：： SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) 方法以非同步方式完成之後傳送。</span><span class="sxs-lookup"><span data-stu-id="f122a-106">This event is sent after the [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="f122a-107">事件值</span><span class="sxs-lookup"><span data-stu-id="f122a-107">Event values</span></span>

<span data-ttu-id="f122a-108">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="f122a-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="f122a-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="f122a-109">VARTYPE</span></span>           | <span data-ttu-id="f122a-110">Description</span><span class="sxs-lookup"><span data-stu-id="f122a-110">Description</span></span>                                   |
|-------------------|-----------------------------------------------|
| <span data-ttu-id="f122a-111">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="f122a-111">VT\_R4</span></span><br/> | <span data-ttu-id="f122a-112">新的播放速率。</span><span class="sxs-lookup"><span data-stu-id="f122a-112">The new playback rate.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="f122a-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="f122a-113">Requirements</span></span>



| <span data-ttu-id="f122a-114">需求</span><span class="sxs-lookup"><span data-stu-id="f122a-114">Requirement</span></span> | <span data-ttu-id="f122a-115">值</span><span class="sxs-lookup"><span data-stu-id="f122a-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f122a-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f122a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f122a-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f122a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f122a-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f122a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f122a-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f122a-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f122a-120">標頭</span><span class="sxs-lookup"><span data-stu-id="f122a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f122a-121"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="f122a-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f122a-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f122a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f122a-123">執行速率控制</span><span class="sxs-lookup"><span data-stu-id="f122a-123">Implementing Rate Control</span></span>](implementing-rate-control.md)
</dt> <dt>

[<span data-ttu-id="f122a-124">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="f122a-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="f122a-125">速率控制</span><span class="sxs-lookup"><span data-stu-id="f122a-125">Rate Control</span></span>](rate-control.md)
</dt> <dt>

[<span data-ttu-id="f122a-126">**IMFRateControl::SetRate**</span><span class="sxs-lookup"><span data-stu-id="f122a-126">**IMFRateControl::SetRate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)
</dt> </dl>

 

 




