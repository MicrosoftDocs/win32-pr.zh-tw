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
ms.openlocfilehash: d2a79a5a4ab6b0422705fe737ba3da4a6fd4f923
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119693"
---
# <a name="mm_mim_data-message"></a><span data-ttu-id="1f9af-104">MM \_ MIM \_ 資料訊息</span><span class="sxs-lookup"><span data-stu-id="1f9af-104">MM\_MIM\_DATA message</span></span>

<span data-ttu-id="1f9af-105">當 MIDI 輸入裝置收到完整的 MIDI 訊息時，會將 **MM \_ MIM \_ 資料** 訊息傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="1f9af-105">The **MM\_MIM\_DATA** message is sent to a window when a complete MIDI message is received by a MIDI input device.</span></span>


```C++
MM_MIM_DATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a><span data-ttu-id="1f9af-106">參數</span><span class="sxs-lookup"><span data-stu-id="1f9af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f9af-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="1f9af-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="1f9af-108">接收 MIDI 訊息之 MIDI 輸入裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1f9af-108">Handle to the MIDI input device that received the MIDI message.</span></span>

</dd> <dt>

<span data-ttu-id="1f9af-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="1f9af-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="1f9af-110">收到的 MIDI 訊息。</span><span class="sxs-lookup"><span data-stu-id="1f9af-110">MIDI message that was received.</span></span> <span data-ttu-id="1f9af-111">訊息會封裝成雙字值，如下所示：</span><span class="sxs-lookup"><span data-stu-id="1f9af-111">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="1f9af-112">需求</span><span class="sxs-lookup"><span data-stu-id="1f9af-112">Requirement</span></span> | <span data-ttu-id="1f9af-113">值</span><span class="sxs-lookup"><span data-stu-id="1f9af-113">Value</span></span> | <span data-ttu-id="1f9af-114">描述</span><span class="sxs-lookup"><span data-stu-id="1f9af-114">Description</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="1f9af-115">高單字</span><span class="sxs-lookup"><span data-stu-id="1f9af-115">High word</span></span> | <span data-ttu-id="1f9af-116">高序位位元組</span><span class="sxs-lookup"><span data-stu-id="1f9af-116">High-order byte</span></span> | <span data-ttu-id="1f9af-117">未使用。</span><span class="sxs-lookup"><span data-stu-id="1f9af-117">Not used.</span></span>                                           |
|           | <span data-ttu-id="1f9af-118">低序位位元組</span><span class="sxs-lookup"><span data-stu-id="1f9af-118">Low-order byte</span></span>  | <span data-ttu-id="1f9af-119">視需要) ，包含第二個位元組的 MIDI 資料 (。</span><span class="sxs-lookup"><span data-stu-id="1f9af-119">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="1f9af-120">低字組</span><span class="sxs-lookup"><span data-stu-id="1f9af-120">Low word</span></span>  | <span data-ttu-id="1f9af-121">高序位位元組</span><span class="sxs-lookup"><span data-stu-id="1f9af-121">High-order byte</span></span> | <span data-ttu-id="1f9af-122">當需要) 時，包含第一個 (的 MIDI 資料位元組。</span><span class="sxs-lookup"><span data-stu-id="1f9af-122">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="1f9af-123">低序位位元組</span><span class="sxs-lookup"><span data-stu-id="1f9af-123">Low-order byte</span></span>  | <span data-ttu-id="1f9af-124">包含 MIDI 狀態。</span><span class="sxs-lookup"><span data-stu-id="1f9af-124">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="1f9af-125">這兩個 MIDI 資料位元組是選擇性的，視 MIDI 狀態位元組而定。</span><span class="sxs-lookup"><span data-stu-id="1f9af-125">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f9af-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="1f9af-126">Return Value</span></span>

<span data-ttu-id="1f9af-127">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="1f9af-127">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f9af-128">備註</span><span class="sxs-lookup"><span data-stu-id="1f9af-128">Remarks</span></span>

<span data-ttu-id="1f9af-129">從 MIDI 輸入埠接收的 MIDI 訊息已停用執行中狀態;每個訊息都會展開以包含 MIDI 狀態位元組。</span><span class="sxs-lookup"><span data-stu-id="1f9af-129">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="1f9af-130">收到 MIDI 系統專屬訊息時，不會傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="1f9af-130">This message is not sent when a MIDI system-exclusive message is received.</span></span> <span data-ttu-id="1f9af-131">此訊息沒有可用的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="1f9af-131">No time stamp is available with this message.</span></span> <span data-ttu-id="1f9af-132">針對時間戳記的輸入資料，您必須使用傳送給回呼函式的訊息。</span><span class="sxs-lookup"><span data-stu-id="1f9af-132">For time-stamped input data, you must use the messages that are sent to callback functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f9af-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f9af-133">Requirements</span></span>



| <span data-ttu-id="1f9af-134">需求</span><span class="sxs-lookup"><span data-stu-id="1f9af-134">Requirement</span></span> | <span data-ttu-id="1f9af-135">值</span><span class="sxs-lookup"><span data-stu-id="1f9af-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f9af-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1f9af-136">Minimum supported client</span></span><br/> | <span data-ttu-id="1f9af-137">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1f9af-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1f9af-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1f9af-138">Minimum supported server</span></span><br/> | <span data-ttu-id="1f9af-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1f9af-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1f9af-140">標頭</span><span class="sxs-lookup"><span data-stu-id="1f9af-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f9af-141"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="1f9af-141"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f9af-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f9af-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f9af-143">樂器數位介面 (MIDI)</span><span class="sxs-lookup"><span data-stu-id="1f9af-143">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="1f9af-144">MIDI 訊息</span><span class="sxs-lookup"><span data-stu-id="1f9af-144">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





