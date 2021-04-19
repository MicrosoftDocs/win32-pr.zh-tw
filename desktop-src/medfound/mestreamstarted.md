---
description: 當來源啟動但未搜尋時，由媒體資料流程引發。 當媒體來源引發 MESourceStarted 事件時，媒體資料流程會引發此事件。
ms.assetid: 6652e440-5de9-4767-b7a6-9d919ceece38
title: 'MEStreamStarted 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479726c1295b4497080b2e15abdde1558f0d4888
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977820"
---
# <a name="mestreamstarted-event"></a><span data-ttu-id="bd002-104">MEStreamStarted 事件</span><span class="sxs-lookup"><span data-stu-id="bd002-104">MEStreamStarted event</span></span>

<span data-ttu-id="bd002-105">當來源啟動但未搜尋時，由媒體資料流程引發。</span><span class="sxs-lookup"><span data-stu-id="bd002-105">Raised by a media stream when the source starts without seeking.</span></span> <span data-ttu-id="bd002-106">當媒體來源引發 [MESourceStarted](mesourcestarted.md) 事件時，媒體資料流程會引發此事件。</span><span class="sxs-lookup"><span data-stu-id="bd002-106">A media stream raises this event when the media source raises the [MESourceStarted](mesourcestarted.md) event.</span></span>

## <a name="event-values"></a><span data-ttu-id="bd002-107">事件值</span><span class="sxs-lookup"><span data-stu-id="bd002-107">Event values</span></span>

<span data-ttu-id="bd002-108">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="bd002-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="bd002-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="bd002-109">VARTYPE</span></span>              | <span data-ttu-id="bd002-110">Description</span><span class="sxs-lookup"><span data-stu-id="bd002-110">Description</span></span>                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd002-111">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="bd002-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="bd002-112">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="bd002-112">No event data.</span></span><br/> <br/>                                                                          |
| <span data-ttu-id="bd002-113">VT \_ I8</span><span class="sxs-lookup"><span data-stu-id="bd002-113">VT\_I8</span></span><br/>    | <span data-ttu-id="bd002-114">相對於樣本上時間戳記的開始時間，以 100-毫微秒單位為單位。</span><span class="sxs-lookup"><span data-stu-id="bd002-114">The starting time, in 100-nanosecond units, relative to the time stamps on the samples.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="bd002-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd002-115">Requirements</span></span>



| <span data-ttu-id="bd002-116">需求</span><span class="sxs-lookup"><span data-stu-id="bd002-116">Requirement</span></span> | <span data-ttu-id="bd002-117">值</span><span class="sxs-lookup"><span data-stu-id="bd002-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd002-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bd002-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bd002-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bd002-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bd002-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bd002-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bd002-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bd002-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bd002-122">標頭</span><span class="sxs-lookup"><span data-stu-id="bd002-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd002-123"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="bd002-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd002-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd002-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd002-125">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="bd002-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




