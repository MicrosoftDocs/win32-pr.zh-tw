---
title: 'MM_WIM_CLOSE 訊息 (Mmsystem .h) '
description: '\_ \_ 當波形音訊輸入裝置關閉時，會將 MM WIM 關閉訊息傳送至視窗。 傳送此訊息之後，裝置控制碼已不再有效。'
ms.assetid: 4ea35b66-6bfa-41f0-9d52-a8cf2b0a69dd
keywords:
- MM_WIM_CLOSE message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_WIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d9934ef7045debbcac2f5baf1c2f750d22dad5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024560"
---
# <a name="mm_wim_close-message"></a><span data-ttu-id="aabe2-105">MM \_ WIM \_ 關閉訊息</span><span class="sxs-lookup"><span data-stu-id="aabe2-105">MM\_WIM\_CLOSE message</span></span>

<span data-ttu-id="aabe2-106">當波形音訊輸入裝置關閉時，會將 **MM \_ WIM \_ 關閉** 訊息傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="aabe2-106">The **MM\_WIM\_CLOSE** message is sent to a window when a waveform-audio input device is closed.</span></span> <span data-ttu-id="aabe2-107">傳送此訊息之後，裝置控制碼已不再有效。</span><span class="sxs-lookup"><span data-stu-id="aabe2-107">The device handle is no longer valid after this message has been sent.</span></span>


```C++
MM_WIM_CLOSE 
wParam = (WPARAM) hInputDev 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="aabe2-108">參數</span><span class="sxs-lookup"><span data-stu-id="aabe2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aabe2-109"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span><span class="sxs-lookup"><span data-stu-id="aabe2-109"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span></span>
</dt> <dd>

<span data-ttu-id="aabe2-110">已關閉波形音訊輸入裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="aabe2-110">Handle to the waveform-audio input device that was closed.</span></span>

</dd> <dt>

<span data-ttu-id="aabe2-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="aabe2-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="aabe2-112">保護必須為零。</span><span class="sxs-lookup"><span data-stu-id="aabe2-112">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aabe2-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="aabe2-113">Return Value</span></span>

<span data-ttu-id="aabe2-114">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="aabe2-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="aabe2-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="aabe2-115">Requirements</span></span>



| <span data-ttu-id="aabe2-116">需求</span><span class="sxs-lookup"><span data-stu-id="aabe2-116">Requirement</span></span> | <span data-ttu-id="aabe2-117">值</span><span class="sxs-lookup"><span data-stu-id="aabe2-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aabe2-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aabe2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="aabe2-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aabe2-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="aabe2-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aabe2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="aabe2-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aabe2-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="aabe2-122">標頭</span><span class="sxs-lookup"><span data-stu-id="aabe2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="aabe2-123"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="aabe2-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aabe2-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aabe2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aabe2-125">波形音訊</span><span class="sxs-lookup"><span data-stu-id="aabe2-125">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="aabe2-126">波形訊息</span><span class="sxs-lookup"><span data-stu-id="aabe2-126">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





