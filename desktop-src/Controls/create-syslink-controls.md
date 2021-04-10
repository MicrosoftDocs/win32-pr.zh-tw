---
title: 如何建立 SysLink 控制項
description: 您可以透過控制項初始字串中的標記來執行 SysLink 控制項的超連結，或將 LM SETITEM 訊息傳送給它 \_ 。
ms.assetid: CEE02A87-D85A-4F4D-931D-2B1371320814
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77aa5c5ff3348f35f9c67cb34bea0cc495d403ef
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683196"
---
# <a name="how-to-create-syslink-controls"></a><span data-ttu-id="fef1a-103">如何建立 SysLink 控制項</span><span class="sxs-lookup"><span data-stu-id="fef1a-103">How to Create SysLink Controls</span></span>

<span data-ttu-id="fef1a-104">您可以透過控制項初始字串中的標記來執行 SysLink 控制項的超連結，或將 [**LM \_ SETITEM**](lm-setitem.md) 訊息傳送給它。</span><span class="sxs-lookup"><span data-stu-id="fef1a-104">You implement the SysLink control's hyperlinks through markup in the control's initialization string, or by sending it a [**LM\_SETITEM**](lm-setitem.md) message.</span></span>

> [!Note]  
> <span data-ttu-id="fef1a-105">建立 SysLink 控制項之前，您必須先呼叫 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) 函式，並指定 ICC \_ 連結 \_ 類別。</span><span class="sxs-lookup"><span data-stu-id="fef1a-105">Before creating SysLink controls, you must call the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function, specifying the ICC\_LINK\_CLASS.</span></span>

 

<span data-ttu-id="fef1a-106">若要建立 SysLink，請呼叫 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) 或 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函數，並指定 [**WC \_ 連結**](common-control-window-classes.md) 視窗類別。</span><span class="sxs-lookup"><span data-stu-id="fef1a-106">To create a SysLink, call the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the [**WC\_LINK**](common-control-window-classes.md) window class.</span></span> <span data-ttu-id="fef1a-107">這些函式通用的 *lpWindowName* 參數會指定以零結尾的字串指標，其中包含要顯示的已標記文字。</span><span class="sxs-lookup"><span data-stu-id="fef1a-107">The *lpWindowName* parameter that is common to these functions specifies a pointer to a zero-terminated string that contains the marked-up text to display.</span></span> <span data-ttu-id="fef1a-108">針對 SysLink 控制項的特定視窗樣式，請參閱 [SysLink 控制項樣式](syslink-control-styles.md)。</span><span class="sxs-lookup"><span data-stu-id="fef1a-108">For window styles particular to SysLink controls, see [SysLink Control Styles](syslink-control-styles.md).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="fef1a-109">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="fef1a-109">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="fef1a-110">技術</span><span class="sxs-lookup"><span data-stu-id="fef1a-110">Technologies</span></span>

-   [<span data-ttu-id="fef1a-111">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="fef1a-111">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="fef1a-112">必要條件</span><span class="sxs-lookup"><span data-stu-id="fef1a-112">Prerequisites</span></span>

-   <span data-ttu-id="fef1a-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="fef1a-113">C/C++</span></span>
-   <span data-ttu-id="fef1a-114">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="fef1a-114">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="fef1a-115">指示</span><span class="sxs-lookup"><span data-stu-id="fef1a-115">Instructions</span></span>

### <a name="create-a-syslink-control"></a><span data-ttu-id="fef1a-116">建立 SysLink 控制項</span><span class="sxs-lookup"><span data-stu-id="fef1a-116">Create a SysLink Control</span></span>

<span data-ttu-id="fef1a-117">下列程式碼範例會建立 SysLink 控制項，以顯示兩個超連結。</span><span class="sxs-lookup"><span data-stu-id="fef1a-117">The following example code creates a SysLink control that displays two hyperlinks.</span></span> <span data-ttu-id="fef1a-118">第一個超連結是網際網路 URL，而第二個是應用程式定義。</span><span class="sxs-lookup"><span data-stu-id="fef1a-118">The first hyperlink is an Internet URL, and the second is application-defined.</span></span>


```C++
HWND CreateSysLink(HWND hDlg, HINSTANCE hInst, RECT rect)
{
    return CreateWindowEx(0, WC_LINK, 
        L"For more information, <A HREF=\"https://www.microsoft.com\">click here</A> " \
        L"or <A ID=\"idInfo\">here</A>.", 
        WS_VISIBLE | WS_CHILD | WS_TABSTOP, 
        rect.left, rect.top, rect.right, rect.bottom, 
        hDlg, NULL, hInst, NULL);
}
```



## <a name="remarks"></a><span data-ttu-id="fef1a-119">備註</span><span class="sxs-lookup"><span data-stu-id="fef1a-119">Remarks</span></span>

<span data-ttu-id="fef1a-120">假設已經呼叫 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) 。</span><span class="sxs-lookup"><span data-stu-id="fef1a-120">It is assumed that [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) has already been called.</span></span>

<span data-ttu-id="fef1a-121">指定 [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) 樣式可確保使用者可以選取連結，方法是將其定位至該連結，然後按下 enter 鍵。</span><span class="sxs-lookup"><span data-stu-id="fef1a-121">Specifying the [**WS\_TABSTOP**](/windows/desktop/winmsg/window-styles) style ensures that the user will be able to select a link by tabbing to it and pressing the Enter key.</span></span>

<span data-ttu-id="fef1a-122">第6版的 ComCtl32.dll 僅支援 Unicode。</span><span class="sxs-lookup"><span data-stu-id="fef1a-122">Version 6 of ComCtl32.dll supports Unicode only.</span></span> <span data-ttu-id="fef1a-123">因此，您無法建立 ANSI 版本的 SysLink 控制項，只是 Unicode。</span><span class="sxs-lookup"><span data-stu-id="fef1a-123">Therefore, you cannot create ANSI versions of SysLink controls—only Unicode.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fef1a-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="fef1a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fef1a-125">使用 SysLink 控制項</span><span class="sxs-lookup"><span data-stu-id="fef1a-125">Using SysLink Controls</span></span>](/windows/desktop/Controls/using-syslink-controls)
</dt> <dt>

<span data-ttu-id="fef1a-126">[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="fef1a-126">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 