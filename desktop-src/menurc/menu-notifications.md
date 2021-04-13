---
title: 功能表通知
description: .
ms.assetid: 8ff5671e-a666-483c-9ac1-f8be6eb58ffa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d61f5303253fd3201fd9a4510ecf90fa76c10524
ms.sourcegitcommit: e98f40bef170ae9ce30d91ba96b90600b0446a24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/28/2020
ms.locfileid: "104314575"
---
# <a name="menu-notifications"></a>功能表通知

## <a name="in-this-section"></a>本節內容

-   [**WM \_ 命令**](wm-command.md)
-   [**WM \_ CONTEXTMENU**](wm-contextmenu.md)
-   [**WM \_ ENTERMENULOOP**](wm-entermenuloop.md)
-   [**WM \_ EXITMENULOOP**](wm-exitmenuloop.md)
-   [**WM \_ GETTITLEBARINFOEX**](wm-gettitlebarinfoex.md)
-   [**WM \_ MENUCOMMAND**](wm-menucommand.md)
-   [**WM \_ MENUDRAG**](wm-menudrag.md)
-   [**WM \_ MENUGETOBJECT**](wm-menugetobject.md)
-   [**WM \_ MENURBUTTONUP**](wm-menurbuttonup.md)
-   [**WM \_ NEXTMENU**](wm-nextmenu.md)
-   [**WM \_ UNINITMENUPOPUP**](wm-uninitmenupopup.md)


## <a name="example"></a>範例

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
從 GitHub 上的 [Windows 傳統範例](https://github.com/microsoft/Windows-classic-samples) 取得的範例。

 




