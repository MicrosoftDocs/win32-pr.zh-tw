---
title: 處理來自 SplitButtons 的 BCN_DROPDOWN 通知
description: 本主題說明在對話方塊程式中回應 BCN 下拉式通知的一個可能方法 \_ 。
ms.assetid: 847DD645-AE29-4F62-BC32-F235BA409E1E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a368dd28c5347f438feff75fbddb129a420caae7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104093403"
---
# <a name="how-to-handle-the-bcn_dropdown-notification-from-a-split-button"></a><span data-ttu-id="a73c0-103">如何處理 \_ 分割按鈕的 BCN 下拉式清單通知</span><span class="sxs-lookup"><span data-stu-id="a73c0-103">How to Handle the BCN\_DROPDOWN Notification from a Split Button</span></span>

<span data-ttu-id="a73c0-104">本主題說明在對話方塊程式中回應 [BCN \_ 下拉式](bcn-dropdown.md) 通知的一個可能方法。</span><span class="sxs-lookup"><span data-stu-id="a73c0-104">This topic describes one possible way of responding to the [BCN\_DROPDOWN](bcn-dropdown.md) notification in a dialog procedure.</span></span>

<span data-ttu-id="a73c0-105">C + + 應用程式會從通知標頭抓取按鈕的用戶端座標，並將其轉換為螢幕座標。</span><span class="sxs-lookup"><span data-stu-id="a73c0-105">The C++ application retrieves the client coordinates of the button from the notification header and converts them to screen coordinates.</span></span> <span data-ttu-id="a73c0-106">然後，它會建立快顯功能表，並將其顯示在按鈕的底部。</span><span class="sxs-lookup"><span data-stu-id="a73c0-106">It then creates a popup menu and displays it at the bottom of the button.</span></span> <span data-ttu-id="a73c0-107">為了讓範例保持簡單，系統不會針對功能表執行鍵盤快速鍵。</span><span class="sxs-lookup"><span data-stu-id="a73c0-107">To keep the example simple, keyboard shortcuts are not implemented for the menu.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="a73c0-108">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="a73c0-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="a73c0-109">技術</span><span class="sxs-lookup"><span data-stu-id="a73c0-109">Technologies</span></span>

-   [<span data-ttu-id="a73c0-110">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="a73c0-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="a73c0-111">必要條件</span><span class="sxs-lookup"><span data-stu-id="a73c0-111">Prerequisites</span></span>

-   <span data-ttu-id="a73c0-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="a73c0-112">C/C++</span></span>
-   <span data-ttu-id="a73c0-113">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="a73c0-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="a73c0-114">指示</span><span class="sxs-lookup"><span data-stu-id="a73c0-114">Instructions</span></span>

### <a name="step-1-wait-for-the-bcn_dropdown-notification"></a><span data-ttu-id="a73c0-115">步驟1：等候 BCN 的 *\_ 下拉式清單* 通知。</span><span class="sxs-lookup"><span data-stu-id="a73c0-115">Step 1: Wait for the *BCN\_DROPDOWN* notification.</span></span>


```C++
case BCN_DROPDOWN:
{
    NMBCDROPDOWN* pDropDown = (NMBCDROPDOWN*)lParam;
    if (pDropDown->hdr.hwndFrom = GetDlgItem(hDlg, IDC_SPLIT))
    {
```



### <a name="step-2-get-the-screen-coordinates-of-the-button"></a><span data-ttu-id="a73c0-116">步驟2：取得按鈕的螢幕座標。</span><span class="sxs-lookup"><span data-stu-id="a73c0-116">Step 2: Get the screen coordinates of the button.</span></span>

<span data-ttu-id="a73c0-117">您可以使用 [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) 函式，將按鈕左下邊緣的視窗座標轉換成螢幕座標。</span><span class="sxs-lookup"><span data-stu-id="a73c0-117">Use the [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) function to convert the window coordinates of the button's lower left edge to screen coordinates.</span></span>


```C++
POINT pt;
pt.x = pDropDown->rcButton.left;
pt.y = pDropDown->rcButton.bottom;
ClientToScreen(pDropDown->hdr.hwndFrom, &pt);
```



### <a name="step-3-create-a-menu-and-add-items"></a><span data-ttu-id="a73c0-118">步驟3：建立功能表並新增專案。</span><span class="sxs-lookup"><span data-stu-id="a73c0-118">Step 3: Create a menu and add items.</span></span>

<span data-ttu-id="a73c0-119">使用 [**CreatePopupMenu**](/windows/desktop/api/winuser/nf-winuser-createpopupmenu) 函式來建立功能表。</span><span class="sxs-lookup"><span data-stu-id="a73c0-119">Use the [**CreatePopupMenu**](/windows/desktop/api/winuser/nf-winuser-createpopupmenu) function to create a menu.</span></span> <span data-ttu-id="a73c0-120">您可以使用 [**AppendMenu**](/windows/desktop/menurc/u) 函式，將專案加入至功能表中。</span><span class="sxs-lookup"><span data-stu-id="a73c0-120">Use the [**AppendMenu**](/windows/desktop/menurc/u) function to add items to the menu.</span></span> <span data-ttu-id="a73c0-121">IDC \_ MENUCOMMAND1 和 idc \_ MENUCOMMAND2 是適用于功能表命令的應用程式定義常數。</span><span class="sxs-lookup"><span data-stu-id="a73c0-121">IDC\_MENUCOMMAND1 and IDC\_MENUCOMMAND2 are application-defined constants for menu commands.</span></span>


```C++
HMENU hSplitMenu = CreatePopupMenu();
AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND1, L"Menu item 1");
AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND2, L"Menu item 2");
```



### <a name="step-4-display-the-menu"></a><span data-ttu-id="a73c0-122">步驟4：顯示功能表。</span><span class="sxs-lookup"><span data-stu-id="a73c0-122">Step 4: Display the menu.</span></span>

<span data-ttu-id="a73c0-123">[**Trackpopupmenu 讓**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu)函式會在指定的位置顯示快捷方式功能表，並追蹤功能表上的專案選取專案。</span><span class="sxs-lookup"><span data-stu-id="a73c0-123">The [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) function displays a shortcut menu at the specified location and tracks the selection of items on the menu.</span></span>


```C++
TrackPopupMenu(hSplitMenu, TPM_LEFTALIGN | TPM_TOPALIGN, pt.x, pt.y, 0, hDlg, NULL);
```



## <a name="complete-example"></a><span data-ttu-id="a73c0-124">完整範例</span><span class="sxs-lookup"><span data-stu-id="a73c0-124">Complete example</span></span>


```C++
case WM_NOTIFY:
    switch (((LPNMHDR)lParam)->code)
    {
        case BCN_DROPDOWN:
        {
            NMBCDROPDOWN* pDropDown = (NMBCDROPDOWN*)lParam;
            if (pDropDown->hdr.hwndFrom = GetDlgItem(hDlg, IDC_SPLIT))
            {

                // Get screen coordinates of the button.
                POINT pt;
                pt.x = pDropDown->rcButton.left;
                pt.y = pDropDown->rcButton.bottom;
                ClientToScreen(pDropDown->hdr.hwndFrom, &pt);
        
                // Create a menu and add items.
                HMENU hSplitMenu = CreatePopupMenu();
                AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND1, L"Menu item 1");
                AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND2, L"Menu item 2");
        
                // Display the menu.
                TrackPopupMenu(hSplitMenu, TPM_LEFTALIGN | TPM_TOPALIGN, pt.x, pt.y, 0, hDlg, NULL);
                return TRUE;
            }
            break;
        }
    }
    return FALSE;
}
```



## <a name="related-topics"></a><span data-ttu-id="a73c0-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="a73c0-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a73c0-126">BCN \_ 下拉式通知碼</span><span class="sxs-lookup"><span data-stu-id="a73c0-126">BCN\_DROPDOWN Notification Code</span></span>](bcn-dropdown.md)
</dt> <dt>

[<span data-ttu-id="a73c0-127">關於按鈕</span><span class="sxs-lookup"><span data-stu-id="a73c0-127">About Buttons</span></span>](about-buttons.md)
</dt> <dt>

[<span data-ttu-id="a73c0-128">按鈕控制項參考</span><span class="sxs-lookup"><span data-stu-id="a73c0-128">Button Control Reference</span></span>](bumper-button-button-control-reference.md)
</dt> <dt>

[<span data-ttu-id="a73c0-129">使用按鈕</span><span class="sxs-lookup"><span data-stu-id="a73c0-129">Using Buttons</span></span>](using-buttons.md)
</dt> <dt>

[<span data-ttu-id="a73c0-130">按鈕</span><span class="sxs-lookup"><span data-stu-id="a73c0-130">Button</span></span>](buttons.md)
</dt> </dl>

 

 