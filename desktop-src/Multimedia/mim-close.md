---
title: 'MIM_CLOSE 訊息 (Mmsystem .h) '
description: '\_當 midi 輸入裝置關閉時，會將 MIM 關閉訊息傳送至 midi 輸入回撥函式。'
ms.assetid: c19ecd3a-c3a5-4f17-9d44-d0d71eefcb15
keywords:
- MIM_CLOSE message Windows 多媒體
topic_type:
- apiref
api_name:
- MIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5549d9bef1e802b0b34ab6437b1386519a25d349
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508328"
---
# <a name="mim_close-message"></a><span data-ttu-id="0d1a1-104">MIM \_ 關閉訊息</span><span class="sxs-lookup"><span data-stu-id="0d1a1-104">MIM\_CLOSE message</span></span>

<span data-ttu-id="0d1a1-105">當 MIDI 輸入裝置關閉時，會將 **MIM \_ 關閉** 訊息傳送至 midi 輸入回撥函式。</span><span class="sxs-lookup"><span data-stu-id="0d1a1-105">The **MIM\_CLOSE** message is sent to a MIDI input callback function when a MIDI input device is closed.</span></span>


```C++
MIM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="0d1a1-106">參數</span><span class="sxs-lookup"><span data-stu-id="0d1a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d1a1-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="0d1a1-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="0d1a1-108">保護請勿使用。</span><span class="sxs-lookup"><span data-stu-id="0d1a1-108">Reserved; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="0d1a1-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="0d1a1-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="0d1a1-110">保護請勿使用。</span><span class="sxs-lookup"><span data-stu-id="0d1a1-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d1a1-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="0d1a1-111">Return Value</span></span>

<span data-ttu-id="0d1a1-112">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0d1a1-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d1a1-113">備註</span><span class="sxs-lookup"><span data-stu-id="0d1a1-113">Remarks</span></span>

<span data-ttu-id="0d1a1-114">傳送此訊息之後，裝置控制碼已不再有效。</span><span class="sxs-lookup"><span data-stu-id="0d1a1-114">The device handle is no longer valid after this message has been sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d1a1-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d1a1-115">Requirements</span></span>



| <span data-ttu-id="0d1a1-116">需求</span><span class="sxs-lookup"><span data-stu-id="0d1a1-116">Requirement</span></span> | <span data-ttu-id="0d1a1-117">值</span><span class="sxs-lookup"><span data-stu-id="0d1a1-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d1a1-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0d1a1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0d1a1-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0d1a1-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0d1a1-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0d1a1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0d1a1-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0d1a1-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0d1a1-122">標頭</span><span class="sxs-lookup"><span data-stu-id="0d1a1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d1a1-123"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="0d1a1-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d1a1-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d1a1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d1a1-125">樂器數位介面 (MIDI)</span><span class="sxs-lookup"><span data-stu-id="0d1a1-125">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="0d1a1-126">MIDI 訊息</span><span class="sxs-lookup"><span data-stu-id="0d1a1-126">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





