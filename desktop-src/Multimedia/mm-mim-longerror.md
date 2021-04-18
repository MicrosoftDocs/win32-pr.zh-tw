---
title: 'MM_MIM_LONGERROR 訊息 (Mmsystem .h) '
description: '\_ \_ 當收到無效或不完整的 MIDI 系統專屬訊息時，會將 MM MIM LONGERROR 訊息傳送至視窗。'
ms.assetid: 2de4c2f8-2ded-4994-934c-6e72c95637b2
keywords:
- MM_MIM_LONGERROR message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_MIM_LONGERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e274faca26a90a5cd3b3915a7e8e1ed27bcfd77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965106"
---
# <a name="mm_mim_longerror-message"></a><span data-ttu-id="b223b-104">MM \_ MIM \_ LONGERROR 訊息</span><span class="sxs-lookup"><span data-stu-id="b223b-104">MM\_MIM\_LONGERROR message</span></span>

<span data-ttu-id="b223b-105">當收到無效或不完整的 MIDI 系統專屬訊息時，會將 **MM \_ MIM \_ LONGERROR** 訊息傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="b223b-105">The **MM\_MIM\_LONGERROR** message is sent to a window when an invalid or incomplete MIDI system-exclusive message is received.</span></span>


```C++
MM_MIM_LONGERROR 
wParam = (WPARAM) hInput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a><span data-ttu-id="b223b-106">參數</span><span class="sxs-lookup"><span data-stu-id="b223b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b223b-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="b223b-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="b223b-108">接收無效訊息之 MIDI 輸入裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b223b-108">Handle to the MIDI input device that received the invalid message.</span></span>

</dd> <dt>

<span data-ttu-id="b223b-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span><span class="sxs-lookup"><span data-stu-id="b223b-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="b223b-110">[**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)結構的指標，識別包含無效訊息的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b223b-110">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the buffer containing the invalid message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b223b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b223b-111">Return Value</span></span>

<span data-ttu-id="b223b-112">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b223b-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b223b-113">備註</span><span class="sxs-lookup"><span data-stu-id="b223b-113">Remarks</span></span>

<span data-ttu-id="b223b-114">傳回的緩衝區可能不完整。</span><span class="sxs-lookup"><span data-stu-id="b223b-114">The returned buffer might not be full.</span></span> <span data-ttu-id="b223b-115">若要判斷記錄到傳回緩衝區的位元組數目，請使用 *lpMidiHdr* 所指定之 [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)結構的 **dwBytesRecorded** 成員。</span><span class="sxs-lookup"><span data-stu-id="b223b-115">To determine the number of bytes recorded into the returned buffer, use the **dwBytesRecorded** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure specified by *lpMidiHdr*.</span></span>

## <a name="requirements"></a><span data-ttu-id="b223b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="b223b-116">Requirements</span></span>



| <span data-ttu-id="b223b-117">需求</span><span class="sxs-lookup"><span data-stu-id="b223b-117">Requirement</span></span> | <span data-ttu-id="b223b-118">值</span><span class="sxs-lookup"><span data-stu-id="b223b-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b223b-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b223b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b223b-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b223b-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b223b-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b223b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b223b-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b223b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b223b-123">標頭</span><span class="sxs-lookup"><span data-stu-id="b223b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b223b-124"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b223b-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b223b-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b223b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b223b-126">樂器數位介面 (MIDI)</span><span class="sxs-lookup"><span data-stu-id="b223b-126">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="b223b-127">MIDI 訊息</span><span class="sxs-lookup"><span data-stu-id="b223b-127">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

