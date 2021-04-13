---
title: 'MIM_LONGERROR 訊息 (Mmsystem .h) '
description: '\_當收到無效或不完整的 midi 系統專屬訊息時，會將 MIM LONGERROR 訊息傳送至 MIDI 輸入回撥函式。'
ms.assetid: 7e3b0716-33c4-449c-a200-e5ba72428dc1
keywords:
- MIM_LONGERROR message Windows 多媒體
topic_type:
- apiref
api_name:
- MIM_LONGERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 631c4fdcd31eef01d691aea80100427d116ae7d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464504"
---
# <a name="mim_longerror-message"></a><span data-ttu-id="82b14-104">MIM \_ LONGERROR 訊息</span><span class="sxs-lookup"><span data-stu-id="82b14-104">MIM\_LONGERROR message</span></span>

<span data-ttu-id="82b14-105">當收到無效或不完整的 MIDI 系統專屬訊息時，會將 **MIM \_ LONGERROR** 訊息傳送至 MIDI 輸入回撥函式。</span><span class="sxs-lookup"><span data-stu-id="82b14-105">The **MIM\_LONGERROR** message is sent to a MIDI input callback function when an invalid or incomplete MIDI system-exclusive message is received.</span></span>


```C++
MIM_LONGERROR 
dwParam1 = (DWORD) lpMidiHdr 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="82b14-106">參數</span><span class="sxs-lookup"><span data-stu-id="82b14-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82b14-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span><span class="sxs-lookup"><span data-stu-id="82b14-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="82b14-108">[**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)結構的指標，識別包含無效訊息的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="82b14-108">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the buffer containing the invalid message.</span></span>

</dd> <dt>

<span data-ttu-id="82b14-109"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span><span class="sxs-lookup"><span data-stu-id="82b14-109"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="82b14-110">輸入裝置磁碟機收到資料的時間。</span><span class="sxs-lookup"><span data-stu-id="82b14-110">Time that the data was received by the input device driver.</span></span> <span data-ttu-id="82b14-111">時間戳記是以毫秒為單位來指定，在呼叫 [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) 函式時從零開始。</span><span class="sxs-lookup"><span data-stu-id="82b14-111">The time stamp is specified in milliseconds, beginning at zero when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82b14-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="82b14-112">Return Value</span></span>

<span data-ttu-id="82b14-113">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="82b14-113">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="82b14-114">備註</span><span class="sxs-lookup"><span data-stu-id="82b14-114">Remarks</span></span>

<span data-ttu-id="82b14-115">傳回的緩衝區可能不完整。</span><span class="sxs-lookup"><span data-stu-id="82b14-115">The returned buffer might not be full.</span></span> <span data-ttu-id="82b14-116">若要判斷記錄到傳回緩衝區的位元組數目，請使用 *lpMidiHdr* 所指定之 [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)結構的 **dwBytesRecorded** 成員。</span><span class="sxs-lookup"><span data-stu-id="82b14-116">To determine the number of bytes recorded into the returned buffer, use the **dwBytesRecorded** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure specified by *lpMidiHdr*.</span></span>

## <a name="requirements"></a><span data-ttu-id="82b14-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="82b14-117">Requirements</span></span>



| <span data-ttu-id="82b14-118">需求</span><span class="sxs-lookup"><span data-stu-id="82b14-118">Requirement</span></span> | <span data-ttu-id="82b14-119">值</span><span class="sxs-lookup"><span data-stu-id="82b14-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82b14-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="82b14-120">Minimum supported client</span></span><br/> | <span data-ttu-id="82b14-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="82b14-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="82b14-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="82b14-122">Minimum supported server</span></span><br/> | <span data-ttu-id="82b14-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="82b14-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="82b14-124">標頭</span><span class="sxs-lookup"><span data-stu-id="82b14-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="82b14-125"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="82b14-125"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82b14-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="82b14-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82b14-127">樂器數位介面 (MIDI)</span><span class="sxs-lookup"><span data-stu-id="82b14-127">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="82b14-128">MIDI 訊息</span><span class="sxs-lookup"><span data-stu-id="82b14-128">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

