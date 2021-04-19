---
description: 當 IMFMediaSource：： Stop 方法以非同步方式完成時，由媒體資料流程引發。
ms.assetid: 80280820-b618-43d9-881e-6119dfa36e22
title: 'MEStreamStopped 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3e28060505afc6b16aa6359af21c77cf92df972
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980382"
---
# <a name="mestreamstopped-event"></a><span data-ttu-id="ab6f3-103">MEStreamStopped 事件</span><span class="sxs-lookup"><span data-stu-id="ab6f3-103">MEStreamStopped event</span></span>

<span data-ttu-id="ab6f3-104">當 [**IMFMediaSource：： Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) 方法以非同步方式完成時，由媒體資料流程引發。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-104">Raised by a media stream when the [**IMFMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="ab6f3-105">事件值</span><span class="sxs-lookup"><span data-stu-id="ab6f3-105">Event values</span></span>

<span data-ttu-id="ab6f3-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="ab6f3-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ab6f3-107">VARTYPE</span></span>              | <span data-ttu-id="ab6f3-108">Description</span><span class="sxs-lookup"><span data-stu-id="ab6f3-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="ab6f3-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="ab6f3-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="ab6f3-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="ab6f3-111">備註</span><span class="sxs-lookup"><span data-stu-id="ab6f3-111">Remarks</span></span>

<span data-ttu-id="ab6f3-112">簡報中的每個作用中資料流程都會傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-112">Each active stream in the presentation sends this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab6f3-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab6f3-113">Requirements</span></span>



| <span data-ttu-id="ab6f3-114">需求</span><span class="sxs-lookup"><span data-stu-id="ab6f3-114">Requirement</span></span> | <span data-ttu-id="ab6f3-115">值</span><span class="sxs-lookup"><span data-stu-id="ab6f3-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab6f3-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ab6f3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ab6f3-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab6f3-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ab6f3-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ab6f3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ab6f3-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab6f3-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ab6f3-120">標頭</span><span class="sxs-lookup"><span data-stu-id="ab6f3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab6f3-121"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="ab6f3-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab6f3-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab6f3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab6f3-123">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="ab6f3-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




