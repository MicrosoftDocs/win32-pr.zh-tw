---
title: 'WM_CAP_GET_AUDIOFORMAT 訊息 (Vfw .h) '
description: WM \_ CAP \_ GET \_ AUDIOFORMAT 訊息會取得音訊格式或音訊格式的大小。 您可以使用 capGetAudioFormat 和 capGetAudioFormatSize 宏明確地傳送此訊息。
ms.assetid: 25e58863-2b1e-4ed8-9f34-c39617a15bc1
keywords:
- WM_CAP_GET_AUDIOFORMAT message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_GET_AUDIOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9508972c173c9e189bdc092a63d849adf3be739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383846"
---
# <a name="wm_cap_get_audioformat-message"></a><span data-ttu-id="94efc-105">WM \_ CAP \_ 取得 \_ AUDIOFORMAT 訊息</span><span class="sxs-lookup"><span data-stu-id="94efc-105">WM\_CAP\_GET\_AUDIOFORMAT message</span></span>

<span data-ttu-id="94efc-106">**WM \_ CAP \_ GET \_ AUDIOFORMAT** 訊息會取得音訊格式或音訊格式的大小。</span><span class="sxs-lookup"><span data-stu-id="94efc-106">The **WM\_CAP\_GET\_AUDIOFORMAT** message obtains the audio format or the size of the audio format.</span></span> <span data-ttu-id="94efc-107">您可以使用 [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) 和 [**capGetAudioFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="94efc-107">You can send this message explicitly or by using the [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) and [**capGetAudioFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) macros.</span></span>


```C++
WM_CAP_GET_AUDIOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPWAVEFORMATEX) (psAudioFormat); 
```



## <a name="parameters"></a><span data-ttu-id="94efc-108">參數</span><span class="sxs-lookup"><span data-stu-id="94efc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94efc-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="94efc-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="94efc-110">**S** 所參考之結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="94efc-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="94efc-111"><span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*psAudioFormat*</span><span class="sxs-lookup"><span data-stu-id="94efc-111"><span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*psAudioFormat*</span></span>
</dt> <dd>

<span data-ttu-id="94efc-112">[**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex)結構的指標，或 **為 Null**。</span><span class="sxs-lookup"><span data-stu-id="94efc-112">Pointer to a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure, or **NULL**.</span></span> <span data-ttu-id="94efc-113">如果值為 **Null**，則會傳回保存結構所需的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="94efc-113">If the value is **NULL**, the size, in bytes, required to hold the structure is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94efc-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="94efc-114">Return Value</span></span>

<span data-ttu-id="94efc-115">傳回音頻格式的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="94efc-115">Returns the size, in bytes, of the audio format.</span></span>

## <a name="remarks"></a><span data-ttu-id="94efc-116">備註</span><span class="sxs-lookup"><span data-stu-id="94efc-116">Remarks</span></span>

<span data-ttu-id="94efc-117">由於壓縮的音訊格式因大小需求而異，因此應用程式必須先取出大小，然後配置記憶體，最後要求音訊格式資料。</span><span class="sxs-lookup"><span data-stu-id="94efc-117">Because compressed audio formats vary in size requirements applications must first retrieve the size, then allocate memory, and finally request the audio format data.</span></span>

## <a name="requirements"></a><span data-ttu-id="94efc-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="94efc-118">Requirements</span></span>



| <span data-ttu-id="94efc-119">需求</span><span class="sxs-lookup"><span data-stu-id="94efc-119">Requirement</span></span> | <span data-ttu-id="94efc-120">值</span><span class="sxs-lookup"><span data-stu-id="94efc-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="94efc-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="94efc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="94efc-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="94efc-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="94efc-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="94efc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="94efc-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="94efc-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="94efc-125">標頭</span><span class="sxs-lookup"><span data-stu-id="94efc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="94efc-126"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="94efc-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94efc-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="94efc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94efc-128">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="94efc-128">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="94efc-129">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="94efc-129">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

