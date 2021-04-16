---
title: 'MIM_OPEN 訊息 (Mmsystem .h) '
description: '\_開啟 midi 輸入裝置時，會將 MIM 開啟訊息傳送至 midi 輸入回撥函式。'
ms.assetid: c7a8b856-aedd-457d-8a21-0ec2e9303960
keywords:
- MIM_OPEN message Windows 多媒體
topic_type:
- apiref
api_name:
- MIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49fcfd05ef7702fbc7bf3108365e49660071ae9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383978"
---
# <a name="mim_open-message"></a><span data-ttu-id="b0765-104">MIM \_ 開啟訊息</span><span class="sxs-lookup"><span data-stu-id="b0765-104">MIM\_OPEN message</span></span>

<span data-ttu-id="b0765-105">開啟 MIDI 輸入裝置時，會將 **MIM \_ 開啟** 訊息傳送至 midi 輸入回撥函式。</span><span class="sxs-lookup"><span data-stu-id="b0765-105">The **MIM\_OPEN** message is sent to a MIDI input callback function when a MIDI input device is opened.</span></span>


```C++
MIM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="b0765-106">參數</span><span class="sxs-lookup"><span data-stu-id="b0765-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0765-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="b0765-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="b0765-108">保護請勿使用。</span><span class="sxs-lookup"><span data-stu-id="b0765-108">Reserved; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="b0765-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="b0765-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="b0765-110">保護請勿使用。</span><span class="sxs-lookup"><span data-stu-id="b0765-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0765-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b0765-111">Return Value</span></span>

<span data-ttu-id="b0765-112">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b0765-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0765-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0765-113">Requirements</span></span>



| <span data-ttu-id="b0765-114">需求</span><span class="sxs-lookup"><span data-stu-id="b0765-114">Requirement</span></span> | <span data-ttu-id="b0765-115">值</span><span class="sxs-lookup"><span data-stu-id="b0765-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0765-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b0765-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b0765-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0765-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b0765-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b0765-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b0765-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0765-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b0765-120">標頭</span><span class="sxs-lookup"><span data-stu-id="b0765-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0765-121"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b0765-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0765-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b0765-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0765-123">樂器數位介面 (MIDI)</span><span class="sxs-lookup"><span data-stu-id="b0765-123">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="b0765-124">MIDI 訊息</span><span class="sxs-lookup"><span data-stu-id="b0765-124">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





