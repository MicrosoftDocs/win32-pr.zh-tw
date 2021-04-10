---
title: 'MM_MOM_POSITIONCB 訊息 (Mmsystem .h) '
description: 當您 \_ \_ \_ \_ 在 MIDI 輸出資料流程中到達 MEVT F 回呼事件時，會將 MM MOM POSITIONCB 訊息傳送至視窗。
ms.assetid: afd2ba4c-ff6a-4e47-a7e8-a0da62650963
keywords:
- MM_MOM_POSITIONCB message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_MOM_POSITIONCB
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86fd6f34ab44d307bbbb0e5fc9fd61d083ccda4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933979"
---
# <a name="mm_mom_positioncb-message"></a><span data-ttu-id="8d446-104">MM \_ MOM \_ POSITIONCB 訊息</span><span class="sxs-lookup"><span data-stu-id="8d446-104">MM\_MOM\_POSITIONCB message</span></span>

<span data-ttu-id="8d446-105">當 **您 \_ \_** \_ \_ 在 MIDI 輸出資料流程中到達 MEVT F 回呼事件時，會將 MM MOM POSITIONCB 訊息傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="8d446-105">The **MM\_MOM\_POSITIONCB** message is sent to a window when an MEVT\_F\_CALLBACK event is reached in the MIDI output stream.</span></span>


```C++
MM_MOM_POSITIONCB 
wParam = (WPARAM) lpMidiHdr 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="8d446-106">參數</span><span class="sxs-lookup"><span data-stu-id="8d446-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d446-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span><span class="sxs-lookup"><span data-stu-id="8d446-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="8d446-108">[**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)結構的指標，可識別造成回呼的事件。</span><span class="sxs-lookup"><span data-stu-id="8d446-108">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure that identifies the event that caused the callback.</span></span> <span data-ttu-id="8d446-109">**DwOffset** 成員會提供事件的位移。</span><span class="sxs-lookup"><span data-stu-id="8d446-109">The **dwOffset** member gives the offset of the event.</span></span>

</dd> <dt>

<span data-ttu-id="8d446-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="8d446-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="8d446-111">保護請勿使用。</span><span class="sxs-lookup"><span data-stu-id="8d446-111">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d446-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="8d446-112">Return Value</span></span>

<span data-ttu-id="8d446-113">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8d446-113">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d446-114">備註</span><span class="sxs-lookup"><span data-stu-id="8d446-114">Remarks</span></span>

<span data-ttu-id="8d446-115">即使在執行回呼函式時，也會繼續播放資料流程緩衝區。</span><span class="sxs-lookup"><span data-stu-id="8d446-115">Playback of the stream buffer continues even while the callback function is executing.</span></span> <span data-ttu-id="8d446-116">在 \_ 緩衝區中 MEVT F 回呼事件之後的任何事件 \_ 都會排程，並在一段時間內傳送，不論回呼函數中花費了多少時間。</span><span class="sxs-lookup"><span data-stu-id="8d446-116">Any events after the MEVT\_F\_CALLBACK event in the buffer will be scheduled and sent on time regardless of how much time is spent in the callback function.</span></span>

<span data-ttu-id="8d446-117">如果要產生的位置回呼比您的應用程式可以處理的還要快， [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)結構的 **dwOffset** 成員可能會參考您的應用程式尚未處理的事件。</span><span class="sxs-lookup"><span data-stu-id="8d446-117">If position callbacks are being generated more quickly than your application can process them, the **dwOffset** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure might refer to an event your application has not yet processed.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d446-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d446-118">Requirements</span></span>



| <span data-ttu-id="8d446-119">需求</span><span class="sxs-lookup"><span data-stu-id="8d446-119">Requirement</span></span> | <span data-ttu-id="8d446-120">值</span><span class="sxs-lookup"><span data-stu-id="8d446-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d446-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8d446-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8d446-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8d446-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8d446-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8d446-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8d446-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8d446-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8d446-125">標頭</span><span class="sxs-lookup"><span data-stu-id="8d446-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d446-126"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="8d446-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d446-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8d446-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d446-128">MIDI 訊息</span><span class="sxs-lookup"><span data-stu-id="8d446-128">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

