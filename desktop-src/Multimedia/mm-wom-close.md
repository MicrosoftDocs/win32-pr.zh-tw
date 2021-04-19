---
title: 'MM_WOM_CLOSE 訊息 (Mmsystem .h) '
description: '\_ \_ 當波形音訊輸出裝置關閉時，會將 MM WOM 關閉訊息傳送至視窗。 傳送此訊息之後，裝置控制碼已不再有效。'
ms.assetid: 6505b688-88a1-43b2-ad4e-2f88e496430a
keywords:
- MM_WOM_CLOSE message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_WOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9dccdae49efc107a513e047282922f3a6de73e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106998032"
---
# <a name="mm_wom_close-message"></a><span data-ttu-id="1e0dd-105">MM \_ WOM \_ 關閉訊息</span><span class="sxs-lookup"><span data-stu-id="1e0dd-105">MM\_WOM\_CLOSE message</span></span>

<span data-ttu-id="1e0dd-106">當波形音訊輸出裝置關閉時，會將 **MM \_ WOM \_ 關閉** 訊息傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="1e0dd-106">The **MM\_WOM\_CLOSE** message is sent to a window when a waveform-audio output device is closed.</span></span> <span data-ttu-id="1e0dd-107">傳送此訊息之後，裝置控制碼已不再有效。</span><span class="sxs-lookup"><span data-stu-id="1e0dd-107">The device handle is no longer valid after this message has been sent.</span></span>


```C++
MM_WOM_CLOSE 
wParam = (WPARAM) hOutputDev 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="1e0dd-108">參數</span><span class="sxs-lookup"><span data-stu-id="1e0dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e0dd-109"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*</span><span class="sxs-lookup"><span data-stu-id="1e0dd-109"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*</span></span>
</dt> <dd>

<span data-ttu-id="1e0dd-110">已關閉之裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1e0dd-110">Handle to the device that was closed.</span></span>

</dd> <dt>

<span data-ttu-id="1e0dd-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="1e0dd-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="1e0dd-112">保護必須為零。</span><span class="sxs-lookup"><span data-stu-id="1e0dd-112">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e0dd-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="1e0dd-113">Return Value</span></span>

<span data-ttu-id="1e0dd-114">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="1e0dd-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e0dd-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e0dd-115">Requirements</span></span>



| <span data-ttu-id="1e0dd-116">需求</span><span class="sxs-lookup"><span data-stu-id="1e0dd-116">Requirement</span></span> | <span data-ttu-id="1e0dd-117">值</span><span class="sxs-lookup"><span data-stu-id="1e0dd-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e0dd-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1e0dd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1e0dd-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e0dd-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1e0dd-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1e0dd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1e0dd-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e0dd-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1e0dd-122">標頭</span><span class="sxs-lookup"><span data-stu-id="1e0dd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e0dd-123"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="1e0dd-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e0dd-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1e0dd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e0dd-125">波形音訊</span><span class="sxs-lookup"><span data-stu-id="1e0dd-125">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="1e0dd-126">波形訊息</span><span class="sxs-lookup"><span data-stu-id="1e0dd-126">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





