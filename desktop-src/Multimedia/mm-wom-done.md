---
title: 'MM_WOM_DONE 訊息 (Mmsystem .h) '
description: '\_ \_ 當給定的輸出緩衝區傳回給應用程式時，會將 MM WOM 完成訊息傳送至視窗。 當應用程式被播放時，或呼叫 waveOutReset 函式的結果，會將緩衝區傳回給應用程式。'
ms.assetid: bbdebb68-82e5-4963-90bb-f93f8a91a8cf
keywords:
- MM_WOM_DONE message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_WOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7198aa2f60a7f5a0e6d839a3ee5b453a3a4d3f59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686635"
---
# <a name="mm_wom_done-message"></a><span data-ttu-id="5854c-105">MM \_ WOM \_ 完成訊息</span><span class="sxs-lookup"><span data-stu-id="5854c-105">MM\_WOM\_DONE message</span></span>

<span data-ttu-id="5854c-106">當給定的輸出緩衝區傳回給應用程式時，會將 **MM \_ WOM \_ 完成** 訊息傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="5854c-106">The **MM\_WOM\_DONE** message is sent to a window when the given output buffer is being returned to the application.</span></span> <span data-ttu-id="5854c-107">當應用程式被播放時，或呼叫 [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) 函式的結果，會將緩衝區傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="5854c-107">Buffers are returned to the application when they have been played, or as the result of a call to the [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) function.</span></span>


```C++
MM_WOM_DONE 
wParam = (WPARAM) hOutputDev 
lParam = (LONG) lpwvhdr 
```



## <a name="parameters"></a><span data-ttu-id="5854c-108">參數</span><span class="sxs-lookup"><span data-stu-id="5854c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5854c-109"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*</span><span class="sxs-lookup"><span data-stu-id="5854c-109"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*</span></span>
</dt> <dd>

<span data-ttu-id="5854c-110">播放緩衝區之波形音訊輸出裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="5854c-110">Handle to the waveform-audio output device that played the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="5854c-111"><span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*</span><span class="sxs-lookup"><span data-stu-id="5854c-111"><span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*</span></span>
</dt> <dd>

<span data-ttu-id="5854c-112">識別緩衝區之 [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="5854c-112">Pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure identifying the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5854c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5854c-113">Return Value</span></span>

<span data-ttu-id="5854c-114">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="5854c-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5854c-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="5854c-115">Requirements</span></span>



| <span data-ttu-id="5854c-116">需求</span><span class="sxs-lookup"><span data-stu-id="5854c-116">Requirement</span></span> | <span data-ttu-id="5854c-117">值</span><span class="sxs-lookup"><span data-stu-id="5854c-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5854c-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5854c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5854c-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5854c-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5854c-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5854c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5854c-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5854c-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5854c-122">標頭</span><span class="sxs-lookup"><span data-stu-id="5854c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5854c-123"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="5854c-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5854c-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5854c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5854c-125">波形音訊</span><span class="sxs-lookup"><span data-stu-id="5854c-125">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="5854c-126">波形訊息</span><span class="sxs-lookup"><span data-stu-id="5854c-126">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

