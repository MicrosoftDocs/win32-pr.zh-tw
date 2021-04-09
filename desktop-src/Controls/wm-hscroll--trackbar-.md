---
title: 'WM_HSCROLL (的)  (Winuser 通知碼) '
description: '\_當滑杆變更位置時，會將 WM HSCROLL 訊息傳送給水準的 [顯示] 控制項的擁有者。 視窗會透過其 WindowProc 函數接收此訊息。'
ms.assetid: EC4AF407-E13F-4562-A0A6-FA109C15101B
keywords:
- WM_HSCROLL (的程式碼段) 通知程式碼 Windows 控制項
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
ms.openlocfilehash: 10727b745900520e8af31561236c8e93eeeb3a81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025026"
---
# <a name="wm_hscroll-trackbar-notification-code"></a><span data-ttu-id="abff5-105">WM \_ HSCROLL (的) 通知碼</span><span class="sxs-lookup"><span data-stu-id="abff5-105">WM\_HSCROLL (Trackbar) notification code</span></span>

<span data-ttu-id="abff5-106">當滑杆變更位置時，會將 **WM \_ HSCROLL** 訊息傳送給水準的 [顯示] 控制項的擁有者。</span><span class="sxs-lookup"><span data-stu-id="abff5-106">The **WM\_HSCROLL** message is sent to the owner of a horizontal trackbar control when the slider changes position.</span></span>

<span data-ttu-id="abff5-107">視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="abff5-107">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_HSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="abff5-108">參數</span><span class="sxs-lookup"><span data-stu-id="abff5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abff5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="abff5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="abff5-110">如果 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是 tb THUMBPOSITION 或 tb THUMBTRACK， [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定滑杆的目前位置 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="abff5-110">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the current position of the slider if the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is TB\_THUMBPOSITION or TB\_THUMBTRACK.</span></span> <span data-ttu-id="abff5-111">若為所有其他通知碼，高序位字是零;傳送 [**TBM \_ GETPOS**](tbm-getpos.md) 訊息來判斷滑杆的位置。</span><span class="sxs-lookup"><span data-stu-id="abff5-111">For all other notification codes, the high-order word is zero; send the [**TBM\_GETPOS**](tbm-getpos.md) message to determine the slider position.</span></span>

<span data-ttu-id="abff5-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定通知碼，指出使用者與該使用者的互動。</span><span class="sxs-lookup"><span data-stu-id="abff5-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies a notification code that indicates the user's interaction with the trackbar.</span></span> <span data-ttu-id="abff5-113">這個單字可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="abff5-113">This word can be one of the following values.</span></span>



| <span data-ttu-id="abff5-114">值</span><span class="sxs-lookup"><span data-stu-id="abff5-114">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="abff5-115">意義</span><span class="sxs-lookup"><span data-stu-id="abff5-115">Meaning</span></span>                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TB_BOTTOM"></span><span id="tb_bottom"></span><dl> <span data-ttu-id="abff5-116"><dt>**TB \_ 底部**</dt></span><span class="sxs-lookup"><span data-stu-id="abff5-116"><dt>**TB\_BOTTOM**</dt></span></span> </dl>                      | <span data-ttu-id="abff5-117">使用者按下 END 鍵 ([**VK \_ end**](/windows/desktop/inputdev/virtual-key-codes)) 。</span><span class="sxs-lookup"><span data-stu-id="abff5-117">The user pressed the END key ([**VK\_END**](/windows/desktop/inputdev/virtual-key-codes)).</span></span><br/>                                                                                          |
| <span id="TB_ENDTRACK"></span><span id="tb_endtrack"></span><dl> <span data-ttu-id="abff5-118"><dt>**TB \_ ENDTRACK**</dt></span><span class="sxs-lookup"><span data-stu-id="abff5-118"><dt>**TB\_ENDTRACK**</dt></span></span> </dl>                | <span data-ttu-id="abff5-119">這些程式碼段收到了 [**WM 的 \_ KEYUP**](/windows/desktop/inputdev/wm-keyup)，這表示使用者發行了一個已傳送相關虛擬金鑰程式碼的金鑰。</span><span class="sxs-lookup"><span data-stu-id="abff5-119">The trackbar received [**WM\_KEYUP**](/windows/desktop/inputdev/wm-keyup), meaning that the user released a key that sent a relevant virtual key code.</span></span> <br/>                                           |
| <span id="TB_LINEDOWN"></span><span id="tb_linedown"></span><dl> <span data-ttu-id="abff5-120"><dt>**TB \_ LINEDOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="abff5-120"><dt>**TB\_LINEDOWN**</dt></span></span> </dl>                | <span data-ttu-id="abff5-121">使用者按下向右箭號 ([**VK \_ 右**](/windows/desktop/inputdev/virtual-key-codes)) 或向下箭號 ([**\_ 向下 VK**](/windows/desktop/inputdev/virtual-key-codes)) 按鍵。</span><span class="sxs-lookup"><span data-stu-id="abff5-121">The user pressed the RIGHT ARROW ([**VK\_RIGHT**](/windows/desktop/inputdev/virtual-key-codes)) or DOWN ARROW ([**VK\_DOWN**](/windows/desktop/inputdev/virtual-key-codes)) key.</span></span><br/> |
| <span id="TB_LINEUP"></span><span id="tb_lineup"></span><dl> <span data-ttu-id="abff5-122"><dt>**TB 的 \_ 系列**</dt></span><span class="sxs-lookup"><span data-stu-id="abff5-122"><dt>**TB\_LINEUP**</dt></span></span> </dl>                      | <span data-ttu-id="abff5-123">使用者按下左方箭號 ([**VK \_ 左**](/windows/desktop/inputdev/virtual-key-codes)) 或向上箭號 [**(\_ 向上 VK**](/windows/desktop/inputdev/virtual-key-codes)) 鍵。</span><span class="sxs-lookup"><span data-stu-id="abff5-123">The user pressed the LEFT ARROW ([**VK\_LEFT**](/windows/desktop/inputdev/virtual-key-codes)) or UP ARROW ([**VK\_UP**](/windows/desktop/inputdev/virtual-key-codes)) key.</span></span><br/>             |
| <span id="TB_PAGEDOWN"></span><span id="tb_pagedown"></span><dl> <span data-ttu-id="abff5-124"><dt>**TB \_ PAGEDOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="abff5-124"><dt>**TB\_PAGEDOWN**</dt></span></span> </dl>                | <span data-ttu-id="abff5-125">使用者按一下滑杆下方或右邊的頻道 ([**VK \_ 下一個**](/windows/desktop/inputdev/virtual-key-codes)) 。</span><span class="sxs-lookup"><span data-stu-id="abff5-125">The user clicked the channel below or to the right of the slider ([**VK\_NEXT**](/windows/desktop/inputdev/virtual-key-codes)).</span></span><br/>                                                   |
| <span id="TB_PAGEUP"></span><span id="tb_pageup"></span><dl> <span data-ttu-id="abff5-126"><dt>**TB \_ PAGEUP**</dt></span><span class="sxs-lookup"><span data-stu-id="abff5-126"><dt>**TB\_PAGEUP**</dt></span></span> </dl>                      | <span data-ttu-id="abff5-127">使用者按一下滑杆上方或左邊的頻道 ([**VK \_ 之前**](/windows/desktop/inputdev/virtual-key-codes) 的) 。</span><span class="sxs-lookup"><span data-stu-id="abff5-127">The user clicked the channel above or to the left of the slider ([**VK\_PRIOR**](/windows/desktop/inputdev/virtual-key-codes)).</span></span><br/>                                                 |
| <span id="TB_THUMBPOSITION"></span><span id="tb_thumbposition"></span><dl> <span data-ttu-id="abff5-128"><dt>**TB \_ THUMBPOSITION**</dt></span><span class="sxs-lookup"><span data-stu-id="abff5-128"><dt>**TB\_THUMBPOSITION**</dt></span></span> </dl> | <span data-ttu-id="abff5-129">這些程式碼段在 THUMBTRACK 通知碼之後收到了 [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) \_ 。</span><span class="sxs-lookup"><span data-stu-id="abff5-129">The trackbar received [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) following a TB\_THUMBTRACK notification code.</span></span><br/>                                                                   |
| <span id="TB_THUMBTRACK"></span><span id="tb_thumbtrack"></span><dl> <span data-ttu-id="abff5-130"><dt>**TB \_ THUMBTRACK**</dt></span><span class="sxs-lookup"><span data-stu-id="abff5-130"><dt>**TB\_THUMBTRACK**</dt></span></span> </dl>          | <span data-ttu-id="abff5-131">使用者拖曳滑杆。</span><span class="sxs-lookup"><span data-stu-id="abff5-131">The user dragged the slider.</span></span><br/>                                                                                                                                                     |
| <span id="TB_TOP"></span><span id="tb_top"></span><dl> <span data-ttu-id="abff5-132"><dt>**TB \_ TOP**</dt></span><span class="sxs-lookup"><span data-stu-id="abff5-132"><dt>**TB\_TOP**</dt></span></span> </dl>                               | <span data-ttu-id="abff5-133">使用者按下 HOME 鍵 ([**VK \_ home**](/windows/desktop/inputdev/virtual-key-codes)) 。</span><span class="sxs-lookup"><span data-stu-id="abff5-133">The user pressed the HOME key ([**VK\_HOME**](/windows/desktop/inputdev/virtual-key-codes)).</span></span> <br/>                                                                                     |



 

</dd> <dt>

<span data-ttu-id="abff5-134">*lParam*</span><span class="sxs-lookup"><span data-stu-id="abff5-134">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="abff5-135">[處理] 控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="abff5-135">The handle to the trackbar control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abff5-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="abff5-136">Return value</span></span>

<span data-ttu-id="abff5-137">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="abff5-137">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="abff5-138">備註</span><span class="sxs-lookup"><span data-stu-id="abff5-138">Remarks</span></span>

<span data-ttu-id="abff5-139">\_當使用者拖曳捲動方塊時，提供意見反應的應用程式通常會使用 TB THUMBTRACK 程式碼。</span><span class="sxs-lookup"><span data-stu-id="abff5-139">The TB\_THUMBTRACK code is typically used by applications that provide feedback as the user drags the scroll box.</span></span>

<span data-ttu-id="abff5-140">請注意， **WM \_ HSCROLL** 訊息只會攜帶16位的位置資料。</span><span class="sxs-lookup"><span data-stu-id="abff5-140">Note that the **WM\_HSCROLL** message carries only 16 bits of position data.</span></span> <span data-ttu-id="abff5-141">因此，僅依賴 **WM \_ HSCROLL** (和 [**wm \_ VSCROLL**](wm-vscroll--trackbar-.md)) 的滑杆位置資料的應用程式，其實際最大位置值為65535。</span><span class="sxs-lookup"><span data-stu-id="abff5-141">Thus, applications that rely solely on **WM\_HSCROLL** (and [**WM\_VSCROLL**](wm-vscroll--trackbar-.md)) for slider position data have a practical maximum position value of 65,535.</span></span>

## <a name="requirements"></a><span data-ttu-id="abff5-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="abff5-142">Requirements</span></span>



| <span data-ttu-id="abff5-143">需求</span><span class="sxs-lookup"><span data-stu-id="abff5-143">Requirement</span></span> | <span data-ttu-id="abff5-144">值</span><span class="sxs-lookup"><span data-stu-id="abff5-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abff5-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="abff5-145">Minimum supported client</span></span><br/> | <span data-ttu-id="abff5-146">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="abff5-146">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="abff5-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="abff5-147">Minimum supported server</span></span><br/> | <span data-ttu-id="abff5-148">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="abff5-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="abff5-149">標頭</span><span class="sxs-lookup"><span data-stu-id="abff5-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="abff5-150"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="abff5-150"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abff5-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="abff5-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="abff5-152">**參考**</span><span class="sxs-lookup"><span data-stu-id="abff5-152">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="abff5-153">**WM \_ VSCROLL**</span><span class="sxs-lookup"><span data-stu-id="abff5-153">**WM\_VSCROLL**</span></span>](wm-vscroll--trackbar-.md)
</dt> </dl>

 

