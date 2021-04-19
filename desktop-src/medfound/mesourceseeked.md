---
description: 當媒體來源搜尋至新位置時引發。 如果來源是執行中或已暫停，而且應用程式呼叫 IMFMediaSource：： Start 的開始時間不等於目前的位置，則媒體來源會引發此事件。
ms.assetid: 51ce770e-ddc7-41c1-8e31-59481cafe2b0
title: 'MESourceSeeked 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 589e6619b4b4147da65a327681ad4ed2eace89c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983325"
---
# <a name="mesourceseeked-event"></a><span data-ttu-id="621a4-104">MESourceSeeked 事件</span><span class="sxs-lookup"><span data-stu-id="621a4-104">MESourceSeeked event</span></span>

<span data-ttu-id="621a4-105">當媒體來源搜尋至新位置時引發。</span><span class="sxs-lookup"><span data-stu-id="621a4-105">Raised when a media source seeks to a new position.</span></span> <span data-ttu-id="621a4-106">如果來源是執行中或已暫停，而且應用程式呼叫 [**IMFMediaSource：： start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) 的開始時間不等於目前的位置，則媒體來源會引發此事件。</span><span class="sxs-lookup"><span data-stu-id="621a4-106">A media source raises this event if the source is running or paused and the application calls [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) with a start time that does not equal the current position.</span></span>

## <a name="event-values"></a><span data-ttu-id="621a4-107">事件值</span><span class="sxs-lookup"><span data-stu-id="621a4-107">Event values</span></span>

<span data-ttu-id="621a4-108">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="621a4-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="621a4-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="621a4-109">VARTYPE</span></span>           | <span data-ttu-id="621a4-110">Description</span><span class="sxs-lookup"><span data-stu-id="621a4-110">Description</span></span>                                                                |
|-------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="621a4-111">VT \_ I8</span><span class="sxs-lookup"><span data-stu-id="621a4-111">VT\_I8</span></span><br/> | <span data-ttu-id="621a4-112">新的開始位置，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="621a4-112">The new starting position, in 100-nanosecond units.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="621a4-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="621a4-113">Requirements</span></span>



| <span data-ttu-id="621a4-114">需求</span><span class="sxs-lookup"><span data-stu-id="621a4-114">Requirement</span></span> | <span data-ttu-id="621a4-115">值</span><span class="sxs-lookup"><span data-stu-id="621a4-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="621a4-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="621a4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="621a4-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="621a4-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="621a4-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="621a4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="621a4-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="621a4-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="621a4-120">標頭</span><span class="sxs-lookup"><span data-stu-id="621a4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="621a4-121"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="621a4-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="621a4-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="621a4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="621a4-123">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="621a4-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




