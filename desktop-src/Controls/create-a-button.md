---
title: 如何建立按鈕
description: 若要動態建立按鈕，請使用 CreateWindow 或 CreateWindowEx 函數。 本主題將示範如何使用 CreateWindow 函式來建立預設的推播按鈕。
ms.assetid: A8C56D09-90A3-4C70-9907-61390521D1DA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dadc53f91f773e5fce9e29bdf1ae50cc59bfdfd
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104024356"
---
# <a name="how-to-create-a-button"></a>如何建立按鈕

若要動態建立按鈕，請使用 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) 或 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函數。 本主題將示範如何使用 **CreateWindow** 函式來建立預設的推播按鈕。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示


使用 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) 函數來建立按鈕控制項。

在下列 c + + 範例中， *m \_ hwnd* 參數是父視窗的控制碼。 [**BS \_ DEFPUSHBUTTON**](button-styles.md)樣式指定應該建立預設的 [推送] 按鈕。 請注意，您必須指定大小和位置值，因為使用按鈕的 **CW \_ USEDEFAULT** 將值設為零。


```C++
HWND hwndButton = CreateWindow( 
    L"BUTTON",  // Predefined class; Unicode assumed 
    L"OK",      // Button text 
    WS_TABSTOP | WS_VISIBLE | WS_CHILD | BS_DEFPUSHBUTTON,  // Styles 
    10,         // x position 
    10,         // y position 
    100,        // Button width
    100,        // Button height
    m_hwnd,     // Parent window
    NULL,       // No menu.
    (HINSTANCE)GetWindowLongPtr(m_hwnd, GWLP_HINSTANCE), 
    NULL);      // Pointer not needed.
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於按鈕](about-buttons.md)
</dt> <dt>

[按鈕控制項參考](bumper-button-button-control-reference.md)
</dt> <dt>

[使用按鈕](using-buttons.md)
</dt> <dt>

[按鈕](buttons.md)
</dt> </dl>

 

 