---
title: 功能表通知
description: 功能表通知
ms.assetid: 8ff5671e-a666-483c-9ac1-f8be6eb58ffa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f593e3007dff82241dc9e917a6cfa140cc443679
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112526"
---
# <a name="menu-notifications"></a><span data-ttu-id="5eb3c-103">功能表通知</span><span class="sxs-lookup"><span data-stu-id="5eb3c-103">Menu Notifications</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5eb3c-104">本節內容</span><span class="sxs-lookup"><span data-stu-id="5eb3c-104">In This Section</span></span>

-   [<span data-ttu-id="5eb3c-105">**WM \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-105">**WM\_COMMAND**</span></span>](wm-command.md)
-   [<span data-ttu-id="5eb3c-106">**WM \_ CONTEXTMENU**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-106">**WM\_CONTEXTMENU**</span></span>](wm-contextmenu.md)
-   [<span data-ttu-id="5eb3c-107">**WM \_ ENTERMENULOOP**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-107">**WM\_ENTERMENULOOP**</span></span>](wm-entermenuloop.md)
-   [<span data-ttu-id="5eb3c-108">**WM \_ EXITMENULOOP**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-108">**WM\_EXITMENULOOP**</span></span>](wm-exitmenuloop.md)
-   [<span data-ttu-id="5eb3c-109">**WM \_ GETTITLEBARINFOEX**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-109">**WM\_GETTITLEBARINFOEX**</span></span>](wm-gettitlebarinfoex.md)
-   [<span data-ttu-id="5eb3c-110">**WM \_ MENUCOMMAND**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-110">**WM\_MENUCOMMAND**</span></span>](wm-menucommand.md)
-   [<span data-ttu-id="5eb3c-111">**WM \_ MENUDRAG**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-111">**WM\_MENUDRAG**</span></span>](wm-menudrag.md)
-   [<span data-ttu-id="5eb3c-112">**WM \_ MENUGETOBJECT**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-112">**WM\_MENUGETOBJECT**</span></span>](wm-menugetobject.md)
-   [<span data-ttu-id="5eb3c-113">**WM \_ MENURBUTTONUP**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-113">**WM\_MENURBUTTONUP**</span></span>](wm-menurbuttonup.md)
-   [<span data-ttu-id="5eb3c-114">**WM \_ NEXTMENU**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-114">**WM\_NEXTMENU**</span></span>](wm-nextmenu.md)
-   [<span data-ttu-id="5eb3c-115">**WM \_ UNINITMENUPOPUP**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-115">**WM\_UNINITMENUPOPUP**</span></span>](wm-uninitmenupopup.md)


## <a name="example"></a><span data-ttu-id="5eb3c-116">範例</span><span class="sxs-lookup"><span data-stu-id="5eb3c-116">Example</span></span>

```c
BOOL AboutDlg (
    HWND hDlg, 
    UINT message, 
    WPARAM wParam, 
    LPARAM lParam)
{
    BOOL bRet = FALSE;
    
    switch (message) 
    {
        case WM_INITDIALOG:
            bRet = TRUE;
            break;

        case WM_COMMAND:
            if (wParam == IDOK ||
                wParam == IDCANCEL) 
            {
                EndDialog(hDlg, TRUE);
                bRet = TRUE;
            }
            break;
    }

    return bRet;
}
```
<span data-ttu-id="5eb3c-117">從 GitHub 上的 [Windows 傳統範例](https://github.com/microsoft/Windows-classic-samples) 取得的範例。</span><span class="sxs-lookup"><span data-stu-id="5eb3c-117">Example taken from [Windows classic samples](https://github.com/microsoft/Windows-classic-samples) on GitHub.</span></span>

 




