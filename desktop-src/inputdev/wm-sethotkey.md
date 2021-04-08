---
title: 'WM_SETHOTKEY 訊息 (Winuser .h) '
description: 傳送至視窗，以將熱鍵與視窗相關聯。 當使用者按下快速鍵時，系統會啟動視窗。
ms.assetid: b2c7e6ca-da71-440b-a05e-17f2da419d18
keywords:
- WM_SETHOTKEY 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_SETHOTKEY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ed27a91ddf9506cd12b988db4bd141a988c13e
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "103696296"
---
# <a name="wm_sethotkey-message"></a><span data-ttu-id="103ab-105">WM \_ SETHOTKEY 訊息</span><span class="sxs-lookup"><span data-stu-id="103ab-105">WM\_SETHOTKEY message</span></span>

<span data-ttu-id="103ab-106">傳送至視窗，以將熱鍵與視窗相關聯。</span><span class="sxs-lookup"><span data-stu-id="103ab-106">Sent to a window to associate a hot key with the window.</span></span> <span data-ttu-id="103ab-107">當使用者按下快速鍵時，系統會啟動視窗。</span><span class="sxs-lookup"><span data-stu-id="103ab-107">When the user presses the hot key, the system activates the window.</span></span>


```C++
#define WM_SETHOTKEY                    0x0032
```



## <a name="parameters"></a><span data-ttu-id="103ab-108">參數</span><span class="sxs-lookup"><span data-stu-id="103ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="103ab-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="103ab-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="103ab-110">低序位字組可指定要與視窗相關聯的虛擬按鍵碼。</span><span class="sxs-lookup"><span data-stu-id="103ab-110">The low-order word specifies the virtual-key code to associate with the window.</span></span>

<span data-ttu-id="103ab-111">高序位單字可以是 CommCtrl 中的一或多個下列值。</span><span class="sxs-lookup"><span data-stu-id="103ab-111">The high-order word can be one or more of the following values from CommCtrl.h.</span></span>

<span data-ttu-id="103ab-112">將 *wParam* 設定為 **Null** ，就會移除與視窗相關聯的快速鍵。</span><span class="sxs-lookup"><span data-stu-id="103ab-112">Setting *wParam* to **NULL** removes the hot key associated with a window.</span></span>



| <span data-ttu-id="103ab-113">值</span><span class="sxs-lookup"><span data-stu-id="103ab-113">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="103ab-114">意義</span><span class="sxs-lookup"><span data-stu-id="103ab-114">Meaning</span></span>                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="HOTKEYF_ALT"></span><span id="hotkeyf_alt"></span><dl> <span data-ttu-id="103ab-115"><dt>**HOTKEYF \_ALT**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="103ab-115"><dt>**HOTKEYF\_ALT**</dt> <dt>0x04</dt></span></span> </dl>             | <span data-ttu-id="103ab-116">ALT 鍵</span><span class="sxs-lookup"><span data-stu-id="103ab-116">ALT key</span></span><br/>      |
| <span id="HOTKEYF_CONTROL"></span><span id="hotkeyf_control"></span><dl> <span data-ttu-id="103ab-117"><dt>**HOTKEYF \_控制**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="103ab-117"><dt>**HOTKEYF\_CONTROL**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="103ab-118">CTRL 鍵</span><span class="sxs-lookup"><span data-stu-id="103ab-118">CTRL key</span></span><br/>     |
| <span id="HOTKEYF_EXT"></span><span id="hotkeyf_ext"></span><dl> <span data-ttu-id="103ab-119"><dt>**HOTKEYF \_EXT**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="103ab-119"><dt>**HOTKEYF\_EXT**</dt> <dt>0x08</dt></span></span> </dl>             | <span data-ttu-id="103ab-120">擴充金鑰</span><span class="sxs-lookup"><span data-stu-id="103ab-120">Extended key</span></span><br/> |
| <span id="HOTKEYF_SHIFT"></span><span id="hotkeyf_shift"></span><dl> <span data-ttu-id="103ab-121"><dt>**HOTKEYF \_SHIFT**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="103ab-121"><dt>**HOTKEYF\_SHIFT**</dt> <dt>0x01</dt></span></span> </dl>       | <span data-ttu-id="103ab-122">SHIFT 鍵</span><span class="sxs-lookup"><span data-stu-id="103ab-122">SHIFT key</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="103ab-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="103ab-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="103ab-124">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="103ab-124">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="103ab-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="103ab-125">Return value</span></span>

<span data-ttu-id="103ab-126">傳回值是下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="103ab-126">The return value is one of the following.</span></span>



| <span data-ttu-id="103ab-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="103ab-127">Return value</span></span>                                                                  | <span data-ttu-id="103ab-128">描述</span><span class="sxs-lookup"><span data-stu-id="103ab-128">Description</span></span>                                                                             |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="103ab-129"><dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="103ab-129"><dt>-1</dt></span></span> </dl> | <span data-ttu-id="103ab-130">函數不成功;快速鍵無效。</span><span class="sxs-lookup"><span data-stu-id="103ab-130">The function is unsuccessful; the hot key is invalid.</span></span><br/>                        |
| <dl> <span data-ttu-id="103ab-131"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="103ab-131"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="103ab-132">函數不成功;視窗無效。</span><span class="sxs-lookup"><span data-stu-id="103ab-132">The function is unsuccessful; the window is invalid.</span></span><br/>                         |
| <dl> <span data-ttu-id="103ab-133"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="103ab-133"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="103ab-134">函式成功，而且沒有其他視窗具有相同的快速鍵。</span><span class="sxs-lookup"><span data-stu-id="103ab-134">The function is successful, and no other window has the same hot key.</span></span><br/>        |
| <dl> <span data-ttu-id="103ab-135"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="103ab-135"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="103ab-136">函式成功，但另一個視窗已經有相同的快速鍵。</span><span class="sxs-lookup"><span data-stu-id="103ab-136">The function is successful, but another window already has the same hot key.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="103ab-137">備註</span><span class="sxs-lookup"><span data-stu-id="103ab-137">Remarks</span></span>

<span data-ttu-id="103ab-138">快速鍵無法與子視窗相關聯。</span><span class="sxs-lookup"><span data-stu-id="103ab-138">A hot key cannot be associated with a child window.</span></span>

<span data-ttu-id="103ab-139">**VK \_[ESCAPE**]、[ **VK \_ SPACE**] 和 [ **VK \_ ]** 索引標籤都是不正確快速鍵。</span><span class="sxs-lookup"><span data-stu-id="103ab-139">**VK\_ESCAPE**, **VK\_SPACE**, and **VK\_TAB** are invalid hot keys.</span></span>

<span data-ttu-id="103ab-140">當使用者按下快速鍵時，系統會產生一個 *wParam* 等於 **SC \_ 熱鍵** 的 [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)訊息，而 *lParam* 等於視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="103ab-140">When the user presses the hot key, the system generates a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message with *wParam* equal to **SC\_HOTKEY** and *lParam* equal to the window's handle.</span></span> <span data-ttu-id="103ab-141">如果將此訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)，系統會將視窗的最後一個作用中快顯 (（如果有的話）) 或視窗本身 (如果前景沒有快顯視窗) 。</span><span class="sxs-lookup"><span data-stu-id="103ab-141">If this message is passed on to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), the system will bring the window's last active popup (if it exists) or the window itself (if there is no popup window) to the foreground.</span></span>

<span data-ttu-id="103ab-142">一個視窗只能有一個快速鍵。</span><span class="sxs-lookup"><span data-stu-id="103ab-142">A window can only have one hot key.</span></span> <span data-ttu-id="103ab-143">如果視窗已經有與其相關聯的熱鍵，則新的熱鍵會取代舊的金鑰。</span><span class="sxs-lookup"><span data-stu-id="103ab-143">If the window already has a hot key associated with it, the new hot key replaces the old one.</span></span> <span data-ttu-id="103ab-144">如果有一個以上的視窗具有相同的熱鍵，則由熱鍵啟動的視窗是隨機的。</span><span class="sxs-lookup"><span data-stu-id="103ab-144">If more than one window has the same hot key, the window that is activated by the hot key is random.</span></span>

<span data-ttu-id="103ab-145">這些快速鍵與 [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey)所設定的快速鍵無關。</span><span class="sxs-lookup"><span data-stu-id="103ab-145">These hot keys are unrelated to the hot keys set by [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey).</span></span>

## <a name="requirements"></a><span data-ttu-id="103ab-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="103ab-146">Requirements</span></span>



| <span data-ttu-id="103ab-147">需求</span><span class="sxs-lookup"><span data-stu-id="103ab-147">Requirement</span></span> | <span data-ttu-id="103ab-148">值</span><span class="sxs-lookup"><span data-stu-id="103ab-148">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="103ab-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="103ab-149">Minimum supported client</span></span><br/> | <span data-ttu-id="103ab-150">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="103ab-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="103ab-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="103ab-151">Minimum supported server</span></span><br/> | <span data-ttu-id="103ab-152">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="103ab-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="103ab-153">標頭</span><span class="sxs-lookup"><span data-stu-id="103ab-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="103ab-154"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="103ab-154"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="103ab-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="103ab-155">See also</span></span>

<dl> <dt>

<span data-ttu-id="103ab-156">**參考**</span><span class="sxs-lookup"><span data-stu-id="103ab-156">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="103ab-157">**RegisterHotKey**</span><span class="sxs-lookup"><span data-stu-id="103ab-157">**RegisterHotKey**</span></span>](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[<span data-ttu-id="103ab-158">**WM \_ GETHOTKEY**</span><span class="sxs-lookup"><span data-stu-id="103ab-158">**WM\_GETHOTKEY**</span></span>](wm-gethotkey.md)
</dt> <dt>

[<span data-ttu-id="103ab-159">**WM \_ SYSCOMMAND**</span><span class="sxs-lookup"><span data-stu-id="103ab-159">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="103ab-160">**概念**</span><span class="sxs-lookup"><span data-stu-id="103ab-160">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="103ab-161">鍵盤輸入</span><span class="sxs-lookup"><span data-stu-id="103ab-161">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

