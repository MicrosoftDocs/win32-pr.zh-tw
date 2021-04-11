---
title: 'MM_MIM_CLOSE 訊息 (Mmsystem .h) '
description: '\_ \_ 當 MIDI 輸入裝置關閉時，會將 MM MIM 關閉訊息傳送至視窗。'
ms.assetid: 261021aa-4df6-44d8-aad3-5f98b1213459
keywords:
- MM_MIM_CLOSE message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_MIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8ce511365b1faa49faefaf4ed25c5b8befb2288
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934680"
---
# <a name="mm_mim_close-message"></a><span data-ttu-id="fa136-104">MM \_ MIM \_ 關閉訊息</span><span class="sxs-lookup"><span data-stu-id="fa136-104">MM\_MIM\_CLOSE message</span></span>

<span data-ttu-id="fa136-105">當 MIDI 輸入裝置關閉時，會將 **MM \_ MIM \_ 關閉** 訊息傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="fa136-105">The **MM\_MIM\_CLOSE** message is sent to a window when a MIDI input device is closed.</span></span>


```C++
MM_MIM_CLOSE 
wParam = (WPARAM) hInput 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="fa136-106">參數</span><span class="sxs-lookup"><span data-stu-id="fa136-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa136-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="fa136-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="fa136-108">已關閉之 MIDI 輸入裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fa136-108">Handle to the MIDI input device that was closed.</span></span>

</dd> <dt>

<span data-ttu-id="fa136-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="fa136-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="fa136-110">保護請勿使用。</span><span class="sxs-lookup"><span data-stu-id="fa136-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa136-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="fa136-111">Return Value</span></span>

<span data-ttu-id="fa136-112">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="fa136-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa136-113">備註</span><span class="sxs-lookup"><span data-stu-id="fa136-113">Remarks</span></span>

<span data-ttu-id="fa136-114">傳送此訊息之後，裝置控制碼已不再有效。</span><span class="sxs-lookup"><span data-stu-id="fa136-114">The device handle is no longer valid after this message has been sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa136-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa136-115">Requirements</span></span>



| <span data-ttu-id="fa136-116">需求</span><span class="sxs-lookup"><span data-stu-id="fa136-116">Requirement</span></span> | <span data-ttu-id="fa136-117">值</span><span class="sxs-lookup"><span data-stu-id="fa136-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa136-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa136-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fa136-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa136-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fa136-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa136-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fa136-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa136-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fa136-122">標頭</span><span class="sxs-lookup"><span data-stu-id="fa136-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa136-123"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="fa136-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa136-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa136-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa136-125">樂器數位介面 (MIDI)</span><span class="sxs-lookup"><span data-stu-id="fa136-125">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="fa136-126">MIDI 訊息</span><span class="sxs-lookup"><span data-stu-id="fa136-126">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





