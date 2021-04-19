---
description: 發出嚴重錯誤的信號。 任何媒體基礎元件都可以隨時傳送此事件。 呼叫 IMFMediaEvent：： GetStatus，以取得失敗作業的錯誤碼。
ms.assetid: bff80041-77d8-43b1-a410-9cefaf45eb2c
title: 'MEError 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0eb557dffb2c73a63031a193c331edabe470db7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989302"
---
# <a name="meerror-event"></a><span data-ttu-id="53b68-105">MEError 事件</span><span class="sxs-lookup"><span data-stu-id="53b68-105">MEError event</span></span>

<span data-ttu-id="53b68-106">發出嚴重錯誤的信號。</span><span class="sxs-lookup"><span data-stu-id="53b68-106">Signals a serious error.</span></span> <span data-ttu-id="53b68-107">任何媒體基礎元件都可以隨時傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="53b68-107">Any Media Foundation component can send this event at any time.</span></span> <span data-ttu-id="53b68-108">呼叫 [**IMFMediaEvent：： GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) ，以取得失敗作業的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="53b68-108">Call [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) to get the error code of the operation that failed.</span></span>

## <a name="event-values"></a><span data-ttu-id="53b68-109">事件值</span><span class="sxs-lookup"><span data-stu-id="53b68-109">Event values</span></span>

<span data-ttu-id="53b68-110">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="53b68-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="53b68-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="53b68-111">VARTYPE</span></span>              | <span data-ttu-id="53b68-112">Description</span><span class="sxs-lookup"><span data-stu-id="53b68-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="53b68-113">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="53b68-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="53b68-114">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="53b68-114">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="53b68-115">備註</span><span class="sxs-lookup"><span data-stu-id="53b68-115">Remarks</span></span>

<span data-ttu-id="53b68-116">此事件只應用於非預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="53b68-116">This event should be used only for unexpected errors.</span></span> <span data-ttu-id="53b68-117">請勿傳送此事件來表示非同步方法失敗。</span><span class="sxs-lookup"><span data-stu-id="53b68-117">Do not send this event to signal that an asynchronous method failed.</span></span> <span data-ttu-id="53b68-118">如果非同步方法失敗，則會在該方法的正常事件中傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="53b68-118">If an asynchronous method fails, the error code is returned in the normal event for that method.</span></span>

<span data-ttu-id="53b68-119">如果串流期間發生可復原的錯誤，請傳送 [MENonFatalError](menonfatalerror.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="53b68-119">If a recoverable error occurs during streaming, send the [MENonFatalError](menonfatalerror.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="53b68-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="53b68-120">Requirements</span></span>



| <span data-ttu-id="53b68-121">需求</span><span class="sxs-lookup"><span data-stu-id="53b68-121">Requirement</span></span> | <span data-ttu-id="53b68-122">值</span><span class="sxs-lookup"><span data-stu-id="53b68-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53b68-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="53b68-123">Minimum supported client</span></span><br/> | <span data-ttu-id="53b68-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53b68-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="53b68-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="53b68-125">Minimum supported server</span></span><br/> | <span data-ttu-id="53b68-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53b68-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="53b68-127">標頭</span><span class="sxs-lookup"><span data-stu-id="53b68-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="53b68-128"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="53b68-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53b68-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53b68-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53b68-130">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="53b68-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




