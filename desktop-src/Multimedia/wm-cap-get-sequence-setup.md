---
title: 'WM_CAP_GET_SEQUENCE_SETUP 訊息 (Vfw .h) '
description: WM \_ CAP \_ GET \_ SEQUENCE 設定訊息會抓取 \_ 串流處理捕獲參數的目前設定。 您可以使用 capCaptureGetSetup 宏明確地傳送此訊息。
ms.assetid: 2220c92a-1994-4f15-9730-1cf01972dda6
keywords:
- WM_CAP_GET_SEQUENCE_SETUP message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_GET_SEQUENCE_SETUP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5cd1585b165581f9c9646741b92c5dc841472ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933893"
---
# <a name="wm_cap_get_sequence_setup-message"></a><span data-ttu-id="48932-105">WM \_ CAP \_ 取得 \_ 順序 \_ 設定訊息</span><span class="sxs-lookup"><span data-stu-id="48932-105">WM\_CAP\_GET\_SEQUENCE\_SETUP message</span></span>

<span data-ttu-id="48932-106">**WM \_ CAP \_ GET \_ SEQUENCE \_ 設定** 訊息會抓取串流處理捕獲參數的目前設定。</span><span class="sxs-lookup"><span data-stu-id="48932-106">The **WM\_CAP\_GET\_SEQUENCE\_SETUP** message retrieves the current settings of the streaming capture parameters.</span></span> <span data-ttu-id="48932-107">您可以使用 [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="48932-107">You can send this message explicitly or by using the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro.</span></span>


```C++
WM_CAP_GET_SEQUENCE_SETUP 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPTUREPARMS) (s); 
```



## <a name="parameters"></a><span data-ttu-id="48932-108">參數</span><span class="sxs-lookup"><span data-stu-id="48932-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48932-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="48932-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="48932-110">**S** 所參考之結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="48932-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="48932-111"><span id="s"></span><span id="S"></span>*！*</span><span class="sxs-lookup"><span data-stu-id="48932-111"><span id="s"></span><span id="S"></span>*s*</span></span>
</dt> <dd>

<span data-ttu-id="48932-112">[**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="48932-112">Pointer to a [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48932-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="48932-113">Return Value</span></span>

<span data-ttu-id="48932-114">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="48932-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="48932-115">備註</span><span class="sxs-lookup"><span data-stu-id="48932-115">Remarks</span></span>

<span data-ttu-id="48932-116">如需用來控制串流處理捕獲之參數的相關資訊，請參閱 [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) 結構。</span><span class="sxs-lookup"><span data-stu-id="48932-116">For information about the parameters used to control streaming capture, see the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="48932-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="48932-117">Requirements</span></span>



| <span data-ttu-id="48932-118">需求</span><span class="sxs-lookup"><span data-stu-id="48932-118">Requirement</span></span> | <span data-ttu-id="48932-119">值</span><span class="sxs-lookup"><span data-stu-id="48932-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="48932-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="48932-120">Minimum supported client</span></span><br/> | <span data-ttu-id="48932-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48932-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="48932-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="48932-122">Minimum supported server</span></span><br/> | <span data-ttu-id="48932-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48932-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="48932-124">標頭</span><span class="sxs-lookup"><span data-stu-id="48932-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="48932-125"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="48932-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48932-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48932-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48932-127">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="48932-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="48932-128">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="48932-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





