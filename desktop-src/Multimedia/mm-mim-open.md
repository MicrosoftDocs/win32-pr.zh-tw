---
title: 'MM_MIM_OPEN 訊息 (Mmsystem .h) '
description: '\_ \_ 當開啟 MIDI 輸入裝置時，會將 MM MIM 開啟訊息傳送至視窗。'
ms.assetid: 8dfc24a0-0ab8-4f49-954f-0c0a55fa28bc
keywords:
- MM_MIM_OPEN message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_MIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7d87e391336b948d0c784048baeffa7bba88b29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843040"
---
# <a name="mm_mim_open-message"></a><span data-ttu-id="b150d-104">MM \_ MIM \_ 開啟訊息</span><span class="sxs-lookup"><span data-stu-id="b150d-104">MM\_MIM\_OPEN message</span></span>

<span data-ttu-id="b150d-105">當開啟 MIDI 輸入裝置時，會將 **MM \_ MIM \_ 開啟** 訊息傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="b150d-105">The **MM\_MIM\_OPEN** message is sent to a window when a MIDI input device is opened.</span></span>


```C++
MM_MIM_OPEN 
wParam = (WPARAM) hInput 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="b150d-106">參數</span><span class="sxs-lookup"><span data-stu-id="b150d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b150d-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="b150d-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="b150d-108">開啟之 MIDI 輸入裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b150d-108">Handle to the MIDI input device that was opened.</span></span>

</dd> <dt>

<span data-ttu-id="b150d-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="b150d-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="b150d-110">保護請勿使用。</span><span class="sxs-lookup"><span data-stu-id="b150d-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b150d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b150d-111">Return Value</span></span>

<span data-ttu-id="b150d-112">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b150d-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b150d-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="b150d-113">Requirements</span></span>



| <span data-ttu-id="b150d-114">需求</span><span class="sxs-lookup"><span data-stu-id="b150d-114">Requirement</span></span> | <span data-ttu-id="b150d-115">值</span><span class="sxs-lookup"><span data-stu-id="b150d-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b150d-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b150d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b150d-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b150d-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b150d-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b150d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b150d-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b150d-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b150d-120">標頭</span><span class="sxs-lookup"><span data-stu-id="b150d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b150d-121"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b150d-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b150d-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b150d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b150d-123">樂器數位介面 (MIDI)</span><span class="sxs-lookup"><span data-stu-id="b150d-123">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="b150d-124">MIDI 訊息</span><span class="sxs-lookup"><span data-stu-id="b150d-124">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





