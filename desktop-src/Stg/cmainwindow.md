---
title: CMainWindow
description: 下列範例程式碼說明此程式。
ms.assetid: a2998232-db71-48ce-b14b-5e17de147172
keywords:
- CMainWindow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3e9cb538246dfa6931a2f036ba75cab5e962a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967593"
---
# <a name="cmainwindow"></a>CMainWindow

Microsoft Windows 作業系統會將下列使用者動作轉譯成標準視窗訊息，並將它們傳送至 **StoClien** 應用程式中的主要程式：

-   使用者按一下滑鼠左鍵或 tablet 裝置中的 [畫筆提示] 參數，以起始線條繪圖順序。
-   使用者按一下並按住按鈕，並移動滑鼠來繪製線條。
-   放開滑鼠左鍵時，會結束序列。

下列範例程式碼說明此程式。

## <a name="cmainwindowwindowproc-stocliencpp"></a>CMainWindow：： WindowProc (STOCLIEN。CPP) 


```C++
LRESULT CMainWindow::WindowProc(
            UINT uMsg,
            WPARAM wParam,
            LPARAM lParam)
  {
    LRESULT lResult = FALSE;

    switch (uMsg)
    {
      case WM_CREATE:
        break;

      case WM_ACTIVATE:
        // A mouse click reactivates the paint procedure.
        // This is used to paint a new window when a user
        // selects a portion of the STOCLIEN window that is 
        // visible beneath another window. This message is  
        // sent in the WindowProc handle.
        if (WA_CLICKACTIVE == LOWORD(wParam))
          m_pGuiPaper->PaintWin();
        lResult = ::DefWindowProc(m_hWnd, uMsg, wParam, lParam);
        break;

      case WM_SIZE:
        // Handle a resize of this window.
        m_wWidth = LOWORD(lParam);
        m_wHeight = HIWORD(lParam);
        // Inform CGuiPaper of the change.
        m_pGuiPaper->Resize(m_wWidth, m_wHeight);
        break;

      case WM_PAINT:
        // This is a message to repaint the window.
        {
          PAINTSTRUCT ps;

          if(BeginPaint(m_hWnd, &ps))
            EndPaint(m_hWnd, &ps);

          m_pGuiPaper->PaintWin();
        }
        break;

      case WM_LBUTTONDOWN:
        // Start sequence of ink drawing to the paper.
        m_pGuiPaper->InkStart(LOWORD(lParam), HIWORD(lParam));
        break;

      case WM_MOUSEMOVE:
        // Draw inking sequence data.
        m_pGuiPaper->InkDraw(LOWORD(lParam), HIWORD(lParam));
        break;

      case WM_LBUTTONUP:
        // Stop an ink drawing sequence.
        m_pGuiPaper->InkStop(LOWORD(lParam), HIWORD(lParam));
        break;

      case WM_COMMAND:
        // Dispatch and handle any Menu command messages received.
        lResult = DoMenu(wParam, lParam);
        break;

      case WM_CHAR:
        if (wParam == 0x1b)
        {
          // Exit this application if user presses the ESC key.
          ::PostMessage(m_hWnd, WM_CLOSE, 0, 0);
        }
        break;

      case WM_CLOSE:
        // The user selected Close on the main window System menu
        // or Exit on the File menu.
        // If there is unsaved ink data, then prompt
        // the user. If the user cancels, do not close the window.
        if (IDCANCEL == m_pGuiPaper->AskSave())
          break;
      case WM_QUIT:
        // When exiting the application, close any associated help
        // windows.
        // ::WinHelp(m_hWnd, m_szHelpFile, HELP_QUIT, 0);
      default:
        // If there are any messages that have not been handled,
        // send them to the default window procedure.
        lResult = ::DefWindowProc(m_hWnd, uMsg, wParam, lParam);
        break;
    }

    return(lResult);
  }
```



當 WM \_ LBUTTONDOWN 訊息傳遞滑鼠位置資料時，就會開始線條繪圖順序。

CMainWindow 具有 CGuiPaper 物件的指標，並會呼叫 [**CGuiPaper：： InkStart**](cguipaper-methods.md) 方法來啟動線條繪圖順序。

當滑鼠移至繪圖時，會將包含滑鼠位置資料的個別 **WM \_ MOUSEMOVE** 訊息序列提供給 [CGuiPaper：： InkDraw](cguipaper-methods.md) 方法。

放開滑鼠左鍵時，會收到 **WM \_ LBUTTONUP** 訊息。 [CGuiPaper：： InkStop](cguipaper-methods.md)方法會停止線條繪圖順序。

 

 




