---
title: 如何建立命令連結
description: 本主題說明建立命令連結的其中一種方式。
ms.assetid: F342075B-2D3B-40E0-B657-E1C57EDC2E3A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c61888921f06e017ec1ea625730c3cc52de5ab364db22fc01fd021ce5629c63
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920898"
---
# <a name="how-to-create-a-command-link"></a>如何建立命令連結

本主題說明建立命令連結的其中一種方式。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows控制](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="step-1-create-an-instance-of-the-command-link-button"></a>步驟1：建立命令連結按鈕的實例。

在下列 c + + 程式碼範例中，style 常數 [**BS \_ COMMANDLINK**](button-styles.md) 會將按鈕指定為命令連結按鈕。


```C++
HWND hwndCommandLink = CreateWindow(
    L"BUTTON",  // Predefined class; Unicode assumed
    L"",        // Text will be defined later
    WS_TABSTOP | WS_VISIBLE | WS_CHILD | BS_COMMANDLINK,  // Styles
    200,        // x position 
    10,         // y position 
    100,        // Button width
    100,        // Button height
    m_hwnd,     // Parent window
    NULL,       // No menu
    (HINSTANCE)GetWindowLongPtr(m_hwnd, GWLP_HINSTANCE), 
    NULL);      // Pointer not needed
```



### <a name="step-2-set-the-command-link-label-and-explanation-text"></a>步驟2：設定命令連結標籤和解說文字

您可以使用 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 函式，透過 [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) 訊息和 [**BCM \_ SETNOTE**](bcm-setnote.md) 訊息分別設定命令連結標籤和補充文字。


```C++
SendMessage(hwndCommandLink, WM_SETTEXT, 0, (LPARAM)L"Command link");
SendMessage(hwndCommandLink, BCM_SETNOTE, 0, (LPARAM)L"with note");
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

 

 