---
title: 'MM_MIM_MOREDATA 訊息 (Mmsystem .h) '
description: '\_ \_ 當 midi 輸入裝置收到 midi 訊息時，會將 MM mim MOREDATA 訊息傳送至回呼視窗，但應用程式不會快速處理 MIM \_ 資料訊息，而足以跟上輸入裝置磁碟機。'
ms.assetid: 25d507f9-01d4-4a9a-afdd-693d74e3bd22
keywords:
- MM_MIM_MOREDATA message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_MIM_MOREDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67835a67c957a250fe1ae6d391f5ebd56d5301b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025069"
---
# <a name="mm_mim_moredata-message"></a><span data-ttu-id="caf7c-104">MM \_ MIM \_ MOREDATA 訊息</span><span class="sxs-lookup"><span data-stu-id="caf7c-104">MM\_MIM\_MOREDATA message</span></span>

<span data-ttu-id="caf7c-105">當 MIDI 輸入裝置收到 MIDI 訊息時，會將 **MM \_ mim \_ MOREDATA** 訊息傳送至回呼視窗，但應用程式不會快速處理 [**MIM \_ 資料**](mim-data.md) 訊息，而足以跟上輸入裝置磁碟機。</span><span class="sxs-lookup"><span data-stu-id="caf7c-105">The **MM\_MIM\_MOREDATA** message is sent to a callback window when a MIDI message is received by a MIDI input device but the application is not processing [**MIM\_DATA**](mim-data.md) messages fast enough to keep up with the input device driver.</span></span> <span data-ttu-id="caf7c-106">只有當應用程式在 MidiInOpen 函式 \_ \_ 的呼叫中指定了 MIDI IO 狀態[](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)時，此視窗才會收到此訊息。</span><span class="sxs-lookup"><span data-stu-id="caf7c-106">The window receives this message only when the application specifies MIDI\_IO\_STATUS in the call to the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function.</span></span>


```C++
MM_MIM_MOREDATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a><span data-ttu-id="caf7c-107">參數</span><span class="sxs-lookup"><span data-stu-id="caf7c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="caf7c-108"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="caf7c-108"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="caf7c-109">接收 MIDI 訊息之 MIDI 輸入裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="caf7c-109">Handle to the MIDI input device that received the MIDI message.</span></span>

</dd> <dt>

<span data-ttu-id="caf7c-110"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="caf7c-110"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="caf7c-111">指定收到的 MIDI 訊息。</span><span class="sxs-lookup"><span data-stu-id="caf7c-111">Specifies the MIDI message that was received.</span></span> <span data-ttu-id="caf7c-112">訊息會封裝成雙字值，如下所示：</span><span class="sxs-lookup"><span data-stu-id="caf7c-112">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="caf7c-113">需求</span><span class="sxs-lookup"><span data-stu-id="caf7c-113">Requirement</span></span> | <span data-ttu-id="caf7c-114">值</span><span class="sxs-lookup"><span data-stu-id="caf7c-114">Value</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="caf7c-115">高單字</span><span class="sxs-lookup"><span data-stu-id="caf7c-115">High word</span></span> | <span data-ttu-id="caf7c-116">高序位位元組</span><span class="sxs-lookup"><span data-stu-id="caf7c-116">High-order byte</span></span> | <span data-ttu-id="caf7c-117">未使用。</span><span class="sxs-lookup"><span data-stu-id="caf7c-117">Not used.</span></span>                                           |
|           | <span data-ttu-id="caf7c-118">低序位位元組</span><span class="sxs-lookup"><span data-stu-id="caf7c-118">Low-order byte</span></span>  | <span data-ttu-id="caf7c-119">視需要) ，包含第二個位元組的 MIDI 資料 (。</span><span class="sxs-lookup"><span data-stu-id="caf7c-119">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="caf7c-120">低字組</span><span class="sxs-lookup"><span data-stu-id="caf7c-120">Low word</span></span>  | <span data-ttu-id="caf7c-121">高序位位元組</span><span class="sxs-lookup"><span data-stu-id="caf7c-121">High-order byte</span></span> | <span data-ttu-id="caf7c-122">當需要) 時，包含第一個 (的 MIDI 資料位元組。</span><span class="sxs-lookup"><span data-stu-id="caf7c-122">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="caf7c-123">低序位位元組</span><span class="sxs-lookup"><span data-stu-id="caf7c-123">Low-order byte</span></span>  | <span data-ttu-id="caf7c-124">包含 MIDI 狀態。</span><span class="sxs-lookup"><span data-stu-id="caf7c-124">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="caf7c-125">這兩個 MIDI 資料位元組是選擇性的，視 MIDI 狀態位元組而定。</span><span class="sxs-lookup"><span data-stu-id="caf7c-125">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="caf7c-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="caf7c-126">Return Value</span></span>

<span data-ttu-id="caf7c-127">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="caf7c-127">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="caf7c-128">備註</span><span class="sxs-lookup"><span data-stu-id="caf7c-128">Remarks</span></span>

<span data-ttu-id="caf7c-129">如果您的應用程式將會以更快的速度接收 MIDI 資料，則您不應該使用視窗回呼機制。</span><span class="sxs-lookup"><span data-stu-id="caf7c-129">If your application will receive MIDI data faster than it can process it, you should not use a window callback mechanism.</span></span> <span data-ttu-id="caf7c-130">若要最大化速度，請使用回呼函式，並使用 [**mim \_ MOREDATA**](mim-moredata.md) 訊息，而不是使用 \_ mim \_ MOREDATA。</span><span class="sxs-lookup"><span data-stu-id="caf7c-130">To maximize speed, use a callback function, and use the [**MIM\_MOREDATA**](mim-moredata.md) message instead of MM\_MIM\_MOREDATA.</span></span>

<span data-ttu-id="caf7c-131">應用程式應該只對 MM \_ MIM MOREDATA 訊息進行最低限度的處理 \_ 。</span><span class="sxs-lookup"><span data-stu-id="caf7c-131">An application should do only a minimal amount of processing of MM\_MIM\_MOREDATA messages.</span></span> <span data-ttu-id="caf7c-132"> (特別是，應用程式在處理 MM MIM MOREDATA 時不應呼叫 [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) 函式 \_ \_ 。 ) 相反地，應用程式應該將事件資料放入緩衝區，然後再傳回。</span><span class="sxs-lookup"><span data-stu-id="caf7c-132">(In particular, applications should not call the [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) function while processing MM\_MIM\_MOREDATA.) Instead, the application should place the event data into a buffer and then return.</span></span>

<span data-ttu-id="caf7c-133">當應用程式在一系列的 MOREDATA 訊息之後收到 [**mm \_ mim \_ 資料**](mm-mim-data.md) 訊息時 \_ ，它會攔截 \_ 傳入的 MIDI 事件，並且可以安全地呼叫需要大量時間的函式。</span><span class="sxs-lookup"><span data-stu-id="caf7c-133">When an application receives an [**MM\_MIM\_DATA**](mm-mim-data.md) message after a series of MM\_MIM\_MOREDATA messages, it has caught up with incoming MIDI events and can safely call time-intensive functions.</span></span>

<span data-ttu-id="caf7c-134">從 MIDI 輸入埠接收的 MIDI 訊息已停用執行中狀態;每個訊息都會展開以包含 MIDI 狀態位元組。</span><span class="sxs-lookup"><span data-stu-id="caf7c-134">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="caf7c-135">收到 MIDI 系統專屬訊息時，不會傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="caf7c-135">This message is not sent when a MIDI system-exclusive message is received.</span></span> <span data-ttu-id="caf7c-136">此訊息沒有可用的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="caf7c-136">No time stamp is available with this message.</span></span> <span data-ttu-id="caf7c-137">針對時間戳記的輸入資料，您必須使用傳送給回呼函式的訊息。</span><span class="sxs-lookup"><span data-stu-id="caf7c-137">For time-stamped input data, you must use the messages that are sent to callback functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="caf7c-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="caf7c-138">Requirements</span></span>



| <span data-ttu-id="caf7c-139">需求</span><span class="sxs-lookup"><span data-stu-id="caf7c-139">Requirement</span></span> | <span data-ttu-id="caf7c-140">值</span><span class="sxs-lookup"><span data-stu-id="caf7c-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="caf7c-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="caf7c-141">Minimum supported client</span></span><br/> | <span data-ttu-id="caf7c-142">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="caf7c-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="caf7c-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="caf7c-143">Minimum supported server</span></span><br/> | <span data-ttu-id="caf7c-144">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="caf7c-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="caf7c-145">標頭</span><span class="sxs-lookup"><span data-stu-id="caf7c-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="caf7c-146"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="caf7c-146"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="caf7c-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="caf7c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caf7c-148">樂器數位介面 (MIDI)</span><span class="sxs-lookup"><span data-stu-id="caf7c-148">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="caf7c-149">MIDI 訊息</span><span class="sxs-lookup"><span data-stu-id="caf7c-149">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

