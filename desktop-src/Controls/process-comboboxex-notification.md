---
title: 如何處理 ComboBoxEx 通知
description: 本主題將示範如何處理 ComboBoxEx 通知訊息。
ms.assetid: 375634BC-CDD6-4D72-A41E-FCBFCBFE7F03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a9787e22aa01d51478ca55f0dde5d7ac944decb
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103933760"
---
# <a name="how-to-process-comboboxex-notifications"></a><span data-ttu-id="a8341-103">如何處理 ComboBoxEx 通知</span><span class="sxs-lookup"><span data-stu-id="a8341-103">How to Process ComboBoxEx Notifications</span></span>

<span data-ttu-id="a8341-104">本主題將示範如何處理 ComboBoxEx 通知訊息。</span><span class="sxs-lookup"><span data-stu-id="a8341-104">This topic demonstrates how to process ComboBoxEx notification messages.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="a8341-105">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="a8341-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="a8341-106">技術</span><span class="sxs-lookup"><span data-stu-id="a8341-106">Technologies</span></span>

-   [<span data-ttu-id="a8341-107">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="a8341-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="a8341-108">必要條件</span><span class="sxs-lookup"><span data-stu-id="a8341-108">Prerequisites</span></span>

-   <span data-ttu-id="a8341-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="a8341-109">C/C++</span></span>
-   <span data-ttu-id="a8341-110">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="a8341-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="a8341-111">指示</span><span class="sxs-lookup"><span data-stu-id="a8341-111">Instructions</span></span>


<span data-ttu-id="a8341-112">ComboBoxEx 控制項藉由傳送 [**WM \_ 通知**](wm-notify.md) 訊息，來通知其父視窗的事件。</span><span class="sxs-lookup"><span data-stu-id="a8341-112">A ComboBoxEx control notifies its parent window of events by sending [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="a8341-113">它也會將它從它所包含的下拉式方塊接收的 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 通知訊息，傳遞給要處理的父視窗。</span><span class="sxs-lookup"><span data-stu-id="a8341-113">It also passes the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) notification messages that it receives from the combo box contained within it to the parent window to be processed.</span></span> <span data-ttu-id="a8341-114">因此，您的應用程式必須準備好處理從 ComboBoxEx 子下拉式方塊控制項轉送的 ComboBoxEx 和 **wm \_ 命令** 訊息中的 **wm \_ 通知** 訊息。</span><span class="sxs-lookup"><span data-stu-id="a8341-114">Therefore, your application must be prepared to process **WM\_NOTIFY** messages from the ComboBoxEx and **WM\_COMMAND** messages that are forwarded from the ComboBoxEx child combo box control.</span></span>

<span data-ttu-id="a8341-115">本節中的範例會呼叫對應的應用程式定義函數來處理這些訊息，以處理來自 ComboBoxEx 控制項的 [**wm \_ 通知**](wm-notify.md) 和 [**wm \_ 命令**](/windows/desktop/menurc/wm-command) 訊息。</span><span class="sxs-lookup"><span data-stu-id="a8341-115">The example in this section handles the [**WM\_NOTIFY**](wm-notify.md) and [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages from a ComboBoxEx control by calling a corresponding application-defined function to process these messages.</span></span>

## <a name="complete-example"></a><span data-ttu-id="a8341-116">完整範例</span><span class="sxs-lookup"><span data-stu-id="a8341-116">Complete example</span></span>


```C++
LRESULT CALLBACK WndProc (HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam)
{
    switch(msg){

        case WM_COMMAND: // notification from the child ComboBox within the ComboBoxEx control.
            if((HWND)lParam == g_hwndCB)
                DoOldNotify(hwnd,  wParam);  
            break;

        case WM_NOTIFY: // notification from the ComboBoxEx control
            return (DoCBEXNotify(hwnd, lParam));

        case WM_PAINT:
            hdc = BeginPaint(hwnd, &ps);
            EndPaint(hwnd, &ps);
            break;

        case WM_DESTROY:
            PostQuitMessage(0);
            break;

        default:
            return DefWindowProc(hwnd, msg, wParam, lParam);
            break;
    }

    return FALSE;
}
```



## <a name="related-topics"></a><span data-ttu-id="a8341-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="a8341-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8341-118">關於 ComboBoxEx 控制項</span><span class="sxs-lookup"><span data-stu-id="a8341-118">About ComboBoxEx Controls</span></span>](comboboxex-controls.md)
</dt> <dt>

[<span data-ttu-id="a8341-119">ComboBoxEx 控制項參考</span><span class="sxs-lookup"><span data-stu-id="a8341-119">ComboBoxEx Control Reference</span></span>](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[<span data-ttu-id="a8341-120">使用 ComboBoxEx 控制項</span><span class="sxs-lookup"><span data-stu-id="a8341-120">Using ComboBoxEx Controls</span></span>](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[<span data-ttu-id="a8341-121">ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="a8341-121">ComboBoxEx</span></span>](comboboxex-control-reference.md)
</dt> </dl>

 

 