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
# <a name="how-to-create-syslink-controls"></a>如何建立 SysLink 控制項

您可以透過控制項初始字串中的標記來執行 SysLink 控制項的超連結，或將 [**LM \_ SETITEM**](lm-setitem.md) 訊息傳送給它。

> [!Note]  
> 建立 SysLink 控制項之前，您必須先呼叫 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) 函式，並指定 ICC \_ 連結 \_ 類別。

 

若要建立 SysLink，請呼叫 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) 或 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函數，並指定 [**WC \_ 連結**](common-control-window-classes.md) 視窗類別。 這些函式通用的 *lpWindowName* 參數會指定以零結尾的字串指標，其中包含要顯示的已標記文字。 針對 SysLink 控制項的特定視窗樣式，請參閱 [SysLink 控制項樣式](syslink-control-styles.md)。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="create-a-syslink-control"></a>建立 SysLink 控制項

下列程式碼範例會建立 SysLink 控制項，以顯示兩個超連結。 第一個超連結是網際網路 URL，而第二個是應用程式定義。


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



## <a name="remarks"></a>備註

假設已經呼叫 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) 。

指定 [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) 樣式可確保使用者可以選取連結，方法是將其定位至該連結，然後按下 enter 鍵。

第6版的 ComCtl32.dll 僅支援 Unicode。 因此，您無法建立 ANSI 版本的 SysLink 控制項，只是 Unicode。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 SysLink 控制項](/windows/desktop/Controls/using-syslink-controls)
</dt> <dt>

[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 