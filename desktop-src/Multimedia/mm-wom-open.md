---
title: 'MM_WOM_OPEN 訊息 (Mmsystem .h) '
description: '\_ \_ 當指定的波形音訊輸出裝置開啟時，MM WOM 開啟的訊息會傳送至視窗。'
ms.assetid: 1b0366de-61cd-4203-9173-ababaefdb153
keywords:
- MM_WOM_OPEN message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_WOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 783910389f2b9be9193c8f7bb0722f70261f5fce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106518"
---
# <a name="mm_wom_open-message"></a><span data-ttu-id="0e106-104">MM \_ WOM \_ 開啟的訊息</span><span class="sxs-lookup"><span data-stu-id="0e106-104">MM\_WOM\_OPEN message</span></span>

<span data-ttu-id="0e106-105">當指定的波形音訊輸出裝置開啟時， **MM \_ WOM \_ 開啟** 的訊息會傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="0e106-105">The **MM\_WOM\_OPEN** message is sent to a window when the given waveform-audio output device is opened.</span></span>


```C++
MM_WOM_OPEN 
wParam = (WPARAM) hOutputDev 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="0e106-106">參數</span><span class="sxs-lookup"><span data-stu-id="0e106-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e106-107"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*</span><span class="sxs-lookup"><span data-stu-id="0e106-107"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*</span></span>
</dt> <dd>

<span data-ttu-id="0e106-108">開啟之裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0e106-108">Handle to the device that was opened.</span></span>

</dd> <dt>

<span data-ttu-id="0e106-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="0e106-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="0e106-110">保護必須為零。</span><span class="sxs-lookup"><span data-stu-id="0e106-110">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e106-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="0e106-111">Return Value</span></span>

<span data-ttu-id="0e106-112">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0e106-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e106-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e106-113">Requirements</span></span>



| <span data-ttu-id="0e106-114">需求</span><span class="sxs-lookup"><span data-stu-id="0e106-114">Requirement</span></span> | <span data-ttu-id="0e106-115">值</span><span class="sxs-lookup"><span data-stu-id="0e106-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e106-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0e106-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0e106-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e106-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0e106-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0e106-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0e106-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e106-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0e106-120">標頭</span><span class="sxs-lookup"><span data-stu-id="0e106-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e106-121"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="0e106-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e106-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0e106-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e106-123">波形音訊</span><span class="sxs-lookup"><span data-stu-id="0e106-123">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="0e106-124">波形訊息</span><span class="sxs-lookup"><span data-stu-id="0e106-124">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





