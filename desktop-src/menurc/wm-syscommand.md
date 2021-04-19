---
title: 'WM_SYSCOMMAND 訊息 (Winuser .h) '
description: 當使用者選擇 [視窗])  (功能表中的命令時，如果使用者選擇 [最大化] 按鈕、[最小化] 按鈕、[還原] 按鈕或 [關閉] 按鈕，就會收到此訊息。
ms.assetid: 82c7cc95-82d5-4f0f-8c78-ab325561b04e
keywords:
- WM_SYSCOMMAND 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_SYSCOMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 25596f30457063bc90124f14489963507f85ff70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978420"
---
# <a name="wm_syscommand-message"></a><span data-ttu-id="5e430-104">WM \_ SYSCOMMAND 訊息</span><span class="sxs-lookup"><span data-stu-id="5e430-104">WM\_SYSCOMMAND message</span></span>

<span data-ttu-id="5e430-105">當使用者選擇 [ **視窗]**)  (功能表中的命令時，如果使用者選擇 [最大化] 按鈕、[最小化] 按鈕、[還原] 按鈕或 [關閉] 按鈕，就會收到此訊息。</span><span class="sxs-lookup"><span data-stu-id="5e430-105">A window receives this message when the user chooses a command from the **Window** menu (formerly known as the system or control menu) or when the user chooses the maximize button, minimize button, restore button, or close button.</span></span>


```C++
#define WM_SYSCOMMAND                   0x0112
```

## <a name="example"></a><span data-ttu-id="5e430-106">範例</span><span class="sxs-lookup"><span data-stu-id="5e430-106">Example</span></span>

```cpp
 case WM_SYSCOMMAND:
        if (wParam == SC_CLOSE)
        {
            EndDialog (hDlg, TRUE);
            return(TRUE);
        }
        break;

```
<span data-ttu-id="5e430-107">從 GitHub 上的 [Windows 傳統範例](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/registry/RegExplorer.c) 取得的範例。</span><span class="sxs-lookup"><span data-stu-id="5e430-107">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/registry/RegExplorer.c) on GitHub.</span></span>

## <a name="parameters"></a><span data-ttu-id="5e430-108">參數</span><span class="sxs-lookup"><span data-stu-id="5e430-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e430-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5e430-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e430-110">要求的系統命令類型。</span><span class="sxs-lookup"><span data-stu-id="5e430-110">The type of system command requested.</span></span> <span data-ttu-id="5e430-111">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="5e430-111">This parameter can be one of the following values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5e430-112">值</span><span class="sxs-lookup"><span data-stu-id="5e430-112">Value</span></span></th>
<th><span data-ttu-id="5e430-113">意義</span><span class="sxs-lookup"><span data-stu-id="5e430-113">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="SC_CLOSE"></span><span id="sc_close"></span><dl> <span data-ttu-id="5e430-114"><dt><strong>SC_CLOSE</strong></dt> <dt>0xF060</dt> </span><span class="sxs-lookup"><span data-stu-id="5e430-114"><dt><strong>SC_CLOSE</strong></dt> <dt>0xF060</dt> </span></span></dl></td>
<td><span data-ttu-id="5e430-115">關閉視窗。</span><span class="sxs-lookup"><span data-stu-id="5e430-115">Closes the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_CONTEXTHELP"></span><span id="sc_contexthelp"></span><dl> <span data-ttu-id="5e430-116"><dt><strong>SC_CONTEXTHELP</strong></dt> <dt>0xF180</dt> </span><span class="sxs-lookup"><span data-stu-id="5e430-116"><dt><strong>SC_CONTEXTHELP</strong></dt> <dt>0xF180</dt> </span></span></dl></td>
<td><span data-ttu-id="5e430-117">將游標變更為具有指標的問號。</span><span class="sxs-lookup"><span data-stu-id="5e430-117">Changes the cursor to a question mark with a pointer.</span></span> <span data-ttu-id="5e430-118">如果使用者接著按一下對話方塊中的控制項，控制項就會收到 <a href="/windows/desktop/shell/wm-help"><strong>WM_HELP</strong></a> 的訊息。</span><span class="sxs-lookup"><span data-stu-id="5e430-118">If the user then clicks a control in the dialog box, the control receives a <a href="/windows/desktop/shell/wm-help"><strong>WM_HELP</strong></a> message.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_DEFAULT"></span><span id="sc_default"></span><dl> <span data-ttu-id="5e430-119"><dt><strong>SC_DEFAULT</strong></dt> <dt>0xF160</dt> </span><span class="sxs-lookup"><span data-stu-id="5e430-119"><dt><strong>SC_DEFAULT</strong></dt> <dt>0xF160</dt> </span></span></dl></td>
<td><span data-ttu-id="5e430-120">選取預設專案;使用者按兩下 [視窗] 功能表。</span><span class="sxs-lookup"><span data-stu-id="5e430-120">Selects the default item; the user double-clicked the window menu.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_HOTKEY"></span><span id="sc_hotkey"></span><dl> <span data-ttu-id="5e430-121"><dt><strong>SC_HOTKEY</strong></dt> <dt>0xF150</dt> </span><span class="sxs-lookup"><span data-stu-id="5e430-121"><dt><strong>SC_HOTKEY</strong></dt> <dt>0xF150</dt> </span></span></dl></td>
<td><span data-ttu-id="5e430-122">啟用與應用程式指定之熱鍵相關聯的視窗。</span><span class="sxs-lookup"><span data-stu-id="5e430-122">Activates the window associated with the application-specified hot key.</span></span> <span data-ttu-id="5e430-123"><em>LParam</em>參數會識別要啟動的視窗。</span><span class="sxs-lookup"><span data-stu-id="5e430-123">The <em>lParam</em> parameter identifies the window to activate.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_HSCROLL"></span><span id="sc_hscroll"></span><dl> <span data-ttu-id="5e430-124"><dt><strong>SC_HSCROLL</strong></dt> <dt>0xF080</dt> </span><span class="sxs-lookup"><span data-stu-id="5e430-124"><dt><strong>SC_HSCROLL</strong></dt> <dt>0xF080</dt> </span></span></dl></td>
<td><span data-ttu-id="5e430-125">水準滾動。</span><span class="sxs-lookup"><span data-stu-id="5e430-125">Scrolls horizontally.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SCF_ISSECURE"></span><span id="scf_issecure"></span><dl> <span data-ttu-id="5e430-126"><dt><strong>SCF_ISSECURE</strong></dt> <dt>0x00000001</dt> </span><span class="sxs-lookup"><span data-stu-id="5e430-126"><dt><strong>SCF_ISSECURE</strong></dt> <dt>0x00000001</dt> </span></span></dl></td>
<td><span data-ttu-id="5e430-127">指出螢幕保護裝置是否安全。</span><span class="sxs-lookup"><span data-stu-id="5e430-127">Indicates whether the screen saver is secure.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="SC_KEYMENU"></span><span id="sc_keymenu"></span><dl> <span data-ttu-id="5e430-128"><dt><strong>SC_KEYMENU</strong></dt> <dt>0xF100</dt> </span><span class="sxs-lookup"><span data-stu-id="5e430-128"><dt><strong>SC_KEYMENU</strong></dt> <dt>0xF100</dt> </span></span></dl></td>
<td><span data-ttu-id="5e430-129">以按鍵的結果形式抓取視窗功能表。</span><span class="sxs-lookup"><span data-stu-id="5e430-129">Retrieves the window menu as a result of a keystroke.</span></span> <span data-ttu-id="5e430-130">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="5e430-130">For more information, see the Remarks section.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_MAXIMIZE"></span><span id="sc_maximize"></span><dl> <span data-ttu-id="5e430-131"><dt><strong>SC_MAXIMIZE</strong></dt> <dt>0xF030</dt> </span><span class="sxs-lookup"><span data-stu-id="5e430-131"><dt><strong>SC_MAXIMIZE</strong></dt> <dt>0xF030</dt> </span></span></dl></td>
<td><span data-ttu-id="5e430-132">將視窗最大化。</span><span class="sxs-lookup"><span data-stu-id="5e430-132">Maximizes the window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_MINIMIZE"></span><span id="sc_minimize"></span><dl> <span data-ttu-id="5e430-133"><dt><strong>SC_MINIMIZE</strong></dt> <dt>0xF020</dt> </span><span class="sxs-lookup"><span data-stu-id="5e430-133"><dt><strong>SC_MINIMIZE</strong></dt> <dt>0xF020</dt> </span></span></dl></td>
<td><span data-ttu-id="5e430-134">將視窗最小化。</span><span class="sxs-lookup"><span data-stu-id="5e430-134">Minimizes the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_MONITORPOWER"></span><span id="sc_monitorpower"></span><dl> <span data-ttu-id="5e430-135"><dt><strong>SC_MONITORPOWER</strong></dt> <dt>0xF170</dt> </span><span class="sxs-lookup"><span data-stu-id="5e430-135"><dt><strong>SC_MONITORPOWER</strong></dt> <dt>0xF170</dt> </span></span></dl></td>
<td><span data-ttu-id="5e430-136">設定顯示器的狀態。</span><span class="sxs-lookup"><span data-stu-id="5e430-136">Sets the state of the display.</span></span> <span data-ttu-id="5e430-137">此命令支援具有省電功能的裝置，例如電池供電的個人電腦。</span><span class="sxs-lookup"><span data-stu-id="5e430-137">This command supports devices that have power-saving features, such as a battery-powered personal computer.</span></span> <br/> <span data-ttu-id="5e430-138"><em>LParam</em>參數可以有下列值：</span><span class="sxs-lookup"><span data-stu-id="5e430-138">The <em>lParam</em> parameter can have the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="5e430-139">-1 (顯示器開啟電源) </span><span class="sxs-lookup"><span data-stu-id="5e430-139">-1 (the display is powering on)</span></span></li>
<li><span data-ttu-id="5e430-140">1 (顯示器會進入低電源) </span><span class="sxs-lookup"><span data-stu-id="5e430-140">1 (the display is going to low power)</span></span></li>
<li><span data-ttu-id="5e430-141">2 (正在關閉顯示) </span><span class="sxs-lookup"><span data-stu-id="5e430-141">2 (the display is being shut off)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="SC_MOUSEMENU"></span><span id="sc_mousemenu"></span><dl> <span data-ttu-id="5e430-142"><dt><strong>SC_MOUSEMENU</strong></dt> <dt>0xF090</dt> </span><span class="sxs-lookup"><span data-stu-id="5e430-142"><dt><strong>SC_MOUSEMENU</strong></dt> <dt>0xF090</dt> </span></span></dl></td>
<td><span data-ttu-id="5e430-143">以滑鼠點擊的結果形式抓取視窗功能表。</span><span class="sxs-lookup"><span data-stu-id="5e430-143">Retrieves the window menu as a result of a mouse click.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_MOVE"></span><span id="sc_move"></span><dl> <span data-ttu-id="5e430-144"><dt><strong>SC_MOVE</strong></dt> <dt>0xF010</dt> </span><span class="sxs-lookup"><span data-stu-id="5e430-144"><dt><strong>SC_MOVE</strong></dt> <dt>0xF010</dt> </span></span></dl></td>
<td><span data-ttu-id="5e430-145">移動視窗。</span><span class="sxs-lookup"><span data-stu-id="5e430-145">Moves the window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_NEXTWINDOW"></span><span id="sc_nextwindow"></span><dl> <span data-ttu-id="5e430-146"><dt><strong>SC_NEXTWINDOW</strong></dt> <dt>0xF040</dt> </span><span class="sxs-lookup"><span data-stu-id="5e430-146"><dt><strong>SC_NEXTWINDOW</strong></dt> <dt>0xF040</dt> </span></span></dl></td>
<td><span data-ttu-id="5e430-147">移至下一個視窗。</span><span class="sxs-lookup"><span data-stu-id="5e430-147">Moves to the next window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_PREVWINDOW"></span><span id="sc_prevwindow"></span><dl> <span data-ttu-id="5e430-148"><dt><strong>SC_PREVWINDOW</strong></dt> <dt>0xF050</dt> </span><span class="sxs-lookup"><span data-stu-id="5e430-148"><dt><strong>SC_PREVWINDOW</strong></dt> <dt>0xF050</dt> </span></span></dl></td>
<td><span data-ttu-id="5e430-149">移至上一個視窗。</span><span class="sxs-lookup"><span data-stu-id="5e430-149">Moves to the previous window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_RESTORE"></span><span id="sc_restore"></span><dl> <span data-ttu-id="5e430-150"><dt><strong>SC_RESTORE</strong></dt> <dt>0xF120</dt> </span><span class="sxs-lookup"><span data-stu-id="5e430-150"><dt><strong>SC_RESTORE</strong></dt> <dt>0xF120</dt> </span></span></dl></td>
<td><span data-ttu-id="5e430-151">將視窗還原成其正常位置和大小。</span><span class="sxs-lookup"><span data-stu-id="5e430-151">Restores the window to its normal position and size.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_SCREENSAVE"></span><span id="sc_screensave"></span><dl> <span data-ttu-id="5e430-152"><dt><strong>SC_SCREENSAVE</strong></dt> <dt>0xF140</dt> </span><span class="sxs-lookup"><span data-stu-id="5e430-152"><dt><strong>SC_SCREENSAVE</strong></dt> <dt>0xF140</dt> </span></span></dl></td>
<td><span data-ttu-id="5e430-153">執行 System.ini 檔案的 [boot] 區段中指定的螢幕保護裝置應用程式。</span><span class="sxs-lookup"><span data-stu-id="5e430-153">Executes the screen saver application specified in the [boot] section of the System.ini file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_SIZE"></span><span id="sc_size"></span><dl> <span data-ttu-id="5e430-154"><dt><strong>SC_SIZE</strong></dt> <dt>0xF000</dt> </span><span class="sxs-lookup"><span data-stu-id="5e430-154"><dt><strong>SC_SIZE</strong></dt> <dt>0xF000</dt> </span></span></dl></td>
<td><span data-ttu-id="5e430-155">調整視窗的大小。</span><span class="sxs-lookup"><span data-stu-id="5e430-155">Sizes the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_TASKLIST"></span><span id="sc_tasklist"></span><dl> <span data-ttu-id="5e430-156"><dt><strong>SC_TASKLIST</strong></dt> <dt>0xF130</dt> </span><span class="sxs-lookup"><span data-stu-id="5e430-156"><dt><strong>SC_TASKLIST</strong></dt> <dt>0xF130</dt> </span></span></dl></td>
<td><span data-ttu-id="5e430-157">啟用 [ <strong>開始</strong> ] 功能表。</span><span class="sxs-lookup"><span data-stu-id="5e430-157">Activates the <strong>Start</strong> menu.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_VSCROLL"></span><span id="sc_vscroll"></span><dl> <span data-ttu-id="5e430-158"><dt><strong>SC_VSCROLL</strong></dt> <dt>0xF070</dt> </span><span class="sxs-lookup"><span data-stu-id="5e430-158"><dt><strong>SC_VSCROLL</strong></dt> <dt>0xF070</dt> </span></span></dl></td>
<td><span data-ttu-id="5e430-159">垂直捲動。</span><span class="sxs-lookup"><span data-stu-id="5e430-159">Scrolls vertically.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="5e430-160">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5e430-160">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e430-161">低序位單字會指定游標的水準位置（在螢幕座標中），如果已選擇使用滑鼠的視窗功能表命令。</span><span class="sxs-lookup"><span data-stu-id="5e430-161">The low-order word specifies the horizontal position of the cursor, in screen coordinates, if a window menu command is chosen with the mouse.</span></span> <span data-ttu-id="5e430-162">否則，就不會使用此參數。</span><span class="sxs-lookup"><span data-stu-id="5e430-162">Otherwise, this parameter is not used.</span></span>

<span data-ttu-id="5e430-163">高序位單字會指定游標的垂直位置（在螢幕座標中），如果使用滑鼠來選擇視窗功能表命令，則為。</span><span class="sxs-lookup"><span data-stu-id="5e430-163">The high-order word specifies the vertical position of the cursor, in screen coordinates, if a window menu command is chosen with the mouse.</span></span> <span data-ttu-id="5e430-164">如果使用系統加速器選擇命令，此參數為1，如果使用助憶鍵，則為零。</span><span class="sxs-lookup"><span data-stu-id="5e430-164">This parameter is  1 if the command is chosen using a system accelerator, or zero if using a mnemonic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e430-165">傳回值</span><span class="sxs-lookup"><span data-stu-id="5e430-165">Return value</span></span>

<span data-ttu-id="5e430-166">如果應用程式處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="5e430-166">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e430-167">備註</span><span class="sxs-lookup"><span data-stu-id="5e430-167">Remarks</span></span>

<span data-ttu-id="5e430-168">若要取得螢幕座標中的位置座標，請使用下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="5e430-168">To obtain the position coordinates in screen coordinates, use the following code:</span></span>


```
xPos = GET_X_LPARAM(lParam);    // horizontal position 
yPos = GET_Y_LPARAM(lParam);    // vertical position
```



<span data-ttu-id="5e430-169">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會針對上表中指定的預先定義動作，執行視窗功能表要求。</span><span class="sxs-lookup"><span data-stu-id="5e430-169">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function carries out the window menu request for the predefined actions specified in the previous table.</span></span>

<span data-ttu-id="5e430-170">在 **WM \_ SYSCOMMAND** 訊息中，系統會在內部使用 *wParam* 參數的四個低序位位。</span><span class="sxs-lookup"><span data-stu-id="5e430-170">In **WM\_SYSCOMMAND** messages, the four low-order bits of the *wParam* parameter are used internally by the system.</span></span> <span data-ttu-id="5e430-171">若要在測試 *wParam* 的值時取得正確的結果，應用程式必須使用位 and 運算子，將值0XFFF0 與 *wParam* 值結合。</span><span class="sxs-lookup"><span data-stu-id="5e430-171">To obtain the correct result when testing the value of *wParam*, an application must combine the value 0xFFF0 with the *wParam* value by using the bitwise AND operator.</span></span>

<span data-ttu-id="5e430-172">您可以使用 [**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu)、 [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua)、 [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)、 [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua)、 [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema)和 [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) 函數來修改視窗功能表中的功能表項目。</span><span class="sxs-lookup"><span data-stu-id="5e430-172">The menu items in a window menu can be modified by using the [**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu), [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema), and [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) functions.</span></span> <span data-ttu-id="5e430-173">修改視窗功能表的應用程式必須處理 **WM \_ SYSCOMMAND** 訊息。</span><span class="sxs-lookup"><span data-stu-id="5e430-173">Applications that modify the window menu must process **WM\_SYSCOMMAND** messages.</span></span>

<span data-ttu-id="5e430-174">應用程式可以在任何時間執行任何系統命令，方法是將 **WM \_ SYSCOMMAND** 訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)。</span><span class="sxs-lookup"><span data-stu-id="5e430-174">An application can carry out any system command at any time by passing a **WM\_SYSCOMMAND** message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="5e430-175">應用程式未處理的任何 **WM \_ SYSCOMMAND** 訊息都必須傳遞至 **DefWindowProc**。</span><span class="sxs-lookup"><span data-stu-id="5e430-175">Any **WM\_SYSCOMMAND** messages not handled by the application must be passed to **DefWindowProc**.</span></span> <span data-ttu-id="5e430-176">應用程式所新增的任何命令值都必須由應用程式處理，而且無法傳遞至 **DefWindowProc**。</span><span class="sxs-lookup"><span data-stu-id="5e430-176">Any command values added by an application must be processed by the application and cannot be passed to **DefWindowProc**.</span></span>

<span data-ttu-id="5e430-177">如果原則啟用密碼保護，則不論應用程式如何使用 **SC \_ SCREENSAVE** 通知，即使無法將它傳遞給 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)，也會啟動畫面保護。</span><span class="sxs-lookup"><span data-stu-id="5e430-177">If password protection is enabled by policy, the screen saver is started regardless of what an application does with the **SC\_SCREENSAVE** notification even if fails to pass it to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="5e430-178">定義為從 [視窗] 功能表選擇專案的快速鍵會轉譯成 **wm \_ SYSCOMMAND** 訊息; 所有其他快速鍵按鍵都會轉譯成 [**wm \_ 命令**](wm-command.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="5e430-178">Accelerator keys that are defined to choose items from the window menu are translated into **WM\_SYSCOMMAND** messages; all other accelerator keystrokes are translated into [**WM\_COMMAND**](wm-command.md) messages.</span></span>

<span data-ttu-id="5e430-179">如果 *wParam* 是 **SC \_ KEYMENU**， *lParam* 就會包含用來顯示快顯功能表的 ALT 鍵的字元碼。</span><span class="sxs-lookup"><span data-stu-id="5e430-179">If the *wParam* is **SC\_KEYMENU**, *lParam* contains the character code of the key that is used with the ALT key to display the popup menu.</span></span> <span data-ttu-id="5e430-180">例如，按 ALT + F 顯示檔案快顯視窗，會導致 *wParam* 等於 **SC \_ KEYMENU** 且 *LParam* 等於 ' F ' 的 **WM \_ SYSCOMMAND** 。</span><span class="sxs-lookup"><span data-stu-id="5e430-180">For example, pressing ALT+F to display the File popup will cause a **WM\_SYSCOMMAND** with *wParam* equal to **SC\_KEYMENU** and *lParam* equal to 'f'.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e430-181">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e430-181">Requirements</span></span>



| <span data-ttu-id="5e430-182">需求</span><span class="sxs-lookup"><span data-stu-id="5e430-182">Requirement</span></span> | <span data-ttu-id="5e430-183">值</span><span class="sxs-lookup"><span data-stu-id="5e430-183">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e430-184">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5e430-184">Minimum supported client</span></span><br/> | <span data-ttu-id="5e430-185">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e430-185">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5e430-186">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5e430-186">Minimum supported server</span></span><br/> | <span data-ttu-id="5e430-187">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e430-187">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5e430-188">標頭</span><span class="sxs-lookup"><span data-stu-id="5e430-188">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e430-189"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="5e430-189"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e430-190">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5e430-190">See also</span></span>

<dl> <dt>

<span data-ttu-id="5e430-191">**參考**</span><span class="sxs-lookup"><span data-stu-id="5e430-191">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5e430-192">**AppendMenu**</span><span class="sxs-lookup"><span data-stu-id="5e430-192">**AppendMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-appendmenua)
</dt> <dt>

[<span data-ttu-id="5e430-193">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="5e430-193">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="5e430-194">**取得 \_ X \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="5e430-194">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="5e430-195">**取得 \_ Y \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="5e430-195">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="5e430-196">**GetSystemMenu**</span><span class="sxs-lookup"><span data-stu-id="5e430-196">**GetSystemMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu)
</dt> <dt>

[<span data-ttu-id="5e430-197">**InsertMenu**</span><span class="sxs-lookup"><span data-stu-id="5e430-197">**InsertMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-insertmenua)
</dt> <dt>

[<span data-ttu-id="5e430-198">**ModifyMenu**</span><span class="sxs-lookup"><span data-stu-id="5e430-198">**ModifyMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-modifymenua)
</dt> <dt>

[<span data-ttu-id="5e430-199">**WM \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="5e430-199">**WM\_COMMAND**</span></span>](wm-command.md)
</dt> <dt>

<span data-ttu-id="5e430-200">**概念**</span><span class="sxs-lookup"><span data-stu-id="5e430-200">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5e430-201">鍵盤加速器</span><span class="sxs-lookup"><span data-stu-id="5e430-201">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

