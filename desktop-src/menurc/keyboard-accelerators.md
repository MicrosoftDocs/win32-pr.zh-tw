---
title: 鍵盤快速操作
description: 本節討論鍵盤加速器。 鍵盤對應鍵是為應用程式產生命令訊息的按鍵或按鍵組合。
ms.assetid: vs|winui|~\winui\windowsuserinterface\userinput\keyboardaccelerators.htm
keywords:
- 使用者輸入，鍵盤快速鍵
- 捕獲使用者輸入，鍵盤快捷
- 鍵盤加速器
- 加速器
- WM_COMMAND 訊息
- WM_SYS 命令訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df67f4879edc2e0e81a8715155bf2edfac05f1e5ce9d3557f9b051ae682a6afa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118734466"
---
# <a name="keyboard-accelerators"></a>鍵盤快速操作

*鍵盤快捷* (或快速鍵) ，是為應用程式產生 [**WM \_ 命令**](wm-command.md)或 [**WM \_ SYSCOMMAND**](wm-syscommand.md)訊息的按鍵或按鍵組合。

### <a name="in-this-section"></a>本節內容



| 名稱                                                                 | 描述                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------|
| [關於鍵盤加速器](about-keyboard-accelerators.md)       | 討論鍵盤加速器。<br/>                                |
| [使用鍵盤加速器](using-keyboard-accelerators.md)       | 討論與鍵盤快速鍵相關聯的工作。<br/> |
| [鍵盤快速鍵參考](keyboard-accelerator-reference.md) | 包含 API 參考。<br/>                                     |



 

### <a name="keyboard-accelerator-functions"></a>鍵盤對應函式



| 名稱                                                       | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CopyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-copyacceleratortablea)       | 複製指定的快速鍵對應表。 此函數是用來取得對應于快速鍵表控制碼的快速鍵對應表資料，或用來決定快速鍵資料表資料的大小。 <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea)   | 建立快速鍵對應表。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) | 終結快速鍵對應表。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa)               | 載入指定的快速鍵對應表。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora)       | 處理功能表命令的快速鍵。 如果指定的快速鍵對應) 表中有索引鍵的專案，則函式會將 [**wm 的 \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) 或 [**wm \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) 訊息轉譯為 [**wm \_ 命令**](wm-command.md) 或 [**wm \_ SYSCOMMAND**](wm-syscommand.md) 訊息 (，然後直接將 **wm \_ 命令** 或 **wm \_ SYSCOMMAND** 訊息傳送至指定的視窗程式。 在視窗程式處理訊息之前， [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora)不會傳回。 <br/> |



 

### <a name="keyboard-accelerator-messages"></a>鍵盤快捷按鍵訊息



| 名稱                                          | 描述                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) | 傳送以表示 UI 狀態應變更。<br/>                                                                                                                                                                                                                                                  |
| [**WM \_ INITMENU**](wm-initmenu.md)           | 當功能表即將變成作用中時傳送。 當使用者按一下功能表列上的專案，或按下功能表鍵時，就會發生此問題。 這可讓應用程式在功能表顯示前修改功能表。 <br/> 視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。 <br/> |
| [**WM \_ QUERYUISTATE**](wm-queryuistate.md)   | 傳送以取得視窗的 UI 狀態。<br/>                                                                                                                                                                                                                                                            |
| [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) | 傳送以變更指定視窗及其所有子視窗的 UI 狀態。<br/>                                                                                                                                                                                                                        |



 

### <a name="keyboard-accelerator-notifications"></a>鍵盤快速鍵通知



| 名稱                                          | 描述                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ INITMENUPOPUP**](wm-initmenupopup.md) | 當下拉功能表或子功能表即將變成作用中時傳送。 這可讓應用程式在功能表顯示前修改功能表，而不需要變更整個功能表。 <br/>                                                                                                                                              |
| [**WM \_ MENUCHAR**](wm-menuchar.md)           | 當功能表在使用中，且使用者按下未對應至任何助憶鍵或快速鍵的按鍵時傳送。 這則訊息會傳送至擁有功能表的視窗。 <br/>                                                                                                                                             |
| [**WM \_ MENUSELECT**](wm-menuselect.md)       | 當使用者選取功能表項目時，傳送至功能表的擁有者視窗。 <br/>                                                                                                                                                                                                                                                      |
| [**WM \_ SYSCHAR**](wm-syschar.md)             | 當 [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)函數轉譯了 [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown)訊息時，以鍵盤焦點張貼至視窗。 它會指定系統字元索引鍵的字元碼，也就是在 ALT 鍵關閉時按下的字元按鍵。 <br/> |
| [**WM \_ SYSCOMMAND**](wm-syscommand.md)       | 當使用者選擇 [ **視窗]** 功能表中的命令，或當使用者選擇 [最大化] 按鈕、最小化按鈕、還原按鈕或 [關閉] 按鈕時，視窗就會收到此訊息。<br/>                                                                                                                                |



 

### <a name="keyboard-accelerator-structures"></a>鍵盤加速器結構



| 名稱                   | 描述                                                          |
|------------------------|----------------------------------------------------------------------|
| [**ACCEL**](/windows/win32/api/winuser/ns-winuser-accel) | 定義快速鍵對應表中使用的快速鍵。 <br/> |



 

 

