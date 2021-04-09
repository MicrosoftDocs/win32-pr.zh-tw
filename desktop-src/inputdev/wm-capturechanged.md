---
title: 'WM_CAPTURECHANGED 訊息 (Winuser .h) '
description: 傳送至遺失滑鼠捕捉的視窗。
ms.assetid: 79c8f65e-31fa-4bdb-9e88-0160a52b5b7d
keywords:
- WM_CAPTURECHANGED 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_CAPTURECHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050bc00a7ab19e22e0fe4ea1f35271707180d4d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094355"
---
# <a name="wm_capturechanged-message"></a><span data-ttu-id="0bf86-104">WM \_ CAPTURECHANGED 訊息</span><span class="sxs-lookup"><span data-stu-id="0bf86-104">WM\_CAPTURECHANGED message</span></span>

<span data-ttu-id="0bf86-105">傳送至遺失滑鼠捕捉的視窗。</span><span class="sxs-lookup"><span data-stu-id="0bf86-105">Sent to the window that is losing the mouse capture.</span></span>

<span data-ttu-id="0bf86-106">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="0bf86-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CAPTURECHANGED               0x0215
```



## <a name="parameters"></a><span data-ttu-id="0bf86-107">參數</span><span class="sxs-lookup"><span data-stu-id="0bf86-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bf86-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0bf86-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0bf86-109">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="0bf86-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0bf86-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0bf86-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0bf86-111">取得滑鼠捕捉的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="0bf86-111">A handle to the window gaining the mouse capture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bf86-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="0bf86-112">Return value</span></span>

<span data-ttu-id="0bf86-113">如果應用程式處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="0bf86-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bf86-114">備註</span><span class="sxs-lookup"><span data-stu-id="0bf86-114">Remarks</span></span>

<span data-ttu-id="0bf86-115">即使視窗呼叫 [**ReleaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture) 本身，也會收到此訊息。</span><span class="sxs-lookup"><span data-stu-id="0bf86-115">A window receives this message even if it calls [**ReleaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture) itself.</span></span> <span data-ttu-id="0bf86-116">應用程式不應該嘗試設定滑鼠捕捉以回應此訊息。</span><span class="sxs-lookup"><span data-stu-id="0bf86-116">An application should not attempt to set the mouse capture in response to this message.</span></span>

<span data-ttu-id="0bf86-117">當它收到這則訊息時，視窗應該視需要重繪自己，以反映新的滑鼠捕捉狀態。</span><span class="sxs-lookup"><span data-stu-id="0bf86-117">When it receives this message, a window should redraw itself, if necessary, to reflect the new mouse-capture state.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bf86-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="0bf86-118">Requirements</span></span>



| <span data-ttu-id="0bf86-119">需求</span><span class="sxs-lookup"><span data-stu-id="0bf86-119">Requirement</span></span> | <span data-ttu-id="0bf86-120">值</span><span class="sxs-lookup"><span data-stu-id="0bf86-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bf86-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0bf86-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0bf86-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0bf86-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0bf86-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0bf86-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0bf86-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0bf86-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0bf86-125">標頭</span><span class="sxs-lookup"><span data-stu-id="0bf86-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0bf86-126"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="0bf86-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bf86-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0bf86-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="0bf86-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="0bf86-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0bf86-129">**ReleaseCapture**</span><span class="sxs-lookup"><span data-stu-id="0bf86-129">**ReleaseCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-releasecapture)
</dt> <dt>

[<span data-ttu-id="0bf86-130">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="0bf86-130">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

<span data-ttu-id="0bf86-131">**概念**</span><span class="sxs-lookup"><span data-stu-id="0bf86-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0bf86-132">滑鼠輸入</span><span class="sxs-lookup"><span data-stu-id="0bf86-132">Mouse Input</span></span>](mouse-input.md)
</dt> </dl>

 

