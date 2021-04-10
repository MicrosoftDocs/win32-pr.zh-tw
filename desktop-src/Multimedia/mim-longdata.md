---
title: 'MIM_LONGDATA 訊息 (Mmsystem .h) '
description: '\_當系統專屬緩衝區已填滿資料，並傳回給應用程式時，會將 MIM LONGDATA 訊息傳送至 MIDI 輸入回撥函式。'
ms.assetid: 3a11ed21-e7c5-4b78-9536-f0d862e26a02
keywords:
- MIM_LONGDATA message Windows 多媒體
topic_type:
- apiref
api_name:
- MIM_LONGDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bc5f83b1f0468540da18d0d8317dae42cbf33bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106529"
---
# <a name="mim_longdata-message"></a><span data-ttu-id="a832b-104">MIM \_ LONGDATA 訊息</span><span class="sxs-lookup"><span data-stu-id="a832b-104">MIM\_LONGDATA message</span></span>

<span data-ttu-id="a832b-105">當系統專屬緩衝區已填滿資料，並傳回給應用程式時，會將 **MIM \_ LONGDATA** 訊息傳送至 MIDI 輸入回撥函式。</span><span class="sxs-lookup"><span data-stu-id="a832b-105">The **MIM\_LONGDATA** message is sent to a MIDI input callback function when a system-exclusive buffer has been filled with data and is being returned to the application.</span></span>


```C++
MIM_LONGDATA 
dwParam1 = (DWORD) lpMidiHdr 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="a832b-106">參數</span><span class="sxs-lookup"><span data-stu-id="a832b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a832b-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span><span class="sxs-lookup"><span data-stu-id="a832b-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="a832b-108">識別輸入緩衝區之 [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="a832b-108">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the input buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a832b-109"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span><span class="sxs-lookup"><span data-stu-id="a832b-109"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="a832b-110">輸入裝置磁碟機收到資料的時間。</span><span class="sxs-lookup"><span data-stu-id="a832b-110">Time that the data was received by the input device driver.</span></span> <span data-ttu-id="a832b-111">時間戳記是以毫秒為單位來指定，在呼叫 [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) 函式時從零開始。</span><span class="sxs-lookup"><span data-stu-id="a832b-111">The time stamp is specified in milliseconds, beginning at zero when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a832b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="a832b-112">Return Value</span></span>

<span data-ttu-id="a832b-113">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a832b-113">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a832b-114">備註</span><span class="sxs-lookup"><span data-stu-id="a832b-114">Remarks</span></span>

<span data-ttu-id="a832b-115">傳回的緩衝區可能不完整。</span><span class="sxs-lookup"><span data-stu-id="a832b-115">The returned buffer might not be full.</span></span> <span data-ttu-id="a832b-116">若要判斷記錄到傳回緩衝區的位元組數目，請使用 *lpMidiHdr* 所指定之 [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)結構的 **dwBytesRecorded** 成員。</span><span class="sxs-lookup"><span data-stu-id="a832b-116">To determine the number of bytes recorded into the returned buffer, use the **dwBytesRecorded** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure specified by *lpMidiHdr*.</span></span>

## <a name="requirements"></a><span data-ttu-id="a832b-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="a832b-117">Requirements</span></span>



| <span data-ttu-id="a832b-118">需求</span><span class="sxs-lookup"><span data-stu-id="a832b-118">Requirement</span></span> | <span data-ttu-id="a832b-119">值</span><span class="sxs-lookup"><span data-stu-id="a832b-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a832b-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a832b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a832b-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a832b-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a832b-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a832b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a832b-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a832b-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a832b-124">標頭</span><span class="sxs-lookup"><span data-stu-id="a832b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a832b-125"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="a832b-125"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a832b-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a832b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a832b-127">樂器數位介面 (MIDI)</span><span class="sxs-lookup"><span data-stu-id="a832b-127">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="a832b-128">MIDI 訊息</span><span class="sxs-lookup"><span data-stu-id="a832b-128">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

