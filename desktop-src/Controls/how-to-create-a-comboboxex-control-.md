---
title: 如何建立 ComboBoxEx 控制項
description: 本主題將示範如何建立 ComboBoxEx 控制項。
ms.assetid: E3D577AF-3290-431E-AA6C-1E9A9ED6448C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73989124982cb563fc008d7f3c543388cca685a5
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103933756"
---
# <a name="how-to-create-a-comboboxex-control"></a><span data-ttu-id="7872b-103">如何建立 ComboBoxEx 控制項</span><span class="sxs-lookup"><span data-stu-id="7872b-103">How to Create a ComboBoxEx Control</span></span>

<span data-ttu-id="7872b-104">本主題將示範如何建立 ComboBoxEx 控制項。</span><span class="sxs-lookup"><span data-stu-id="7872b-104">This topic demonstrates how to create a ComboBoxEx control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="7872b-105">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="7872b-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="7872b-106">技術</span><span class="sxs-lookup"><span data-stu-id="7872b-106">Technologies</span></span>

-   [<span data-ttu-id="7872b-107">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="7872b-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="7872b-108">必要條件</span><span class="sxs-lookup"><span data-stu-id="7872b-108">Prerequisites</span></span>

-   <span data-ttu-id="7872b-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="7872b-109">C/C++</span></span>
-   <span data-ttu-id="7872b-110">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="7872b-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="7872b-111">指示</span><span class="sxs-lookup"><span data-stu-id="7872b-111">Instructions</span></span>


<span data-ttu-id="7872b-112">若要建立 ComboBoxEx 控制項，請呼叫 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式，並使用 [**WC \_ ComboBoxEx**](common-control-window-classes.md) 做為視窗類別。</span><span class="sxs-lookup"><span data-stu-id="7872b-112">To create a ComboBoxEx control, call the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, using [**WC\_COMBOBOXEX**](common-control-window-classes.md) as the window class.</span></span> <span data-ttu-id="7872b-113">您必須先呼叫 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) 函式來註冊視窗類別，並 \_ \_ 在伴隨的 [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) 結構中指定 ICC USEREX 類別位。</span><span class="sxs-lookup"><span data-stu-id="7872b-113">You must first register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function, while specifying the ICC\_USEREX\_CLASSES bit in the accompanying [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>

## <a name="complete-example"></a><span data-ttu-id="7872b-114">完整範例</span><span class="sxs-lookup"><span data-stu-id="7872b-114">Complete example</span></span>

<span data-ttu-id="7872b-115">下列應用程式定義函式會使用主視窗中的 [**CBS \_ 下拉式**](combo-box-styles.md) 樣式來建立 ComboBoxEx 控制項。</span><span class="sxs-lookup"><span data-stu-id="7872b-115">The following application-defined function creates a ComboBoxEx control with the [**CBS\_DROPDOWN**](combo-box-styles.md) style in the main window.</span></span>


```C++
// CreateComboEx - Registers the ComboBoxEx window class and creates
// a ComboBoxEx control in the client area of the main window.
//
// g_hwndMain - A handle to the main window.
// g_hinst    - A handle to the program instance.
HWND WINAPI CreateComboEx(void)
{
    HWND hwnd;
    INITCOMMONCONTROLSEX icex;

    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC = ICC_USEREX_CLASSES;

    InitCommonControlsEx(&icex);

    hwnd = CreateWindowEx(0, WC_COMBOBOXEX, NULL,
                    WS_BORDER | WS_VISIBLE |
                    WS_CHILD | CBS_DROPDOWN,
                    // No size yet--resize after setting image list.
                    0,      // Vertical position of Combobox
                    0,      // Horizontal position of Combobox
                    0,      // Sets the width of Combobox
                    100,    // Sets the height of Combobox
                    g_hwndMain,
                    NULL,
                    g_hinst,
                    NULL);

    return (hwnd);
}
```



## <a name="related-topics"></a><span data-ttu-id="7872b-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="7872b-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7872b-117">關於 ComboBoxEx 控制項</span><span class="sxs-lookup"><span data-stu-id="7872b-117">About ComboBoxEx Controls</span></span>](comboboxex-controls.md)
</dt> <dt>

[<span data-ttu-id="7872b-118">ComboBoxEx 控制項參考</span><span class="sxs-lookup"><span data-stu-id="7872b-118">ComboBoxEx Control Reference</span></span>](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[<span data-ttu-id="7872b-119">使用 ComboBoxEx 控制項</span><span class="sxs-lookup"><span data-stu-id="7872b-119">Using ComboBoxEx Controls</span></span>](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[<span data-ttu-id="7872b-120">ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="7872b-120">ComboBoxEx</span></span>](comboboxex-control-reference.md)
</dt> </dl>

 

 