---
title: 'MOM_POSITIONCB 訊息 (Mmsystem .h) '
description: 當您 \_ \_ \_ 在 MIDI 輸出資料流程中到達 MEVT F 回呼事件時，會傳送 MOM 位置訊息。
ms.assetid: 0464d74d-7d1f-4aab-a9e7-03397872f3c0
keywords:
- MOM_POSITIONCB message Windows 多媒體
topic_type:
- apiref
api_name:
- MOM_POSITIONCB
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e5c9528e8f91778c53ed4761c98bb67d405ec14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686371"
---
# <a name="mom_positioncb-message"></a><span data-ttu-id="6a93b-104">MOM \_ POSITIONCB 訊息</span><span class="sxs-lookup"><span data-stu-id="6a93b-104">MOM\_POSITIONCB message</span></span>

<span data-ttu-id="6a93b-105">當您在 MIDI 輸出資料流程中到達 **MEVT \_ F \_ 回呼** 事件時，會傳送 **MOM \_ 位置** 訊息。</span><span class="sxs-lookup"><span data-stu-id="6a93b-105">The **MOM\_POSITION** message is sent when an **MEVT\_F\_CALLBACK** event is reached in the MIDI output stream.</span></span>

## <a name="parameters"></a><span data-ttu-id="6a93b-106">參數</span><span class="sxs-lookup"><span data-stu-id="6a93b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a93b-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="6a93b-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="6a93b-108">識別輸入緩衝區之 [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="6a93b-108">A pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the input buffer.</span></span>

</dd> <dt>

<span data-ttu-id="6a93b-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="6a93b-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="6a93b-110">未使用。</span><span class="sxs-lookup"><span data-stu-id="6a93b-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a93b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6a93b-111">Return Value</span></span>

<span data-ttu-id="6a93b-112">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6a93b-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a93b-113">備註</span><span class="sxs-lookup"><span data-stu-id="6a93b-113">Remarks</span></span>

<span data-ttu-id="6a93b-114">即使在執行回呼函式時，也會繼續播放資料流程緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6a93b-114">Playback of the stream buffer continues even while the callback function is executing.</span></span> <span data-ttu-id="6a93b-115">在緩衝區中 **MEVT \_ F \_ 回呼** 事件之後的任何事件都會排程，並在一段時間內傳送，不論回呼函數中花費了多少時間。</span><span class="sxs-lookup"><span data-stu-id="6a93b-115">Any events after the **MEVT\_F\_CALLBACK** event in the buffer will be scheduled and sent on time regardless of how much time is spent in the callback function.</span></span>

<span data-ttu-id="6a93b-116">如果要產生的位置回呼比您的應用程式可以處理的還要快， [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)結構的 **dwOffset** 成員可能會參考您的應用程式尚未處理的事件。</span><span class="sxs-lookup"><span data-stu-id="6a93b-116">If position callbacks are being generated more quickly than your application can process them, the **dwOffset** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure might refer to an event your application has not yet processed.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a93b-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a93b-117">Requirements</span></span>



| <span data-ttu-id="6a93b-118">需求</span><span class="sxs-lookup"><span data-stu-id="6a93b-118">Requirement</span></span> | <span data-ttu-id="6a93b-119">值</span><span class="sxs-lookup"><span data-stu-id="6a93b-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a93b-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6a93b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6a93b-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6a93b-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6a93b-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6a93b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6a93b-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6a93b-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6a93b-124">標頭</span><span class="sxs-lookup"><span data-stu-id="6a93b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a93b-125"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="6a93b-125"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a93b-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a93b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a93b-127">MIDI 訊息</span><span class="sxs-lookup"><span data-stu-id="6a93b-127">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

