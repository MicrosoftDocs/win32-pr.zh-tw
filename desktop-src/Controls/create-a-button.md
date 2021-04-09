---
title: 如何建立按鈕
description: 若要動態建立按鈕，請使用 CreateWindow 或 CreateWindowEx 函數。 本主題將示範如何使用 CreateWindow 函式來建立預設的推播按鈕。
ms.assetid: A8C56D09-90A3-4C70-9907-61390521D1DA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dadc53f91f773e5fce9e29bdf1ae50cc59bfdfd
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104024356"
---
# <a name="how-to-create-a-button"></a><span data-ttu-id="ba338-104">如何建立按鈕</span><span class="sxs-lookup"><span data-stu-id="ba338-104">How to Create a Button</span></span>

<span data-ttu-id="ba338-105">若要動態建立按鈕，請使用 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) 或 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函數。</span><span class="sxs-lookup"><span data-stu-id="ba338-105">To create buttons dynamically, you use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="ba338-106">本主題將示範如何使用 **CreateWindow** 函式來建立預設的推播按鈕。</span><span class="sxs-lookup"><span data-stu-id="ba338-106">This topic demonstrates how to use the **CreateWindow** function to create a default push button.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="ba338-107">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="ba338-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="ba338-108">技術</span><span class="sxs-lookup"><span data-stu-id="ba338-108">Technologies</span></span>

-   [<span data-ttu-id="ba338-109">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="ba338-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="ba338-110">必要條件</span><span class="sxs-lookup"><span data-stu-id="ba338-110">Prerequisites</span></span>

-   <span data-ttu-id="ba338-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="ba338-111">C/C++</span></span>
-   <span data-ttu-id="ba338-112">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="ba338-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="ba338-113">指示</span><span class="sxs-lookup"><span data-stu-id="ba338-113">Instructions</span></span>


<span data-ttu-id="ba338-114">使用 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) 函數來建立按鈕控制項。</span><span class="sxs-lookup"><span data-stu-id="ba338-114">Use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) function to create a button control.</span></span>

<span data-ttu-id="ba338-115">在下列 c + + 範例中， *m \_ hwnd* 參數是父視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ba338-115">In the following C++ example, the *m\_hwnd* parameter is the handle to the parent window.</span></span> <span data-ttu-id="ba338-116">[**BS \_ DEFPUSHBUTTON**](button-styles.md)樣式指定應該建立預設的 [推送] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="ba338-116">The [**BS\_DEFPUSHBUTTON**](button-styles.md) style specifies that a default push button should be created.</span></span> <span data-ttu-id="ba338-117">請注意，您必須指定大小和位置值，因為使用按鈕的 **CW \_ USEDEFAULT** 將值設為零。</span><span class="sxs-lookup"><span data-stu-id="ba338-117">Note that the size and position values must be specified because using **CW\_USEDEFAULT** for a button sets the values to zero.</span></span>


```C++
HWND hwndButton = CreateWindow( 
    L"BUTTON",  // Predefined class; Unicode assumed 
    L"OK",      // Button text 
    WS_TABSTOP | WS_VISIBLE | WS_CHILD | BS_DEFPUSHBUTTON,  // Styles 
    10,         // x position 
    10,         // y position 
    100,        // Button width
    100,        // Button height
    m_hwnd,     // Parent window
    NULL,       // No menu.
    (HINSTANCE)GetWindowLongPtr(m_hwnd, GWLP_HINSTANCE), 
    NULL);      // Pointer not needed.
```



## <a name="related-topics"></a><span data-ttu-id="ba338-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="ba338-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba338-119">關於按鈕</span><span class="sxs-lookup"><span data-stu-id="ba338-119">About Buttons</span></span>](about-buttons.md)
</dt> <dt>

[<span data-ttu-id="ba338-120">按鈕控制項參考</span><span class="sxs-lookup"><span data-stu-id="ba338-120">Button Control Reference</span></span>](bumper-button-button-control-reference.md)
</dt> <dt>

[<span data-ttu-id="ba338-121">使用按鈕</span><span class="sxs-lookup"><span data-stu-id="ba338-121">Using Buttons</span></span>](using-buttons.md)
</dt> <dt>

[<span data-ttu-id="ba338-122">按鈕</span><span class="sxs-lookup"><span data-stu-id="ba338-122">Button</span></span>](buttons.md)
</dt> </dl>

 

 