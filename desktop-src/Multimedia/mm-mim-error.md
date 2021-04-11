---
title: 'MM_MIM_ERROR 訊息 (Mmsystem .h) '
description: '\_ \_ 當收到不正確 MIDI 訊息時，會將 MM MIM 錯誤訊息傳送至視窗。'
ms.assetid: 03760bfc-a4ef-48cd-97a9-1b93b56fc641
keywords:
- MM_MIM_ERROR message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_MIM_ERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76b45988259601b40a804f9eb8acfbb085bddcda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093983"
---
# <a name="mm_mim_error-message"></a><span data-ttu-id="65d7e-104">MM \_ MIM \_ 錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="65d7e-104">MM\_MIM\_ERROR message</span></span>

<span data-ttu-id="65d7e-105">當收到不正確 MIDI 訊息時，會將 **MM \_ MIM \_ 錯誤** 訊息傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="65d7e-105">The **MM\_MIM\_ERROR** message is sent to a window when an invalid MIDI message is received.</span></span>


```C++
MM_MIM_ERROR 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a><span data-ttu-id="65d7e-106">參數</span><span class="sxs-lookup"><span data-stu-id="65d7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65d7e-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="65d7e-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="65d7e-108">接收無效訊息之 MIDI 輸入裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="65d7e-108">Handle to the MIDI input device that received the invalid message.</span></span>

</dd> <dt>

<span data-ttu-id="65d7e-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="65d7e-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="65d7e-110">不正確 MIDI 訊息。</span><span class="sxs-lookup"><span data-stu-id="65d7e-110">Invalid MIDI message.</span></span> <span data-ttu-id="65d7e-111">訊息會以低序位位元組的訊息的第一個位元組封裝成 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="65d7e-111">The message is packed into a **DWORD** value with the first byte of the message in the low-order byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65d7e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="65d7e-112">Return Value</span></span>

<span data-ttu-id="65d7e-113">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="65d7e-113">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="65d7e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="65d7e-114">Requirements</span></span>



| <span data-ttu-id="65d7e-115">需求</span><span class="sxs-lookup"><span data-stu-id="65d7e-115">Requirement</span></span> | <span data-ttu-id="65d7e-116">值</span><span class="sxs-lookup"><span data-stu-id="65d7e-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65d7e-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65d7e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="65d7e-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65d7e-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="65d7e-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65d7e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="65d7e-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65d7e-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="65d7e-121">標頭</span><span class="sxs-lookup"><span data-stu-id="65d7e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="65d7e-122"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="65d7e-122"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65d7e-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65d7e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65d7e-124">樂器數位介面 (MIDI)</span><span class="sxs-lookup"><span data-stu-id="65d7e-124">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="65d7e-125">MIDI 訊息</span><span class="sxs-lookup"><span data-stu-id="65d7e-125">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





