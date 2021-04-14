---
title: 'WM_CAP_DRIVER_GET_CAPS 訊息 (Vfw .h) '
description: 「WM \_ cap \_ 驅動程式 \_ 取得 cap」訊息會傳回 \_ 目前連接到「捕獲」視窗之「capture 驅動程式」的硬體功能。 您可以使用 capDriverGetCaps 宏明確地傳送此訊息。
ms.assetid: 898a800c-1109-47cd-bcc9-cb61d86a4a2e
keywords:
- WM_CAP_DRIVER_GET_CAPS message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_CAPS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 027e530be82c76afebc343ceebe4905daef9b126
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509363"
---
# <a name="wm_cap_driver_get_caps-message"></a><span data-ttu-id="7498c-105">WM \_ cap \_ 驅動程式 \_ 取得 \_ cap 訊息</span><span class="sxs-lookup"><span data-stu-id="7498c-105">WM\_CAP\_DRIVER\_GET\_CAPS message</span></span>

<span data-ttu-id="7498c-106">「 **WM \_ cap \_ 驅動程式 \_ 取得 \_ cap** 」訊息會傳回目前連接到「捕獲」視窗之「capture 驅動程式」的硬體功能。</span><span class="sxs-lookup"><span data-stu-id="7498c-106">The **WM\_CAP\_DRIVER\_GET\_CAPS** message returns the hardware capabilities of the capture driver currently connected to a capture window.</span></span> <span data-ttu-id="7498c-107">您可以使用 [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="7498c-107">You can send this message explicitly or by using the [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) macro.</span></span>


```C++
WM_CAP_DRIVER_GET_CAPS 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPDRIVERCAPS) (psCaps); 
```



## <a name="parameters"></a><span data-ttu-id="7498c-108">參數</span><span class="sxs-lookup"><span data-stu-id="7498c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7498c-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="7498c-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="7498c-110">**S** 所參考之結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7498c-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="7498c-111"><span id="psCaps"></span><span id="pscaps"></span><span id="PSCAPS"></span>*psCaps*</span><span class="sxs-lookup"><span data-stu-id="7498c-111"><span id="psCaps"></span><span id="pscaps"></span><span id="PSCAPS"></span>*psCaps*</span></span>
</dt> <dd>

<span data-ttu-id="7498c-112">[**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps)結構的指標，包含硬體功能。</span><span class="sxs-lookup"><span data-stu-id="7498c-112">Pointer to the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure to contain the hardware capabilities.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7498c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7498c-113">Return Value</span></span>

<span data-ttu-id="7498c-114">如果成功，則傳回 **TRUE** ，如果捕捉視窗未連接到 capture 驅動程式，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="7498c-114">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="7498c-115">備註</span><span class="sxs-lookup"><span data-stu-id="7498c-115">Remarks</span></span>

<span data-ttu-id="7498c-116">在 [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) 中傳回的功能對指定的捕獲驅動程式是常數。</span><span class="sxs-lookup"><span data-stu-id="7498c-116">The capabilities returned in [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) are constant for a given capture driver.</span></span> <span data-ttu-id="7498c-117">當 capture 驅動程式第一次連接到 capture 視窗時，應用程式需要取出這項資訊一次。</span><span class="sxs-lookup"><span data-stu-id="7498c-117">Applications need to retrieve this information once when the capture driver is first connected to a capture window.</span></span>

## <a name="requirements"></a><span data-ttu-id="7498c-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="7498c-118">Requirements</span></span>



| <span data-ttu-id="7498c-119">需求</span><span class="sxs-lookup"><span data-stu-id="7498c-119">Requirement</span></span> | <span data-ttu-id="7498c-120">值</span><span class="sxs-lookup"><span data-stu-id="7498c-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7498c-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7498c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7498c-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7498c-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7498c-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7498c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7498c-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7498c-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7498c-125">標頭</span><span class="sxs-lookup"><span data-stu-id="7498c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7498c-126"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="7498c-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7498c-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7498c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7498c-128">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="7498c-128">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="7498c-129">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="7498c-129">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





