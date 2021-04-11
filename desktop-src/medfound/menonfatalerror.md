---
description: 進行串流時發生非嚴重錯誤。
ms.assetid: 04afcca5-34d9-4c99-86bc-b37c19232ec1
title: 'MENonFatalError 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6af26a87b99e9c2ef649684c4ede53e707e7084
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318824"
---
# <a name="menonfatalerror-event"></a><span data-ttu-id="31dba-103">MENonFatalError 事件</span><span class="sxs-lookup"><span data-stu-id="31dba-103">MENonFatalError event</span></span>

<span data-ttu-id="31dba-104">進行串流時發生非嚴重錯誤。</span><span class="sxs-lookup"><span data-stu-id="31dba-104">A non-fatal error occurred during streaming.</span></span> <span data-ttu-id="31dba-105">任何媒體基礎元件都可以隨時傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="31dba-105">Any Media Foundation component can send this event at any time.</span></span>

## <a name="event-values"></a><span data-ttu-id="31dba-106">事件值</span><span class="sxs-lookup"><span data-stu-id="31dba-106">Event values</span></span>

<span data-ttu-id="31dba-107">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="31dba-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="31dba-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="31dba-108">VARTYPE</span></span>            | <span data-ttu-id="31dba-109">Description</span><span class="sxs-lookup"><span data-stu-id="31dba-109">Description</span></span>                                                        |
|--------------------|--------------------------------------------------------------------|
| <span data-ttu-id="31dba-110">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="31dba-110">VT\_UI4</span></span><br/> | <span data-ttu-id="31dba-111">描述錯誤的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="31dba-111">**HRESULT** value that describes the error.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="31dba-112">屬性</span><span class="sxs-lookup"><span data-stu-id="31dba-112">Attributes</span></span>

<span data-ttu-id="31dba-113">未定義此事件的屬性。</span><span class="sxs-lookup"><span data-stu-id="31dba-113">No attributes are defined for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="31dba-114">備註</span><span class="sxs-lookup"><span data-stu-id="31dba-114">Remarks</span></span>

<span data-ttu-id="31dba-115">此事件會在串流處理期間發出未預期但可復原的錯誤。</span><span class="sxs-lookup"><span data-stu-id="31dba-115">This event signals an unexpected but recoverable error during streaming.</span></span> <span data-ttu-id="31dba-116">例如，如果媒體來源卸載封包，則可能會傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="31dba-116">For example, a media source might send this event if it drops a packet.</span></span>

<span data-ttu-id="31dba-117">請勿傳送此事件來表示非同步方法失敗。</span><span class="sxs-lookup"><span data-stu-id="31dba-117">Do not send this event to signal that an asynchronous method failed.</span></span> <span data-ttu-id="31dba-118">如果非同步方法失敗，則會在該方法的正常事件中傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="31dba-118">If an asynchronous method fails, the error code is returned in the normal event for that method.</span></span>

<span data-ttu-id="31dba-119">如果發生無法復原的串流錯誤，請傳送 [MEError](meerror.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="31dba-119">If a non-recoverable streaming error occurs, send the [MEError](meerror.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="31dba-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="31dba-120">Requirements</span></span>



| <span data-ttu-id="31dba-121">需求</span><span class="sxs-lookup"><span data-stu-id="31dba-121">Requirement</span></span> | <span data-ttu-id="31dba-122">值</span><span class="sxs-lookup"><span data-stu-id="31dba-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31dba-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="31dba-123">Minimum supported client</span></span><br/> | <span data-ttu-id="31dba-124">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31dba-124">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="31dba-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="31dba-125">Minimum supported server</span></span><br/> | <span data-ttu-id="31dba-126">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31dba-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="31dba-127">標頭</span><span class="sxs-lookup"><span data-stu-id="31dba-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="31dba-128"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="31dba-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31dba-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31dba-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31dba-130">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="31dba-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




