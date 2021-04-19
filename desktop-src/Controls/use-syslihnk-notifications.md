---
title: 如何使用 SysLink 通知
description: 有兩個通知訊息與 SysLink control \ 郵件相關聯，一個用於滑鼠 (NM \_ 按一下 (SysLink) ) ，另一個則是鍵盤 (NM 傳回 \_) 。
ms.assetid: 77E80EB2-180B-4EDD-9FB5-9930E8886CA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 864a2b8942b1244be51f5c284e6ce07d973ed4db
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2020
ms.locfileid: "106967882"
---
# <a name="how-to-use-syslink-notifications"></a>如何使用 SysLink 通知

有兩個通知訊息與 SysLink 控制項相關聯—一個用於滑鼠 ([nm \_ 按一下 (SysLink) ](nm-click-syslink.md)) ，另一個則是鍵盤 ([NM \_ 傳回](nm-return.md)) 。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="use-syslink-notifications"></a>使用 SysLink 通知

下列範例程式碼示範如何處理當使用者按下 [一個範例](create-syslink-controls.md)中的兩個連結之一時，所產生的 SysLink 通知。 當使用者按一下網際網路 URL 時，會在預設瀏覽器中開啟相關聯的網頁。 當使用者按一下應用程式定義的超連結時，會顯示訊息方塊。


```C++
// g_hLink is the handle of the SysLink control.
case WM_NOTIFY:

    switch (((LPNMHDR)lParam)->code)
    {
    
    case NM_CLICK:          // Fall through to the next case.
    
    case NM_RETURN:
        {
            PNMLINK pNMLink = (PNMLINK)lParam;
            LITEM   item    = pNMLink->item;
            
            if ((((LPNMHDR)lParam)->hwndFrom == g_hLink) && (item.iLink == 0))
              {
                ShellExecute(NULL, L"open", item.szUrl, NULL, NULL, SW_SHOW);
              }
            
            else if (wcscmp(item.szID, L"idInfo") == 0)
              {
                MessageBox(hDlg, L"This isn't much help.", L"Example", MB_OK);
              }
            
            break;
        }
    }
    
    break;
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 SysLink 控制項](using-syslink-controls.md)
</dt> <dt>

[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




