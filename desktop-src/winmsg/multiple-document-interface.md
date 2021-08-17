---
description: 本節將討論多個檔介面，這是定義應用程式使用者介面的規格，可讓使用者同時使用多份檔。
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\multipledocumentinterface.htm
title: 多個檔介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d579d1075f85fae7cd2d4ca6e63e1b8196c6d2118e33102cd511a1e468a18ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118705357"
---
# <a name="multiple-document-interface"></a>多個檔介面

\[許多新的和中繼使用者發現，使用 MDI 應用程式很難學習。 因此，您應該考慮您的使用者介面的其他模型。 不過，您可以針對不容易符合現有模型的應用程式使用 MDI。\]

多重文件介面 (MDI) 是一種規格，可定義應用程式的使用者介面，讓使用者能夠同時使用多份檔。

### <a name="in-this-section"></a>本節內容



| 主題                                                                              | 描述                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [關於多重文件介面](about-the-multiple-document-interface.md) | 描述多個檔介面。<br/>                                     |
| [使用多重文件介面](using-the-multiple-document-interface.md) | 說明如何執行與多個檔介面相關聯的工作。<br/> |
| [MDI 參考](multiple-document-interface-reference.md)                         | 包含 API 參考。<br/>                                                    |



 

### <a name="mdi-functions"></a>MDI 函數



| Name                                                 | 描述                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa)           | 建立 MDI 子視窗。 <br/>                                                                                                                                                                                                                                                                                                                                    |
| [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca)                 | 針對 MDI 框架視窗的視窗程式未處理的任何視窗訊息，提供預設處理。 所有未由視窗程式明確處理的視窗訊息都必須傳遞至 [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) 函式，而不是 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函數。 <br/>                              |
| [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca)           | 針對 MDI 子視窗的視窗程式未處理的任何視窗訊息，提供預設處理。 視窗程式未處理的視窗訊息必須傳遞至 [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) 函式，而不是傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函數。 <br/>                                             |
| [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) | 處理與指定的 MDI 用戶端視窗相關聯之 MDI 子視窗的視窗功能表命令的快速鍵按鍵。 此函式會將 [**wm 的 \_ KEYUP**](/windows/desktop/inputdev/wm-keyup) 和 [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) 訊息轉譯為 [**wm \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) 訊息，並將它們傳送至適當的 MDI 子視窗。 <br/> |



 

### <a name="mdi-messages"></a>MDI 訊息



| Name                                            | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ MDIACTI加值稅E**](wm-mdiactivate.md)       | 傳送至 MDI 用戶端視窗，指示用戶端視窗啟用不同的 MDI 子視窗。 <br/>                                                                                                                                                                                                                                                                                                                               |
| [**WM \_ MDICASCADE**](wm-mdicascade.md)         | 傳送至 MDI 用戶端視窗，以串聯格式排列其所有子視窗。 <br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**WM \_ MDICREATE**](wm-mdicreate.md)           | 傳送至 MDI 用戶端視窗，以建立 MDI 子視窗。 <br/>                                                                                                                                                                                                                                                                                                                                                                        |
| [**WM \_ MDIDESTROY**](wm-mdidestroy.md)         | 傳送至 MDI 用戶端視窗以關閉 MDI 子視窗。 <br/>                                                                                                                                                                                                                                                                                                                                                                         |
| [**WM \_ MDIGETACTIVE**](wm-mdigetactive.md)     | 傳送至 MDI 用戶端視窗，以抓取現用 MDI 子視窗的控制碼。 <br/>                                                                                                                                                                                                                                                                                                                                                |
| [**WM \_ MDIICONARRANGE**](wm-mdiiconarrange.md) | 傳送至 MDI 用戶端視窗，以排列所有最小化的 MDI 子視窗。 它不會影響未最小化的子視窗。 <br/>                                                                                                                                                                                                                                                                                                  |
| [**WM \_ MDIMAXIMIZE**](wm-mdimaximize.md)       | 傳送至 MDI 用戶端視窗，以將 MDI 子視窗最大化。 系統會調整子視窗的大小，使其用戶端區域填滿用戶端視窗。 系統會將子視窗的 [視窗] 功能表圖示放置在框架視窗的功能表列最右邊的位置，並將子視窗的 [還原] 圖示放在最左邊的位置。 系統也會將子視窗的標題列文字附加至框架視窗的標題列文字。 <br/> |
| [**WM \_ MDINEXT**](wm-mdinext.md)               | 傳送至 MDI 用戶端視窗，以啟動下一個或上一個子視窗。 <br/>                                                                                                                                                                                                                                                                                                                                                        |
| [**WM \_ MDIREFRESHMENU**](wm-mdirefreshmenu.md) | 傳送至 MDI 用戶端視窗，以重新整理 MDI 框架視窗的 [視窗] 功能表。 <br/>                                                                                                                                                                                                                                                                                                                                                   |
| [**WM \_ MDIRESTORE**](wm-mdirestore.md)         | 傳送至 MDI 用戶端視窗，從最大化或最小化的大小還原 MDI 子視窗。 <br/>                                                                                                                                                                                                                                                                                                                                      |
| [**WM \_ MDISETMENU**](wm-mdisetmenu.md)         | 傳送至 MDI 用戶端視窗，以取代 MDI 框架視窗的整個功能表、取代框架視窗的視窗功能表，或兩者。 <br/>                                                                                                                                                                                                                                                                                           |
| [**WM \_ MDITILE**](wm-mditile.md)               | 傳送至 MDI 用戶端視窗，以磚格式排列所有的 MDI 子視窗。 <br/>                                                                                                                                                                                                                                                                                                                                             |



 

### <a name="mdi-structures"></a>MDI 結構



| Name                                       | 描述                                                                                               |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) | 包含 MDI 子視窗之類別、標題、擁有者、位置和大小的相關資訊。 <br/> |



 

 

