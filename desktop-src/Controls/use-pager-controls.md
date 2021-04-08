---
title: 如何使用呼機控制項
description: 本節說明如何在您的應用程式中執行呼機控制項。
ms.assetid: 5703FE4B-987E-49DA-9741-F8B45AD26467
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586bfff0c8d8097c4b0e861506bb73f55467b711
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024176"
---
# <a name="how-to-use-pager-controls"></a><span data-ttu-id="e3163-103">如何使用呼機控制項</span><span class="sxs-lookup"><span data-stu-id="e3163-103">How to Use Pager Controls</span></span>

<span data-ttu-id="e3163-104">本節說明如何在您的應用程式中執行呼機控制項。</span><span class="sxs-lookup"><span data-stu-id="e3163-104">This section describes how to implement the pager control in your application.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="e3163-105">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="e3163-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="e3163-106">技術</span><span class="sxs-lookup"><span data-stu-id="e3163-106">Technologies</span></span>

-   [<span data-ttu-id="e3163-107">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="e3163-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="e3163-108">必要條件</span><span class="sxs-lookup"><span data-stu-id="e3163-108">Prerequisites</span></span>

-   <span data-ttu-id="e3163-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="e3163-109">C/C++</span></span>
-   <span data-ttu-id="e3163-110">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="e3163-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="e3163-111">指示</span><span class="sxs-lookup"><span data-stu-id="e3163-111">Instructions</span></span>

### <a name="initialize-a-pager-control"></a><span data-ttu-id="e3163-112">初始化呼機控制項</span><span class="sxs-lookup"><span data-stu-id="e3163-112">Initialize a Pager Control</span></span>

<span data-ttu-id="e3163-113">若要使用分頁控制項，您必須使用 [](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) \_ \_ [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex)結構的 **dwICC** 成員中設定的 ICC PAGESCROLLER 類別旗標來呼叫 InitCommonControlsEx 函式。</span><span class="sxs-lookup"><span data-stu-id="e3163-113">To use the pager control, you must call the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function with the ICC\_PAGESCROLLER\_CLASS flag set in the **dwICC** member of the [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>

### <a name="create-a-pager-control"></a><span data-ttu-id="e3163-114">建立呼機控制項</span><span class="sxs-lookup"><span data-stu-id="e3163-114">Create a Pager Control</span></span>

<span data-ttu-id="e3163-115">使用 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) 或 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) API 來建立呼機控制項。</span><span class="sxs-lookup"><span data-stu-id="e3163-115">Use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) API to create a pager control.</span></span> <span data-ttu-id="e3163-116">控制項的類別名稱是 [**WC \_ PAGESCROLLER**](common-control-window-classes.md)，定義于 Commctrl 中。</span><span class="sxs-lookup"><span data-stu-id="e3163-116">The class name for the control is [**WC\_PAGESCROLLER**](common-control-window-classes.md), which is defined in Commctrl.h.</span></span> <span data-ttu-id="e3163-117">[**Pg \_ HORZ**](pager-control-styles.md)樣式是用來建立水準呼機，而 pg 垂直樣式 [**\_**](pager-control-styles.md)則是用來建立垂直呼機。</span><span class="sxs-lookup"><span data-stu-id="e3163-117">The [**PGS\_HORZ**](pager-control-styles.md) style is used to create a horizontal pager, and the [**PGS\_VERT**](pager-control-styles.md) style is used to create a vertical pager.</span></span> <span data-ttu-id="e3163-118">因為這是子控制項，所以也應該使用 [**WS \_ 子**](/windows/desktop/winmsg/window-styles) 樣式。</span><span class="sxs-lookup"><span data-stu-id="e3163-118">Because this is a child control, the [**WS\_CHILD**](/windows/desktop/winmsg/window-styles) style should also be used.</span></span>

<span data-ttu-id="e3163-119">建立了呼機控制項之後，您很可能會想要指派內含的視窗給它。</span><span class="sxs-lookup"><span data-stu-id="e3163-119">After the pager control is created, you will most likely want to assign a contained window to it.</span></span> <span data-ttu-id="e3163-120">如果包含的視窗是子視窗，您應該將子視窗設為分頁控制項的子系，以便正確地計算大小和位置。</span><span class="sxs-lookup"><span data-stu-id="e3163-120">If the contained window is a child window, you should make the child window a child of the pager control so that the size and position will be calculated correctly.</span></span> <span data-ttu-id="e3163-121">然後，您可以使用 [**PGM \_ SETCHILD**](pgm-setchild.md) 訊息，將視窗指派給呼機控制項。</span><span class="sxs-lookup"><span data-stu-id="e3163-121">You then assign the window to the pager control with the [**PGM\_SETCHILD**](pgm-setchild.md) message.</span></span> <span data-ttu-id="e3163-122">請注意，此訊息並不會實際變更包含視窗的父視窗;它只會指派包含的視窗。</span><span class="sxs-lookup"><span data-stu-id="e3163-122">Be aware that this message does not actually change the parent window of the contained window; it simply assigns the contained window.</span></span> <span data-ttu-id="e3163-123">如果包含的視窗是其中一個通用控制項，它必須具有 [**CCS \_ NORESIZE**](common-control-styles.md) 樣式，以防止控制項嘗試將自己的大小調整為呼機控制項的大小。</span><span class="sxs-lookup"><span data-stu-id="e3163-123">If the contained window is one of the common controls, it must have the [**CCS\_NORESIZE**](common-control-styles.md) style to prevent the control from attempting to resize itself to the pager control's size.</span></span>

### <a name="process-pager-control-notifications"></a><span data-ttu-id="e3163-124">處理呼機控制項通知</span><span class="sxs-lookup"><span data-stu-id="e3163-124">Process Pager Control Notifications</span></span>

<span data-ttu-id="e3163-125">您至少必須處理 [PGN \_ CALCSIZE](pgn-calcsize.md) 通知。</span><span class="sxs-lookup"><span data-stu-id="e3163-125">At a minimum, it is necessary to process the [PGN\_CALCSIZE](pgn-calcsize.md) notification.</span></span> <span data-ttu-id="e3163-126">如果您未處理此通知，並輸入寬度或高度的值，則不會顯示分頁控制項中的滾動箭號。</span><span class="sxs-lookup"><span data-stu-id="e3163-126">If you do not process this notification and enter a value for the width or height, the scroll arrows in the pager control will not be displayed.</span></span> <span data-ttu-id="e3163-127">這是因為呼機控制項會使用 PGN CALCSIZE 通知中提供的寬度或高度 \_ ，判斷所包含視窗的「理想」大小。</span><span class="sxs-lookup"><span data-stu-id="e3163-127">This is because the pager control uses the width or height supplied in the PGN\_CALCSIZE notification to determine the "ideal" size of the contained window.</span></span>

<span data-ttu-id="e3163-128">下列範例示範如何處理 [PGN \_ CALCSIZE](pgn-calcsize.md) 通知案例。</span><span class="sxs-lookup"><span data-stu-id="e3163-128">The following example demonstrates how to process the [PGN\_CALCSIZE](pgn-calcsize.md) notification case.</span></span> <span data-ttu-id="e3163-129">在此範例中，包含的視窗是工具列控制項，包含未知大小的未知按鈕數目。</span><span class="sxs-lookup"><span data-stu-id="e3163-129">In this example, the contained window is a toolbar control that contains an unknown number of buttons at an unknown size.</span></span> <span data-ttu-id="e3163-130">此範例示範如何使用 [**TB \_ GETMAXSIZE**](tb-getmaxsize.md) 訊息來判斷工具列中所有專案的大小。</span><span class="sxs-lookup"><span data-stu-id="e3163-130">The example shows how to use the [**TB\_GETMAXSIZE**](tb-getmaxsize.md) message to determine the size of all of the items in the toolbar.</span></span> <span data-ttu-id="e3163-131">然後，此範例會將所有專案的寬度放入傳遞給通知之 [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize)結構的 **iWidth** 成員中。</span><span class="sxs-lookup"><span data-stu-id="e3163-131">The example then places the width of all of the items into the **iWidth** member of the [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) structure that is passed to the notification.</span></span>


```C++
case PGN_SCROLL:{

    LPNMPGSCROLL pScroll = (LPNMPGSCROLL)lParam;
 
    switch(pScroll->iDir){
     
        case PGF_SCROLLLEFT:
        case PGF_SCROLLRIGHT:
        case PGF_SCROLLUP:
        case PGF_SCROLLDOWN:
     
            pScroll->iScroll = 20;
        
            break;
        }
    }
  
return 0;
```



## <a name="related-topics"></a><span data-ttu-id="e3163-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="e3163-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3163-133">使用呼機控制項</span><span class="sxs-lookup"><span data-stu-id="e3163-133">Using Pager Controls</span></span>](using-pager-controls.md)
</dt> <dt>

<span data-ttu-id="e3163-134">[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="e3163-134">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 