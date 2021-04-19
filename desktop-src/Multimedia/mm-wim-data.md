---
title: 'MM_WIM_DATA 訊息 (Mmsystem .h) '
description: '\_ \_ 當輸入緩衝區中有波形音訊資料，而且緩衝區傳回給應用程式時，會將 MM WIM 資料訊息傳送至視窗。 當緩衝區已滿或呼叫 waveInReset 函數之後，就可以傳送此訊息。'
ms.assetid: 14298153-ea2f-40b7-bca7-196f4e6c1155
keywords:
- MM_WIM_DATA message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_WIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c663d669635116500bc8aa7e7fdc994cdccd6dfe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106984969"
---
# <a name="mm_wim_data-message"></a><span data-ttu-id="fe203-105">MM \_ WIM \_ 資料訊息</span><span class="sxs-lookup"><span data-stu-id="fe203-105">MM\_WIM\_DATA message</span></span>

<span data-ttu-id="fe203-106">當輸入緩衝區中有波形音訊資料，而且緩衝區傳回給應用程式時，會將 **MM \_ WIM \_ 資料** 訊息傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="fe203-106">The **MM\_WIM\_DATA** message is sent to a window when waveform-audio data is present in the input buffer and the buffer is being returned to the application.</span></span> <span data-ttu-id="fe203-107">當緩衝區已滿或呼叫 [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) 函數之後，就可以傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="fe203-107">The message can be sent either when the buffer is full or after the [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) function is called.</span></span>


```C++
MM_WIM_DATA 
wParam = (WPARAM) hInputDev 
lParam = (LONG) lpwvhdr 
```



## <a name="parameters"></a><span data-ttu-id="fe203-108">參數</span><span class="sxs-lookup"><span data-stu-id="fe203-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe203-109"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span><span class="sxs-lookup"><span data-stu-id="fe203-109"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span></span>
</dt> <dd>

<span data-ttu-id="fe203-110">接收資料之波形音訊輸入裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fe203-110">Handle to the waveform-audio input device that received the data.</span></span>

</dd> <dt>

<span data-ttu-id="fe203-111"><span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*</span><span class="sxs-lookup"><span data-stu-id="fe203-111"><span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*</span></span>
</dt> <dd>

<span data-ttu-id="fe203-112">[**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)結構的指標，識別包含資料的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="fe203-112">Pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies the buffer containing the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe203-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="fe203-113">Return Value</span></span>

<span data-ttu-id="fe203-114">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="fe203-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe203-115">備註</span><span class="sxs-lookup"><span data-stu-id="fe203-115">Remarks</span></span>

<span data-ttu-id="fe203-116">傳回的緩衝區可能不完整。</span><span class="sxs-lookup"><span data-stu-id="fe203-116">The returned buffer might not be full.</span></span> <span data-ttu-id="fe203-117">您可以使用 *lParam* 所指定之 [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)結構的 **dwBytesRecorded** 成員，判斷記錄至傳回之緩衝區的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="fe203-117">Use the **dwBytesRecorded** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure specified by *lParam* to determine the number of bytes recorded into the returned buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe203-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe203-118">Requirements</span></span>



| <span data-ttu-id="fe203-119">需求</span><span class="sxs-lookup"><span data-stu-id="fe203-119">Requirement</span></span> | <span data-ttu-id="fe203-120">值</span><span class="sxs-lookup"><span data-stu-id="fe203-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe203-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fe203-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fe203-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe203-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fe203-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fe203-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fe203-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe203-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fe203-125">標頭</span><span class="sxs-lookup"><span data-stu-id="fe203-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe203-126"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="fe203-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe203-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe203-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe203-128">波形音訊</span><span class="sxs-lookup"><span data-stu-id="fe203-128">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="fe203-129">波形訊息</span><span class="sxs-lookup"><span data-stu-id="fe203-129">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

