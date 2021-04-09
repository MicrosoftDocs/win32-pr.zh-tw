---
title: 如何建立標準捲軸的鍵盤介面
description: 雖然捲軸控制項提供內建的鍵盤介面，但標準捲軸不是。
ms.assetid: 249D0077-6E61-479A-91D5-A4BD9752B82E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b739638d95d9f3e530718f8e9b9e6168069420
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842776"
---
# <a name="how-to-create-a-keyboard-interface-for-standard-scroll-bars"></a><span data-ttu-id="bc1b4-103">如何建立標準捲軸的鍵盤介面</span><span class="sxs-lookup"><span data-stu-id="bc1b4-103">How to Create a Keyboard Interface for Standard Scroll Bars</span></span>

<span data-ttu-id="bc1b4-104">雖然捲軸控制項提供內建的鍵盤介面，但標準捲軸不是。</span><span class="sxs-lookup"><span data-stu-id="bc1b4-104">Although a scroll bar control provides a built-in keyboard interface, a standard scroll bar does not.</span></span> <span data-ttu-id="bc1b4-105">若要執行標準捲軸的鍵盤介面，視窗程式必須處理 [**WM 的 \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) 訊息，並檢查 *wParam* 參數所指定的虛擬機器碼程式碼。</span><span class="sxs-lookup"><span data-stu-id="bc1b4-105">To implement a keyboard interface for a standard scroll bar, a window procedure must process the [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message and examine the virtual-key code specified by the *wParam* parameter.</span></span> <span data-ttu-id="bc1b4-106">如果虛擬按鍵程式碼對應到箭號鍵，則視窗程式會將一組 [**wm \_ HSCROLL**](wm-hscroll.md) 或 [**wm \_ VSCROLL**](wm-vscroll.md) 訊息傳送給自己，並將 *wParam* 參數的低序位字組設定為適當的捲軸要求碼。</span><span class="sxs-lookup"><span data-stu-id="bc1b4-106">If the virtual-key code corresponds to an arrow key, the window procedure sends itself a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message with the low-order word of the *wParam* parameter set to the appropriate scroll bar request code.</span></span>

<span data-ttu-id="bc1b4-107">例如，當使用者按下向上鍵時，視窗程式會收到 *wParam* 等於 VK UP 的 [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)訊息 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bc1b4-107">For example, when the user presses the UP arrow key, the window procedure receives a [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message with *wParam* equal to VK\_UP.</span></span> <span data-ttu-id="bc1b4-108">在回應中，視窗程式會將具有低序位單字 *wParam* 的一 [**\_ VSCROLL**](wm-vscroll.md)訊息傳送給自己，並將設定為 SB 的 \_ 要求碼。</span><span class="sxs-lookup"><span data-stu-id="bc1b4-108">In response, the window procedure sends itself a [**WM\_VSCROLL**](wm-vscroll.md) message with the low-order word of *wParam* set to the SB\_LINEUP request code.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="bc1b4-109">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="bc1b4-109">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="bc1b4-110">技術</span><span class="sxs-lookup"><span data-stu-id="bc1b4-110">Technologies</span></span>

-   [<span data-ttu-id="bc1b4-111">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="bc1b4-111">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="bc1b4-112">必要條件</span><span class="sxs-lookup"><span data-stu-id="bc1b4-112">Prerequisites</span></span>

-   <span data-ttu-id="bc1b4-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="bc1b4-113">C/C++</span></span>
-   <span data-ttu-id="bc1b4-114">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="bc1b4-114">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="bc1b4-115">指示</span><span class="sxs-lookup"><span data-stu-id="bc1b4-115">Instructions</span></span>

### <a name="create-a-keyboard-interface-for-a-standard-scroll-bar"></a><span data-ttu-id="bc1b4-116">建立標準捲軸的鍵盤介面</span><span class="sxs-lookup"><span data-stu-id="bc1b4-116">Create a Keyboard Interface for a Standard Scroll Bar</span></span>

<span data-ttu-id="bc1b4-117">下列程式碼範例示範如何包含標準捲軸的鍵盤介面。</span><span class="sxs-lookup"><span data-stu-id="bc1b4-117">The following code example demonstrates how to include a keyboard interface for a standard scroll bar.</span></span>


```C++
    case WM_KEYDOWN: 
    {
        WORD wScrollNotify = 0xFFFF;

        switch (wParam) 
        { 
            case VK_UP: 
                wScrollNotify = SB_LINEUP; 
                break; 
 
            case VK_PRIOR: 
                wScrollNotify = SB_PAGEUP; 
                break; 
 
            case VK_NEXT: 
                wScrollNotify = SB_PAGEDOWN; 
                break; 
 
            case VK_DOWN: 
                wScrollNotify = SB_LINEDOWN; 
                break; 
 
            case VK_HOME: 
                wScrollNotify = SB_TOP; 
                break; 
 
            case VK_END: 
                wScrollNotify = SB_BOTTOM; 
                break; 
        } 
 
        if (wScrollNotify != -1) 
            SendMessage(hwnd, WM_VSCROLL, MAKELONG(wScrollNotify, 0), 0L); 
 
        break; 
    }
```



## <a name="related-topics"></a><span data-ttu-id="bc1b4-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="bc1b4-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc1b4-119">使用捲軸</span><span class="sxs-lookup"><span data-stu-id="bc1b4-119">Using Scroll Bars</span></span>](using-scroll-bars.md)
</dt> <dt>

<span data-ttu-id="bc1b4-120">[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="bc1b4-120">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 