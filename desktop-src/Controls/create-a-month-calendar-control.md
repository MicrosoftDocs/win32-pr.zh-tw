---
title: 如何建立月曆控制項
description: 本主題示範如何使用 CreateWindowEx 函式，以動態方式建立月曆控制項。
ms.assetid: 35ADDA85-5D7D-46F4-A637-99FEE4592B3B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f3824618e9801b68eb67b13c64c638a5057481
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103684261"
---
# <a name="how-to-create-a-month-calendar-control"></a><span data-ttu-id="e3c84-103">如何建立月曆控制項</span><span class="sxs-lookup"><span data-stu-id="e3c84-103">How to Create a Month Calendar Control</span></span>

<span data-ttu-id="e3c84-104">本主題示範如何使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式，以動態方式建立月曆控制項。</span><span class="sxs-lookup"><span data-stu-id="e3c84-104">This topic demonstrates how to dynamically create a month calendar control by using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="e3c84-105">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="e3c84-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="e3c84-106">技術</span><span class="sxs-lookup"><span data-stu-id="e3c84-106">Technologies</span></span>

-   [<span data-ttu-id="e3c84-107">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="e3c84-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="e3c84-108">必要條件</span><span class="sxs-lookup"><span data-stu-id="e3c84-108">Prerequisites</span></span>

-   <span data-ttu-id="e3c84-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="e3c84-109">C/C++</span></span>
-   <span data-ttu-id="e3c84-110">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="e3c84-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="e3c84-111">指示</span><span class="sxs-lookup"><span data-stu-id="e3c84-111">Instructions</span></span>


<span data-ttu-id="e3c84-112">若要建立月曆控制項，請使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式，將 [**MONTHCAL \_ 類別**](common-control-window-classes.md) 指定為 window 類別。</span><span class="sxs-lookup"><span data-stu-id="e3c84-112">To create a month calendar control, use the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying [**MONTHCAL\_CLASS**](common-control-window-classes.md) as the window class.</span></span> <span data-ttu-id="e3c84-113">您必須先呼叫 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex)函式來註冊視窗類別，並在伴隨的 [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex)結構中指定 **ICC \_ 日期 \_ 類別** 位。</span><span class="sxs-lookup"><span data-stu-id="e3c84-113">You must first register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function, specifying the **ICC\_DATE\_CLASSES** bit in the accompanying [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>

<span data-ttu-id="e3c84-114">下列範例示範如何在現有的非強制回應對話方塊中建立月曆控制項。</span><span class="sxs-lookup"><span data-stu-id="e3c84-114">The following example demonstrates how to create a month calendar control in an existing modeless dialog box.</span></span> <span data-ttu-id="e3c84-115">請注意，傳遞給 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 的大小值都是零。</span><span class="sxs-lookup"><span data-stu-id="e3c84-115">Note that the size values passed to [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) are all zeros.</span></span> <span data-ttu-id="e3c84-116">因為所需的最小大小取決於控制項所使用的字型，所以此範例會使用 [**MonthCal \_ GetMinReqRect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) 宏來要求大小資訊，然後藉由呼叫 [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos)來調整控制項的大小。</span><span class="sxs-lookup"><span data-stu-id="e3c84-116">Because the minimum required size depends on the font that the control uses, the example uses the [**MonthCal\_GetMinReqRect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) macro to request size information and then resizes the control by calling [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span></span> <span data-ttu-id="e3c84-117">如果您之後使用 [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)來變更字型，控制項的維度將不會變更。</span><span class="sxs-lookup"><span data-stu-id="e3c84-117">If you subsequently change the font with [**WM\_SETFONT**](/windows/desktop/winmsg/wm-setfont), the dimensions of the control will not change.</span></span> <span data-ttu-id="e3c84-118">您必須再次呼叫 **MonthCal \_ GetMinReqRect** ，並調整控制項的大小以符合新的字型。</span><span class="sxs-lookup"><span data-stu-id="e3c84-118">You must call **MonthCal\_GetMinReqRect** again and resize the control to fit the new font.</span></span>



```C++
// Child window identifier of the month calendar.
#define IDC_MONTHCAL 101

// Symbols used by SetWindowPos function (arbitrary values).
#define LEFT 35
#define TOP  40

// Description:
//   Creates a month calendar control in a dialog box.  
// Parameters:
//   hwndOwner - handle of the owner window.
// Nonlocal variables:
//   MonthCalDlgProc - window procedure of the dialog box that 
//     contains the month calendar.
//   g_hInst - global instance handle.
//
HRESULT CreateMonthCalDialog(HWND hwndOwner)
{
    RECT rc;
    INITCOMMONCONTROLSEX icex;
    HWND hwndDlg = NULL;
    HWND hwndMonthCal = NULL;

    // Return an error code if the owner handle is invalid.
    if (hwndOwner == NULL)
        return E_INVALIDARG;

    // Load the window class.
    icex.dwSize = sizeof(icex);
    icex.dwICC  = ICC_DATE_CLASSES;
    InitCommonControlsEx(&icex);

    // Create a modeless dialog box to hold the control.
    hwndDlg = CreateDialog(g_hInst,
                    MAKEINTRESOURCE(IDD_DATE_PICKER),
                    hwndOwner,
                    MonthCalDlgProc);
   
    // Return if creating the dialog box failed. 
    if (hwndDlg == NULL)
        return HRESULT_FROM_WIN32(GetLastError()); 
                        
    // Create the month calendar.
    hwndMonthCal  = CreateWindowEx(0,
                    MONTHCAL_CLASS,
                    L"",
                    WS_BORDER | WS_CHILD | WS_VISIBLE | MCS_DAYSTATE,
                    0,0,0,0, // resize it later
                    hwndDlg,
                    (HMENU) IDC_MONTHCAL,
                    g_hInst,
                    NULL);

    // Return if creating the month calendar failed. 
    if (hwndMonthCal == NULL)
        return HRESULT_FROM_WIN32(GetLastError()); 
                     
    // Get the size required to show an entire month.
    MonthCal_GetMinReqRect(hwndMonthCal, &rc);

    // Resize the control now that the size values have been obtained.
    SetWindowPos(hwndMonthCal, NULL, LEFT, TOP, 
        rc.right, rc.bottom, SWP_NOZORDER);

    // Set the calendar to the annual view.
    MonthCal_SetCurrentView(hwndMonthCal, MCMV_YEAR);

    // Make the window visible.
    ShowWindow(hwndDlg, SW_SHOW);

    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="e3c84-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="e3c84-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3c84-120">月曆控制項參考</span><span class="sxs-lookup"><span data-stu-id="e3c84-120">Month Calendar Control Reference</span></span>](bumper-month-calendar-month-calendar-control-reference.md)
</dt> <dt>

[<span data-ttu-id="e3c84-121">關於 Month Calendar 控制項</span><span class="sxs-lookup"><span data-stu-id="e3c84-121">About Month Calendar Controls</span></span>](month-calendar-controls.md)
</dt> <dt>

[<span data-ttu-id="e3c84-122">使用月曆控制項</span><span class="sxs-lookup"><span data-stu-id="e3c84-122">Using Month Calendar Controls</span></span>](using-month-calendar-controls.md)
</dt> </dl>

 

 