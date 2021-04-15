---
title: 如何建立 IP 位址控制項
description: 本主題示範如何建立 IP 位址控制項的實例。
ms.assetid: E4DBECA6-B3F2-405F-8D95-32FA2334114D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8427a5695c0b9c79c19d328f4abc2ab0ffb2e5a
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104093527"
---
# <a name="how-to-create-an-ip-address-control"></a>如何建立 IP 位址控制項

本主題示範如何建立 IP 位址控制項的實例。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示


建立 IP 位址控制項之前，請先呼叫 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex)來載入通用控制項 DLL。 然後使用 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) 或 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函數來建立實例 IP 位址控制項。 控制項的類別名稱是 [**WC \_ IPADDRESS**](common-control-window-classes.md)。 使用 [**WS \_ 子**](/windows/desktop/winmsg/window-styles) 樣式，因為沒有與 IP 位址控制項相關聯的特定樣式常數。

在下列 c + + 程式碼範例中，應用程式定義函式會先呼叫 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) ，並將 [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex)結構的 **dwICC** 成員設定為 [**ICC \_ 網際網路 \_ 類別**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex)，以指定 IP 位址類別。 然後，它會呼叫 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 來建立 IP 位址控制項的實例。


```C++
// CreateIPAdressFld - creates a IPAddress control.
// Returns the handle to the new control
// TO DO:  calling procedure needs to check whether the handle is NULL, in case 
// of an error in creation.
// int xcoord, ycoord the coordinates of location of the control in the parent window
// HINST hInst is the global handle to the application instance.
// HWND  hWndParent is the handle to the control's parent window. 
//
//
HWND CreateIPAddressFld (HWND hwndParent, int xcoord, int ycoord) 
{     
     
    INITCOMMONCONTROLSEX icex;
    
    // Ensure that the common control DLL is loaded. 
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC  = ICC_INTERNET_CLASSES ;
    InitCommonControlsEx(&icex); 
    
    // Create the IPAddress control.        
    HWND hWndIPAddressFld = CreateWindow(WC_IPADDRESS, 
                                L"", 
                                WS_CHILD | WS_OVERLAPPED | WS_VISIBLE, 
                                xcoord, 
                                ycoord,
                                150, 
                                20,  
                                hwndParent, 
                                NULL, 
                                hInst, 
                                NULL); 
                                
    return (hWndIPAddressFld);
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[IP 位址控制參考](bumper-ip-address-control-ip-address-control-reference.md)
</dt> <dt>

[關於 IP 位址控制項](ip-address-controls.md)
</dt> <dt>

[使用 IP 位址控制項](using-ip-address-controls.md)
</dt> </dl>

 

 