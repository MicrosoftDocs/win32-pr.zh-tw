---
title: 'WM_CONTEXTMENU 訊息 (Winuser .h) '
description: 通知視窗，使用者按一下滑鼠右鍵， (以滑鼠右鍵按一下視窗中的) 。
ms.assetid: e607a61a-0f9b-4d11-b8c0-b01a2e7fb35b
keywords:
- WM_CONTEXTMENU 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_CONTEXTMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff7764926709bfc8ab6aa95be330a9d45d38bc48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968553"
---
# <a name="wm_contextmenu-message"></a><span data-ttu-id="2fe1a-104">WM \_ CONTEXTMENU 訊息</span><span class="sxs-lookup"><span data-stu-id="2fe1a-104">WM\_CONTEXTMENU message</span></span>

<span data-ttu-id="2fe1a-105">通知視窗，使用者希望顯示內容功能表。</span><span class="sxs-lookup"><span data-stu-id="2fe1a-105">Notifies a window that the user desires a context menu to appear.</span></span>  <span data-ttu-id="2fe1a-106">使用者可能按一下滑鼠右鍵， (在視窗中以滑鼠右鍵按一下) ，按下 Shift + F10 鍵，或按下應用程式鍵 (內容功能表鍵) 可在某些鍵盤上使用。</span><span class="sxs-lookup"><span data-stu-id="2fe1a-106">The user may have clicked the right mouse button (right-clicked) in the window, pressed Shift+F10 or pressed the applications key (context menu key) available on some keyboards.</span></span>


```C++
#define WM_CONTEXTMENU                  0x007B
```



## <a name="parameters"></a><span data-ttu-id="2fe1a-107">參數</span><span class="sxs-lookup"><span data-stu-id="2fe1a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fe1a-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2fe1a-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2fe1a-109">視窗的控制碼，使用者以滑鼠右鍵按一下該視窗。</span><span class="sxs-lookup"><span data-stu-id="2fe1a-109">A handle to the window in which the user right-clicked the mouse.</span></span> <span data-ttu-id="2fe1a-110">這可以是接收訊息之視窗的子視窗。</span><span class="sxs-lookup"><span data-stu-id="2fe1a-110">This can be a child window of the window receiving the message.</span></span> <span data-ttu-id="2fe1a-111">如需有關處理此訊息的詳細資訊，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="2fe1a-111">For more information about processing this message, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="2fe1a-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2fe1a-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2fe1a-113">低序位單字會指定游標在滑鼠按一下時的水準位置（在螢幕座標中）。</span><span class="sxs-lookup"><span data-stu-id="2fe1a-113">The low-order word specifies the horizontal position of the cursor, in screen coordinates, at the time of the mouse click.</span></span>

<span data-ttu-id="2fe1a-114">高序位單字會指定游標在滑鼠按一下時的垂直位置（以螢幕座標表示）。</span><span class="sxs-lookup"><span data-stu-id="2fe1a-114">The high-order word specifies the vertical position of the cursor, in screen coordinates, at the time of the mouse click.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fe1a-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="2fe1a-115">Return value</span></span>

<span data-ttu-id="2fe1a-116">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="2fe1a-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fe1a-117">備註</span><span class="sxs-lookup"><span data-stu-id="2fe1a-117">Remarks</span></span>

<span data-ttu-id="2fe1a-118">視窗可以藉由使用 [**trackpopupmenu 讓**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) 或 [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) 函數顯示快捷方式功能表來處理此訊息。</span><span class="sxs-lookup"><span data-stu-id="2fe1a-118">A window can process this message by displaying a shortcut menu using the [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) or [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) functions.</span></span> <span data-ttu-id="2fe1a-119">若要取得水準和垂直位置，請使用下列程式碼。</span><span class="sxs-lookup"><span data-stu-id="2fe1a-119">To obtain the horizontal and vertical positions, use the following code.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="2fe1a-120">如果視窗未顯示快捷方式功能表，則應該將此訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式。</span><span class="sxs-lookup"><span data-stu-id="2fe1a-120">If a window does not display a shortcut menu it should pass this message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="2fe1a-121">如果視窗是子視窗， **DefWindowProc** 會將訊息傳送至父視窗。</span><span class="sxs-lookup"><span data-stu-id="2fe1a-121">If a window is a child window, **DefWindowProc** sends the message to the parent.</span></span> <span data-ttu-id="2fe1a-122">否則，如果指定的位置是在視窗的標題中， **DefWindowProc** 會顯示預設的快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="2fe1a-122">Otherwise, **DefWindowProc** displays a default shortcut menu if the specified position is in the window's caption.</span></span>

<span data-ttu-id="2fe1a-123">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)會在處理 [**Wm \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)或 [**WM \_ NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup)訊息或使用者輸入 SHIFT + F10 時產生 **wm \_ CONTEXTMENU** 訊息。</span><span class="sxs-lookup"><span data-stu-id="2fe1a-123">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) generates the **WM\_CONTEXTMENU** message when it processes the [**WM\_RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup) or [**WM\_NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup) message or when the user types SHIFT+F10.</span></span> <span data-ttu-id="2fe1a-124">當使用者按下並釋放 [**VK \_ APPS**](/windows/desktop/inputdev/virtual-key-codes)金鑰時，也會產生 **WM \_ CONTEXTMENU** 訊息。</span><span class="sxs-lookup"><span data-stu-id="2fe1a-124">The **WM\_CONTEXTMENU** message is also generated when the user presses and releases the [**VK\_APPS**](/windows/desktop/inputdev/virtual-key-codes) key.</span></span>

<span data-ttu-id="2fe1a-125">如果內容功能表是從鍵盤產生的，例如，如果使用者輸入 SHIFT + F10，則 x 和 y 座標為-1，而應用程式應該在目前選取範圍的位置顯示操作功能表，而不是在 (xPos、yPos) 。</span><span class="sxs-lookup"><span data-stu-id="2fe1a-125">If the context menu is generated from the keyboard for example, if the user types SHIFT+F10 then the x- and y-coordinates are -1 and the application should display the context menu at the location of the current selection rather than at (xPos, yPos).</span></span>

## <a name="requirements"></a><span data-ttu-id="2fe1a-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="2fe1a-126">Requirements</span></span>



| <span data-ttu-id="2fe1a-127">需求</span><span class="sxs-lookup"><span data-stu-id="2fe1a-127">Requirement</span></span> | <span data-ttu-id="2fe1a-128">值</span><span class="sxs-lookup"><span data-stu-id="2fe1a-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fe1a-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2fe1a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2fe1a-130">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2fe1a-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2fe1a-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2fe1a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2fe1a-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2fe1a-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2fe1a-133">標頭</span><span class="sxs-lookup"><span data-stu-id="2fe1a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fe1a-134"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="2fe1a-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fe1a-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2fe1a-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="2fe1a-136">**參考**</span><span class="sxs-lookup"><span data-stu-id="2fe1a-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2fe1a-137">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="2fe1a-137">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="2fe1a-138">**取得 \_ X \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="2fe1a-138">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="2fe1a-139">**取得 \_ Y \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="2fe1a-139">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="2fe1a-140">**Trackpopupmenu 讓**</span><span class="sxs-lookup"><span data-stu-id="2fe1a-140">**TrackPopupMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu)
</dt> <dt>

[<span data-ttu-id="2fe1a-141">**TrackPopupMenuEx**</span><span class="sxs-lookup"><span data-stu-id="2fe1a-141">**TrackPopupMenuEx**</span></span>](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex)
</dt> <dt>

[<span data-ttu-id="2fe1a-142">**WM \_ NCRBUTTONUP**</span><span class="sxs-lookup"><span data-stu-id="2fe1a-142">**WM\_NCRBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-ncrbuttonup)
</dt> <dt>

[<span data-ttu-id="2fe1a-143">**WM \_ RBUTTONUP**</span><span class="sxs-lookup"><span data-stu-id="2fe1a-143">**WM\_RBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-rbuttonup)
</dt> <dt>

<span data-ttu-id="2fe1a-144">**概念**</span><span class="sxs-lookup"><span data-stu-id="2fe1a-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2fe1a-145">功能表</span><span class="sxs-lookup"><span data-stu-id="2fe1a-145">Menus</span></span>](menus.md)
</dt> </dl>

 

