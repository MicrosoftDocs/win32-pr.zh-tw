---
title: 'MIM_MOREDATA 訊息 (Mmsystem .h) '
description: '\_當 midi 輸入裝置收到 midi 訊息，但應用程式未及時處理 MIM \_ 資料訊息，以跟上輸入裝置磁碟機時，就會將 mim MOREDATA 訊息傳送至 midi 輸入回撥函式。'
ms.assetid: 74ed46ab-a18e-4df5-bf36-ab3dec7fafa5
keywords:
- MIM_MOREDATA message Windows 多媒體
topic_type:
- apiref
api_name:
- MIM_MOREDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ececb41bc0f9dc0cef187c083afc72ba5fc899a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686643"
---
# <a name="mim_moredata-message"></a><span data-ttu-id="3da3b-104">MIM \_ MOREDATA 訊息</span><span class="sxs-lookup"><span data-stu-id="3da3b-104">MIM\_MOREDATA message</span></span>

<span data-ttu-id="3da3b-105">當 MIDI 輸入裝置收到 MIDI 訊息，但應用程式未及時處理 [**MIM \_ 資料**](mim-data.md)訊息，以跟上輸入裝置磁碟機時，就會將 **mim \_ MOREDATA** 訊息傳送至 midi 輸入回撥函式。</span><span class="sxs-lookup"><span data-stu-id="3da3b-105">The **MIM\_MOREDATA** message is sent to a MIDI input callback function when a MIDI message is received by a MIDI input device but the application is not processing [**MIM\_DATA**](mim-data.md) messages fast enough to keep up with the input device driver.</span></span> <span data-ttu-id="3da3b-106">只有當應用程式在 MidiInOpen 函式 \_ \_ 的呼叫中指定 MIDI IO 狀態[](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)時，回呼函式才會收到此訊息。</span><span class="sxs-lookup"><span data-stu-id="3da3b-106">The callback function receives this message only when the application specifies MIDI\_IO\_STATUS in the call to the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function.</span></span>


```C++
MIM_MOREDATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="3da3b-107">參數</span><span class="sxs-lookup"><span data-stu-id="3da3b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3da3b-108"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="3da3b-108"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="3da3b-109">指定收到的 MIDI 訊息。</span><span class="sxs-lookup"><span data-stu-id="3da3b-109">Specifies the MIDI message that was received.</span></span> <span data-ttu-id="3da3b-110">訊息會封裝成 **DWORD** 值，如下所示：</span><span class="sxs-lookup"><span data-stu-id="3da3b-110">The message is packed into a **DWORD** value as follows:</span></span>



| <span data-ttu-id="3da3b-111">需求</span><span class="sxs-lookup"><span data-stu-id="3da3b-111">Requirement</span></span> | <span data-ttu-id="3da3b-112">值</span><span class="sxs-lookup"><span data-stu-id="3da3b-112">Value</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="3da3b-113">高單字</span><span class="sxs-lookup"><span data-stu-id="3da3b-113">High word</span></span> | <span data-ttu-id="3da3b-114">高序位位元組</span><span class="sxs-lookup"><span data-stu-id="3da3b-114">High-order byte</span></span> | <span data-ttu-id="3da3b-115">未使用。</span><span class="sxs-lookup"><span data-stu-id="3da3b-115">Not used.</span></span>                                           |
|           | <span data-ttu-id="3da3b-116">低序位位元組</span><span class="sxs-lookup"><span data-stu-id="3da3b-116">Low-order byte</span></span>  | <span data-ttu-id="3da3b-117">視需要) ，包含第二個位元組的 MIDI 資料 (。</span><span class="sxs-lookup"><span data-stu-id="3da3b-117">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="3da3b-118">低字組</span><span class="sxs-lookup"><span data-stu-id="3da3b-118">Low word</span></span>  | <span data-ttu-id="3da3b-119">高序位位元組</span><span class="sxs-lookup"><span data-stu-id="3da3b-119">High-order byte</span></span> | <span data-ttu-id="3da3b-120">當需要) 時，包含第一個 (的 MIDI 資料位元組。</span><span class="sxs-lookup"><span data-stu-id="3da3b-120">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="3da3b-121">低序位位元組</span><span class="sxs-lookup"><span data-stu-id="3da3b-121">Low-order byte</span></span>  | <span data-ttu-id="3da3b-122">包含 MIDI 狀態。</span><span class="sxs-lookup"><span data-stu-id="3da3b-122">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="3da3b-123">這兩個 MIDI 資料位元組是選擇性的，視 MIDI 狀態位元組而定。</span><span class="sxs-lookup"><span data-stu-id="3da3b-123">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> <dt>

<span data-ttu-id="3da3b-124"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span><span class="sxs-lookup"><span data-stu-id="3da3b-124"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="3da3b-125">指定輸入裝置磁碟機接收訊息的時間。</span><span class="sxs-lookup"><span data-stu-id="3da3b-125">Specifies the time that the message was received by the input device driver.</span></span> <span data-ttu-id="3da3b-126">時間戳記是以毫秒為單位來指定，從0開始呼叫 [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) 函式。</span><span class="sxs-lookup"><span data-stu-id="3da3b-126">The time stamp is specified in milliseconds, beginning at 0 when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3da3b-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="3da3b-127">Return Value</span></span>

<span data-ttu-id="3da3b-128">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="3da3b-128">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3da3b-129">備註</span><span class="sxs-lookup"><span data-stu-id="3da3b-129">Remarks</span></span>

<span data-ttu-id="3da3b-130">應用程式應該只進行最低限度的 MIM \_ MOREDATA 訊息處理。</span><span class="sxs-lookup"><span data-stu-id="3da3b-130">An application should do only a minimal amount of processing of MIM\_MOREDATA messages.</span></span> <span data-ttu-id="3da3b-131"> (特別是，應用程式在處理 MIM MOREDATA 時不應呼叫 [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) 函式 \_ 。 ) 相反地，應用程式應該將事件資料放入緩衝區，然後再傳回。</span><span class="sxs-lookup"><span data-stu-id="3da3b-131">(In particular, applications should not call the [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) function while processing MIM\_MOREDATA.) Instead, the application should place the event data into a buffer and then return.</span></span>

<span data-ttu-id="3da3b-132">當應用程式在一系列的 MIM MOREDATA 訊息之後收到 [**mim \_ 資料**](mim-data.md) 訊息時 \_ ，它會攔截傳入的 MIDI 事件，並且可以安全地呼叫需要大量時間的函式。</span><span class="sxs-lookup"><span data-stu-id="3da3b-132">When an application receives an [**MIM\_DATA**](mim-data.md) message after a series of MIM\_MOREDATA messages, it has caught up with incoming MIDI events and can safely call time-intensive functions.</span></span>

<span data-ttu-id="3da3b-133">從 MIDI 輸入埠接收的 MIDI 訊息已停用執行中狀態;每個訊息都會展開以包含 MIDI 狀態位元組。</span><span class="sxs-lookup"><span data-stu-id="3da3b-133">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="3da3b-134">收到 MIDI 系統專屬訊息時，不會傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="3da3b-134">This message is not sent when a MIDI system-exclusive message is received.</span></span>

## <a name="requirements"></a><span data-ttu-id="3da3b-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="3da3b-135">Requirements</span></span>



| <span data-ttu-id="3da3b-136">需求</span><span class="sxs-lookup"><span data-stu-id="3da3b-136">Requirement</span></span> | <span data-ttu-id="3da3b-137">值</span><span class="sxs-lookup"><span data-stu-id="3da3b-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3da3b-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3da3b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="3da3b-139">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3da3b-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3da3b-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3da3b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="3da3b-141">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3da3b-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3da3b-142">標頭</span><span class="sxs-lookup"><span data-stu-id="3da3b-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="3da3b-143"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="3da3b-143"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3da3b-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3da3b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3da3b-145">樂器數位介面 (MIDI)</span><span class="sxs-lookup"><span data-stu-id="3da3b-145">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="3da3b-146">MIDI 訊息</span><span class="sxs-lookup"><span data-stu-id="3da3b-146">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

