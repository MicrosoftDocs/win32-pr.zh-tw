---
title: 'WM_MENUSELECT 訊息 (Winuser .h) '
description: 當使用者選取功能表項目時，傳送至功能表的擁有者視窗。
ms.assetid: 57684a19-dfaa-4e0c-a8ff-010533322cb0
keywords:
- WM_MENUSELECT 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_MENUSELECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdee9187ba2074944b3611fee10f5a22c2cc25ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106973306"
---
# <a name="wm_menuselect-message"></a><span data-ttu-id="2c310-104">WM \_ MENUSELECT 訊息</span><span class="sxs-lookup"><span data-stu-id="2c310-104">WM\_MENUSELECT message</span></span>

<span data-ttu-id="2c310-105">當使用者選取功能表項目時，傳送至功能表的擁有者視窗。</span><span class="sxs-lookup"><span data-stu-id="2c310-105">Sent to a menu's owner window when the user selects a menu item.</span></span>


```C++
#define WM_MENUSELECT                   0x011F
```



## <a name="parameters"></a><span data-ttu-id="2c310-106">參數</span><span class="sxs-lookup"><span data-stu-id="2c310-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c310-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2c310-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c310-108">低序位字組會指定功能表項目或子功能表索引。</span><span class="sxs-lookup"><span data-stu-id="2c310-108">The low-order word specifies the menu item or submenu index.</span></span> <span data-ttu-id="2c310-109">如果選取的專案是命令專案，這個參數會包含功能表項目的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2c310-109">If the selected item is a command item, this parameter contains the identifier of the menu item.</span></span> <span data-ttu-id="2c310-110">如果選取的專案開啟下拉式功能表或子功能表，則此參數包含主功能表中下拉式功能表或子功能表的索引，而 *lParam* 參數包含主 (按一下) 功能表的控制碼;您可以使用 [**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) 函式來取得下拉式功能表或子功能表的功能表控制碼。</span><span class="sxs-lookup"><span data-stu-id="2c310-110">If the selected item opens a drop-down menu or submenu, this parameter contains the index of the drop-down menu or submenu in the main menu, and the *lParam* parameter contains the handle to the main (clicked) menu; use the [**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) function to get the menu handle to the drop-down menu or submenu.</span></span>

<span data-ttu-id="2c310-111">高序位字組指定一或多個功能表旗標。</span><span class="sxs-lookup"><span data-stu-id="2c310-111">The high-order word specifies one or more menu flags.</span></span> <span data-ttu-id="2c310-112">這個參數可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="2c310-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="2c310-113">值</span><span class="sxs-lookup"><span data-stu-id="2c310-113">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="2c310-114">意義</span><span class="sxs-lookup"><span data-stu-id="2c310-114">Meaning</span></span>                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_BITMAP"></span><span id="mf_bitmap"></span><dl> <span data-ttu-id="2c310-115"><dt>**MF \_點陣圖**</dt> <dt>0x00000004L</dt></span><span class="sxs-lookup"><span data-stu-id="2c310-115"><dt>**MF\_BITMAP**</dt> <dt>0x00000004L</dt></span></span> </dl>                | <span data-ttu-id="2c310-116">專案會顯示點陣圖。</span><span class="sxs-lookup"><span data-stu-id="2c310-116">Item displays a bitmap.</span></span><br/>                                                                                                 |
| <span id="MF_CHECKED"></span><span id="mf_checked"></span><dl> <span data-ttu-id="2c310-117"><dt>**MF \_已檢查**</dt> <dt>0x00000008L</dt></span><span class="sxs-lookup"><span data-stu-id="2c310-117"><dt>**MF\_CHECKED**</dt> <dt>0x00000008L</dt></span></span> </dl>             | <span data-ttu-id="2c310-118">已檢查項目。</span><span class="sxs-lookup"><span data-stu-id="2c310-118">Item is checked.</span></span><br/>                                                                                                        |
| <span id="MF_DISABLED"></span><span id="mf_disabled"></span><dl> <span data-ttu-id="2c310-119"><dt>**MF \_停用**</dt>的 <dt>0x00000002L</dt></span><span class="sxs-lookup"><span data-stu-id="2c310-119"><dt>**MF\_DISABLED**</dt> <dt>0x00000002L</dt></span></span> </dl>          | <span data-ttu-id="2c310-120">專案已停用。</span><span class="sxs-lookup"><span data-stu-id="2c310-120">Item is disabled.</span></span><br/>                                                                                                       |
| <span id="MF_GRAYED"></span><span id="mf_grayed"></span><dl> <span data-ttu-id="2c310-121"><dt>**MF \_灰色**</dt> <dt>0x00000001L</dt></span><span class="sxs-lookup"><span data-stu-id="2c310-121"><dt>**MF\_GRAYED**</dt> <dt>0x00000001L</dt></span></span> </dl>                | <span data-ttu-id="2c310-122">專案會呈現灰色。</span><span class="sxs-lookup"><span data-stu-id="2c310-122">Item is grayed.</span></span><br/>                                                                                                         |
| <span id="MF_HILITE"></span><span id="mf_hilite"></span><dl> <span data-ttu-id="2c310-123"><dt>**MF \_HILITE**</dt> <dt>0x00000080L</dt></span><span class="sxs-lookup"><span data-stu-id="2c310-123"><dt>**MF\_HILITE**</dt> <dt>0x00000080L</dt></span></span> </dl>                | <span data-ttu-id="2c310-124">專案已反白顯示。</span><span class="sxs-lookup"><span data-stu-id="2c310-124">Item is highlighted.</span></span><br/>                                                                                                    |
| <span id="MF_MOUSESELECT"></span><span id="mf_mouseselect"></span><dl> <span data-ttu-id="2c310-125"><dt>**MF \_MOUSESELECT**</dt> <dt>0x00008000L</dt></span><span class="sxs-lookup"><span data-stu-id="2c310-125"><dt>**MF\_MOUSESELECT**</dt> <dt>0x00008000L</dt></span></span> </dl> | <span data-ttu-id="2c310-126">使用滑鼠來選取專案。</span><span class="sxs-lookup"><span data-stu-id="2c310-126">Item is selected with the mouse.</span></span><br/>                                                                                        |
| <span id="MF_OWNERDRAW"></span><span id="mf_ownerdraw"></span><dl> <span data-ttu-id="2c310-127"><dt>**MF \_OWNERDRAW**</dt> <dt>0x00000100L</dt></span><span class="sxs-lookup"><span data-stu-id="2c310-127"><dt>**MF\_OWNERDRAW**</dt> <dt>0x00000100L</dt></span></span> </dl>       | <span data-ttu-id="2c310-128">專案是擁有者繪製的專案。</span><span class="sxs-lookup"><span data-stu-id="2c310-128">Item is an owner-drawn item.</span></span><br/>                                                                                            |
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <span data-ttu-id="2c310-129"><dt>**MF \_快顯視窗**</dt> <dt>0x00000010L</dt></span><span class="sxs-lookup"><span data-stu-id="2c310-129"><dt>**MF\_POPUP**</dt> <dt>0x00000010L</dt></span></span> </dl>                   | <span data-ttu-id="2c310-130">專案會開啟下拉式功能表或子功能表。</span><span class="sxs-lookup"><span data-stu-id="2c310-130">Item opens a drop-down menu or submenu.</span></span><br/>                                                                                 |
| <span id="MF_SYSMENU"></span><span id="mf_sysmenu"></span><dl> <span data-ttu-id="2c310-131"><dt>**MF \_SYSMENU**</dt> <dt>0x00002000L</dt></span><span class="sxs-lookup"><span data-stu-id="2c310-131"><dt>**MF\_SYSMENU**</dt> <dt>0x00002000L</dt></span></span> </dl>             | <span data-ttu-id="2c310-132">專案會包含在 [視窗] 功能表中。</span><span class="sxs-lookup"><span data-stu-id="2c310-132">Item is contained in the window menu.</span></span> <span data-ttu-id="2c310-133">*LParam* 參數包含與訊息相關聯之功能表的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2c310-133">The *lParam* parameter contains a handle to the menu associated with the message.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2c310-134">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2c310-134">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c310-135">已按下之功能表的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2c310-135">A handle to the menu that was clicked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c310-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="2c310-136">Return value</span></span>

<span data-ttu-id="2c310-137">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="2c310-137">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c310-138">備註</span><span class="sxs-lookup"><span data-stu-id="2c310-138">Remarks</span></span>

<span data-ttu-id="2c310-139">如果 *wParam* 的高序位字包含0xffff，而 *LParam* 參數包含 **Null**，則系統已關閉功能表。</span><span class="sxs-lookup"><span data-stu-id="2c310-139">If the high-order word of *wParam* contains 0xFFFF and the *lParam* parameter contains **NULL**, the system has closed the menu.</span></span>

<span data-ttu-id="2c310-140">請勿針對 *wParam* 的高序位字使用值1，因為此值指定為 (**UINT**) [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) (*wParam*) 。</span><span class="sxs-lookup"><span data-stu-id="2c310-140">Do not use the value  1 for the high-order word of *wParam*, because this value is specified as (**UINT**) [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(*wParam*).</span></span> <span data-ttu-id="2c310-141">如果值為0xFFFF，則會將它轉譯為0x0000FFFF，而不是1，因為轉換成 **UINT**。</span><span class="sxs-lookup"><span data-stu-id="2c310-141">If the value is 0xFFFF, it would be interpreted as 0x0000FFFF, not  1, because of the cast to a **UINT**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c310-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c310-142">Requirements</span></span>



| <span data-ttu-id="2c310-143">需求</span><span class="sxs-lookup"><span data-stu-id="2c310-143">Requirement</span></span> | <span data-ttu-id="2c310-144">值</span><span class="sxs-lookup"><span data-stu-id="2c310-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c310-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2c310-145">Minimum supported client</span></span><br/> | <span data-ttu-id="2c310-146">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c310-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2c310-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2c310-147">Minimum supported server</span></span><br/> | <span data-ttu-id="2c310-148">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c310-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2c310-149">標頭</span><span class="sxs-lookup"><span data-stu-id="2c310-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c310-150"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="2c310-150"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c310-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c310-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="2c310-152">**參考**</span><span class="sxs-lookup"><span data-stu-id="2c310-152">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2c310-153">**GetSubMenu**</span><span class="sxs-lookup"><span data-stu-id="2c310-153">**GetSubMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getsubmenu)
</dt> <dt>

<span data-ttu-id="2c310-154">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2c310-154">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="2c310-155">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2c310-155">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="2c310-156">**概念**</span><span class="sxs-lookup"><span data-stu-id="2c310-156">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2c310-157">鍵盤加速器</span><span class="sxs-lookup"><span data-stu-id="2c310-157">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

