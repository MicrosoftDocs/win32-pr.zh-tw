---
title: 停用遊戲中的快速鍵
description: 本文說明如何在 Microsoft Windows 中暫時停用鍵盤快速鍵，以防止全螢幕遊戲的遊戲播放中斷。
ms.assetid: 732523f9-ecff-c6c2-646d-1bc3443232ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aff426e0d728150cf5f6ac3cd8d46a711c9b4f8b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463349"
---
# <a name="disabling-shortcut-keys-in-games"></a><span data-ttu-id="1f58f-103">停用遊戲中的快速鍵</span><span class="sxs-lookup"><span data-stu-id="1f58f-103">Disabling Shortcut Keys in Games</span></span>

<span data-ttu-id="1f58f-104">本文說明如何在 Microsoft Windows 中暫時停用鍵盤快速鍵，以防止全螢幕遊戲的遊戲播放中斷。</span><span class="sxs-lookup"><span data-stu-id="1f58f-104">This articles describes how to temporarily disable keyboard shortcuts in Microsoft Windows to prevent disruption of game play for full screen games.</span></span> <span data-ttu-id="1f58f-105">SHIFT 鍵和 CTRL 鍵通常用來做為遊戲中的火或 run 按鈕。</span><span class="sxs-lookup"><span data-stu-id="1f58f-105">The SHIFT key and the CTRL key are often used as fire or run buttons in games.</span></span> <span data-ttu-id="1f58f-106">如果使用者不小心按下位於這些機碼附近的 Windows 鍵 () ，它們可能會讓自己突然跳離毀損遊戲體驗的應用程式。</span><span class="sxs-lookup"><span data-stu-id="1f58f-106">If users accidentally press the Windows key (located near these keys), they can cause themselves to suddenly jump out of the application, which ruins the game experience.</span></span> <span data-ttu-id="1f58f-107">只要使用 SHIFT 鍵作為遊戲按鈕，就會不慎執行相黏鍵快捷方式，而這可能會顯示警告對話方塊。</span><span class="sxs-lookup"><span data-stu-id="1f58f-107">Simply using the SHIFT key as a game button can inadvertently execute the StickyKeys shortcut which may display a warning dialog.</span></span> <span data-ttu-id="1f58f-108">若要避免這些問題，您應該在以全螢幕模式執行時停用這些金鑰，並在以視窗模式執行時，將索引鍵恢復為預設處理常式，或結束應用程式。</span><span class="sxs-lookup"><span data-stu-id="1f58f-108">To avoid these issues, you should disable these keys when running in full-screen mode, and either enable the keys back to their default handlers when running in windowed mode or exit the application.</span></span>

<span data-ttu-id="1f58f-109">本文說明如何執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="1f58f-109">This article describes how to do the following:</span></span>

-   [<span data-ttu-id="1f58f-110">使用鍵盤掛勾來停用 Windows 鍵</span><span class="sxs-lookup"><span data-stu-id="1f58f-110">Disable the Windows Key with a Keyboard Hook</span></span>](#disable-the-windows-key-with-a-keyboard-hook)
-   [<span data-ttu-id="1f58f-111">停用協助工具快速鍵</span><span class="sxs-lookup"><span data-stu-id="1f58f-111">Disable the Accessibility Shortcut Keys</span></span>](#disable-the-accessibility-shortcut-keys)

## <a name="disable-the-windows-key-with-a-keyboard-hook"></a><span data-ttu-id="1f58f-112">使用鍵盤掛勾來停用 Windows 鍵</span><span class="sxs-lookup"><span data-stu-id="1f58f-112">Disable the Windows Key with a Keyboard Hook</span></span>

<span data-ttu-id="1f58f-113">使用低層級的鍵盤攔截，以篩選出要處理的 Windows 鍵。</span><span class="sxs-lookup"><span data-stu-id="1f58f-113">Use a low-level keyboard hook to filter out the Windows key from being processed.</span></span> <span data-ttu-id="1f58f-114">即使使用者將視窗最小化或切換至另一個應用程式，範例1中所顯示的低層級鍵盤攔截仍會保持有效。</span><span class="sxs-lookup"><span data-stu-id="1f58f-114">The low-level keyboard hook shown in Example 1 remains in effect even if a user minimizes the window or switches to another application.</span></span> <span data-ttu-id="1f58f-115">這表示當應用程式停用時，您必須小心確保 Windows 金鑰不會被停用。</span><span class="sxs-lookup"><span data-stu-id="1f58f-115">This means that you must be careful to ensure that the Windows key is not disabled when the application is deactivated.</span></span> <span data-ttu-id="1f58f-116">範例1中的程式碼會藉由處理 WM ACTI加值稅EAPP 訊息來執行此操作 \_ 。</span><span class="sxs-lookup"><span data-stu-id="1f58f-116">The code in Example 1 does this by handling the WM\_ACTIVATEAPP message.</span></span>

> [!Note]  
> <span data-ttu-id="1f58f-117">此方法適用于 Windows 2000 和更新版本的 Windows。</span><span class="sxs-lookup"><span data-stu-id="1f58f-117">This method works on Windows 2000 and later versions of Windows.</span></span> <span data-ttu-id="1f58f-118">此方法也適用于最低許可權的使用者帳戶 (也稱為限制使用者帳戶) 。</span><span class="sxs-lookup"><span data-stu-id="1f58f-118">This method also works with least-privileged user accounts (also known as limited-user accounts).</span></span>

 

<span data-ttu-id="1f58f-119">這個方法是由 DXUT 使用，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="1f58f-119">This method is used by DXUT and is illustrated in the following code example.</span></span>

<span data-ttu-id="1f58f-120">**範例1。使用低層級的鍵盤勾點來停用 Windows 鍵**</span><span class="sxs-lookup"><span data-stu-id="1f58f-120">**Example 1. Using a low-level keyboard hook to disable the Windows key**</span></span>


```C++
HHOOK g_hKeyboardHook;
BOOL g_bFullscreen;
 
INT WINAPI WinMain( HINSTANCE, HINSTANCE, LPSTR, int )
{
    // Initialization
    g_hKeyboardHook = SetWindowsHookEx( WH_KEYBOARD_LL,  LowLevelKeyboardProc, GetModuleHandle(NULL), 0 );
 
    // 
    // main application code here
    // 
 
    // Cleanup before shutdown
    UnhookWindowsHookEx( g_hKeyboardHook );
}
 
 
LRESULT CALLBACK LowLevelKeyboardProc( int nCode, WPARAM wParam, LPARAM lParam )
{
    if (nCode < 0 || nCode != HC_ACTION )  // do not process message 
        return CallNextHookEx( g_hKeyboardHook, nCode, wParam, lParam); 
 
    bool bEatKeystroke = false;
    KBDLLHOOKSTRUCT* p = (KBDLLHOOKSTRUCT*)lParam;
    switch (wParam) 
    {
        case WM_KEYDOWN:  
        case WM_KEYUP:    
        {
            bEatKeystroke = (g_bFullscreen && g_bWindowActive && ((p->vkCode == VK_LWIN) || (p->vkCode == VK_RWIN)));
            break;
        }
    }
 
    if( bEatKeystroke )
        return 1;
    else
        return CallNextHookEx( g_hKeyboardHook, nCode, wParam, lParam );
}
 
 
LRESULT CALLBACK WndProc( HWND hWnd, UINT uMsg, WPARAM wParam, LPARAM lParam )
{
    switch( uMsg )
    {
       case WM_ACTIVATEAPP:
            // g_bWindowActive is used to control if the Windows key is filtered by the keyboard hook or not.
            if( wParam == TRUE )
                g_bWindowActive  = true;           
            else 
                g_bWindowActive  = false;           
            break;
    }
}
```



## <a name="disable-the-accessibility-shortcut-keys"></a><span data-ttu-id="1f58f-121">停用協助工具快速鍵</span><span class="sxs-lookup"><span data-stu-id="1f58f-121">Disable the Accessibility Shortcut Keys</span></span>

<span data-ttu-id="1f58f-122">Windows 包含一些協助工具功能，例如「相黏鍵」、「篩選篩選」和「切換鍵」 (查看[Windows 輔助) 功能](/previous-versions/visualstudio/visual-studio-6.0/aa227589(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="1f58f-122">Windows includes accessibility features such as StickyKeys, FilterKeys, and ToggleKeys (see [Windows Accessibility](/previous-versions/visualstudio/visual-studio-6.0/aa227589(v=vs.60))).</span></span> <span data-ttu-id="1f58f-123">每個都有不同的用途;例如，相黏鍵是針對難以同時按住兩個或多個索引鍵的人員所設計。</span><span class="sxs-lookup"><span data-stu-id="1f58f-123">Each of these serves a different purpose; StickyKeys for example, is designed for people who have difficulty holding down two or more keys simultaneously.</span></span> <span data-ttu-id="1f58f-124">這些協助工具的每一項也都有鍵盤快速鍵，可讓您開啟或關閉此功能。</span><span class="sxs-lookup"><span data-stu-id="1f58f-124">Each of these accessibility features also has a keyboard shortcut that allows the feature to be turned on or off.</span></span> <span data-ttu-id="1f58f-125">例如，您可以按下 SHIFT 鍵五次來觸發相黏鍵快捷方式。</span><span class="sxs-lookup"><span data-stu-id="1f58f-125">For example, the StickyKeys shortcut is triggered by pressing the SHIFT key five times.</span></span> <span data-ttu-id="1f58f-126">如果遊戲中也使用 SHIFT 鍵，使用者在玩遊戲時，可能會不小心觸發此快捷方式。</span><span class="sxs-lookup"><span data-stu-id="1f58f-126">If the SHIFT key is also used in the game, the user could accidentally trigger this shortcut during game play.</span></span> <span data-ttu-id="1f58f-127">觸發快捷方式時，Windows (預設) 在對話方塊中顯示警告，這會導致 Windows 將執行全螢幕模式的遊戲降至最低。</span><span class="sxs-lookup"><span data-stu-id="1f58f-127">When the shortcut is triggered, Windows (by default) presents a warning in a dialog box, which would cause Windows to minimize a game running in full-screen mode.</span></span> <span data-ttu-id="1f58f-128">當然，這可能會對遊戲的播放產生重大影響。</span><span class="sxs-lookup"><span data-stu-id="1f58f-128">This, of course, can have a drastic effect on game play.</span></span>

<span data-ttu-id="1f58f-129">某些客戶需要協助工具功能，而且本身不會干擾全螢幕遊戲;因此，您不應該變更協助工具設定。</span><span class="sxs-lookup"><span data-stu-id="1f58f-129">The accessibility features are required for some customers and do not themselves interfere with full-screen games; therefore, you should not change the accessibility settings.</span></span> <span data-ttu-id="1f58f-130">不過，由於協助工具功能的快捷方式可能會在意外觸發時干擾遊戲播放，因此只有在未藉由呼叫 [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60))來啟用該功能時，才會關閉協助工具快捷方式。</span><span class="sxs-lookup"><span data-stu-id="1f58f-130">However, because the shortcuts for accessibility features can disrupt game play if triggered accidentally, you should turn off an accessibility shortcut only when that feature is not enabled by calling [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)).</span></span>

<span data-ttu-id="1f58f-131">即使在應用程式結束後， [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)) 關閉的協助工具快速鍵仍會關閉。</span><span class="sxs-lookup"><span data-stu-id="1f58f-131">An accessibility shortcut that is turned off by [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)) remains turned off even after the application has exited.</span></span> <span data-ttu-id="1f58f-132">這表示您必須在結束應用程式之前先還原設定。</span><span class="sxs-lookup"><span data-stu-id="1f58f-132">This means that you must restore the settings before exiting the application.</span></span> <span data-ttu-id="1f58f-133">由於應用程式可能無法正確地結束，因此您應該將這些設定寫入持續性儲存體，以便在應用程式再次執行時加以還原。</span><span class="sxs-lookup"><span data-stu-id="1f58f-133">Because it is possible for the application to fail to exit correctly, you should write these settings to persistent storage so that they can be restored when the application is run again.</span></span> <span data-ttu-id="1f58f-134">如果發生損毀，您也可以使用例外狀況處理常式來還原這些設定。</span><span class="sxs-lookup"><span data-stu-id="1f58f-134">You could also use an exception handler to restore these settings if a crash occurs.</span></span>

<span data-ttu-id="1f58f-135">**關閉這些快捷方式**</span><span class="sxs-lookup"><span data-stu-id="1f58f-135">**To turn off these shortcuts**</span></span>

1.  <span data-ttu-id="1f58f-136">在停用之前，請先捕獲目前的協助工具設定。</span><span class="sxs-lookup"><span data-stu-id="1f58f-136">Capture the current accessibility settings before disabling them.</span></span>
2.  <span data-ttu-id="1f58f-137">如果協助工具功能已關閉，當應用程式進入全螢幕模式時，請停用協助工具快捷方式。</span><span class="sxs-lookup"><span data-stu-id="1f58f-137">Disable the accessibility shortcut when the application goes into full-screen mode if the accessibility feature is off.</span></span>
3.  <span data-ttu-id="1f58f-138">當應用程式進入視窗模式或離開時，還原協助工具設定。</span><span class="sxs-lookup"><span data-stu-id="1f58f-138">Restore the accessibility settings when the application goes into windowed mode or exits.</span></span>

<span data-ttu-id="1f58f-139">這個方法是在 DXUT 中使用，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="1f58f-139">This method is used in DXUT, and is illustrated in the following code example.</span></span>

> [!Note]  
> <span data-ttu-id="1f58f-140">此方法適用于在受限的使用者帳戶上執行。</span><span class="sxs-lookup"><span data-stu-id="1f58f-140">This method works when running on a limited user account.</span></span>

 

<span data-ttu-id="1f58f-141">**範例2。停用協助工具快速鍵**</span><span class="sxs-lookup"><span data-stu-id="1f58f-141">**Example 2. Disabling accessibility shortcut keys**</span></span>


```C++
STICKYKEYS g_StartupStickyKeys = {sizeof(STICKYKEYS), 0};
TOGGLEKEYS g_StartupToggleKeys = {sizeof(TOGGLEKEYS), 0};
FILTERKEYS g_StartupFilterKeys = {sizeof(FILTERKEYS), 0};    
 
 
INT WINAPI WinMain( HINSTANCE, HINSTANCE, LPSTR, int )
{
    // Save the current sticky/toggle/filter key settings so they can be restored them later
    SystemParametersInfo(SPI_GETSTICKYKEYS, sizeof(STICKYKEYS), &g_StartupStickyKeys, 0);
    SystemParametersInfo(SPI_GETTOGGLEKEYS, sizeof(TOGGLEKEYS), &g_StartupToggleKeys, 0);
    SystemParametersInfo(SPI_GETFILTERKEYS, sizeof(FILTERKEYS), &g_StartupFilterKeys, 0);
 
    // Disable when full screen
    AllowAccessibilityShortcutKeys( true );
 
    // Restore back when going to windowed or shutting down
    AllowAccessibilityShortcutKeys( false );
}
 
 
void AllowAccessibilityShortcutKeys( bool bAllowKeys )
{
    if( bAllowKeys )
    {
        // Restore StickyKeys/etc to original state and enable Windows key      
        STICKYKEYS sk = g_StartupStickyKeys;
        TOGGLEKEYS tk = g_StartupToggleKeys;
        FILTERKEYS fk = g_StartupFilterKeys;
        
        SystemParametersInfo(SPI_SETSTICKYKEYS, sizeof(STICKYKEYS), &g_StartupStickyKeys, 0);
        SystemParametersInfo(SPI_SETTOGGLEKEYS, sizeof(TOGGLEKEYS), &g_StartupToggleKeys, 0);
        SystemParametersInfo(SPI_SETFILTERKEYS, sizeof(FILTERKEYS), &g_StartupFilterKeys, 0);
    }
    else
    {
        // Disable StickyKeys/etc shortcuts but if the accessibility feature is on, 
        // then leave the settings alone as its probably being usefully used
 
        STICKYKEYS skOff = g_StartupStickyKeys;
        if( (skOff.dwFlags & SKF_STICKYKEYSON) == 0 )
        {
            // Disable the hotkey and the confirmation
            skOff.dwFlags &= ~SKF_HOTKEYACTIVE;
            skOff.dwFlags &= ~SKF_CONFIRMHOTKEY;
 
            SystemParametersInfo(SPI_SETSTICKYKEYS, sizeof(STICKYKEYS), &skOff, 0);
        }
 
        TOGGLEKEYS tkOff = g_StartupToggleKeys;
        if( (tkOff.dwFlags & TKF_TOGGLEKEYSON) == 0 )
        {
            // Disable the hotkey and the confirmation
            tkOff.dwFlags &= ~TKF_HOTKEYACTIVE;
            tkOff.dwFlags &= ~TKF_CONFIRMHOTKEY;
 
            SystemParametersInfo(SPI_SETTOGGLEKEYS, sizeof(TOGGLEKEYS), &tkOff, 0);
        }
 
        FILTERKEYS fkOff = g_StartupFilterKeys;
        if( (fkOff.dwFlags & FKF_FILTERKEYSON) == 0 )
        {
            // Disable the hotkey and the confirmation
            fkOff.dwFlags &= ~FKF_HOTKEYACTIVE;
            fkOff.dwFlags &= ~FKF_CONFIRMHOTKEY;
 
            SystemParametersInfo(SPI_SETFILTERKEYS, sizeof(FILTERKEYS), &fkOff, 0);
        }
    }
}
```



 

 