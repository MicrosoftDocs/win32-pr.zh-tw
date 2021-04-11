---
title: 'MIM_ERROR 訊息 (Mmsystem .h) '
description: '\_收到不正確 midi 訊息時，會將 MIM 錯誤訊息傳送至 MIDI 輸入回撥函式。'
ms.assetid: ea720da5-1f18-4d0d-ac9d-45cd1c3219d6
keywords:
- MIM_ERROR message Windows 多媒體
topic_type:
- apiref
api_name:
- MIM_ERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: add5b675a557ab25d41e79d99864e090364d384c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093992"
---
# <a name="mim_error-message"></a><span data-ttu-id="a3ad2-104">MIM \_ 錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="a3ad2-104">MIM\_ERROR message</span></span>

<span data-ttu-id="a3ad2-105">收到不正確 MIDI 訊息時，會將 **MIM \_ 錯誤** 訊息傳送至 MIDI 輸入回撥函式。</span><span class="sxs-lookup"><span data-stu-id="a3ad2-105">The **MIM\_ERROR** message is sent to a MIDI input callback function when an invalid MIDI message is received.</span></span>


```C++
MIM_ERROR 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="a3ad2-106">參數</span><span class="sxs-lookup"><span data-stu-id="a3ad2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3ad2-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="a3ad2-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="a3ad2-108">收到的 MIDI 訊息無效。</span><span class="sxs-lookup"><span data-stu-id="a3ad2-108">Invalid MIDI message that was received.</span></span> <span data-ttu-id="a3ad2-109">訊息會以低序位位元組中訊息的第一個位元組，封裝成雙位元組值。</span><span class="sxs-lookup"><span data-stu-id="a3ad2-109">The message is packed into a doubleword value with the first byte of the message in the low-order byte.</span></span>

</dd> <dt>

<span data-ttu-id="a3ad2-110"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span><span class="sxs-lookup"><span data-stu-id="a3ad2-110"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="a3ad2-111">輸入裝置磁碟機收到訊息的時間。</span><span class="sxs-lookup"><span data-stu-id="a3ad2-111">Time that the message was received by the input device driver.</span></span> <span data-ttu-id="a3ad2-112">時間戳記是以毫秒為單位來指定，在呼叫 [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) 函式時從零開始。</span><span class="sxs-lookup"><span data-stu-id="a3ad2-112">The time stamp is specified in milliseconds, beginning at zero when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3ad2-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a3ad2-113">Return Value</span></span>

<span data-ttu-id="a3ad2-114">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a3ad2-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3ad2-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="a3ad2-115">Requirements</span></span>



| <span data-ttu-id="a3ad2-116">需求</span><span class="sxs-lookup"><span data-stu-id="a3ad2-116">Requirement</span></span> | <span data-ttu-id="a3ad2-117">值</span><span class="sxs-lookup"><span data-stu-id="a3ad2-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3ad2-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a3ad2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a3ad2-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3ad2-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a3ad2-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a3ad2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a3ad2-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3ad2-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a3ad2-122">標頭</span><span class="sxs-lookup"><span data-stu-id="a3ad2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3ad2-123"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="a3ad2-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3ad2-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a3ad2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3ad2-125">樂器數位介面 (MIDI)</span><span class="sxs-lookup"><span data-stu-id="a3ad2-125">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="a3ad2-126">MIDI 訊息</span><span class="sxs-lookup"><span data-stu-id="a3ad2-126">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

