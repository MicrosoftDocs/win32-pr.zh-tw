---
title: 'WIM_DATA 訊息 (Mmsystem .h) '
description: '\_當輸入緩衝區中有波形音訊資料，而且緩衝區傳回給應用程式時，會將 WIM 資料訊息傳送至指定的波形-音訊輸入回撥函式。'
ms.assetid: 94cc02b8-61c4-44b9-9f8e-041fe989c1a6
keywords:
- WIM_DATA message Windows 多媒體
topic_type:
- apiref
api_name:
- WIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28bcfdd249dda5621d4914d75d3ffc7b13e4d767
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966529"
---
# <a name="wim_data-message"></a><span data-ttu-id="6b5f7-104">WIM \_ 資料訊息</span><span class="sxs-lookup"><span data-stu-id="6b5f7-104">WIM\_DATA message</span></span>

<span data-ttu-id="6b5f7-105">當輸入緩衝區中有波形音訊資料，而且緩衝區傳回給應用程式時，會將 **WIM \_ 資料** 訊息傳送至指定的波形-音訊輸入回撥函式。</span><span class="sxs-lookup"><span data-stu-id="6b5f7-105">The **WIM\_DATA** message is sent to the given waveform-audio input callback function when waveform-audio data is present in the input buffer and the buffer is being returned to the application.</span></span> <span data-ttu-id="6b5f7-106">當緩衝區已滿或呼叫 [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) 函數之後，就可以傳送訊息。</span><span class="sxs-lookup"><span data-stu-id="6b5f7-106">The message can be sent when the buffer is full or after the [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) function is called.</span></span>


```C++
WIM_DATA 
dwParam1 = (DWORD) lpwvhdr 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="6b5f7-107">參數</span><span class="sxs-lookup"><span data-stu-id="6b5f7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b5f7-108"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="6b5f7-108"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="6b5f7-109">[**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)結構的指標，識別包含資料的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6b5f7-109">Pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies the buffer containing the data.</span></span>

</dd> <dt>

<span data-ttu-id="6b5f7-110"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="6b5f7-110"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="6b5f7-111">保護必須為零。</span><span class="sxs-lookup"><span data-stu-id="6b5f7-111">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b5f7-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="6b5f7-112">Return Value</span></span>

<span data-ttu-id="6b5f7-113">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6b5f7-113">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b5f7-114">備註</span><span class="sxs-lookup"><span data-stu-id="6b5f7-114">Remarks</span></span>

<span data-ttu-id="6b5f7-115">傳回的緩衝區可能不完整。</span><span class="sxs-lookup"><span data-stu-id="6b5f7-115">The returned buffer might not be full.</span></span> <span data-ttu-id="6b5f7-116">您可以使用 *lpwvhdr* 所指定之 [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)結構的 **dwBytesRecorded** 成員，判斷記錄至傳回之緩衝區的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="6b5f7-116">Use the **dwBytesRecorded** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure specified by *lpwvhdr* to determine the number of bytes recorded into the returned buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b5f7-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b5f7-117">Requirements</span></span>



| <span data-ttu-id="6b5f7-118">需求</span><span class="sxs-lookup"><span data-stu-id="6b5f7-118">Requirement</span></span> | <span data-ttu-id="6b5f7-119">值</span><span class="sxs-lookup"><span data-stu-id="6b5f7-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b5f7-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6b5f7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6b5f7-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b5f7-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6b5f7-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6b5f7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6b5f7-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b5f7-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6b5f7-124">標頭</span><span class="sxs-lookup"><span data-stu-id="6b5f7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b5f7-125"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="6b5f7-125"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b5f7-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b5f7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b5f7-127">波形音訊</span><span class="sxs-lookup"><span data-stu-id="6b5f7-127">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="6b5f7-128">波形訊息</span><span class="sxs-lookup"><span data-stu-id="6b5f7-128">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

