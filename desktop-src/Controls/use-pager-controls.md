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
# <a name="how-to-use-pager-controls"></a>如何使用呼機控制項

本節說明如何在您的應用程式中執行呼機控制項。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="initialize-a-pager-control"></a>初始化呼機控制項

若要使用分頁控制項，您必須使用 [](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) \_ \_ [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex)結構的 **dwICC** 成員中設定的 ICC PAGESCROLLER 類別旗標來呼叫 InitCommonControlsEx 函式。

### <a name="create-a-pager-control"></a>建立呼機控制項

使用 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) 或 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) API 來建立呼機控制項。 控制項的類別名稱是 [**WC \_ PAGESCROLLER**](common-control-window-classes.md)，定義于 Commctrl 中。 [**Pg \_ HORZ**](pager-control-styles.md)樣式是用來建立水準呼機，而 pg 垂直樣式 [**\_**](pager-control-styles.md)則是用來建立垂直呼機。 因為這是子控制項，所以也應該使用 [**WS \_ 子**](/windows/desktop/winmsg/window-styles) 樣式。

建立了呼機控制項之後，您很可能會想要指派內含的視窗給它。 如果包含的視窗是子視窗，您應該將子視窗設為分頁控制項的子系，以便正確地計算大小和位置。 然後，您可以使用 [**PGM \_ SETCHILD**](pgm-setchild.md) 訊息，將視窗指派給呼機控制項。 請注意，此訊息並不會實際變更包含視窗的父視窗;它只會指派包含的視窗。 如果包含的視窗是其中一個通用控制項，它必須具有 [**CCS \_ NORESIZE**](common-control-styles.md) 樣式，以防止控制項嘗試將自己的大小調整為呼機控制項的大小。

### <a name="process-pager-control-notifications"></a>處理呼機控制項通知

您至少必須處理 [PGN \_ CALCSIZE](pgn-calcsize.md) 通知。 如果您未處理此通知，並輸入寬度或高度的值，則不會顯示分頁控制項中的滾動箭號。 這是因為呼機控制項會使用 PGN CALCSIZE 通知中提供的寬度或高度 \_ ，判斷所包含視窗的「理想」大小。

下列範例示範如何處理 [PGN \_ CALCSIZE](pgn-calcsize.md) 通知案例。 在此範例中，包含的視窗是工具列控制項，包含未知大小的未知按鈕數目。 此範例示範如何使用 [**TB \_ GETMAXSIZE**](tb-getmaxsize.md) 訊息來判斷工具列中所有專案的大小。 然後，此範例會將所有專案的寬度放入傳遞給通知之 [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize)結構的 **iWidth** 成員中。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用呼機控制項](using-pager-controls.md)
</dt> <dt>

[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 