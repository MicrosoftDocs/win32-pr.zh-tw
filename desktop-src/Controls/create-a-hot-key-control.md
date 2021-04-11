---
title: 如何建立快速鍵控制項
description: 本主題將示範如何建立快速鍵控制項。 您可以使用 CreateWindowEx 函式來建立快速鍵控制項，以指定快速鍵 \_ 類別視窗類別。
ms.assetid: A6723D4E-B8F6-4365-8FCD-99B73D2C0470
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 498005efcdfbbf001283551bbeea4906ebc854cf
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103842912"
---
# <a name="how-to-create-a-hot-key-control"></a><span data-ttu-id="a87fc-104">如何建立快速鍵控制項</span><span class="sxs-lookup"><span data-stu-id="a87fc-104">How to Create a Hot Key Control</span></span>

<span data-ttu-id="a87fc-105">本主題將示範如何建立快速鍵控制項。</span><span class="sxs-lookup"><span data-stu-id="a87fc-105">This topic demonstrates how to create a hot key control.</span></span> <span data-ttu-id="a87fc-106">您可以使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式來建立快速鍵控制項，以指定快速鍵 \_ 類別視窗類別。</span><span class="sxs-lookup"><span data-stu-id="a87fc-106">You create a hot key control by using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the HOTKEY\_CLASS window class.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="a87fc-107">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="a87fc-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="a87fc-108">技術</span><span class="sxs-lookup"><span data-stu-id="a87fc-108">Technologies</span></span>

-   [<span data-ttu-id="a87fc-109">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="a87fc-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="a87fc-110">必要條件</span><span class="sxs-lookup"><span data-stu-id="a87fc-110">Prerequisites</span></span>

-   <span data-ttu-id="a87fc-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="a87fc-111">C/C++</span></span>
-   <span data-ttu-id="a87fc-112">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="a87fc-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="a87fc-113">指示</span><span class="sxs-lookup"><span data-stu-id="a87fc-113">Instructions</span></span>


<span data-ttu-id="a87fc-114">建立快速鍵控制項之前，請確定已載入通用控制項 DLL。</span><span class="sxs-lookup"><span data-stu-id="a87fc-114">Before you create the hot key control, ensure that the common controls DLL is loaded.</span></span>

<span data-ttu-id="a87fc-115">在下列 c + + 程式碼範例中，應用程式定義函式會呼叫 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) 函式來載入通用控制項 DLL。</span><span class="sxs-lookup"><span data-stu-id="a87fc-115">In the following C++ code example, the application-defined function calls the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function to load the common control DLL.</span></span> <span data-ttu-id="a87fc-116">然後，它會呼叫 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式，並指定快速鍵 **\_ 類別** 視窗類別來建立快速鍵控制項。</span><span class="sxs-lookup"><span data-stu-id="a87fc-116">Then it calls the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the **HOTKEY\_CLASS** window class, to create a hot key control.</span></span> <span data-ttu-id="a87fc-117">它會使用 [**HKM \_ SETRULES**](hkm-setrules.md) 和 [**HKM \_ SETHOTKEY**](hkm-sethotkey.md) 訊息來初始化控制項，並將控制碼傳回給控制項。</span><span class="sxs-lookup"><span data-stu-id="a87fc-117">It uses the [**HKM\_SETRULES**](hkm-setrules.md) and [**HKM\_SETHOTKEY**](hkm-sethotkey.md) messages to initialize the control and returns a handle to the control.</span></span>

<span data-ttu-id="a87fc-118">此熱鍵控制項不允許使用者選擇以單一未修改的金鑰為依據的熱鍵，也不允許使用者只選擇 SHIFT 和 key。</span><span class="sxs-lookup"><span data-stu-id="a87fc-118">This hot key control does not allow the user to choose a hot key that is a single unmodified key, nor does it permit the user to choose only SHIFT and a key.</span></span> <span data-ttu-id="a87fc-119">這些規則可有效地防止使用者選擇在輸入文字時可能會不小心輸入的快速鍵。</span><span class="sxs-lookup"><span data-stu-id="a87fc-119">These rules effectively prevent the user from choosing a hot key that might be entered accidentally while typing text.</span></span>



```C++
// Creates a hot key control and sets rules and default settings for it.
// 
// Returns the handle of the hot key control. 
//
// Parameter
//     hwndDlg - Handle of the parent window (dialog box). 
// 
// Global variable 
//     g_hinst - Handle of the application instance. 

extern HINSTANCE g_hinst; 

HWND WINAPI InitializeHotkey(HWND hwndDlg) 
{ 
    HWND hwndHot = NULL;
    
    // Ensure that the common control DLL is loaded. 
    INITCOMMONCONTROLSEX icex;  //declare an INITCOMMONCONTROLSEX Structure
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC = ICC_HOTKEY_CLASS;   //set dwICC member to ICC_HOTKEY_CLASS    
                                     // this loads the Hot Key control class.
    InitCommonControlsEx(&icex);  
 
    hwndHot = CreateWindowEx(0,                        // no extended styles 
                             HOTKEY_CLASS,             // class name 
                             TEXT(""),                 // no title (caption) 
                             WS_CHILD | WS_VISIBLE,    // style 
                             15, 10,                   // position 
                             200, 20,                  // size 
                             hwndDlg,                  // parent window 
                             NULL,                     // uses class menu 
                             g_hinst,                  // instance 
                             NULL);                    // no WM_CREATE parameter 
 
    SetFocus(hwndHot); 
 
    // Set rules for invalid key combinations. If the user does not supply a
    // modifier key, use ALT as a modifier. If the user supplies SHIFT as a 
    // modifier key, use SHIFT + ALT instead.
    SendMessage(hwndHot, 
                HKM_SETRULES, 
                (WPARAM) HKCOMB_NONE | HKCOMB_S,   // invalid key combinations 
                MAKELPARAM(HOTKEYF_ALT, 0));       // add ALT to invalid entries 
 
    // Set CTRL + ALT + A as the default hot key for this window. 
    // 0x41 is the virtual key code for 'A'. 
    SendMessage(hwndHot, 
                HKM_SETHOTKEY, 
                MAKEWORD(0x41, HOTKEYF_CONTROL | HOTKEYF_ALT), 
                0); 
 
    return hwndHot; 
}
```



## <a name="related-topics"></a><span data-ttu-id="a87fc-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="a87fc-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a87fc-121">快速鍵控制參考</span><span class="sxs-lookup"><span data-stu-id="a87fc-121">Hot Key Control Reference</span></span>](bumper-hot-key-hot-key-control-reference.md)
</dt> <dt>

[<span data-ttu-id="a87fc-122">關於快速鍵控制項</span><span class="sxs-lookup"><span data-stu-id="a87fc-122">About Hot Key Controls</span></span>](hot-key-controls.md)
</dt> <dt>

[<span data-ttu-id="a87fc-123">使用快速鍵控制項</span><span class="sxs-lookup"><span data-stu-id="a87fc-123">Using Hot Key Controls</span></span>](using-hot-key-controls.md)
</dt> </dl>

 

 