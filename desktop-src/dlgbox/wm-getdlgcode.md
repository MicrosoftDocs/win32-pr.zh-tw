---
title: 'WM_GETDLGCODE 訊息 (Winuser .h) '
description: 傳送至與控制項相關聯的視窗程式。
ms.assetid: 96d2caee-be6e-46e9-98b3-bffc3af1c003
keywords:
- WM_GETDLGCODE 訊息對話方塊
topic_type:
- apiref
api_name:
- WM_GETDLGCODE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89d6e1ddb3be21e227c4dad404a06113f5c50a49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966130"
---
# <a name="wm_getdlgcode-message"></a><span data-ttu-id="58761-104">WM \_ GETDLGCODE 訊息</span><span class="sxs-lookup"><span data-stu-id="58761-104">WM\_GETDLGCODE message</span></span>

<span data-ttu-id="58761-105">傳送至與控制項相關聯的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="58761-105">Sent to the window procedure associated with a control.</span></span> <span data-ttu-id="58761-106">根據預設，系統會處理所有鍵盤輸入至控制項;系統會將特定類型的鍵盤輸入視為對話方塊流覽鍵。</span><span class="sxs-lookup"><span data-stu-id="58761-106">By default, the system handles all keyboard input to the control; the system interprets certain types of keyboard input as dialog box navigation keys.</span></span> <span data-ttu-id="58761-107">若要覆寫此預設行為，控制項可以回應 **WM \_ GETDLGCODE** 訊息，以指出它所要處理的輸入類型。</span><span class="sxs-lookup"><span data-stu-id="58761-107">To override this default behavior, the control can respond to the **WM\_GETDLGCODE** message to indicate the types of input it wants to process itself.</span></span>


```C++
#define WM_GETDLGCODE                   0x0087
```



## <a name="parameters"></a><span data-ttu-id="58761-108">參數</span><span class="sxs-lookup"><span data-stu-id="58761-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58761-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="58761-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58761-110">使用者按下的虛擬機器碼，會提示 Windows 發出此通知。</span><span class="sxs-lookup"><span data-stu-id="58761-110">The virtual key, pressed by the user, that prompted Windows to issue this notification.</span></span> <span data-ttu-id="58761-111">處理常式必須選擇性地處理這些金鑰。</span><span class="sxs-lookup"><span data-stu-id="58761-111">The handler must selectively handle these keys.</span></span> <span data-ttu-id="58761-112">例如，處理常式可能會接受並處理 **VK \_** 傳回，但是會將 [ **VK \_ ]** 索引標籤委派給擁有者視窗。</span><span class="sxs-lookup"><span data-stu-id="58761-112">For instance, the handler might accept and process **VK\_RETURN** but delegate **VK\_TAB** to the owner window.</span></span> <span data-ttu-id="58761-113">如需值清單，請參閱 [**虛擬機器碼程式碼**](/windows/desktop/inputdev/virtual-key-codes)。</span><span class="sxs-lookup"><span data-stu-id="58761-113">For a list of values, see [**Virtual-Key Codes**](/windows/desktop/inputdev/virtual-key-codes).</span></span>

</dd> <dt>

<span data-ttu-id="58761-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="58761-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58761-115">訊息 [**結構的**](/windows/win32/api/winuser/ns-winuser-msg) 指標 (如果系統正在執行查詢) ，則為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="58761-115">A pointer to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure (or **NULL** if the system is performing a query).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58761-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="58761-116">Return value</span></span>

<span data-ttu-id="58761-117">傳回值是下列其中一個或多個值，指出應用程式處理的輸入類型。</span><span class="sxs-lookup"><span data-stu-id="58761-117">The return value is one or more of the following values, indicating which type of input the application processes.</span></span>



| <span data-ttu-id="58761-118">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="58761-118">Return code/value</span></span>                                                                                                                                                | <span data-ttu-id="58761-119">Description</span><span class="sxs-lookup"><span data-stu-id="58761-119">Description</span></span>                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="58761-120"><dt>**DLGC \_按鈕**</dt> <dt>0x2000</dt></span><span class="sxs-lookup"><span data-stu-id="58761-120"><dt>**DLGC\_BUTTON**</dt> <dt>0x2000</dt></span></span> </dl>          | <span data-ttu-id="58761-121">按鈕。</span><span class="sxs-lookup"><span data-stu-id="58761-121">Button.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="58761-122"><dt>**DLGC \_DEFPUSHBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="58761-122"><dt>**DLGC\_DEFPUSHBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>   | <span data-ttu-id="58761-123">預設的 [推送] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="58761-123">Default push button.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="58761-124"><dt>**DLGC \_HASSETSEL**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="58761-124"><dt>**DLGC\_HASSETSEL**</dt> <dt>0x0008</dt></span></span> </dl>       | <span data-ttu-id="58761-125">[**EM \_SETSEL**](/windows/desktop/Controls/em-setsel) 訊息。</span><span class="sxs-lookup"><span data-stu-id="58761-125">[**EM\_SETSEL**](/windows/desktop/Controls/em-setsel) messages.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="58761-126"><dt>**DLGC \_選項按鈕**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="58761-126"><dt>**DLGC\_RADIOBUTTON**</dt> <dt>0x0040</dt></span></span> </dl>     | <span data-ttu-id="58761-127">選項按鈕。</span><span class="sxs-lookup"><span data-stu-id="58761-127">Radio button.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="58761-128"><dt>**DLGC \_靜態**</dt> <dt>0x0100</dt></span><span class="sxs-lookup"><span data-stu-id="58761-128"><dt>**DLGC\_STATIC**</dt> <dt>0x0100</dt></span></span> </dl>          | <span data-ttu-id="58761-129">靜態控制項。</span><span class="sxs-lookup"><span data-stu-id="58761-129">Static control.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="58761-130"><dt>**DLGC \_UNDEFPUSHBUTTON**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="58761-130"><dt>**DLGC\_UNDEFPUSHBUTTON**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="58761-131">非預設的推送按鈕。</span><span class="sxs-lookup"><span data-stu-id="58761-131">Non-default push button.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="58761-132"><dt>**DLGC \_WANTALLKEYS**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="58761-132"><dt>**DLGC\_WANTALLKEYS**</dt> <dt>0x0004</dt></span></span> </dl>     | <span data-ttu-id="58761-133">所有鍵盤輸入。</span><span class="sxs-lookup"><span data-stu-id="58761-133">All keyboard input.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="58761-134"><dt>**DLGC \_WANTARROWS**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="58761-134"><dt>**DLGC\_WANTARROWS**</dt> <dt>0x0001</dt></span></span> </dl>      | <span data-ttu-id="58761-135">方向按鍵。</span><span class="sxs-lookup"><span data-stu-id="58761-135">Direction keys.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="58761-136"><dt>**DLGC \_WANTCHARS**</dt> <dt>0x0080</dt></span><span class="sxs-lookup"><span data-stu-id="58761-136"><dt>**DLGC\_WANTCHARS**</dt> <dt>0x0080</dt></span></span> </dl>       | <span data-ttu-id="58761-137">[**WM \_CHAR**](/windows/desktop/inputdev/wm-char) 訊息。</span><span class="sxs-lookup"><span data-stu-id="58761-137">[**WM\_CHAR**](/windows/desktop/inputdev/wm-char) messages.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="58761-138"><dt>**DLGC \_WANTMESSAGE**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="58761-138"><dt>**DLGC\_WANTMESSAGE**</dt> <dt>0x0004</dt></span></span> </dl>     | <span data-ttu-id="58761-139">所有鍵盤輸入 (應用程式 [**都會將訊息結構中**](/windows/win32/api/winuser/ns-winuser-msg) 的這個訊息傳遞給控制項) 。</span><span class="sxs-lookup"><span data-stu-id="58761-139">All keyboard input (the application passes this message in the [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure to the control).</span></span><br/> |
| <dl> <span data-ttu-id="58761-140"><dt>**DLGC \_WANTTAB**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="58761-140"><dt>**DLGC\_WANTTAB**</dt> <dt>0x0002</dt></span></span> </dl>         | <span data-ttu-id="58761-141">TAB 鍵。</span><span class="sxs-lookup"><span data-stu-id="58761-141">TAB key.</span></span><br/>                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="58761-142">備註</span><span class="sxs-lookup"><span data-stu-id="58761-142">Remarks</span></span>

<span data-ttu-id="58761-143">雖然 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式一律會傳回零以回應 **WM \_ GETDLGCODE** 訊息，但預先定義之控制項類別的視窗程式會傳回適用于每個類別的程式碼。</span><span class="sxs-lookup"><span data-stu-id="58761-143">Although the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function always returns zero in response to the **WM\_GETDLGCODE** message, the window procedure for the predefined control classes return a code appropriate for each class.</span></span>

<span data-ttu-id="58761-144">只有使用者定義的對話方塊控制項或子類別修改的標準控制項，才能使用 **WM \_ GETDLGCODE** 訊息和傳回的值。</span><span class="sxs-lookup"><span data-stu-id="58761-144">The **WM\_GETDLGCODE** message and the returned values are useful only with user-defined dialog box controls or standard controls modified by subclassing.</span></span>

## <a name="requirements"></a><span data-ttu-id="58761-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="58761-145">Requirements</span></span>



| <span data-ttu-id="58761-146">需求</span><span class="sxs-lookup"><span data-stu-id="58761-146">Requirement</span></span> | <span data-ttu-id="58761-147">值</span><span class="sxs-lookup"><span data-stu-id="58761-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58761-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="58761-148">Minimum supported client</span></span><br/> | <span data-ttu-id="58761-149">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58761-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="58761-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="58761-150">Minimum supported server</span></span><br/> | <span data-ttu-id="58761-151">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58761-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="58761-152">標頭</span><span class="sxs-lookup"><span data-stu-id="58761-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="58761-153"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="58761-153"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58761-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="58761-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="58761-155">**參考**</span><span class="sxs-lookup"><span data-stu-id="58761-155">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="58761-156">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="58761-156">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="58761-157">**EM \_ SETSEL**</span><span class="sxs-lookup"><span data-stu-id="58761-157">**EM\_SETSEL**</span></span>](/windows/desktop/Controls/em-setsel)
</dt> <dt>

[<span data-ttu-id="58761-158">**味精**</span><span class="sxs-lookup"><span data-stu-id="58761-158">**MSG**</span></span>](/windows/win32/api/winuser/ns-winuser-msg)
</dt> <dt>

[<span data-ttu-id="58761-159">**WM \_ 字元**</span><span class="sxs-lookup"><span data-stu-id="58761-159">**WM\_CHAR**</span></span>](/windows/desktop/inputdev/wm-char)
</dt> <dt>

<span data-ttu-id="58761-160">**概念**</span><span class="sxs-lookup"><span data-stu-id="58761-160">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="58761-161">對話方塊</span><span class="sxs-lookup"><span data-stu-id="58761-161">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> </dl>

 

