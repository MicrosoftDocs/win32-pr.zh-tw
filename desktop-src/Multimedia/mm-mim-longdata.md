---
title: 'MM_MIM_LONGDATA 訊息 (Mmsystem .h) '
description: '\_ \_ 當收到完整的 MIDI 系統專屬訊息或緩衝區已填滿系統專屬的資料時，會將 MM MIM LONGDATA 訊息傳送至視窗。'
ms.assetid: 72b9eade-4224-436f-bfef-32204eaf51ae
keywords:
- MM_MIM_LONGDATA message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_MIM_LONGDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25bf1900ef2e9394b9d8772747eba873f8d607f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105905"
---
# <a name="mm_mim_longdata-message"></a><span data-ttu-id="4679c-104">MM \_ MIM \_ LONGDATA 訊息</span><span class="sxs-lookup"><span data-stu-id="4679c-104">MM\_MIM\_LONGDATA message</span></span>

<span data-ttu-id="4679c-105">當收到完整的 MIDI 系統專屬訊息或緩衝區已填滿系統專屬的資料時，會將 **MM \_ MIM \_ LONGDATA** 訊息傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="4679c-105">The **MM\_MIM\_LONGDATA** message is sent to a window when either a complete MIDI system-exclusive message is received or when a buffer has been filled with system-exclusive data.</span></span>


```C++
MM_MIM_LONGDATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a><span data-ttu-id="4679c-106">參數</span><span class="sxs-lookup"><span data-stu-id="4679c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4679c-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="4679c-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="4679c-108">接收資料之 MIDI 輸入裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4679c-108">Handle to the MIDI input device that received the data.</span></span>

</dd> <dt>

<span data-ttu-id="4679c-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span><span class="sxs-lookup"><span data-stu-id="4679c-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="4679c-110">識別緩衝區之 [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="4679c-110">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4679c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4679c-111">Return Value</span></span>

<span data-ttu-id="4679c-112">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4679c-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4679c-113">備註</span><span class="sxs-lookup"><span data-stu-id="4679c-113">Remarks</span></span>

<span data-ttu-id="4679c-114">傳回的緩衝區可能不完整。</span><span class="sxs-lookup"><span data-stu-id="4679c-114">The returned buffer might not be full.</span></span> <span data-ttu-id="4679c-115">若要判斷記錄到傳回緩衝區的位元組數目，請使用 *lpMidiHdr* 所指向之 [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)結構的 **dwBytesRecorded** 成員。</span><span class="sxs-lookup"><span data-stu-id="4679c-115">To determine the number of bytes recorded into the returned buffer, use the **dwBytesRecorded** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure pointed to by *lpMidiHdr*.</span></span>

<span data-ttu-id="4679c-116">此訊息沒有可用的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="4679c-116">No time stamp is available with this message.</span></span> <span data-ttu-id="4679c-117">針對時間戳記的輸入資料，您必須使用傳送給回呼函式的訊息。</span><span class="sxs-lookup"><span data-stu-id="4679c-117">For time-stamped input data, you must use the messages that are sent to callback functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4679c-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="4679c-118">Requirements</span></span>



| <span data-ttu-id="4679c-119">需求</span><span class="sxs-lookup"><span data-stu-id="4679c-119">Requirement</span></span> | <span data-ttu-id="4679c-120">值</span><span class="sxs-lookup"><span data-stu-id="4679c-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4679c-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4679c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4679c-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4679c-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4679c-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4679c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4679c-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4679c-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4679c-125">標頭</span><span class="sxs-lookup"><span data-stu-id="4679c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4679c-126"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="4679c-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4679c-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4679c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4679c-128">樂器數位介面 (MIDI)</span><span class="sxs-lookup"><span data-stu-id="4679c-128">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="4679c-129">MIDI 訊息</span><span class="sxs-lookup"><span data-stu-id="4679c-129">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

