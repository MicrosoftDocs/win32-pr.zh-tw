---
description: 當 IMFMediaSource：:P ause 方法以非同步方式完成時，由媒體資料流程引發。
ms.assetid: 8fafb9a1-95a4-44b6-acd6-fb007d515915
title: 'MEStreamPaused 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ca78147c7cdd7cb6e391052111e11ef0ac92b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106999861"
---
# <a name="mestreampaused-event"></a><span data-ttu-id="2cef4-103">MEStreamPaused 事件</span><span class="sxs-lookup"><span data-stu-id="2cef4-103">MEStreamPaused event</span></span>

<span data-ttu-id="2cef4-104">當 [**IMFMediaSource：:P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) 方法以非同步方式完成時，由媒體資料流程引發。</span><span class="sxs-lookup"><span data-stu-id="2cef4-104">Raised by a media stream when the [**IMFMediaSource::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="2cef4-105">事件值</span><span class="sxs-lookup"><span data-stu-id="2cef4-105">Event values</span></span>

<span data-ttu-id="2cef4-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="2cef4-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="2cef4-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="2cef4-107">VARTYPE</span></span>              | <span data-ttu-id="2cef4-108">Description</span><span class="sxs-lookup"><span data-stu-id="2cef4-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="2cef4-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="2cef4-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="2cef4-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="2cef4-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="2cef4-111">備註</span><span class="sxs-lookup"><span data-stu-id="2cef4-111">Remarks</span></span>

<span data-ttu-id="2cef4-112">簡報中的每個作用中資料流程都會傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="2cef4-112">Each active stream in the presentation sends this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cef4-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="2cef4-113">Requirements</span></span>



| <span data-ttu-id="2cef4-114">需求</span><span class="sxs-lookup"><span data-stu-id="2cef4-114">Requirement</span></span> | <span data-ttu-id="2cef4-115">值</span><span class="sxs-lookup"><span data-stu-id="2cef4-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cef4-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2cef4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2cef4-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2cef4-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2cef4-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2cef4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2cef4-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2cef4-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2cef4-120">標頭</span><span class="sxs-lookup"><span data-stu-id="2cef4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cef4-121"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="2cef4-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cef4-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2cef4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cef4-123">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="2cef4-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




