---
description: 當播放速率變更時由媒體會話引發。 此事件會在 IMFRateControl：： SetRate 方法以非同步方式完成之後傳送。
ms.assetid: 6bef923f-4083-46e1-9a2e-49a6825467ec
title: 'MESessionRateChanged 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4cbbd8254dfb988c94cf2016164726d578d8906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848538"
---
# <a name="mesessionratechanged-event"></a><span data-ttu-id="c8b15-104">MESessionRateChanged 事件</span><span class="sxs-lookup"><span data-stu-id="c8b15-104">MESessionRateChanged event</span></span>

<span data-ttu-id="c8b15-105">當播放速率變更時由媒體會話引發。</span><span class="sxs-lookup"><span data-stu-id="c8b15-105">Raised by the Media Session when the playback rate changes.</span></span> <span data-ttu-id="c8b15-106">此事件會在 [**IMFRateControl：： SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) 方法以非同步方式完成之後傳送。</span><span class="sxs-lookup"><span data-stu-id="c8b15-106">This event is sent after the [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="c8b15-107">事件值</span><span class="sxs-lookup"><span data-stu-id="c8b15-107">Event values</span></span>

<span data-ttu-id="c8b15-108">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="c8b15-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="c8b15-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c8b15-109">VARTYPE</span></span>           | <span data-ttu-id="c8b15-110">Description</span><span class="sxs-lookup"><span data-stu-id="c8b15-110">Description</span></span>                                                                                     |
|-------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8b15-111">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="c8b15-111">VT\_R4</span></span><br/> | <span data-ttu-id="c8b15-112">新的播放速率，以正常播放速率的比率表示。</span><span class="sxs-lookup"><span data-stu-id="c8b15-112">The new playback rate, expressed as a ratio of the normal playback rate.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="c8b15-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8b15-113">Requirements</span></span>



| <span data-ttu-id="c8b15-114">需求</span><span class="sxs-lookup"><span data-stu-id="c8b15-114">Requirement</span></span> | <span data-ttu-id="c8b15-115">值</span><span class="sxs-lookup"><span data-stu-id="c8b15-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8b15-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c8b15-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c8b15-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8b15-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c8b15-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c8b15-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c8b15-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8b15-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c8b15-120">標頭</span><span class="sxs-lookup"><span data-stu-id="c8b15-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8b15-121"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="c8b15-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8b15-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8b15-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8b15-123">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="c8b15-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




