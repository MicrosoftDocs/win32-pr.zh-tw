---
title: 'WM_COMMAND 訊息 (Winuser .h) '
description: 當使用者從功能表中選取命令專案時、控制項將通知訊息傳送至其父視窗，或翻譯快速鍵按鍵時傳送。
ms.assetid: 5516098e-fd90-49c8-afb0-78164b028376
keywords:
- WM_COMMAND 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_COMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 1826c4668f3be8a2991c914e60320b55de867e33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001600"
---
# <a name="wm_command-message"></a><span data-ttu-id="8c9b1-104">WM \_ 命令訊息</span><span class="sxs-lookup"><span data-stu-id="8c9b1-104">WM\_COMMAND message</span></span>

<span data-ttu-id="8c9b1-105">當使用者從功能表中選取命令專案時、控制項將通知訊息傳送至其父視窗，或翻譯快速鍵按鍵時傳送。</span><span class="sxs-lookup"><span data-stu-id="8c9b1-105">Sent when the user selects a command item from a menu, when a control sends a notification message to its parent window, or when an accelerator keystroke is translated.</span></span>


```C++
#define WM_COMMAND                      0x0111
```



## <a name="parameters"></a><span data-ttu-id="8c9b1-106">參數</span><span class="sxs-lookup"><span data-stu-id="8c9b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c9b1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8c9b1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c9b1-108">如需此參數的描述，請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="8c9b1-108">For a description of this parameter, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="8c9b1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8c9b1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c9b1-110">如需此參數的描述，請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="8c9b1-110">For a description of this parameter, see Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c9b1-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="8c9b1-111">Return value</span></span>

<span data-ttu-id="8c9b1-112">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="8c9b1-112">If an application processes this message, it should return zero.</span></span>

## <a name="example"></a><span data-ttu-id="8c9b1-113">範例</span><span class="sxs-lookup"><span data-stu-id="8c9b1-113">Example</span></span>

```c
BOOL AboutDlg (
    HWND hDlg, 
    UINT message, 
    WPARAM wParam, 
    LPARAM lParam)
{
    BOOL bRet = FALSE;
    
    switch (message) 
    {
        case WM_INITDIALOG:
            bRet = TRUE;
            break;

        case WM_COMMAND:
            if (wParam == IDOK ||
                wParam == IDCANCEL) 
            {
                EndDialog(hDlg, TRUE);
                bRet = TRUE;
            }
            break;
    }

    return bRet;
}
```
<span data-ttu-id="8c9b1-114">從 GitHub 上的 [Windows 傳統範例](https://github.com/microsoft/Windows-classic-samples) 取得的範例。</span><span class="sxs-lookup"><span data-stu-id="8c9b1-114">Example taken from [Windows classic samples](https://github.com/microsoft/Windows-classic-samples) on GitHub.</span></span>


## <a name="remarks"></a><span data-ttu-id="8c9b1-115">備註</span><span class="sxs-lookup"><span data-stu-id="8c9b1-115">Remarks</span></span>

<span data-ttu-id="8c9b1-116">這裡摘要說明 *wParam* 和 *lParam* 參數的使用方式。</span><span class="sxs-lookup"><span data-stu-id="8c9b1-116">Use of the *wParam* and *lParam* parameters are summarized here.</span></span>



| <span data-ttu-id="8c9b1-117">訊息來源</span><span class="sxs-lookup"><span data-stu-id="8c9b1-117">Message Source</span></span> | <span data-ttu-id="8c9b1-118">wParam (high word) </span><span class="sxs-lookup"><span data-stu-id="8c9b1-118">wParam (high word)</span></span>                | <span data-ttu-id="8c9b1-119">wParam (低字組) </span><span class="sxs-lookup"><span data-stu-id="8c9b1-119">wParam (low word)</span></span>                | <span data-ttu-id="8c9b1-120">lParam</span><span class="sxs-lookup"><span data-stu-id="8c9b1-120">lParam</span></span>                       |
|----------------|-----------------------------------|----------------------------------|------------------------------|
| <span data-ttu-id="8c9b1-121">功能表</span><span class="sxs-lookup"><span data-stu-id="8c9b1-121">Menu</span></span>           | <span data-ttu-id="8c9b1-122">0</span><span class="sxs-lookup"><span data-stu-id="8c9b1-122">0</span></span>                                 | <span data-ttu-id="8c9b1-123"> (IDM) 的功能表識別碼 \_ \*</span><span class="sxs-lookup"><span data-stu-id="8c9b1-123">Menu identifier (IDM\_\*)</span></span>        | <span data-ttu-id="8c9b1-124">0</span><span class="sxs-lookup"><span data-stu-id="8c9b1-124">0</span></span>                            |
| <span data-ttu-id="8c9b1-125">加速器</span><span class="sxs-lookup"><span data-stu-id="8c9b1-125">Accelerator</span></span>    | <span data-ttu-id="8c9b1-126">1</span><span class="sxs-lookup"><span data-stu-id="8c9b1-126">1</span></span>                                 | <span data-ttu-id="8c9b1-127"> (IDM) 的加速器識別碼 \_ \*</span><span class="sxs-lookup"><span data-stu-id="8c9b1-127">Accelerator identifier (IDM\_\*)</span></span> | <span data-ttu-id="8c9b1-128">0</span><span class="sxs-lookup"><span data-stu-id="8c9b1-128">0</span></span>                            |
| <span data-ttu-id="8c9b1-129">控制</span><span class="sxs-lookup"><span data-stu-id="8c9b1-129">Control</span></span>        | <span data-ttu-id="8c9b1-130">控制項定義的通知碼</span><span class="sxs-lookup"><span data-stu-id="8c9b1-130">Control-defined notification code</span></span> | <span data-ttu-id="8c9b1-131">控制項識別碼</span><span class="sxs-lookup"><span data-stu-id="8c9b1-131">Control identifier</span></span>               | <span data-ttu-id="8c9b1-132">控制視窗的控制碼</span><span class="sxs-lookup"><span data-stu-id="8c9b1-132">Handle to the control window</span></span> |



 

### <a name="menus"></a><span data-ttu-id="8c9b1-133">功能表</span><span class="sxs-lookup"><span data-stu-id="8c9b1-133">Menus</span></span>

<span data-ttu-id="8c9b1-134">如果應用程式啟用功能表分隔符號，則當使用者選取分隔符號時，系統會傳送包含 *wParam* 參數低字的 **WM \_ 命令** 訊息（設為零）。</span><span class="sxs-lookup"><span data-stu-id="8c9b1-134">If an application enables a menu separator, the system sends a **WM\_COMMAND** message with the low-word of the *wParam* parameter set to zero when the user selects the separator.</span></span>

<span data-ttu-id="8c9b1-135">如果功能表定義了 [**MENUINFO 的 dwStyle**](/windows/win32/api/winuser/ns-winuser-menuinfo) 值，則會傳送 **\_** [**wm \_ MENUCOMMAND**](wm-menucommand.md) 而非 **wm \_ 命令**。</span><span class="sxs-lookup"><span data-stu-id="8c9b1-135">If a menu is defined with a [**MENUINFO.dwStyle**](/windows/win32/api/winuser/ns-winuser-menuinfo) value of **MNS\_NOTIFYBYPOS**, [**WM\_MENUCOMMAND**](wm-menucommand.md) is sent instead of **WM\_COMMAND**.</span></span>

### <a name="accelerators"></a><span data-ttu-id="8c9b1-136">快速鍵</span><span class="sxs-lookup"><span data-stu-id="8c9b1-136">Accelerators</span></span>

<span data-ttu-id="8c9b1-137">從 [視窗] 功能表中選取專案的快速鍵按鍵會轉譯成 [**WM \_ SYSCOMMAND**](wm-syscommand.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="8c9b1-137">Accelerator keystrokes that select items from the window menu are translated into [**WM\_SYSCOMMAND**](wm-syscommand.md) messages.</span></span>

<span data-ttu-id="8c9b1-138">當擁有功能表的視窗最小化時，如果出現對應至功能表項目的快速鍵按鍵，則不會傳送任何 **WM \_ 命令** 訊息。</span><span class="sxs-lookup"><span data-stu-id="8c9b1-138">If an accelerator keystroke occurs that corresponds to a menu item when the window that owns the menu is minimized, no **WM\_COMMAND** message is sent.</span></span> <span data-ttu-id="8c9b1-139">但是，如果出現的快速鍵不符合視窗功能表或 [視窗] 功能表中的任何專案，則會傳送 **WM \_ 命令** 訊息，即使視窗最小化也一樣。</span><span class="sxs-lookup"><span data-stu-id="8c9b1-139">However, if an accelerator keystroke occurs that does not match any of the items in the window's menu or in the window menu, a **WM\_COMMAND** message is sent, even if the window is minimized.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c9b1-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c9b1-140">Requirements</span></span>



| <span data-ttu-id="8c9b1-141">需求</span><span class="sxs-lookup"><span data-stu-id="8c9b1-141">Requirement</span></span> | <span data-ttu-id="8c9b1-142">值</span><span class="sxs-lookup"><span data-stu-id="8c9b1-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c9b1-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8c9b1-143">Minimum supported client</span></span><br/> | <span data-ttu-id="8c9b1-144">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c9b1-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8c9b1-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8c9b1-145">Minimum supported server</span></span><br/> | <span data-ttu-id="8c9b1-146">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c9b1-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8c9b1-147">標頭</span><span class="sxs-lookup"><span data-stu-id="8c9b1-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c9b1-148"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="8c9b1-148"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c9b1-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c9b1-149">See also</span></span>

<dl> <dt>

<span data-ttu-id="8c9b1-150">**參考**</span><span class="sxs-lookup"><span data-stu-id="8c9b1-150">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="8c9b1-151">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8c9b1-151">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="8c9b1-152">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8c9b1-152">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="8c9b1-153">**概念**</span><span class="sxs-lookup"><span data-stu-id="8c9b1-153">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8c9b1-154">功能表</span><span class="sxs-lookup"><span data-stu-id="8c9b1-154">Menus</span></span>](menus.md)
</dt> </dl>

 

