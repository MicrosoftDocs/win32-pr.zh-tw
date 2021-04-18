---
UID: ''
title: ShellProc 回呼函式
description: 函式會從系統接收 Shell 事件的通知。
old-location: ''
ms.assetid: na
ms.date: 04/05/2019
ms.keywords: ''
ms.topic: reference
req.header: ''
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name: ''
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 4add84011745aeb61659c39775b94fed91028d83
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/11/2020
ms.locfileid: "106968895"
---
# <a name="shellproc-function"></a><span data-ttu-id="767f8-103">ShellProc 函式</span><span class="sxs-lookup"><span data-stu-id="767f8-103">ShellProc function</span></span>

## <a name="description"></a><span data-ttu-id="767f8-104">Description</span><span class="sxs-lookup"><span data-stu-id="767f8-104">Description</span></span>

<span data-ttu-id="767f8-105">搭配 [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) 函式使用的應用程式定義或程式庫定義的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="767f8-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="767f8-106">函式會從系統接收 Shell 事件的通知。</span><span class="sxs-lookup"><span data-stu-id="767f8-106">The function receives notifications of Shell events from the system.</span></span>

<span data-ttu-id="767f8-107">**HOOKPROC** 型別定義此回呼函數的指標。</span><span class="sxs-lookup"><span data-stu-id="767f8-107">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="767f8-108">**ShellProc** 是應用程式定義或程式庫定義函數名稱的預留位置。</span><span class="sxs-lookup"><span data-stu-id="767f8-108">**ShellProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK ShellProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="767f8-109">參數</span><span class="sxs-lookup"><span data-stu-id="767f8-109">Parameters</span></span>

### <a name="ncode-in"></a><span data-ttu-id="767f8-110">nCode [in]</span><span class="sxs-lookup"><span data-stu-id="767f8-110">nCode [in]</span></span>

<span data-ttu-id="767f8-111">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="767f8-111">Type: **int**</span></span>

<span data-ttu-id="767f8-112">攔截程式碼。</span><span class="sxs-lookup"><span data-stu-id="767f8-112">The hook code.</span></span>
<span data-ttu-id="767f8-113">如果 *nCode* 小於零，則攔截程式必須將訊息傳遞至 [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) 函式，而不需要進一步處理，並且應該傳回 **CallNextHookEx** 所傳回的值。</span><span class="sxs-lookup"><span data-stu-id="767f8-113">If *nCode* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="767f8-114">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="767f8-114">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="767f8-115">值</span><span class="sxs-lookup"><span data-stu-id="767f8-115">Value</span></span> | <span data-ttu-id="767f8-116">意義</span><span class="sxs-lookup"><span data-stu-id="767f8-116">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="767f8-117">**HSHELL_ACCESSIBILITYSTATE** 11</span><span class="sxs-lookup"><span data-stu-id="767f8-117">**HSHELL_ACCESSIBILITYSTATE** 11</span></span> | <span data-ttu-id="767f8-118">協助工具狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="767f8-118">The accessibility state has changed.</span></span> |
| <span data-ttu-id="767f8-119">**HSHELL_ACTI加值稅ESHELLWINDOW** 3</span><span class="sxs-lookup"><span data-stu-id="767f8-119">**HSHELL_ACTIVATESHELLWINDOW** 3</span></span> | <span data-ttu-id="767f8-120">Shell 應會啟用其主視窗。</span><span class="sxs-lookup"><span data-stu-id="767f8-120">The shell should activate its main window.</span></span> |
| <span data-ttu-id="767f8-121">**HSHELL_APPCOMMAND** 12</span><span class="sxs-lookup"><span data-stu-id="767f8-121">**HSHELL_APPCOMMAND** 12</span></span> | <span data-ttu-id="767f8-122">使用者已完成輸入事件 (例如，按下滑鼠上的應用程式命令按鈕或鍵盤上的應用程式命令鍵) ，而且應用程式未處理該輸入所產生的 [WM_APPCOMMAND](/windows/desktop/inputdev/wm-appcommand) 訊息。</span><span class="sxs-lookup"><span data-stu-id="767f8-122">The user completed an input event (for example, pressed an application command button on the mouse or an application command key on the keyboard), and the application did not handle the [WM_APPCOMMAND](/windows/desktop/inputdev/wm-appcommand) message generated by that input.</span></span> <span data-ttu-id="767f8-123">如果 Shell 程式處理 [WM_COMMAND](/windows/desktop/menurc/wm-command) 訊息，則不應呼叫 **CallNextHookEx**。</span><span class="sxs-lookup"><span data-stu-id="767f8-123">If the Shell procedure handles the [WM_COMMAND](/windows/desktop/menurc/wm-command) message, it should not call **CallNextHookEx**.</span></span> <span data-ttu-id="767f8-124">如需詳細資訊，請參閱傳回值一節。</span><span class="sxs-lookup"><span data-stu-id="767f8-124">See the Return Value section for more information.</span></span> |
| <span data-ttu-id="767f8-125">**HSHELL_GETMINRECT** 5</span><span class="sxs-lookup"><span data-stu-id="767f8-125">**HSHELL_GETMINRECT** 5</span></span> | <span data-ttu-id="767f8-126">視窗會最小化或最大化。</span><span class="sxs-lookup"><span data-stu-id="767f8-126">A window is being minimized or maximized.</span></span> <span data-ttu-id="767f8-127">系統需要視窗的最小化矩形座標。</span><span class="sxs-lookup"><span data-stu-id="767f8-127">The system needs the coordinates of the minimized rectangle for the window.</span></span> |
| <span data-ttu-id="767f8-128">**HSHELL_LANGUAGE** 8</span><span class="sxs-lookup"><span data-stu-id="767f8-128">**HSHELL_LANGUAGE** 8</span></span> | <span data-ttu-id="767f8-129">鍵盤語言已變更或已載入新的鍵盤配置。</span><span class="sxs-lookup"><span data-stu-id="767f8-129">Keyboard language was changed or a new keyboard layout was loaded.</span></span> |
| <span data-ttu-id="767f8-130">**HSHELL_REDRAW** 6</span><span class="sxs-lookup"><span data-stu-id="767f8-130">**HSHELL_REDRAW** 6</span></span> | <span data-ttu-id="767f8-131">已重新繪製工作列中視窗的標題。</span><span class="sxs-lookup"><span data-stu-id="767f8-131">The title of a window in the task bar has been redrawn.</span></span> |
| <span data-ttu-id="767f8-132">**HSHELL_TASKMAN** 7</span><span class="sxs-lookup"><span data-stu-id="767f8-132">**HSHELL_TASKMAN** 7</span></span> | <span data-ttu-id="767f8-133">使用者已選取 [工作清單]。</span><span class="sxs-lookup"><span data-stu-id="767f8-133">The user has selected the task list.</span></span> <span data-ttu-id="767f8-134">提供工作清單的 shell 應用程式應該會傳回 **TRUE** ，以防止 Windows 啟動其工作清單。</span><span class="sxs-lookup"><span data-stu-id="767f8-134">A shell application that provides a task list should return **TRUE** to prevent Windows from starting its task list.</span></span> |
| <span data-ttu-id="767f8-135">**HSHELL_WINDOWACTI加值稅ED** 4</span><span class="sxs-lookup"><span data-stu-id="767f8-135">**HSHELL_WINDOWACTIVATED** 4</span></span> | <span data-ttu-id="767f8-136">啟用已變更為不同的最上層、無主視窗。</span><span class="sxs-lookup"><span data-stu-id="767f8-136">The activation has changed to a different top-level, unowned window.</span></span> |
| <span data-ttu-id="767f8-137">**HSHELL_WINDOWCREATED** 1</span><span class="sxs-lookup"><span data-stu-id="767f8-137">**HSHELL_WINDOWCREATED** 1</span></span> | <span data-ttu-id="767f8-138">已建立最上層的無主視窗。</span><span class="sxs-lookup"><span data-stu-id="767f8-138">A top-level, unowned window has been created.</span></span> <span data-ttu-id="767f8-139">當系統呼叫此攔截時，會存在此視窗。</span><span class="sxs-lookup"><span data-stu-id="767f8-139">The window exists when the system calls this hook.</span></span> |
| <span data-ttu-id="767f8-140">**HSHELL_WINDOWDESTROYED** 2</span><span class="sxs-lookup"><span data-stu-id="767f8-140">**HSHELL_WINDOWDESTROYED** 2</span></span> | <span data-ttu-id="767f8-141">最上層的無主視窗即將終結。</span><span class="sxs-lookup"><span data-stu-id="767f8-141">A top-level, unowned window is about to be destroyed.</span></span> <span data-ttu-id="767f8-142">當系統呼叫此攔截時，視窗仍然存在。</span><span class="sxs-lookup"><span data-stu-id="767f8-142">The window still exists when the system calls this hook.</span></span> |
| <span data-ttu-id="767f8-143">**HSHELL_WINDOWREPLACED** 13</span><span class="sxs-lookup"><span data-stu-id="767f8-143">**HSHELL_WINDOWREPLACED** 13</span></span> | <span data-ttu-id="767f8-144">即將取代最上層視窗。</span><span class="sxs-lookup"><span data-stu-id="767f8-144">A top-level window is being replaced.</span></span> <span data-ttu-id="767f8-145">當系統呼叫此攔截時，會存在此視窗。</span><span class="sxs-lookup"><span data-stu-id="767f8-145">The window exists when the system calls this hook.</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="767f8-146">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="767f8-146">wParam [in]</span></span>

<span data-ttu-id="767f8-147">類型： **WPARAM**</span><span class="sxs-lookup"><span data-stu-id="767f8-147">Type: **WPARAM**</span></span>

<span data-ttu-id="767f8-148">此參數取決於 *nCode* 參數的值，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="767f8-148">This parameter depends on the value of the *nCode* parameter, as shown in the following table.</span></span>

| <span data-ttu-id="767f8-149">nCode</span><span class="sxs-lookup"><span data-stu-id="767f8-149">nCode</span></span> | <span data-ttu-id="767f8-150">wParam</span><span class="sxs-lookup"><span data-stu-id="767f8-150">wParam</span></span> |
|-------|---------|
| <span data-ttu-id="767f8-151">**HSHELL_ACCESSIBILITYSTATE**</span><span class="sxs-lookup"><span data-stu-id="767f8-151">**HSHELL_ACCESSIBILITYSTATE**</span></span> | <span data-ttu-id="767f8-152">指出哪些協助工具已變更狀態。</span><span class="sxs-lookup"><span data-stu-id="767f8-152">Indicates which accessibility feature has changed state.</span></span> <span data-ttu-id="767f8-153">這個值是下列其中一項： **ACCESS_FILTERKEYS**、 **ACCESS_MOUSEKEYS** 或 **ACCESS_STICKYKEYS**。</span><span class="sxs-lookup"><span data-stu-id="767f8-153">This value is one of the following: **ACCESS_FILTERKEYS**, **ACCESS_MOUSEKEYS**, or **ACCESS_STICKYKEYS**.</span></span> |
| <span data-ttu-id="767f8-154">**HSHELL_APPCOMMAND**</span><span class="sxs-lookup"><span data-stu-id="767f8-154">**HSHELL_APPCOMMAND**</span></span> | <span data-ttu-id="767f8-155">指出 **WM_APPCOMMAND** 訊息最初傳送的位置;例如，視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="767f8-155">Indicates where the **WM_APPCOMMAND** message was originally sent; for example, the handle to a window.</span></span> <span data-ttu-id="767f8-156">如需詳細資訊，請參閱 **WM_APPCOMMAND** 中的 cmd 參數。</span><span class="sxs-lookup"><span data-stu-id="767f8-156">For more information, see cmd parameter in **WM_APPCOMMAND**.</span></span> |
| <span data-ttu-id="767f8-157">**HSHELL_GETMINRECT**</span><span class="sxs-lookup"><span data-stu-id="767f8-157">**HSHELL_GETMINRECT**</span></span> | <span data-ttu-id="767f8-158">最小化或最大化視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="767f8-158">A handle to the minimized or maximized window.</span></span> |
| <span data-ttu-id="767f8-159">**HSHELL_LANGUAGE**</span><span class="sxs-lookup"><span data-stu-id="767f8-159">**HSHELL_LANGUAGE**</span></span> | <span data-ttu-id="767f8-160">視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="767f8-160">A handle to the window.</span></span> |
| <span data-ttu-id="767f8-161">**HSHELL_REDRAW**</span><span class="sxs-lookup"><span data-stu-id="767f8-161">**HSHELL_REDRAW**</span></span> | <span data-ttu-id="767f8-162">重新繪製之視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="767f8-162">A handle to the redrawn window.</span></span> |
| <span data-ttu-id="767f8-163">**HSHELL_WINDOWACTI加值稅ED**</span><span class="sxs-lookup"><span data-stu-id="767f8-163">**HSHELL_WINDOWACTIVATED**</span></span> | <span data-ttu-id="767f8-164">已啟動視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="767f8-164">A handle to the activated window.</span></span> |
| <span data-ttu-id="767f8-165">**HSHELL_WINDOWCREATED**</span><span class="sxs-lookup"><span data-stu-id="767f8-165">**HSHELL_WINDOWCREATED**</span></span> | <span data-ttu-id="767f8-166">已建立之視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="767f8-166">A handle to the created window.</span></span> |
| <span data-ttu-id="767f8-167">**HSHELL_WINDOWDESTROYED**</span><span class="sxs-lookup"><span data-stu-id="767f8-167">**HSHELL_WINDOWDESTROYED**</span></span> | <span data-ttu-id="767f8-168">已損毀視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="767f8-168">A handle to the destroyed window.</span></span> |
| <span data-ttu-id="767f8-169">**HSHELL_WINDOWREPLACED**</span><span class="sxs-lookup"><span data-stu-id="767f8-169">**HSHELL_WINDOWREPLACED**</span></span> | <span data-ttu-id="767f8-170">要取代之視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="767f8-170">A handle to the window being replaced.</span></span> <span data-ttu-id="767f8-171">Windows 2000：不支援。</span><span class="sxs-lookup"><span data-stu-id="767f8-171">Windows 2000:  Not supported.</span></span> |

### <a name="lparam-in"></a><span data-ttu-id="767f8-172">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="767f8-172">lParam [in]</span></span>

<span data-ttu-id="767f8-173">類型： **LPARAM**</span><span class="sxs-lookup"><span data-stu-id="767f8-173">Type: **LPARAM**</span></span>

<span data-ttu-id="767f8-174">此參數取決於 *nCode* 參數的值，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="767f8-174">This parameter depends on the value of the *nCode* parameter, as shown in the following table.</span></span>

| <span data-ttu-id="767f8-175">nCode</span><span class="sxs-lookup"><span data-stu-id="767f8-175">nCode</span></span> | <span data-ttu-id="767f8-176">lParam</span><span class="sxs-lookup"><span data-stu-id="767f8-176">lParam</span></span> |
|-------|---------|
| <span data-ttu-id="767f8-177">**HSHELL_APPCOMMAND**</span><span class="sxs-lookup"><span data-stu-id="767f8-177">**HSHELL_APPCOMMAND**</span></span> | <span data-ttu-id="767f8-178">`GET_APPCOMMAND_LPARAM(lParam)` 是對應至輸入事件的應用程式命令。</span><span class="sxs-lookup"><span data-stu-id="767f8-178">`GET_APPCOMMAND_LPARAM(lParam)` is the application command corresponding to the input event.</span></span> <span data-ttu-id="767f8-179">`GET_DEVICE_LPARAM(lParam)` 表示產生輸入事件的專案;例如滑鼠或鍵盤。</span><span class="sxs-lookup"><span data-stu-id="767f8-179">`GET_DEVICE_LPARAM(lParam)` indicates what generated the input event; for example, the mouse or keyboard.</span></span> <span data-ttu-id="767f8-180">如需詳細資訊，請參閱 **WM_APPCOMMAND** 下的 *uDevice* 參數描述。</span><span class="sxs-lookup"><span data-stu-id="767f8-180">For more information, see the *uDevice* parameter description under **WM_APPCOMMAND**.</span></span> <span data-ttu-id="767f8-181">`GET_FLAGS_LPARAM(lParam)`取決於 **WM_APPCOMMAND** 中 *cmd* 的值。</span><span class="sxs-lookup"><span data-stu-id="767f8-181">`GET_FLAGS_LPARAM(lParam)` depends on the value of *cmd* in **WM_APPCOMMAND**.</span></span> <span data-ttu-id="767f8-182">例如，它可能會指出最初傳送 **WM_APPCOMMAND** 訊息時，哪些虛擬機器碼已關閉。</span><span class="sxs-lookup"><span data-stu-id="767f8-182">For example, it might indicate which virtual keys were held down when the **WM_APPCOMMAND** message was originally sent.</span></span> <span data-ttu-id="767f8-183">如需詳細資訊，請參閱 **WM_APPCOMMAND** 下的 *dwCmdFlags* description 參數。</span><span class="sxs-lookup"><span data-stu-id="767f8-183">For more information, see the *dwCmdFlags* description parameter under **WM_APPCOMMAND**.</span></span> |
| <span data-ttu-id="767f8-184">**HSHELL_GETMINRECT**</span><span class="sxs-lookup"><span data-stu-id="767f8-184">**HSHELL_GETMINRECT**</span></span> | <span data-ttu-id="767f8-185">[矩形](/previous-versions/dd162897(v=vs.85))結構的指標。</span><span class="sxs-lookup"><span data-stu-id="767f8-185">A pointer to a [RECT](/previous-versions/dd162897(v=vs.85)) structure.</span></span> |
| <span data-ttu-id="767f8-186">**HSHELL_LANGUAGE**</span><span class="sxs-lookup"><span data-stu-id="767f8-186">**HSHELL_LANGUAGE**</span></span> | <span data-ttu-id="767f8-187">鍵盤配置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="767f8-187">A handle to a keyboard layout.</span></span> |
| <span data-ttu-id="767f8-188">**HSHELL_MONITORCHANGED**</span><span class="sxs-lookup"><span data-stu-id="767f8-188">**HSHELL_MONITORCHANGED**</span></span> | <span data-ttu-id="767f8-189">移至不同監視的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="767f8-189">A handle to the window that moved to a different monitor.</span></span> |
| <span data-ttu-id="767f8-190">**HSHELL_REDRAW**</span><span class="sxs-lookup"><span data-stu-id="767f8-190">**HSHELL_REDRAW**</span></span> | <span data-ttu-id="767f8-191">如果視窗閃爍，此值為 **TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="767f8-191">The value is **TRUE** if the window is flashing, or **FALSE** otherwise.</span></span> |
| <span data-ttu-id="767f8-192">**HSHELL_WINDOWACTI加值稅ED**</span><span class="sxs-lookup"><span data-stu-id="767f8-192">**HSHELL_WINDOWACTIVATED**</span></span> | <span data-ttu-id="767f8-193">如果視窗處於全螢幕模式，則此值為 TRUE，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="767f8-193">The value is TRUE if the window is in full-screen mode, or **FALSE** otherwise.</span></span> |
| <span data-ttu-id="767f8-194">**HSHELL_WINDOWREPLACED**</span><span class="sxs-lookup"><span data-stu-id="767f8-194">**HSHELL_WINDOWREPLACED**</span></span> | <span data-ttu-id="767f8-195">新視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="767f8-195">A handle to the new window.</span></span> <span data-ttu-id="767f8-196">Windows 2000：不支援。</span><span class="sxs-lookup"><span data-stu-id="767f8-196">Windows 2000:  Not supported.</span></span> |

## <a name="returns"></a><span data-ttu-id="767f8-197">傳回</span><span class="sxs-lookup"><span data-stu-id="767f8-197">Returns</span></span>

<span data-ttu-id="767f8-198">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="767f8-198">Type: **LRESULT**</span></span>

<span data-ttu-id="767f8-199">除非 nCode 的值 **HSHELL_APPCOMMAND** ，而且 shell 程式處理 **WM_COMMAND** 訊息，否則傳回值應為零。</span><span class="sxs-lookup"><span data-stu-id="767f8-199">The return value should be zero unless the value of nCode is **HSHELL_APPCOMMAND** and the shell procedure handles the **WM_COMMAND** message.</span></span>
<span data-ttu-id="767f8-200">在此情況下，傳回值應為非零。</span><span class="sxs-lookup"><span data-stu-id="767f8-200">In this case, the return should be nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="767f8-201">備註</span><span class="sxs-lookup"><span data-stu-id="767f8-201">Remarks</span></span>

<span data-ttu-id="767f8-202">藉由在 **SetWindowsHookEx** 函式的呼叫中指定 [WH_SHELL](about-hooks.md)攔截類型和攔截程式的指標，來安裝此攔截程式。</span><span class="sxs-lookup"><span data-stu-id="767f8-202">Install this hook procedure by specifying the [WH_SHELL](about-hooks.md) hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

## <a name="see-also"></a><span data-ttu-id="767f8-203">另請參閱</span><span class="sxs-lookup"><span data-stu-id="767f8-203">See also</span></span>

[<span data-ttu-id="767f8-204">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="767f8-204">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="767f8-205">SendMessage</span><span class="sxs-lookup"><span data-stu-id="767f8-205">SendMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)

[<span data-ttu-id="767f8-206">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="767f8-206">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="767f8-207">WM_APPCOMMAND</span><span class="sxs-lookup"><span data-stu-id="767f8-207">WM_APPCOMMAND</span></span>](/windows/desktop/inputdev/wm-appcommand)

[<span data-ttu-id="767f8-208">WM_COMMAND</span><span class="sxs-lookup"><span data-stu-id="767f8-208">WM_COMMAND</span></span>](/windows/desktop/menurc/wm-command)

[<span data-ttu-id="767f8-209">鉤</span><span class="sxs-lookup"><span data-stu-id="767f8-209">Hooks</span></span>](hooks.md)
