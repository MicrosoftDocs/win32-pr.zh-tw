---
title: 'MM_WIM_OPEN 訊息 (Mmsystem .h) '
description: '\_ \_ 開啟波形音訊輸入裝置時，會將 MM WIM OPEN 訊息傳送至視窗。'
ms.assetid: 4c646f58-c324-467e-871b-8fc36d5b89bc
keywords:
- MM_WIM_OPEN message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_WIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64ff028dcd9dc851d94699ef5cb75707429ba149
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025495"
---
# <a name="mm_wim_open-message"></a><span data-ttu-id="32fb9-104">MM \_ WIM \_ 開啟訊息</span><span class="sxs-lookup"><span data-stu-id="32fb9-104">MM\_WIM\_OPEN message</span></span>

<span data-ttu-id="32fb9-105">開啟波形音訊輸入裝置時，會將 **MM \_ WIM \_ OPEN** 訊息傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="32fb9-105">The **MM\_WIM\_OPEN** message is sent to a window when a waveform-audio input device is opened.</span></span>


```C++
MM_WIM_OPEN 
wParam = (WPARAM) hInputDev 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="32fb9-106">參數</span><span class="sxs-lookup"><span data-stu-id="32fb9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32fb9-107"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span><span class="sxs-lookup"><span data-stu-id="32fb9-107"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span></span>
</dt> <dd>

<span data-ttu-id="32fb9-108">開啟之裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="32fb9-108">Handle to the device that was opened.</span></span>

</dd> <dt>

<span data-ttu-id="32fb9-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="32fb9-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="32fb9-110">保護必須為零。</span><span class="sxs-lookup"><span data-stu-id="32fb9-110">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32fb9-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="32fb9-111">Return Value</span></span>

<span data-ttu-id="32fb9-112">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="32fb9-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="32fb9-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="32fb9-113">Requirements</span></span>



| <span data-ttu-id="32fb9-114">需求</span><span class="sxs-lookup"><span data-stu-id="32fb9-114">Requirement</span></span> | <span data-ttu-id="32fb9-115">值</span><span class="sxs-lookup"><span data-stu-id="32fb9-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32fb9-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="32fb9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="32fb9-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32fb9-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="32fb9-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="32fb9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="32fb9-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32fb9-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="32fb9-120">標頭</span><span class="sxs-lookup"><span data-stu-id="32fb9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="32fb9-121"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="32fb9-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32fb9-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32fb9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32fb9-123">波形音訊</span><span class="sxs-lookup"><span data-stu-id="32fb9-123">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="32fb9-124">波形訊息</span><span class="sxs-lookup"><span data-stu-id="32fb9-124">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





