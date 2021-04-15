---
title: 處理螢幕保護裝置
description: Microsoft WIN32 API 支援稱為螢幕保護裝置的特殊應用程式。
ms.assetid: cda5e690-71fe-4df7-b8a2-3a2ad65b1bfb
keywords:
- 螢幕保護裝置
- 主控台，螢幕保護裝置
- ScreenSaverConfigureDialog
- 模組定義檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b7e0d0c177af2798b041fa12b4cc5793bf9be0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463096"
---
# <a name="handling-screen-savers"></a><span data-ttu-id="bbf9b-107">處理螢幕保護裝置</span><span class="sxs-lookup"><span data-stu-id="bbf9b-107">Handling Screen Savers</span></span>

<span data-ttu-id="bbf9b-108">Microsoft WIN32 API 支援稱為 *螢幕保護裝置* 的特殊應用程式。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-108">The Microsoft Win32 API supports special applications called *screen savers*.</span></span> <span data-ttu-id="bbf9b-109">當滑鼠和鍵盤閒置一段指定的時間時，就會啟動畫面保護。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-109">Screen savers start when the mouse and keyboard have been idle for a specified period of time.</span></span> <span data-ttu-id="bbf9b-110">原因有下列兩個原因：</span><span class="sxs-lookup"><span data-stu-id="bbf9b-110">They are used for these two reasons:</span></span>

-   <span data-ttu-id="bbf9b-111">保護螢幕免于靜態映射所造成的 phosphor 燒錄。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-111">To protect a screen from phosphor burn caused by static images.</span></span>
-   <span data-ttu-id="bbf9b-112">隱藏畫面上的機密資訊。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-112">To conceal sensitive information left on a screen.</span></span>

<span data-ttu-id="bbf9b-113">本主題分為下列各節。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-113">This topic is divided into the following sections.</span></span>

-   [<span data-ttu-id="bbf9b-114">關於螢幕保護裝置</span><span class="sxs-lookup"><span data-stu-id="bbf9b-114">About Screen Savers</span></span>](#about-screen-savers)
-   [<span data-ttu-id="bbf9b-115">使用螢幕保護裝置函式</span><span class="sxs-lookup"><span data-stu-id="bbf9b-115">Using the Screen Saver Functions</span></span>](#using-the-screen-saver-functions)
    -   [<span data-ttu-id="bbf9b-116">建立螢幕保護裝置程式</span><span class="sxs-lookup"><span data-stu-id="bbf9b-116">Creating a Screen Saver</span></span>](#creating-a-screen-saver)
    -   [<span data-ttu-id="bbf9b-117">安裝新的螢幕保護裝置程式</span><span class="sxs-lookup"><span data-stu-id="bbf9b-117">Installing New Screen Savers</span></span>](#installing-new-screen-savers)
    -   <span data-ttu-id="bbf9b-118">[將說明新增至 [螢幕保護裝置設定] 對話方塊](#adding-help-to-the-screen-saver-configuration-dialog-box)</span><span class="sxs-lookup"><span data-stu-id="bbf9b-118">[Adding Help to the Screen Saver Configuration Dialog Box](#adding-help-to-the-screen-saver-configuration-dialog-box)</span></span>

## <a name="about-screen-savers"></a><span data-ttu-id="bbf9b-119">關於螢幕保護裝置</span><span class="sxs-lookup"><span data-stu-id="bbf9b-119">About Screen Savers</span></span>

<span data-ttu-id="bbf9b-120">Windows 主控台中的桌面應用程式可讓使用者從螢幕保護裝置清單中選取，指定螢幕保護裝置啟動前應該經過多少時間、設定螢幕保護裝置，以及預覽螢幕保護裝置。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-120">The Desktop application in the Windows Control Panel lets users select from a list of screen savers, specify how much time should elapse before the screen saver starts, configure screen savers, and preview screen savers.</span></span> <span data-ttu-id="bbf9b-121">當 Windows 啟動時，或當使用者透過主控台啟動畫面保護時，會自動載入螢幕保護裝置。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-121">Screen savers are loaded automatically when Windows starts or when a user activates the screen saver through the Control Panel.</span></span>

<span data-ttu-id="bbf9b-122">選擇螢幕保護裝置之後，Windows 會監視按鍵和滑鼠移動，然後在閒置一段時間後啟動畫面保護。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-122">Once a screen saver is chosen, Windows monitors keystrokes and mouse movements and then starts the screen saver after a period of inactivity.</span></span> <span data-ttu-id="bbf9b-123">但是，如果有下列任何一種情況，Windows 就不會啟動畫面保護：</span><span class="sxs-lookup"><span data-stu-id="bbf9b-123">However, Windows does not start the screen saver if any of the following conditions exist:</span></span>

-   <span data-ttu-id="bbf9b-124">作用中的應用程式不是以 Windows 為基礎的應用程式。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-124">The active application is not a Windows-based application.</span></span>
-   <span data-ttu-id="bbf9b-125">有以電腦為基礎的訓練 (CBT) 視窗。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-125">A computer-based training (CBT) window is present.</span></span>
-   <span data-ttu-id="bbf9b-126">作用中的應用程式會接收包含 *wParam* 參數設定為 SC SCREENSAVE 值的 [WM \_ SYSCOMMAND](../menurc/wm-syscommand.md)訊息 \_ ，但不會將訊息傳遞至 [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)函數。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-126">The active application receives the [WM\_SYSCOMMAND](../menurc/wm-syscommand.md) message with the *wParam* parameter set to the SC\_SCREENSAVE value, but it does not pass the message to the [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) function.</span></span>

<span data-ttu-id="bbf9b-127">**螢幕保護裝置的安全性內容**</span><span class="sxs-lookup"><span data-stu-id="bbf9b-127">**Security Context of the Screen Saver**</span></span>

<span data-ttu-id="bbf9b-128">螢幕保護裝置的安全性內容取決於使用者是否以互動方式登入。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-128">The security context of the screen saver is dependent on whether a user is interactively logged on.</span></span> <span data-ttu-id="bbf9b-129">如果叫用螢幕保護裝置時以互動方式登入使用者，螢幕保護裝置會在互動式使用者的安全性內容中執行。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-129">If a user is interactively logged on when the screen saver is invoked, the screen saver runs in the security context of the interactive user.</span></span> <span data-ttu-id="bbf9b-130">如果沒有任何使用者登入，則螢幕保護裝置的安全性內容將取決於所使用的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-130">If no user is logged on, the security context of the screen saver is dependent on the version of Windows being used.</span></span>

-   <span data-ttu-id="bbf9b-131">Windows XP 和 Windows 2000-螢幕保護裝置會在具有帳戶限制的 LocalSystem 內容中執行。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-131">Windows XP and Windows 2000 - screen saver runs in the context of LocalSystem with accounts restricted.</span></span>
-   <span data-ttu-id="bbf9b-132">Windows 2003-螢幕保護裝置會在 LocalService 的內容中執行，並移除擁有權限，並停用系統管理員群組。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-132">Windows 2003 - screen saver runs in the context of LocalService with all privileges removed and administrators group disabled.</span></span>
-   <span data-ttu-id="bbf9b-133">不適用於 Windows NT4。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-133">Does not apply to Windows NT4.</span></span>

<span data-ttu-id="bbf9b-134">安全性內容會決定可以從螢幕保護裝置完成的特殊許可權作業層級。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-134">The security context determines the level of privileged operations which can be done from a screen saver.</span></span>

<span data-ttu-id="bbf9b-135">**Windows Vista 和更新版本：** 如果原則啟用密碼保護，則不論應用程式如何使用 SC SCREENSAVE 通知，都會啟動畫面保護 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-135">**Windows Vista and later:** If password protection is enabled by policy, the screen saver is started regardless of what an application does with the SC\_SCREENSAVE notification.</span></span>

<span data-ttu-id="bbf9b-136">螢幕保護裝置包含特定匯出的函式、資源定義和變數宣告。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-136">Screen savers contain specific exported functions, resource definitions, and variable declarations.</span></span> <span data-ttu-id="bbf9b-137">螢幕保護裝置程式庫包含 **主要** 功能，以及螢幕保護裝置程式所需的其他啟動程式碼。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-137">The screen saver library contains the **main** function and other startup code required for a screen saver.</span></span> <span data-ttu-id="bbf9b-138">當螢幕保護裝置啟動時，螢幕保護裝置程式庫中的啟動程式碼會建立全螢幕視窗。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-138">When a screen saver starts, the startup code in the screen saver library creates a full-screen window.</span></span> <span data-ttu-id="bbf9b-139">此視窗的視窗類別宣告如下：</span><span class="sxs-lookup"><span data-stu-id="bbf9b-139">The window class for this window is declared as follows:</span></span>


```
WNDCLASS cls; 
cls.hCursor        = NULL; 
cls.hIcon          = LoadIcon(hInst, MAKEINTATOM(ID_APP)); 
cls.lpszMenuName   = NULL; 
cls.lpszClassName  = "WindowsScreenSaverClass"; 
cls.hbrBackground  = GetStockObject(BLACK_BRUSH); 
cls.hInstance      = hInst; 
cls.style          = CS_VREDRAW  | CS_HREDRAW | CS_SAVEBITS | CS_DBLCLKS; 
cls.lpfnWndProc    = (WNDPROC) ScreenSaverProc; 
cls.cbWndExtra     = 0; 
cls.cbClsExtra     = 0;
```



<span data-ttu-id="bbf9b-140">若要建立螢幕保護裝置，大部分的開發人員會建立包含三個必要功能的原始程式碼模組，並將它們與螢幕保護裝置程式庫連結。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-140">To create a screen saver, most developers create a source code module containing three required functions and link them with the screen saver library.</span></span> <span data-ttu-id="bbf9b-141">螢幕保護裝置模組只負責設定本身以及提供視覺效果。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-141">A screen saver module is responsible only for configuring itself and for providing visual effects.</span></span>

<span data-ttu-id="bbf9b-142">螢幕保護裝置模組中的三個必要功能之一是 [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc)。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-142">One of the three required functions in a screen saver module is [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc).</span></span> <span data-ttu-id="bbf9b-143">此函式會處理特定的訊息，並將任何未處理的訊息傳遞回螢幕保護裝置程式庫。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-143">This function processes specific messages and passes any unprocessed messages back to the screen saver library.</span></span> <span data-ttu-id="bbf9b-144">以下是一些 **ScreenSaverProc** 處理的一般訊息。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-144">Following are some of the typical messages processed by **ScreenSaverProc**.</span></span>



| <span data-ttu-id="bbf9b-145">訊息</span><span class="sxs-lookup"><span data-stu-id="bbf9b-145">Message</span></span>        | <span data-ttu-id="bbf9b-146">意義</span><span class="sxs-lookup"><span data-stu-id="bbf9b-146">Meaning</span></span>                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbf9b-147">WM \_ 建立</span><span class="sxs-lookup"><span data-stu-id="bbf9b-147">WM\_CREATE</span></span>     | <span data-ttu-id="bbf9b-148">從 Regedit.ini 檔案取出任何初始化資料。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-148">Retrieve any initialization data from the Regedit.ini file.</span></span> <span data-ttu-id="bbf9b-149">設定螢幕保護裝置視窗的視窗計時器。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-149">Set a window timer for the screen saver window.</span></span> <span data-ttu-id="bbf9b-150">執行任何其他必要的初始化。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-150">Perform any other required initialization.</span></span>                                     |
| <span data-ttu-id="bbf9b-151">WM \_ ERASEBKGND</span><span class="sxs-lookup"><span data-stu-id="bbf9b-151">WM\_ERASEBKGND</span></span> | <span data-ttu-id="bbf9b-152">清除 [螢幕保護裝置] 視窗，並為後續的繪圖作業做好準備。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-152">Erase the screen saver window and prepare for subsequent drawing operations.</span></span>                                                                                                               |
| <span data-ttu-id="bbf9b-153">WM \_ 計時器</span><span class="sxs-lookup"><span data-stu-id="bbf9b-153">WM\_TIMER</span></span>      | <span data-ttu-id="bbf9b-154">執行繪圖作業。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-154">Perform drawing operations.</span></span>                                                                                                                                                                |
| <span data-ttu-id="bbf9b-155">WM 損 \_ 毀</span><span class="sxs-lookup"><span data-stu-id="bbf9b-155">WM\_DESTROY</span></span>    | <span data-ttu-id="bbf9b-156">終結應用程式處理 [WM \_ 建立](../winmsg/wm-create.md) 訊息時所建立的計時器。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-156">Destroy the timers created when the application processed the [WM\_CREATE](../winmsg/wm-create.md) message.</span></span> <span data-ttu-id="bbf9b-157">執行任何其他必要的清除。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-157">Perform any additional required cleanup.</span></span> |



 

<span data-ttu-id="bbf9b-158">[**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) 藉由呼叫 [**DefScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) 函式，將未處理的訊息傳遞至螢幕保護裝置程式庫。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-158">[**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) passes unprocessed messages to the screen saver library by calling the [**DefScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) function.</span></span> <span data-ttu-id="bbf9b-159">下表說明此函數如何處理各種訊息。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-159">The following table describes how this function processes various messages.</span></span>



| <span data-ttu-id="bbf9b-160">訊息</span><span class="sxs-lookup"><span data-stu-id="bbf9b-160">Message</span></span>         | <span data-ttu-id="bbf9b-161">動作</span><span class="sxs-lookup"><span data-stu-id="bbf9b-161">Action</span></span>                                                                    |
|-----------------|---------------------------------------------------------------------------|
| <span data-ttu-id="bbf9b-162">WM \_ SETCURSOR</span><span class="sxs-lookup"><span data-stu-id="bbf9b-162">WM\_SETCURSOR</span></span>   | <span data-ttu-id="bbf9b-163">將游標設為 null 資料指標，並將它從畫面中移除。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-163">Set the cursor to the null cursor, removing it from the screen.</span></span>           |
| <span data-ttu-id="bbf9b-164">WM \_ 油漆</span><span class="sxs-lookup"><span data-stu-id="bbf9b-164">WM\_PAINT</span></span>       | <span data-ttu-id="bbf9b-165">繪製螢幕背景。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-165">Paint the screen background.</span></span>                                              |
| <span data-ttu-id="bbf9b-166">WM \_ LBUTTONDOWN</span><span class="sxs-lookup"><span data-stu-id="bbf9b-166">WM\_LBUTTONDOWN</span></span> | <span data-ttu-id="bbf9b-167">終止螢幕保護裝置。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-167">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="bbf9b-168">WM \_ MBUTTONDOWN</span><span class="sxs-lookup"><span data-stu-id="bbf9b-168">WM\_MBUTTONDOWN</span></span> | <span data-ttu-id="bbf9b-169">終止螢幕保護裝置。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-169">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="bbf9b-170">WM \_ RBUTTONDOWN</span><span class="sxs-lookup"><span data-stu-id="bbf9b-170">WM\_RBUTTONDOWN</span></span> | <span data-ttu-id="bbf9b-171">終止螢幕保護裝置。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-171">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="bbf9b-172">WM \_ KEYDOWN</span><span class="sxs-lookup"><span data-stu-id="bbf9b-172">WM\_KEYDOWN</span></span>     | <span data-ttu-id="bbf9b-173">終止螢幕保護裝置。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-173">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="bbf9b-174">WM \_ MOUSEMOVE</span><span class="sxs-lookup"><span data-stu-id="bbf9b-174">WM\_MOUSEMOVE</span></span>   | <span data-ttu-id="bbf9b-175">終止螢幕保護裝置。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-175">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="bbf9b-176">WM \_ 啟用</span><span class="sxs-lookup"><span data-stu-id="bbf9b-176">WM\_ACTIVATE</span></span>    | <span data-ttu-id="bbf9b-177">如果 *wParam* 參數設定為 **FALSE**，則終止螢幕保護裝置。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-177">Terminate the screen saver if the *wParam* parameter is set to **FALSE**.</span></span> |



 

<span data-ttu-id="bbf9b-178">螢幕保護裝置模組中的第二個必要功能是 [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog)。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-178">The second required function in a screen saver module is [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog).</span></span> <span data-ttu-id="bbf9b-179">此函式會顯示對話方塊，讓使用者可以設定螢幕保護裝置 (應用程式必須提供對應的對話方塊範本) 。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-179">This function displays a dialog box that enables the user to configure the screen saver (an application must provide a corresponding dialog box template).</span></span> <span data-ttu-id="bbf9b-180">當使用者在主控台的 [螢幕保護裝置] 對話方塊中選取 [安裝] 按鈕時，Windows 會顯示 [ **設定** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-180">Windows displays the configuration dialog box when the user selects the **Setup** button in the Control Panel's Screen Saver dialog box.</span></span>

<span data-ttu-id="bbf9b-181">螢幕保護裝置模組中的第三個必要功能是 [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses)。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-181">The third required function in a screen saver module is [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses).</span></span> <span data-ttu-id="bbf9b-182">所有螢幕保護裝置應用程式都必須呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-182">This function must be called by all screen saver applications.</span></span> <span data-ttu-id="bbf9b-183">不過，在 [設定] 對話方塊中不需要特殊 windows 或自訂控制項的應用程式可以直接傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-183">However, applications that do not require special windows or custom controls in the configuration dialog box can simply return **TRUE**.</span></span> <span data-ttu-id="bbf9b-184">需要特殊 windows 或自訂控制項的應用程式應該使用此函式來註冊對應的視窗類別。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-184">Applications requiring special windows or custom controls should use this function to register the corresponding window classes.</span></span>

<span data-ttu-id="bbf9b-185">除了建立支援上述三個函式的模組之外，螢幕保護裝置還應該提供圖示。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-185">In addition to creating a module that supports the three functions just described, a screen saver should supply an icon.</span></span> <span data-ttu-id="bbf9b-186">只有當螢幕保護裝置以獨立應用程式的形式執行時，才會顯示此圖示。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-186">This icon is visible only when the screen saver is run as a standalone application.</span></span> <span data-ttu-id="bbf9b-187"> (由主控台執行，則螢幕保護裝置的副檔名必須為 .scr;若要以獨立應用程式的形式執行，其必須具有 .exe 副檔名。 ) 在螢幕保護裝置的資源檔中，必須在 \_ Scrnsave .h 標頭檔中定義的常數識別碼應用程式識別該圖示。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-187">(To be run by the Control Panel, a screen saver must have the .scr file name extension; to be run as a standalone application, it must have the .exe file name extension.) The icon must be identified in the screen saver's resource file by the constant ID\_APP, which is defined in the Scrnsave.h header file.</span></span>

<span data-ttu-id="bbf9b-188">最後一個需求是螢幕保護裝置的描述字串。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-188">One final requirement is a screen saver description string.</span></span> <span data-ttu-id="bbf9b-189">螢幕保護裝置的資源檔必須包含主控台顯示為螢幕保護裝置名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-189">The resource file for a screen saver must contain a string that the Control Panel displays as the screen saver name.</span></span> <span data-ttu-id="bbf9b-190">描述字串必須是資源檔的字串資料表中的第一個字串， (以序數值 1) 識別。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-190">The description string must be the first string in the resource file's string table (identified with the ordinal value 1).</span></span> <span data-ttu-id="bbf9b-191">但是，如果螢幕保護裝置的檔案名很長，則主控台會忽略描述字串。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-191">However, the description string is ignored by the Control Panel if the screen saver has a long filename.</span></span> <span data-ttu-id="bbf9b-192">在這種情況下，檔案名會用來做為描述字串。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-192">In such case, the filename will be used as the description string.</span></span>

## <a name="using-the-screen-saver-functions"></a><span data-ttu-id="bbf9b-193">使用螢幕保護裝置函式</span><span class="sxs-lookup"><span data-stu-id="bbf9b-193">Using the Screen Saver Functions</span></span>

<span data-ttu-id="bbf9b-194">本節使用從螢幕保護裝置應用程式取得的範例程式碼來說明下列工作：</span><span class="sxs-lookup"><span data-stu-id="bbf9b-194">This section uses example code taken from a screen saver application to illustrate the following tasks:</span></span>

-   [<span data-ttu-id="bbf9b-195">建立螢幕保護裝置程式</span><span class="sxs-lookup"><span data-stu-id="bbf9b-195">Creating a Screen Saver</span></span>](#creating-a-screen-saver)
-   [<span data-ttu-id="bbf9b-196">安裝新的螢幕保護裝置程式</span><span class="sxs-lookup"><span data-stu-id="bbf9b-196">Installing New Screen Savers</span></span>](#installing-new-screen-savers)
-   <span data-ttu-id="bbf9b-197">[將說明新增至 [螢幕保護裝置設定] 對話方塊](#adding-help-to-the-screen-saver-configuration-dialog-box)</span><span class="sxs-lookup"><span data-stu-id="bbf9b-197">[Adding Help to the Screen Saver Configuration Dialog Box](#adding-help-to-the-screen-saver-configuration-dialog-box)</span></span>

### <a name="creating-a-screen-saver"></a><span data-ttu-id="bbf9b-198">建立螢幕保護裝置程式</span><span class="sxs-lookup"><span data-stu-id="bbf9b-198">Creating a Screen Saver</span></span>

<span data-ttu-id="bbf9b-199">從1到10秒的間隔，此範例中的應用程式會以四種色彩的其中一種來重新繪製畫面：白色、淺灰色、暗灰色和黑色。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-199">At intervals ranging from 1 through 10 seconds, the application in this example repaints the screen with one of four colors: white, light gray, dark gray, and black.</span></span> <span data-ttu-id="bbf9b-200">應用程式會在每次收到 [WM \_ 計時器](../winmsg/wm-timer.md) 訊息時繪製畫面。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-200">The application paints the screen each time it receives a [WM\_TIMER](../winmsg/wm-timer.md) message.</span></span> <span data-ttu-id="bbf9b-201">使用者可以藉由選取應用程式的 [設定] 對話方塊，並調整單一水準捲軸，來調整傳送此訊息的間隔。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-201">The user can adjust the interval at which this message is sent by selecting the application's configuration dialog box and adjusting a single horizontal scroll bar.</span></span>

### <a name="screen-saver-library"></a><span data-ttu-id="bbf9b-202">螢幕保護裝置程式庫</span><span class="sxs-lookup"><span data-stu-id="bbf9b-202">Screen saver library</span></span>

<span data-ttu-id="bbf9b-203">靜態螢幕保護裝置函式包含在螢幕保護裝置程式庫中。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-203">The static screen saver functions are contained in the screen saver library.</span></span> <span data-ttu-id="bbf9b-204">有兩個版本的程式庫可用： Scrnsave .lib 和 Scrnsavw。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-204">There are two versions of the library available, Scrnsave.lib and Scrnsavw.lib.</span></span> <span data-ttu-id="bbf9b-205">您必須使用下列其中一項鍊接您的專案。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-205">You must link your project with one of these.</span></span> <span data-ttu-id="bbf9b-206">Scrnsave 可用於使用 ANSI 字元的螢幕保護裝置，而 Scrnsavw 則用於使用 Unicode 字元的螢幕保護裝置。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-206">Scrnsave.lib is used for screen savers that use ANSI characters, and Scrnsavw.lib is used for screen savers that use Unicode characters.</span></span> <span data-ttu-id="bbf9b-207">與 Scrnsavw 連結的螢幕保護裝置只會在支援 Unicode 的 Windows 平臺上執行，而與 Scrnsave 連結的螢幕保護裝置會在任何 Windows 平臺上執行。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-207">A screen saver that is linked with Scrnsavw.lib will only run on Windows platforms that support Unicode, while a screen saver linked with Scrnsave.lib will run on any Windows platform.</span></span>

### <a name="supporting-the-configuration-dialog-box"></a><span data-ttu-id="bbf9b-208">支援設定對話方塊</span><span class="sxs-lookup"><span data-stu-id="bbf9b-208">Supporting the configuration dialog box</span></span>

<span data-ttu-id="bbf9b-209">大部分的螢幕保護裝置都會提供設定對話方塊，讓使用者指定自訂資料，例如獨特的色彩、繪圖速度、線條粗細、字型等等。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-209">Most screen savers provide a configuration dialog box to let the user specify customization data such as unique colors, drawing speeds, line thickness, fonts, and so on.</span></span> <span data-ttu-id="bbf9b-210">若要支援 [設定] 對話方塊，應用程式必須提供對話方塊範本，而且也必須支援 [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) 函數。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-210">To support the configuration dialog box, the application must provide a dialog box template and must also support the [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) function.</span></span> <span data-ttu-id="bbf9b-211">以下是範例應用程式的對話方塊範本。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-211">Following is the dialog box template for the sample application.</span></span>


```
DLG_SCRNSAVECONFIGURE DIALOG 6, 18, 160, 63
LANGUAGE LANG_NEUTRAL, SUBLANG_NEUTRAL
STYLE DS_MODALFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION | WS_SYSMENU
CAPTION "Sample Screen-Saver Setup"
FONT 8, "MS Shell Dlg"
BEGIN
    GROUPBOX      "Redraw Speed", 101, 0, 6, 98, 40
    SCROLLBAR     ID_SPEED, 5, 31, 89, 10
    LTEXT         "Fast", 103, 6, 21, 20, 8
    LTEXT         "Slow", 104, 75, 21, 20, 8
    PUSHBUTTON    "OK", ID_OK, 117, 10, 40, 14
    PUSHBUTTON    "Cancel", ID_CANCEL, 117, 32, 40, 14
END
```



<span data-ttu-id="bbf9b-212">您必須使用十進位值2003來定義用來識別對話方塊範本的常數，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="bbf9b-212">You must define the constant used to identify the dialog box template by using the decimal value 2003, as in the following example:</span></span>


```
#define  DLG_SCRNSAVECONFIGURE 2003
```



<span data-ttu-id="bbf9b-213">下列範例顯示在範例應用程式中找到的 [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) 函式。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-213">The following example shows the [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) function found in the sample application.</span></span>


```
#define MINVEL  1                 // minimum redraw speed value     
#define MAXVEL  10                // maximum redraw speed value    
#define DEFVEL  5                 // default redraw speed value    
 
LONG    lSpeed = DEFVEL;          // redraw speed variable         
  
extern HINSTANCE hMainInstance;   // screen saver instance handle  
 
CHAR   szAppName[80];             // .ini section name             
CHAR   szTemp[20];                // temporary array of characters  
CHAR   szRedrawSpeed[ ] = "Redraw Speed";   // .ini speed entry 
CHAR   szIniFile[MAXFILELEN];     // .ini or registry file name  
 
BOOL WINAPI ScreenSaverConfigureDialog(hDlg, message, wParam, lParam) 
HWND     hDlg; 
UINT     message; 
DWORD    wParam; 
LONG     lParam; 
HRESULT  hr;
{ 
    static HWND hSpeed;   // handle to speed scroll bar 
    static HWND hOK;      // handle to OK push button  
 
    switch(message) 
    { 
        case WM_INITDIALOG: 
 
            // Retrieve the application name from the .rc file.  
            LoadString(hMainInstance, idsAppName, szAppName, 
                       80 * sizeof(TCHAR)); 
 
            // Retrieve the .ini (or registry) file name. 
            LoadString(hMainInstance, idsIniFile, szIniFile, 
                       MAXFILELEN * sizeof(TCHAR)); 
 
            // TODO: Add error checking to verify LoadString success
            //       for both calls.
            
            // Retrieve any redraw speed data from the registry. 
            lSpeed = GetPrivateProfileInt(szAppName, szRedrawSpeed, 
                                          DEFVEL, szIniFile); 
 
            // If the initialization file does not contain an entry 
            // for this screen saver, use the default value. 
            if(lSpeed > MAXVEL || lSpeed < MINVEL) 
                lSpeed = DEFVEL; 
 
            // Initialize the redraw speed scroll bar control.
            hSpeed = GetDlgItem(hDlg, ID_SPEED); 
            SetScrollRange(hSpeed, SB_CTL, MINVEL, MAXVEL, FALSE); 
            SetScrollPos(hSpeed, SB_CTL, lSpeed, TRUE); 
 
            // Retrieve a handle to the OK push button control.  
            hOK = GetDlgItem(hDlg, ID_OK); 
 
            return TRUE; 
 
        case WM_HSCROLL: 

            // Process scroll bar input, adjusting the lSpeed 
            // value as appropriate. 
            switch (LOWORD(wParam)) 
                { 
                    case SB_PAGEUP: 
                        --lSpeed; 
                    break; 
 
                    case SB_LINEUP: 
                        --lSpeed; 
                    break; 
 
                    case SB_PAGEDOWN: 
                        ++lSpeed; 
                    break; 
 
                    case SB_LINEDOWN: 
                        ++lSpeed; 
                    break; 
 
                    case SB_THUMBPOSITION: 
                        lSpeed = HIWORD(wParam); 
                    break; 
 
                    case SB_BOTTOM: 
                        lSpeed = MINVEL; 
                    break; 
 
                    case SB_TOP: 
                        lSpeed = MAXVEL; 
                    break; 
 
                    case SB_THUMBTRACK: 
                    case SB_ENDSCROLL: 
                        return TRUE; 
                    break; 
                } 

                if ((int) lSpeed <= MINVEL) 
                    lSpeed = MINVEL; 
                if ((int) lSpeed >= MAXVEL) 
                    lSpeed = MAXVEL; 
 
                SetScrollPos((HWND) lParam, SB_CTL, lSpeed, TRUE); 
            break; 
 
        case WM_COMMAND: 
            switch(LOWORD(wParam)) 
            { 
                case ID_OK: 
 
                    // Write the current redraw speed variable to
                    // the .ini file. 
                    hr = StringCchPrintf(szTemp, 20, "%ld", lSpeed);
                    if (SUCCEEDED(hr))
                        WritePrivateProfileString(szAppName, szRedrawSpeed, 
                                                  szTemp, szIniFile); 
 
                case ID_CANCEL: 
                    EndDialog(hDlg, LOWORD(wParam) == ID_OK); 

                return TRUE; 
            } 
    } 
    return FALSE; 
}
```



<span data-ttu-id="bbf9b-214">除了提供對話方塊範本和支援 [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) 函式之外，應用程式也必須支援 [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) 函數。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-214">In addition to providing the dialog box template and supporting the [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) function, an application must also support the [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) function.</span></span> <span data-ttu-id="bbf9b-215">此函式會註冊螢幕保護裝置程式所需的任何非標準視窗類別。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-215">This function registers any nonstandard window classes required by the screen saver.</span></span> <span data-ttu-id="bbf9b-216">因為範例應用程式只在其對話方塊程式中使用標準視窗類別，所以此函式只會傳回 **TRUE**，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="bbf9b-216">Because the sample application used only standard window classes in its dialog box procedure, this function simply returns **TRUE**, as in the following example:</span></span>


```
BOOL WINAPI RegisterDialogClasses(hInst) 
HANDLE  hInst; 
{ 
    return TRUE; 
}
```



### <a name="supporting-the-screen-saver-window-procedure"></a><span data-ttu-id="bbf9b-217">支援螢幕保護裝置視窗程式</span><span class="sxs-lookup"><span data-stu-id="bbf9b-217">Supporting the screen saver window procedure</span></span>

<span data-ttu-id="bbf9b-218">每個螢幕保護裝置都必須支援一個名為 [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc)的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-218">Each screen saver must support a window procedure named [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc).</span></span> <span data-ttu-id="bbf9b-219">和大部分的視窗程式一樣， **ScreenSaverProc** 會處理一組特定的訊息，並將任何未處理的訊息傳遞至預設程式。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-219">Like most window procedures, **ScreenSaverProc** processes a set of specific messages and passes any unprocessed messages to a default procedure.</span></span> <span data-ttu-id="bbf9b-220">但是， **ScreenSaverProc** 會將未處理的訊息傳遞給 [**DefScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc)函式，而不是將它們傳遞給 [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)函數。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-220">However, instead of passing them to the [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) function, **ScreenSaverProc** passes unprocessed messages to the [**DefScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) function.</span></span> <span data-ttu-id="bbf9b-221">**ScreenSaverProc** 和一般視窗程式之間的另一個差異是，傳遞至 **ScreenSaverProc** 的控制碼會識別整個桌面，而不是用戶端視窗。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-221">Another difference between **ScreenSaverProc** and a normal window procedure is that the handle passed to **ScreenSaverProc** identifies the entire desktop rather than a client window.</span></span> <span data-ttu-id="bbf9b-222">下列範例顯示範例螢幕保護裝置的 **ScreenSaverProc** 視窗程式。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-222">The following example shows the **ScreenSaverProc** window procedure for the sample screen saver.</span></span>


```
LONG WINAPI ScreenSaverProc(hwnd, message, wParam, lParam) 
HWND  hwnd; 
UINT  message; 
DWORD wParam; 
LONG  lParam; 
{ 
    static HDC          hdc;      // device-context handle  
    static RECT         rc;       // RECT structure  
    static UINT         uTimer;   // timer identifier  
 
    switch(message) 
    { 
        case WM_CREATE: 
 
            // Retrieve the application name from the .rc file. 
            LoadString(hMainInstance, idsAppName, szAppName, 80 * sizeof(TCHAR)); 
 
            // Retrieve the .ini (or registry) file name. 
            LoadString(hMainInstance, idsIniFile, szIniFile, MAXFILELEN * sizeof(TCHAR)); 
 
            // TODO: Add error checking to verify LoadString success
            //       for both calls.
            
            // Retrieve any redraw speed data from the registry.  
            lSpeed = GetPrivateProfileInt(szAppName, szRedrawSpeed, 
                                          DEFVEL, szIniFile); 
 
            // Set a timer for the screen saver window using the 
            // redraw rate stored in Regedit.ini. 
            uTimer = SetTimer(hwnd, 1, lSpeed * 1000, NULL); 
            break; 
 
        case WM_ERASEBKGND: 
 
            // The WM_ERASEBKGND message is issued before the 
            // WM_TIMER message, allowing the screen saver to 
            // paint the background as appropriate. 

            hdc = GetDC(hwnd); 
            GetClientRect (hwnd, &rc); 
            FillRect (hdc, &rc, GetStockObject(BLACK_BRUSH)); 
            ReleaseDC(hwnd,hdc); 
            break; 
 
        case WM_TIMER: 
 
            // The WM_TIMER message is issued at (lSpeed * 1000) 
            // intervals, where lSpeed == .001 seconds. This 
            // code repaints the entire desktop with a white, 
            // light gray, dark gray, or black brush each 
            // time a WM_TIMER message is issued. 

            hdc = GetDC(hwnd); 
            GetClientRect(hwnd, &rc); 
            if (i++ <= 4) 
                FillRect(hdc, &rc, GetStockObject(i)); 
            else 
                (i = 0); 
            ReleaseDC(hwnd,hdc); 
            break; 
 
        case WM_DESTROY: 
 
            // When the WM_DESTROY message is issued, the screen saver 
            // must destroy any of the timers that were set at WM_CREATE 
            // time. 

            if (uTimer) 
                KillTimer(hwnd, uTimer); 
            break; 
    } 
 
    // DefScreenSaverProc processes any messages ignored by ScreenSaverProc. 
    return DefScreenSaverProc(hwnd, message, wParam, lParam); 
}
```



### <a name="creating-a-module-definition-file"></a><span data-ttu-id="bbf9b-223">建立模組定義檔</span><span class="sxs-lookup"><span data-stu-id="bbf9b-223">Creating a module-definition file</span></span>

<span data-ttu-id="bbf9b-224">[**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc)和 [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog)函數必須在應用程式的模組定義檔中匯出;但是， [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses)不應該匯出。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-224">The [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) and [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) functions must be exported in the application's module-definition file; [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) should not be exported, however.</span></span> <span data-ttu-id="bbf9b-225">下列範例顯示範例應用程式的模組定義檔。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-225">The following example shows the module-definition file for the sample application.</span></span>


```
NAME    SSTEST.SCR 

DESCRIPTION 'SCRNSAVE : Test' 
 
STUB    'WINSTUB.EXE' 
EXETYPE WINDOWS 
 
CODE    MOVEABLE 
DATA    MOVEABLE MULTIPLE 
 
HEAPSIZE  1024 
STACKSIZE 4096 
 
EXPORTS 
        ScreenSaverProc 
        ScreenSaverConfigureDialog
```



### <a name="installing-new-screen-savers"></a><span data-ttu-id="bbf9b-226">安裝新的螢幕保護裝置程式</span><span class="sxs-lookup"><span data-stu-id="bbf9b-226">Installing New Screen Savers</span></span>

<span data-ttu-id="bbf9b-227">編譯可用螢幕保護裝置的清單時，主控台會在 Windows 啟動目錄中搜尋副檔名為 .scr 的檔案。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-227">When compiling the list of available screen savers, the Control Panel searches the Windows Startup directory for files with the .scr extension.</span></span> <span data-ttu-id="bbf9b-228">因為螢幕保護裝置是具有 .exe 副檔名的標準 Windows 可執行檔，所以您必須將它們重新命名，使其具有 .scr 副檔名，然後將它們複製到正確的目錄。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-228">Because screen savers are standard Windows executable files with .exe extensions, you must rename them so they have .scr extensions and copy them to the correct directory.</span></span>

### <a name="adding-help-to-the-screen-saver-configuration-dialog-box"></a><span data-ttu-id="bbf9b-229">將說明新增至 [螢幕保護裝置設定] 對話方塊</span><span class="sxs-lookup"><span data-stu-id="bbf9b-229">Adding Help to the Screen Saver Configuration Dialog Box</span></span>

<span data-ttu-id="bbf9b-230">螢幕保護裝置程式的 [設定] 對話方塊通常會包含 [說明 **] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="bbf9b-230">The configuration dialog box for a screen saver typically includes a **Help** button.</span></span> <span data-ttu-id="bbf9b-231">螢幕保護裝置應用程式可以檢查 [說明] 按鈕識別碼，並以其他以 Windows 為基礎的應用程式中提供的相同方式來呼叫 [**WinHelp**](/windows/desktop/api/winuser/nf-winuser-winhelpa) 函數。</span><span class="sxs-lookup"><span data-stu-id="bbf9b-231">Screen saver applications can check for the Help button identifier and call the [**WinHelp**](/windows/desktop/api/winuser/nf-winuser-winhelpa) function in the same way Help is provided in other Windows-based applications.</span></span>

 

 