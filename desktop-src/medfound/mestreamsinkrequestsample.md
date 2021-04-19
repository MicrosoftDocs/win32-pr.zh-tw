---
description: 由資料流程接收器引發，以從管線要求新的媒體範例。
ms.assetid: 35020a15-942f-4dd0-9ca4-815affdacecf
title: 'MEStreamSinkRequestSample 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1c5afbfa9f0cfe4b320b451e699612a4729c23a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986824"
---
# <a name="mestreamsinkrequestsample-event"></a><span data-ttu-id="c7858-103">MEStreamSinkRequestSample 事件</span><span class="sxs-lookup"><span data-stu-id="c7858-103">MEStreamSinkRequestSample event</span></span>

<span data-ttu-id="c7858-104">由資料流程接收器引發，以從管線要求新的媒體範例。</span><span class="sxs-lookup"><span data-stu-id="c7858-104">Raised by a stream sink to request a new media sample from the pipeline.</span></span> <span data-ttu-id="c7858-105">針對每個 MEStreamSinkRequestSample 事件，管線會向下一個上游元件要求資料。</span><span class="sxs-lookup"><span data-stu-id="c7858-105">For each MEStreamSinkRequestSample event, the pipeline requests data from the next upstream component.</span></span>

## <a name="event-values"></a><span data-ttu-id="c7858-106">事件值</span><span class="sxs-lookup"><span data-stu-id="c7858-106">Event values</span></span>

<span data-ttu-id="c7858-107">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="c7858-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="c7858-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c7858-108">VARTYPE</span></span>              | <span data-ttu-id="c7858-109">Description</span><span class="sxs-lookup"><span data-stu-id="c7858-109">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="c7858-110">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="c7858-110">VT\_EMPTY</span></span><br/> | <span data-ttu-id="c7858-111">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="c7858-111">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="c7858-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7858-112">Requirements</span></span>



| <span data-ttu-id="c7858-113">需求</span><span class="sxs-lookup"><span data-stu-id="c7858-113">Requirement</span></span> | <span data-ttu-id="c7858-114">值</span><span class="sxs-lookup"><span data-stu-id="c7858-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7858-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c7858-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c7858-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7858-116">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c7858-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c7858-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c7858-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7858-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c7858-119">標頭</span><span class="sxs-lookup"><span data-stu-id="c7858-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7858-120"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="c7858-120"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7858-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7858-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7858-122">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="c7858-122">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="c7858-123">媒體接收器</span><span class="sxs-lookup"><span data-stu-id="c7858-123">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




