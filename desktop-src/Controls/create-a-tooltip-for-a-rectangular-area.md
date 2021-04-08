---
title: 如何建立矩形區域的工具提示
description: 下列範例示範如何建立視窗整個工作區的標準工具提示控制項。
ms.assetid: 6AF1CE6E-AD63-4F84-9759-14FE4F16092B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f8daf62bf2ba85c8750fd07a1b9122b0360fc11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671968"
---
# <a name="how-to-create-a-tooltip-for-a-rectangular-area"></a><span data-ttu-id="e8130-103">如何建立矩形區域的工具提示</span><span class="sxs-lookup"><span data-stu-id="e8130-103">How to Create a Tooltip for a Rectangular Area</span></span>

<span data-ttu-id="e8130-104">下列範例示範如何建立視窗整個工作區的標準工具提示控制項。</span><span class="sxs-lookup"><span data-stu-id="e8130-104">The following example demonstrates how to create a standard tooltip control for a window's entire client area.</span></span>

<span data-ttu-id="e8130-105">下圖顯示當滑鼠指標位於對話方塊的用戶端視窗內時，所顯示的工具提示。</span><span class="sxs-lookup"><span data-stu-id="e8130-105">The following illustration shows the tooltip that is displayed when the mouse pointer is within the client window of a dialog box.</span></span> <span data-ttu-id="e8130-106">對話方塊的控制碼已傳遞至上述範例中所示的函式。</span><span class="sxs-lookup"><span data-stu-id="e8130-106">The handle of the dialog box was passed to the function shown in the preceding example.</span></span>

![對話方塊的螢幕擷取畫面;滑鼠指標位於用戶端視窗內，並顯示工具提示](images/tt-rectangle.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="e8130-108">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="e8130-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="e8130-109">技術</span><span class="sxs-lookup"><span data-stu-id="e8130-109">Technologies</span></span>

-   [<span data-ttu-id="e8130-110">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="e8130-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="e8130-111">必要條件</span><span class="sxs-lookup"><span data-stu-id="e8130-111">Prerequisites</span></span>

-   <span data-ttu-id="e8130-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="e8130-112">C/C++</span></span>
-   <span data-ttu-id="e8130-113">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="e8130-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="e8130-114">指示</span><span class="sxs-lookup"><span data-stu-id="e8130-114">Instructions</span></span>

### <a name="create-a-tooltip-for-a-rectangular-area"></a><span data-ttu-id="e8130-115">建立矩形區域的工具提示</span><span class="sxs-lookup"><span data-stu-id="e8130-115">Create a Tooltip for a Rectangular Area</span></span>

<span data-ttu-id="e8130-116">下列範例示範如何建立視窗整個工作區的標準工具提示控制項。</span><span class="sxs-lookup"><span data-stu-id="e8130-116">The following example demonstrates how to create a standard tooltip control for a window's entire client area.</span></span>


```C++
void CreateToolTipForRect(HWND hwndParent)
{
    // Create a tooltip.
    HWND hwndTT = CreateWindowEx(WS_EX_TOPMOST, TOOLTIPS_CLASS, NULL, 
                                 WS_POPUP | TTS_NOPREFIX | TTS_ALWAYSTIP, 
                                 CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, 
                                 hwndParent, NULL, g_hInst,NULL);

    SetWindowPos(hwndTT, HWND_TOPMOST, 0, 0, 0, 0, 
                 SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE);

    // Set up "tool" information. In this case, the "tool" is the entire parent window.
    
    TOOLINFO ti = { 0 };
    ti.cbSize   = sizeof(TOOLINFO);
    ti.uFlags   = TTF_SUBCLASS;
    ti.hwnd     = hwndParent;
    ti.hinst    = g_hInst;
    ti.lpszText = TEXT("This is your tooltip string.");;
    
    GetClientRect (hwndParent, &ti.rect);

    // Associate the tooltip with the "tool" window.
    SendMessage(hwndTT, TTM_ADDTOOL, 0, (LPARAM) (LPTOOLINFO) &ti); 
} 
```



## <a name="related-topics"></a><span data-ttu-id="e8130-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="e8130-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8130-118">使用工具提示控制項</span><span class="sxs-lookup"><span data-stu-id="e8130-118">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 




