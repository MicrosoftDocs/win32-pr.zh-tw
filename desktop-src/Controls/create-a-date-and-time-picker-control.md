---
title: 如何建立日期和時間選擇器控制項
description: 本主題示範如何以動態方式建立日期和時間選擇器 (DTP) 控制項。
ms.assetid: D4ACA939-3004-48D3-ADD9-FC5E53128BA2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1253a2972b8d858a7440b3e472d5b3aa347b8175
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104186103"
---
# <a name="how-to-create-a-date-and-time-picker-control"></a><span data-ttu-id="03f69-103">如何建立日期和時間選擇器控制項</span><span class="sxs-lookup"><span data-stu-id="03f69-103">How to Create a Date and Time Picker Control</span></span>

<span data-ttu-id="03f69-104">本主題示範如何以動態方式建立日期和時間選擇器 (DTP) 控制項。</span><span class="sxs-lookup"><span data-stu-id="03f69-104">This topic demonstrates how to dynamically create a date and time picker (DTP) control.</span></span> <span data-ttu-id="03f69-105">隨附的 c + + 程式碼範例會在非強制回應對話方塊中建立一個 DTP 控制項。</span><span class="sxs-lookup"><span data-stu-id="03f69-105">The accompanying C++ code example creates a DTP control in a modeless dialog box.</span></span> <span data-ttu-id="03f69-106">它會使用 [**DTS \_ SHOWNONE**](date-and-time-picker-control-styles.md) 樣式，讓使用者可以模擬控制項內的日期停用。</span><span class="sxs-lookup"><span data-stu-id="03f69-106">It uses the [**DTS\_SHOWNONE**](date-and-time-picker-control-styles.md) style to enable the user to simulate deactivation of the date within the control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="03f69-107">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="03f69-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="03f69-108">技術</span><span class="sxs-lookup"><span data-stu-id="03f69-108">Technologies</span></span>

-   [<span data-ttu-id="03f69-109">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="03f69-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="03f69-110">必要條件</span><span class="sxs-lookup"><span data-stu-id="03f69-110">Prerequisites</span></span>

-   <span data-ttu-id="03f69-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="03f69-111">C/C++</span></span>
-   <span data-ttu-id="03f69-112">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="03f69-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="03f69-113">指示</span><span class="sxs-lookup"><span data-stu-id="03f69-113">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="03f69-114">步驟 1:</span><span class="sxs-lookup"><span data-stu-id="03f69-114">Step 1:</span></span>

<span data-ttu-id="03f69-115">藉由呼叫 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) 函式，並 \_ \_ 在伴隨的 [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) 結構中指定 ICC 日期類別位，來註冊視窗類別。</span><span class="sxs-lookup"><span data-stu-id="03f69-115">Register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function and specifying the ICC\_DATE\_CLASSES bit in the accompanying [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>


```C++
 INITCOMMONCONTROLSEX icex;

 icex.dwSize = sizeof(icex);
 icex.dwICC = ICC_DATE_CLASSES;

 InitCommonControlsEx(&icex);
```



### <a name="step-2"></a><span data-ttu-id="03f69-116">步驟 2:</span><span class="sxs-lookup"><span data-stu-id="03f69-116">Step 2:</span></span>

<span data-ttu-id="03f69-117">若要建立 DTP 控制項，請使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函數。</span><span class="sxs-lookup"><span data-stu-id="03f69-117">To create the DTP control, use the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="03f69-118">將 [**DATETIMEPICK \_ 類別**](common-control-window-classes.md) 指定為視窗類別，並將控制碼傳遞至父對話方塊。</span><span class="sxs-lookup"><span data-stu-id="03f69-118">Specify [**DATETIMEPICK\_CLASS**](common-control-window-classes.md) as the window class, and pass the handle to the parent dialog box.</span></span>

<span data-ttu-id="03f69-119">下列 c + + 程式碼範例會使用 [**CreateDialog**](/windows/desktop/api/winuser/nf-winuser-createdialoga) 函數來建立非強制回應對話方塊。</span><span class="sxs-lookup"><span data-stu-id="03f69-119">The following C++ code example uses the [**CreateDialog**](/windows/desktop/api/winuser/nf-winuser-createdialoga) function to create a modeless dialog box.</span></span> <span data-ttu-id="03f69-120">然後，它會呼叫 **CreateWindowEx** 來建立 DTP 控制項。</span><span class="sxs-lookup"><span data-stu-id="03f69-120">It then calls **CreateWindowEx** to create the DTP control.</span></span>


```C++
  hwndDlg = CreateDialog  (g_hinst,
                           MAKEINTRESOURCE(IDD_DIALOG1),
                           hwndMain,
                           DlgProc);

  if(hwndDlg)
      hwndDP = CreateWindowEx(0,
                           DATETIMEPICK_CLASS,
                           TEXT("DateTime"),
                           WS_BORDER|WS_CHILD|WS_VISIBLE|DTS_SHOWNONE,
                           20,50,220,20,
                           hwndDlg,
                           NULL,
                           g_hinst,
                           NULL);
```



## <a name="complete-example"></a><span data-ttu-id="03f69-121">完整範例</span><span class="sxs-lookup"><span data-stu-id="03f69-121">Complete example</span></span>


```C++
//  CreateDatePick creates a DTP control within a dialog box.
//  Returns the handle to the new DTP control if successful, or NULL 
//  otherwise.
// 
//    hwndMain - The handle to the main window.
//    g_hinst  - global handle to the program instance.

HWND WINAPI CreateDatePick(HWND hwndMain)
{
    HWND hwndDP = NULL;
    HWND hwndDlg = NULL;

    INITCOMMONCONTROLSEX icex;

    icex.dwSize = sizeof(icex);
    icex.dwICC = ICC_DATE_CLASSES;

    InitCommonControlsEx(&icex);

    hwndDlg = CreateDialog  (g_hinst,
                             MAKEINTRESOURCE(IDD_DIALOG1),
                             hwndMain,
                             DlgProc);

    if(hwndDlg)
        hwndDP = CreateWindowEx(0,
                             DATETIMEPICK_CLASS,
                             TEXT("DateTime"),
                             WS_BORDER|WS_CHILD|WS_VISIBLE|DTS_SHOWNONE,
                             20,50,220,20,
                             hwndDlg,
                             NULL,
                             g_hinst,
                             NULL);

    return (hwndDP);
}

```



## <a name="related-topics"></a><span data-ttu-id="03f69-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="03f69-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03f69-123">使用日期時間選擇器控制項</span><span class="sxs-lookup"><span data-stu-id="03f69-123">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="03f69-124">日期和時間選擇器控制項參考</span><span class="sxs-lookup"><span data-stu-id="03f69-124">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="03f69-125">日期和時間選擇器</span><span class="sxs-lookup"><span data-stu-id="03f69-125">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 