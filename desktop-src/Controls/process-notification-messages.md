---
title: 如何處理通知訊息
description: 屬性工作表會傳送 WM \_ 通知訊息，以從頁面中取出資訊，並通知頁面使用者動作。
ms.assetid: 82768E43-97BA-451A-9373-D5B8FD06ABED
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c544910e44e0c865e738427285d7488147b9c1
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2020
ms.locfileid: "103681602"
---
# <a name="how-to-process-notification-messages"></a>如何處理通知訊息

屬性工作表會傳送 [**WM \_ 通知**](wm-notify.md) 訊息，以從頁面中取出資訊，並通知頁面使用者動作。

訊息的 *lParam* 參數是 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) 結構的位址，其中包含 [屬性工作表] 對話方塊的控制碼、頁面對話方塊的控制碼，以及通知碼。 頁面必須藉由將頁面的 DWL \_ MSGRESULT 值設定為 **TRUE** 或 **FALSE**，來回應某些通知訊息。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="process-notification-messages"></a>處理通知訊息

下列範例是來自頁面之對話方塊程式的程式碼片段。 它會示範如何處理 [PSN 說明 \_ ](psn-help.md) 通知程式碼。


```C++
case WM_NOTIFY:

    switch (((NMHDR FAR *) lParam)->code) 
    {
    case PSN_HELP:
        {
         
        char szBuf[FILE_LEN]; // Buffer for name of Help file

        // Display Help for the font properties page.
        LoadString(g_hinst, IDS_HELPFILE, &szBuf, sizeof(szBuf)/sizeof(szBuf[0]));
        WinHelp(((NMHDR FAR *)lParam)->hwndFrom, &szBuf, HELP_CONTEXT, IDH_FONT_PROPERTIES);                
        
        break;
        
         }
         
        // Process other property sheet notifications here.
    }
    
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用屬性工作表](using-property-sheets.md)
</dt> <dt>

[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




