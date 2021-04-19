---
description: 如果強制執行輸出原則時發生錯誤，則由受信任的輸出引發。
ms.assetid: 0cc62915-1ed6-4d1d-9600-0dac0b9034e3
title: 'MEPolicyError 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b75083974ee0e76d7d8e21f0a2c83c2feee8d59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980759"
---
# <a name="mepolicyerror-event"></a><span data-ttu-id="a024c-103">MEPolicyError 事件</span><span class="sxs-lookup"><span data-stu-id="a024c-103">MEPolicyError event</span></span>

<span data-ttu-id="a024c-104">如果強制執行輸出原則時發生錯誤，則由受信任的輸出引發。</span><span class="sxs-lookup"><span data-stu-id="a024c-104">Raised by a trusted output if an error occurs while enforcing the output policy.</span></span>

<span data-ttu-id="a024c-105">如果媒體會話收到此事件，它會停止播放並將事件轉送到應用程式。</span><span class="sxs-lookup"><span data-stu-id="a024c-105">If the Media Session receives this event, it stops playback and forwards the event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="a024c-106">事件值</span><span class="sxs-lookup"><span data-stu-id="a024c-106">Event values</span></span>

<span data-ttu-id="a024c-107">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="a024c-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="a024c-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="a024c-108">VARTYPE</span></span>              | <span data-ttu-id="a024c-109">Description</span><span class="sxs-lookup"><span data-stu-id="a024c-109">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="a024c-110">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="a024c-110">VT\_EMPTY</span></span><br/> | <span data-ttu-id="a024c-111">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="a024c-111">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="a024c-112">備註</span><span class="sxs-lookup"><span data-stu-id="a024c-112">Remarks</span></span>

<span data-ttu-id="a024c-113">從 [**IMFMediaEvent：： GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="a024c-113">Possible values retrieved from [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) include the following.</span></span>



| <span data-ttu-id="a024c-114">值</span><span class="sxs-lookup"><span data-stu-id="a024c-114">Value</span></span>                      | <span data-ttu-id="a024c-115">描述</span><span class="sxs-lookup"><span data-stu-id="a024c-115">Description</span></span>                                                    |
|----------------------------|----------------------------------------------------------------|
| <span data-ttu-id="a024c-116">\_ \_ 不支援 MF E 原則 \_</span><span class="sxs-lookup"><span data-stu-id="a024c-116">MF\_E\_POLICY\_UNSUPPORTED</span></span> | <span data-ttu-id="a024c-117">受信任的輸出不支援目前的輸出原則。</span><span class="sxs-lookup"><span data-stu-id="a024c-117">The trusted output does not support the current output policy.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="a024c-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="a024c-118">Requirements</span></span>



| <span data-ttu-id="a024c-119">需求</span><span class="sxs-lookup"><span data-stu-id="a024c-119">Requirement</span></span> | <span data-ttu-id="a024c-120">值</span><span class="sxs-lookup"><span data-stu-id="a024c-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a024c-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a024c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a024c-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a024c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a024c-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a024c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a024c-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a024c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a024c-125">標頭</span><span class="sxs-lookup"><span data-stu-id="a024c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a024c-126"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="a024c-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a024c-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a024c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a024c-128">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="a024c-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




