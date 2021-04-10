---
title: 'MIM_DATA 訊息 (Mmsystem .h) '
description: '\_當 midi 輸入裝置收到 midi 訊息時，會將 MIM 資料訊息傳送至 midi 輸入回撥函式。'
ms.assetid: 966aab84-420a-42ce-9989-da5910ced9c0
keywords:
- MIM_DATA message Windows 多媒體
topic_type:
- apiref
api_name:
- MIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48f96d2c23e64700a7a923cdd7633dabfcba9d1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844403"
---
# <a name="mim_data-message"></a><span data-ttu-id="801ca-104">MIM \_ 資料訊息</span><span class="sxs-lookup"><span data-stu-id="801ca-104">MIM\_DATA message</span></span>

<span data-ttu-id="801ca-105">當 MIDI 輸入裝置收到 MIDI 訊息時，會將 **MIM \_ 資料** 訊息傳送至 midi 輸入回撥函式。</span><span class="sxs-lookup"><span data-stu-id="801ca-105">The **MIM\_DATA** message is sent to a MIDI input callback function when a MIDI message is received by a MIDI input device.</span></span>


```C++
MIM_DATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="801ca-106">參數</span><span class="sxs-lookup"><span data-stu-id="801ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="801ca-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="801ca-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="801ca-108">收到的 MIDI 訊息。</span><span class="sxs-lookup"><span data-stu-id="801ca-108">MIDI message that was received.</span></span> <span data-ttu-id="801ca-109">訊息會封裝成雙字值，如下所示：</span><span class="sxs-lookup"><span data-stu-id="801ca-109">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="801ca-110">需求</span><span class="sxs-lookup"><span data-stu-id="801ca-110">Requirement</span></span> | <span data-ttu-id="801ca-111">值</span><span class="sxs-lookup"><span data-stu-id="801ca-111">Value</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="801ca-112">高單字</span><span class="sxs-lookup"><span data-stu-id="801ca-112">High word</span></span> | <span data-ttu-id="801ca-113">高序位位元組</span><span class="sxs-lookup"><span data-stu-id="801ca-113">High-order byte</span></span> | <span data-ttu-id="801ca-114">未使用。</span><span class="sxs-lookup"><span data-stu-id="801ca-114">Not used.</span></span>                                           |
|           | <span data-ttu-id="801ca-115">低序位位元組</span><span class="sxs-lookup"><span data-stu-id="801ca-115">Low-order byte</span></span>  | <span data-ttu-id="801ca-116">視需要) ，包含第二個位元組的 MIDI 資料 (。</span><span class="sxs-lookup"><span data-stu-id="801ca-116">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="801ca-117">低字組</span><span class="sxs-lookup"><span data-stu-id="801ca-117">Low word</span></span>  | <span data-ttu-id="801ca-118">高序位位元組</span><span class="sxs-lookup"><span data-stu-id="801ca-118">High-order byte</span></span> | <span data-ttu-id="801ca-119">當需要) 時，包含第一個 (的 MIDI 資料位元組。</span><span class="sxs-lookup"><span data-stu-id="801ca-119">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="801ca-120">低序位位元組</span><span class="sxs-lookup"><span data-stu-id="801ca-120">Low-order byte</span></span>  | <span data-ttu-id="801ca-121">包含 MIDI 狀態。</span><span class="sxs-lookup"><span data-stu-id="801ca-121">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="801ca-122">這兩個 MIDI 資料位元組是選擇性的，視 MIDI 狀態位元組而定。</span><span class="sxs-lookup"><span data-stu-id="801ca-122">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> <dt>

<span data-ttu-id="801ca-123"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span><span class="sxs-lookup"><span data-stu-id="801ca-123"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="801ca-124">輸入裝置磁碟機收到訊息的時間。</span><span class="sxs-lookup"><span data-stu-id="801ca-124">Time that the message was received by the input device driver.</span></span> <span data-ttu-id="801ca-125">時間戳記是以毫秒為單位來指定，在呼叫 [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) 函式時從零開始。</span><span class="sxs-lookup"><span data-stu-id="801ca-125">The time stamp is specified in milliseconds, beginning at zero when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="801ca-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="801ca-126">Return Value</span></span>

<span data-ttu-id="801ca-127">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="801ca-127">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="801ca-128">備註</span><span class="sxs-lookup"><span data-stu-id="801ca-128">Remarks</span></span>

<span data-ttu-id="801ca-129">從 MIDI 輸入埠接收的 MIDI 訊息已停用執行中狀態;每個訊息都會展開以包含 MIDI 狀態位元組。</span><span class="sxs-lookup"><span data-stu-id="801ca-129">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="801ca-130">收到 MIDI 系統專屬訊息時，不會傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="801ca-130">This message is not sent when a MIDI system-exclusive message is received.</span></span>

## <a name="requirements"></a><span data-ttu-id="801ca-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="801ca-131">Requirements</span></span>



| <span data-ttu-id="801ca-132">需求</span><span class="sxs-lookup"><span data-stu-id="801ca-132">Requirement</span></span> | <span data-ttu-id="801ca-133">值</span><span class="sxs-lookup"><span data-stu-id="801ca-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="801ca-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="801ca-134">Minimum supported client</span></span><br/> | <span data-ttu-id="801ca-135">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="801ca-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="801ca-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="801ca-136">Minimum supported server</span></span><br/> | <span data-ttu-id="801ca-137">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="801ca-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="801ca-138">標頭</span><span class="sxs-lookup"><span data-stu-id="801ca-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="801ca-139"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="801ca-139"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="801ca-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="801ca-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="801ca-141">樂器數位介面 (MIDI)</span><span class="sxs-lookup"><span data-stu-id="801ca-141">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="801ca-142">MIDI 訊息</span><span class="sxs-lookup"><span data-stu-id="801ca-142">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

