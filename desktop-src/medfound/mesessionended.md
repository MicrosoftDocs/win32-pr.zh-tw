---
description: 當媒體會話完成播放佇列中的最後一個簡報時引發。
ms.assetid: e593e51f-c239-49e9-bba8-c6d8238eff24
title: 'MESessionEnded 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 447b222be48dccc0f190329ab0bb6d56d09b266e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989299"
---
# <a name="mesessionended-event"></a><span data-ttu-id="6b714-103">MESessionEnded 事件</span><span class="sxs-lookup"><span data-stu-id="6b714-103">MESessionEnded event</span></span>

<span data-ttu-id="6b714-104">當媒體會話完成播放佇列中的最後一個簡報時引發。</span><span class="sxs-lookup"><span data-stu-id="6b714-104">Raised by the Media Session when it has finished playing the last presentation in the playback queue.</span></span>

## <a name="event-values"></a><span data-ttu-id="6b714-105">事件值</span><span class="sxs-lookup"><span data-stu-id="6b714-105">Event values</span></span>

<span data-ttu-id="6b714-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="6b714-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="6b714-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="6b714-107">VARTYPE</span></span>              | <span data-ttu-id="6b714-108">Description</span><span class="sxs-lookup"><span data-stu-id="6b714-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="6b714-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="6b714-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="6b714-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="6b714-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="6b714-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b714-111">Requirements</span></span>



| <span data-ttu-id="6b714-112">需求</span><span class="sxs-lookup"><span data-stu-id="6b714-112">Requirement</span></span> | <span data-ttu-id="6b714-113">值</span><span class="sxs-lookup"><span data-stu-id="6b714-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b714-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6b714-114">Minimum supported client</span></span><br/> | <span data-ttu-id="6b714-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b714-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6b714-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6b714-116">Minimum supported server</span></span><br/> | <span data-ttu-id="6b714-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b714-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6b714-118">標頭</span><span class="sxs-lookup"><span data-stu-id="6b714-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b714-119"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="6b714-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b714-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b714-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b714-121">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="6b714-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




