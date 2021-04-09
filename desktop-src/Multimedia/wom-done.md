---
title: 'WOM_DONE 訊息 (Mmsystem .h) '
description: '\_當指定的輸出緩衝區傳回給應用程式時，WOM 完成的訊息會傳送到波形音訊輸出回呼函式。'
ms.assetid: cac94a44-d1b0-43de-b3ec-ae34547b1fc3
keywords:
- WOM_DONE message Windows 多媒體
topic_type:
- apiref
api_name:
- WOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab64598a2dfdd329615ca116fb6382909bb83b01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093975"
---
# <a name="wom_done-message"></a><span data-ttu-id="828bf-104">WOM \_ 完成訊息</span><span class="sxs-lookup"><span data-stu-id="828bf-104">WOM\_DONE message</span></span>

<span data-ttu-id="828bf-105">當指定的輸出緩衝區傳回給應用程式時， **WOM \_ 完成** 的訊息會傳送到波形音訊輸出回呼函式。</span><span class="sxs-lookup"><span data-stu-id="828bf-105">The **WOM\_DONE** message is sent to a waveform-audio output callback function when the given output buffer is being returned to the application.</span></span> <span data-ttu-id="828bf-106">當應用程式被播放時，或呼叫 [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) 函式的結果，會將緩衝區傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="828bf-106">Buffers are returned to the application when they have been played, or as the result of a call to the [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) function.</span></span>


```C++
WOM_DONE 
dwParam1 = (DWORD) lpwvhdr 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="828bf-107">參數</span><span class="sxs-lookup"><span data-stu-id="828bf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="828bf-108"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="828bf-108"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="828bf-109">識別緩衝區之 [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="828bf-109">Pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure identifying the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="828bf-110"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="828bf-110"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="828bf-111">保護必須為零。</span><span class="sxs-lookup"><span data-stu-id="828bf-111">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="828bf-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="828bf-112">Return Value</span></span>

<span data-ttu-id="828bf-113">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="828bf-113">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="828bf-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="828bf-114">Requirements</span></span>



| <span data-ttu-id="828bf-115">需求</span><span class="sxs-lookup"><span data-stu-id="828bf-115">Requirement</span></span> | <span data-ttu-id="828bf-116">值</span><span class="sxs-lookup"><span data-stu-id="828bf-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="828bf-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="828bf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="828bf-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="828bf-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="828bf-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="828bf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="828bf-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="828bf-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="828bf-121">標頭</span><span class="sxs-lookup"><span data-stu-id="828bf-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="828bf-122"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="828bf-122"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="828bf-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="828bf-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="828bf-124">波形音訊</span><span class="sxs-lookup"><span data-stu-id="828bf-124">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="828bf-125">波形訊息</span><span class="sxs-lookup"><span data-stu-id="828bf-125">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

