---
title: 如何建立動畫控制項
description: 本主題將示範如何建立動畫控制項。
ms.assetid: 5852B636-F3D0-47A4-82F6-8BE570013E1B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4ff190617996e42e6580b82311fb51f4248000
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021070"
---
# <a name="how-to-create-an-animation-control"></a><span data-ttu-id="36c5b-103">如何建立動畫控制項</span><span class="sxs-lookup"><span data-stu-id="36c5b-103">How to Create an Animation Control</span></span>

<span data-ttu-id="36c5b-104">本主題將示範如何建立動畫控制項。</span><span class="sxs-lookup"><span data-stu-id="36c5b-104">This topic demonstrates how to create an animation control.</span></span> <span data-ttu-id="36c5b-105">隨附的 c + + 程式碼範例會在對話方塊中建立動畫控制項。</span><span class="sxs-lookup"><span data-stu-id="36c5b-105">The accompanying C++ code example creates an animation control in a dialog box.</span></span> <span data-ttu-id="36c5b-106">它會將動畫控制項放在指定的控制項底下，並根據 Audio-Video 交錯 (AVI) 剪輯中的框架維度來設定動畫控制項的尺寸。</span><span class="sxs-lookup"><span data-stu-id="36c5b-106">It positions the animation control below a specified control, and sets the dimensions of the animation control based on the dimensions of a frame in the Audio-Video Interleaved (AVI) clip.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="36c5b-107">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="36c5b-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="36c5b-108">技術</span><span class="sxs-lookup"><span data-stu-id="36c5b-108">Technologies</span></span>

-   [<span data-ttu-id="36c5b-109">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="36c5b-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="36c5b-110">必要條件</span><span class="sxs-lookup"><span data-stu-id="36c5b-110">Prerequisites</span></span>

-   <span data-ttu-id="36c5b-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="36c5b-111">C/C++</span></span>
-   <span data-ttu-id="36c5b-112">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="36c5b-112">Windows User Interface Programming</span></span>
-   <span data-ttu-id="36c5b-113">AVI 檔案</span><span class="sxs-lookup"><span data-stu-id="36c5b-113">AVI files</span></span>

## <a name="instructions"></a><span data-ttu-id="36c5b-114">指示</span><span class="sxs-lookup"><span data-stu-id="36c5b-114">Instructions</span></span>

### <a name="step-1-create-an-instance-of-the-animation-control"></a><span data-ttu-id="36c5b-115">步驟1：建立動畫控制項的實例。</span><span class="sxs-lookup"><span data-stu-id="36c5b-115">Step 1: Create an instance of the animation control.</span></span>

<span data-ttu-id="36c5b-116">使用「 [**\_ 建立**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) 動畫」宏建立動畫控制項的實例。</span><span class="sxs-lookup"><span data-stu-id="36c5b-116">Use the [**Animate\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) macro to create an instance of the animation control.</span></span>


```C++
// IDC_ANIMATE - identifier of the animation control. 
// hwndDlg - handle to the dialog box.
RECT rc;
hwndAnim = Animate_Create(hwndDlg, IDC_ANIMATE, 
    WS_BORDER | WS_CHILD, g_hinst); 
```



### <a name="step-2-position-the-animation-control"></a><span data-ttu-id="36c5b-117">步驟2：放置動畫控制項。</span><span class="sxs-lookup"><span data-stu-id="36c5b-117">Step 2: Position the animation control.</span></span>

<span data-ttu-id="36c5b-118">取得指定控制項按鈕的螢幕座標。</span><span class="sxs-lookup"><span data-stu-id="36c5b-118">Get the screen coordinates of the specified control button.</span></span>


```C++
// nIDCtl - identifier of the control below which the animation control is to be positioned.
GetWindowRect(GetDlgItem(hwndDlg, nIDCtl), &rc); 
```



<span data-ttu-id="36c5b-119">將左下角的座標轉換為工作區座標。</span><span class="sxs-lookup"><span data-stu-id="36c5b-119">Convert the coordinates of the lower-left corner to client coordinates.</span></span>


```C++
POINT pt;
pt.x = rc.left; 
pt.y = rc.bottom; 
ScreenToClient(hwndDlg, &pt); 
```



<span data-ttu-id="36c5b-120">將動畫控制項放在指定的控制項按鈕下方。</span><span class="sxs-lookup"><span data-stu-id="36c5b-120">Position the animation control below the specified control button.</span></span>


```C++
// CX_FRAME, CY_FRAME - width and height of the frames in the AVI clip.      
SetWindowPos(hwndAnim, 0, pt.x, pt.y + 20, 
    CX_FRAME, CY_FRAME, 
    SWP_NOZORDER | SWP_DRAWFRAME);
```



### <a name="step-3-open-the-avi-clip"></a><span data-ttu-id="36c5b-121">步驟3：開啟 AVI 剪輯。</span><span class="sxs-lookup"><span data-stu-id="36c5b-121">Step 3: Open the AVI clip.</span></span>

<span data-ttu-id="36c5b-122">呼叫 [**動畫 \_ 開啟**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) 宏以開啟 AVI 剪輯，並顯示動畫控制項中的第一個畫面格。</span><span class="sxs-lookup"><span data-stu-id="36c5b-122">Call the [**Animate\_Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) macro to open the AVI clip and display the first frame in the animation control.</span></span> <span data-ttu-id="36c5b-123">呼叫 **ShowWindow** 函式，讓動畫控制項可見。</span><span class="sxs-lookup"><span data-stu-id="36c5b-123">Call the **ShowWindow** function to make the animation control visible.</span></span>


```C++
Animate_Open(hwndAnim, "SEARCH.AVI"); 
ShowWindow(hwndAnim, SW_SHOW); 
```



## <a name="complete-example"></a><span data-ttu-id="36c5b-124">完整範例</span><span class="sxs-lookup"><span data-stu-id="36c5b-124">Complete example</span></span>


```C++
// CreateAnimationCtrl - creates an animation control, positions it 
//                       below the specified control in a dialog box, 
//                       and opens the AVI clip for the animation control. 
// Returns the handle to the animation control. 
// hwndDlg             - handle to the dialog box. 
// nIDCtl              - identifier of the control below which the animation control 
//                       is to be positioned. 
// 
// Constants 
//     IDC_ANIMATE - identifier of the animation control. 
//     CX_FRAME, CY_FRAME - width and height of the frames 
//     in the AVI clip. 

HWND CreateAnimationCtrl(HWND hwndDlg, int nIDCtl) 
{ 
    HWND hwndAnim = NULL;    
    
    // Create the animation control.
    // IDC_ANIMATE - identifier of the animation control. 
    // hwndDlg - handle to the dialog box.
    RECT rc;
    hwndAnim = Animate_Create(hwndDlg, IDC_ANIMATE, 
        WS_BORDER | WS_CHILD, g_hinst); 

    // Get the screen coordinates of the specified control button.
    // nIDCtl - identifier of the control below which the animation control is to be positioned.
    GetWindowRect(GetDlgItem(hwndDlg, nIDCtl), &rc); 

    // Convert the coordinates of the lower-left corner to 
    // client coordinates.
    POINT pt;
    pt.x = rc.left; 
    pt.y = rc.bottom; 
    ScreenToClient(hwndDlg, &pt); 

    // Position the animation control below the Stop button.
    // CX_FRAME, CY_FRAME - width and height of the frames in the AVI clip.      
    SetWindowPos(hwndAnim, 0, pt.x, pt.y + 20, 
        CX_FRAME, CY_FRAME, 
        SWP_NOZORDER | SWP_DRAWFRAME);

    // Open the AVI clip, and show the animation control.
    Animate_Open(hwndAnim, "SEARCH.AVI"); 
    ShowWindow(hwndAnim, SW_SHOW); 

    return hwndAnim; 
} 
```



## <a name="related-topics"></a><span data-ttu-id="36c5b-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="36c5b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36c5b-126">關於動畫控制項</span><span class="sxs-lookup"><span data-stu-id="36c5b-126">About Animation Controls</span></span>](animation-control-overview.md)
</dt> <dt>

[<span data-ttu-id="36c5b-127">動畫控制項參考</span><span class="sxs-lookup"><span data-stu-id="36c5b-127">Animation Control Reference</span></span>](bumper-animation-animation-control-reference.md)
</dt> <dt>

[<span data-ttu-id="36c5b-128">使用動畫控制項</span><span class="sxs-lookup"><span data-stu-id="36c5b-128">Using Animation Controls</span></span>](using-animation-control.md)
</dt> <dt>

[<span data-ttu-id="36c5b-129">動畫</span><span class="sxs-lookup"><span data-stu-id="36c5b-129">Animation</span></span>](animation-control-reference.md)
</dt> </dl>

 

 




