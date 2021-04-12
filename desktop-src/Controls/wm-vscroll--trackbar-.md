---
title: 'WM_VSCROLL (的)  (Winuser 通知碼) '
description: '\_當滑杆變更位置時，會將 WM VSCROLL 訊息傳送給垂直的 [對齊程式] 控制項的擁有者。 視窗會透過其 WindowProc 函數接收此訊息。'
ms.assetid: E491E210-9605-4ABB-A667-471830DA7C2B
keywords:
- WM_VSCROLL (的程式碼段) 通知程式碼 Windows 控制項
topic_type:
- apiref
api_name:
- WM_HSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1e13b07fab3335bf99469cd43ed1caa10373a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104417"
---
# <a name="wm_vscroll-trackbar-notification-code"></a><span data-ttu-id="97005-105">WM \_ VSCROLL (的) 通知碼</span><span class="sxs-lookup"><span data-stu-id="97005-105">WM\_VSCROLL (Trackbar) notification code</span></span>

<span data-ttu-id="97005-106">當滑杆變更位置時，會將 **WM \_ VSCROLL** 訊息傳送給垂直的 [對齊程式] 控制項的擁有者。</span><span class="sxs-lookup"><span data-stu-id="97005-106">The **WM\_VSCROLL** message is sent to the owner of a vertical trackbar control when the slider changes position.</span></span>

<span data-ttu-id="97005-107">視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="97005-107">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_HSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="97005-108">參數</span><span class="sxs-lookup"><span data-stu-id="97005-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97005-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="97005-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97005-110">如果 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是 tb THUMBPOSITION 或 tb THUMBTRACK， [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定滑杆的目前位置 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="97005-110">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the current position of the slider if the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is TB\_THUMBPOSITION or TB\_THUMBTRACK.</span></span> <span data-ttu-id="97005-111">若為所有其他通知碼，高序位字是零;傳送 [**TBM \_ GETPOS**](tbm-getpos.md) 訊息來判斷滑杆的位置。</span><span class="sxs-lookup"><span data-stu-id="97005-111">For all other notification codes, the high-order word is zero; send the [**TBM\_GETPOS**](tbm-getpos.md) message to determine the slider position.</span></span>

<span data-ttu-id="97005-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定通知碼，指出使用者與該使用者的互動。</span><span class="sxs-lookup"><span data-stu-id="97005-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies a notification code that indicates the user's interaction with the trackbar.</span></span> <span data-ttu-id="97005-113">這個單字可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="97005-113">This word can be one of the following values.</span></span>



| <span data-ttu-id="97005-114">值</span><span class="sxs-lookup"><span data-stu-id="97005-114">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="97005-115">意義</span><span class="sxs-lookup"><span data-stu-id="97005-115">Meaning</span></span>                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TB_BOTTOM"></span><span id="tb_bottom"></span><dl> <span data-ttu-id="97005-116"><dt>**TB \_ 底部**</dt></span><span class="sxs-lookup"><span data-stu-id="97005-116"><dt>**TB\_BOTTOM**</dt></span></span> </dl>                      | <span data-ttu-id="97005-117">使用者按下 END 鍵 ([**VK \_ end**](/windows/desktop/inputdev/virtual-key-codes)) 。</span><span class="sxs-lookup"><span data-stu-id="97005-117">The user pressed the END key ([**VK\_END**](/windows/desktop/inputdev/virtual-key-codes)).</span></span><br/>                                                                                          |
| <span id="TB_ENDTRACK"></span><span id="tb_endtrack"></span><dl> <span data-ttu-id="97005-118"><dt>**TB \_ ENDTRACK**</dt></span><span class="sxs-lookup"><span data-stu-id="97005-118"><dt>**TB\_ENDTRACK**</dt></span></span> </dl>                | <span data-ttu-id="97005-119">這些程式碼段收到了 [**WM 的 \_ KEYUP**](/windows/desktop/inputdev/wm-keyup)，這表示使用者發行了一個已傳送相關虛擬金鑰程式碼的金鑰。</span><span class="sxs-lookup"><span data-stu-id="97005-119">The trackbar received [**WM\_KEYUP**](/windows/desktop/inputdev/wm-keyup), meaning that the user released a key that sent a relevant virtual key code.</span></span> <br/>                                           |
| <span id="TB_LINEDOWN"></span><span id="tb_linedown"></span><dl> <span data-ttu-id="97005-120"><dt>**TB \_ LINEDOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="97005-120"><dt>**TB\_LINEDOWN**</dt></span></span> </dl>                | <span data-ttu-id="97005-121">使用者按下向右箭號 ([**VK \_ 右**](/windows/desktop/inputdev/virtual-key-codes)) 或向下箭號 ([**\_ 向下 VK**](/windows/desktop/inputdev/virtual-key-codes)) 按鍵。</span><span class="sxs-lookup"><span data-stu-id="97005-121">The user pressed the RIGHT ARROW ([**VK\_RIGHT**](/windows/desktop/inputdev/virtual-key-codes)) or DOWN ARROW ([**VK\_DOWN**](/windows/desktop/inputdev/virtual-key-codes)) key.</span></span><br/> |
| <span id="TB_LINEUP"></span><span id="tb_lineup"></span><dl> <span data-ttu-id="97005-122"><dt>**TB 的 \_ 系列**</dt></span><span class="sxs-lookup"><span data-stu-id="97005-122"><dt>**TB\_LINEUP**</dt></span></span> </dl>                      | <span data-ttu-id="97005-123">使用者按下左方箭號 ([**VK \_ 左**](/windows/desktop/inputdev/virtual-key-codes)) 或向上箭號 [**(\_ 向上 VK**](/windows/desktop/inputdev/virtual-key-codes)) 鍵。</span><span class="sxs-lookup"><span data-stu-id="97005-123">The user pressed the LEFT ARROW ([**VK\_LEFT**](/windows/desktop/inputdev/virtual-key-codes)) or UP ARROW ([**VK\_UP**](/windows/desktop/inputdev/virtual-key-codes)) key.</span></span><br/>             |
| <span id="TB_PAGEDOWN"></span><span id="tb_pagedown"></span><dl> <span data-ttu-id="97005-124"><dt>**TB \_ PAGEDOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="97005-124"><dt>**TB\_PAGEDOWN**</dt></span></span> </dl>                | <span data-ttu-id="97005-125">使用者按一下滑杆下方或右邊的頻道 ([**VK \_ 下一個**](/windows/desktop/inputdev/virtual-key-codes)) 。</span><span class="sxs-lookup"><span data-stu-id="97005-125">The user clicked the channel below or to the right of the slider ([**VK\_NEXT**](/windows/desktop/inputdev/virtual-key-codes)).</span></span><br/>                                                   |
| <span id="TB_PAGEUP"></span><span id="tb_pageup"></span><dl> <span data-ttu-id="97005-126"><dt>**TB \_ PAGEUP**</dt></span><span class="sxs-lookup"><span data-stu-id="97005-126"><dt>**TB\_PAGEUP**</dt></span></span> </dl>                      | <span data-ttu-id="97005-127">使用者按一下滑杆上方或左邊的頻道 ([**VK \_ 之前**](/windows/desktop/inputdev/virtual-key-codes) 的) 。</span><span class="sxs-lookup"><span data-stu-id="97005-127">The user clicked the channel above or to the left of the slider ([**VK\_PRIOR**](/windows/desktop/inputdev/virtual-key-codes)).</span></span><br/>                                                 |
| <span id="TB_THUMBPOSITION"></span><span id="tb_thumbposition"></span><dl> <span data-ttu-id="97005-128"><dt>**TB \_ THUMBPOSITION**</dt></span><span class="sxs-lookup"><span data-stu-id="97005-128"><dt>**TB\_THUMBPOSITION**</dt></span></span> </dl> | <span data-ttu-id="97005-129">這些程式碼段在 THUMBTRACK 通知碼之後收到了 [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) \_ 。</span><span class="sxs-lookup"><span data-stu-id="97005-129">The trackbar received [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) following a TB\_THUMBTRACK notification code.</span></span><br/>                                                                   |
| <span id="TB_THUMBTRACK"></span><span id="tb_thumbtrack"></span><dl> <span data-ttu-id="97005-130"><dt>**TB \_ THUMBTRACK**</dt></span><span class="sxs-lookup"><span data-stu-id="97005-130"><dt>**TB\_THUMBTRACK**</dt></span></span> </dl>          | <span data-ttu-id="97005-131">使用者拖曳滑杆。</span><span class="sxs-lookup"><span data-stu-id="97005-131">The user dragged the slider.</span></span><br/>                                                                                                                                                     |
| <span id="TB_TOP"></span><span id="tb_top"></span><dl> <span data-ttu-id="97005-132"><dt>**TB \_ TOP**</dt></span><span class="sxs-lookup"><span data-stu-id="97005-132"><dt>**TB\_TOP**</dt></span></span> </dl>                               | <span data-ttu-id="97005-133">使用者按下 HOME 鍵 ([**VK \_ home**](/windows/desktop/inputdev/virtual-key-codes)) 。</span><span class="sxs-lookup"><span data-stu-id="97005-133">The user pressed the HOME key ([**VK\_HOME**](/windows/desktop/inputdev/virtual-key-codes)).</span></span> <br/>                                                                                     |



 

</dd> <dt>

<span data-ttu-id="97005-134">*lParam*</span><span class="sxs-lookup"><span data-stu-id="97005-134">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97005-135">[處理] 控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="97005-135">The handle to the trackbar control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97005-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="97005-136">Return value</span></span>

<span data-ttu-id="97005-137">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="97005-137">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="97005-138">備註</span><span class="sxs-lookup"><span data-stu-id="97005-138">Remarks</span></span>

<span data-ttu-id="97005-139">\_當使用者拖曳捲動方塊時，提供意見反應的應用程式通常會使用 TB THUMBTRACK 程式碼。</span><span class="sxs-lookup"><span data-stu-id="97005-139">The TB\_THUMBTRACK code is typically used by applications that provide feedback as the user drags the scroll box.</span></span>

<span data-ttu-id="97005-140">請注意， **WM \_ VSCROLL** 訊息只會攜帶16位的位置資料。</span><span class="sxs-lookup"><span data-stu-id="97005-140">Note that the **WM\_VSCROLL** message carries only 16 bits of position data.</span></span> <span data-ttu-id="97005-141">因此，僅依賴 **WM \_ VSCROLL** (和 [**wm \_ HSCROLL**](wm-hscroll--trackbar-.md)) 的滑杆位置資料的應用程式，其實際最大位置值為65535。</span><span class="sxs-lookup"><span data-stu-id="97005-141">Thus, applications that rely solely on **WM\_VSCROLL** (and [**WM\_HSCROLL**](wm-hscroll--trackbar-.md)) for slider position data have a practical maximum position value of 65,535.</span></span>

## <a name="requirements"></a><span data-ttu-id="97005-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="97005-142">Requirements</span></span>



| <span data-ttu-id="97005-143">需求</span><span class="sxs-lookup"><span data-stu-id="97005-143">Requirement</span></span> | <span data-ttu-id="97005-144">值</span><span class="sxs-lookup"><span data-stu-id="97005-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97005-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="97005-145">Minimum supported client</span></span><br/> | <span data-ttu-id="97005-146">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97005-146">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="97005-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="97005-147">Minimum supported server</span></span><br/> | <span data-ttu-id="97005-148">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97005-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="97005-149">標頭</span><span class="sxs-lookup"><span data-stu-id="97005-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="97005-150"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="97005-150"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97005-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97005-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="97005-152">**參考**</span><span class="sxs-lookup"><span data-stu-id="97005-152">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="97005-153">**WM \_ HSCROLL**</span><span class="sxs-lookup"><span data-stu-id="97005-153">**WM\_HSCROLL**</span></span>](wm-hscroll--trackbar-.md)
</dt> </dl>

 

