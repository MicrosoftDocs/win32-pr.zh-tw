---
title: 'MM_MIM_DATA 訊息 (Mmsystem .h) '
description: '\_ \_ 當 midi 輸入裝置收到完整的 midi 訊息時，會將 MM MIM 資料訊息傳送至視窗。'
ms.assetid: 9c580e48-78f3-4914-bdea-393823fb8482
keywords:
- MM_MIM_DATA message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_MIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa8c015ba5e08302f7567fe8f474bedca74d3064
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024701"
---
# <a name="mm_mim_data-message"></a><span data-ttu-id="04433-104">MM \_ MIM \_ 資料訊息</span><span class="sxs-lookup"><span data-stu-id="04433-104">MM\_MIM\_DATA message</span></span>

<span data-ttu-id="04433-105">當 MIDI 輸入裝置收到完整的 MIDI 訊息時，會將 **MM \_ MIM \_ 資料** 訊息傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="04433-105">The **MM\_MIM\_DATA** message is sent to a window when a complete MIDI message is received by a MIDI input device.</span></span>


```C++
MM_MIM_DATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a><span data-ttu-id="04433-106">參數</span><span class="sxs-lookup"><span data-stu-id="04433-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04433-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="04433-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="04433-108">接收 MIDI 訊息之 MIDI 輸入裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="04433-108">Handle to the MIDI input device that received the MIDI message.</span></span>

</dd> <dt>

<span data-ttu-id="04433-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="04433-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="04433-110">收到的 MIDI 訊息。</span><span class="sxs-lookup"><span data-stu-id="04433-110">MIDI message that was received.</span></span> <span data-ttu-id="04433-111">訊息會封裝成雙字值，如下所示：</span><span class="sxs-lookup"><span data-stu-id="04433-111">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="04433-112">需求</span><span class="sxs-lookup"><span data-stu-id="04433-112">Requirement</span></span> | <span data-ttu-id="04433-113">值</span><span class="sxs-lookup"><span data-stu-id="04433-113">Value</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="04433-114">高單字</span><span class="sxs-lookup"><span data-stu-id="04433-114">High word</span></span> | <span data-ttu-id="04433-115">高序位位元組</span><span class="sxs-lookup"><span data-stu-id="04433-115">High-order byte</span></span> | <span data-ttu-id="04433-116">未使用。</span><span class="sxs-lookup"><span data-stu-id="04433-116">Not used.</span></span>                                           |
|           | <span data-ttu-id="04433-117">低序位位元組</span><span class="sxs-lookup"><span data-stu-id="04433-117">Low-order byte</span></span>  | <span data-ttu-id="04433-118">視需要) ，包含第二個位元組的 MIDI 資料 (。</span><span class="sxs-lookup"><span data-stu-id="04433-118">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="04433-119">低字組</span><span class="sxs-lookup"><span data-stu-id="04433-119">Low word</span></span>  | <span data-ttu-id="04433-120">高序位位元組</span><span class="sxs-lookup"><span data-stu-id="04433-120">High-order byte</span></span> | <span data-ttu-id="04433-121">當需要) 時，包含第一個 (的 MIDI 資料位元組。</span><span class="sxs-lookup"><span data-stu-id="04433-121">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="04433-122">低序位位元組</span><span class="sxs-lookup"><span data-stu-id="04433-122">Low-order byte</span></span>  | <span data-ttu-id="04433-123">包含 MIDI 狀態。</span><span class="sxs-lookup"><span data-stu-id="04433-123">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="04433-124">這兩個 MIDI 資料位元組是選擇性的，視 MIDI 狀態位元組而定。</span><span class="sxs-lookup"><span data-stu-id="04433-124">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04433-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="04433-125">Return Value</span></span>

<span data-ttu-id="04433-126">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="04433-126">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="04433-127">備註</span><span class="sxs-lookup"><span data-stu-id="04433-127">Remarks</span></span>

<span data-ttu-id="04433-128">從 MIDI 輸入埠接收的 MIDI 訊息已停用執行中狀態;每個訊息都會展開以包含 MIDI 狀態位元組。</span><span class="sxs-lookup"><span data-stu-id="04433-128">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="04433-129">收到 MIDI 系統專屬訊息時，不會傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="04433-129">This message is not sent when a MIDI system-exclusive message is received.</span></span> <span data-ttu-id="04433-130">此訊息沒有可用的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="04433-130">No time stamp is available with this message.</span></span> <span data-ttu-id="04433-131">針對時間戳記的輸入資料，您必須使用傳送給回呼函式的訊息。</span><span class="sxs-lookup"><span data-stu-id="04433-131">For time-stamped input data, you must use the messages that are sent to callback functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="04433-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="04433-132">Requirements</span></span>



| <span data-ttu-id="04433-133">需求</span><span class="sxs-lookup"><span data-stu-id="04433-133">Requirement</span></span> | <span data-ttu-id="04433-134">值</span><span class="sxs-lookup"><span data-stu-id="04433-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04433-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="04433-135">Minimum supported client</span></span><br/> | <span data-ttu-id="04433-136">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04433-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="04433-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="04433-137">Minimum supported server</span></span><br/> | <span data-ttu-id="04433-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04433-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="04433-139">標頭</span><span class="sxs-lookup"><span data-stu-id="04433-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="04433-140"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="04433-140"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04433-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04433-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04433-142">樂器數位介面 (MIDI)</span><span class="sxs-lookup"><span data-stu-id="04433-142">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="04433-143">MIDI 訊息</span><span class="sxs-lookup"><span data-stu-id="04433-143">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





