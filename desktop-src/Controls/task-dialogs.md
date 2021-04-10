---
title: 工作對話方塊
description: 本章節包含與工作對話方塊搭配使用之程式設計項目的相關資訊。 工作對話方塊類似于，它比基本訊息方塊更有彈性。
ms.assetid: vs|controls|~\controls\taskdialogs\taskdialogs.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4f115531b9f872c824e9d1822be07777b2bc439
ms.sourcegitcommit: 0c786b1682063d0cae0fc43180945183fa2c7981
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/24/2020
ms.locfileid: "103842880"
---
# <a name="task-dialog"></a>工作對話方塊

本章節包含與工作對話方塊搭配使用之程式設計項目的相關資訊。 工作 *對話方塊* 類似于，它比基本訊息方塊更有彈性。

### <a name="overviews"></a>概觀



| 主題                                           | 目錄                                            |
|-------------------------------------------------|-----------------------------------------------------|
| [關於工作對話方塊](task-dialogs-overview.md) | 描述工作對話方塊的元素。<br/> |



 

### <a name="functions"></a>函式



| 主題                                                  | 目錄                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TaskDialog**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialog)                       | 建立、顯示及操作工作對話方塊。 工作對話方塊包含應用程式定義郵件內文和標題、圖示，以及任何預先定義之推播按鈕的組合。 此函式不支援註冊回呼函數來接收通知。<br/>                                                                                                                |
| [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) | 搭配 [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) 函數使用的應用程式定義函數。 當發生各種事件時，它會從工作對話方塊接收訊息。<br/> **PFTASKDIALOGCALLBACK** 型別定義此回呼函數的指標。 [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) 是應用程式定義函數名稱的預留位置。<br/> |
| [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)       | 建立、顯示及操作工作對話方塊。 工作對話方塊包含應用程式定義的圖示、訊息、標題、驗證核取方塊、命令連結、推播按鈕和選項按鈕。 此函式可以註冊回呼函式來接收通知訊息。<br/>                                                                                                               |



 

### <a name="messages"></a>訊息



| 主題                                                                                           | 目錄                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TDM \_ CLICK \_ 按鈕**](tdm-click-button.md)                                                  | 模擬按鈕在工作對話方塊中按一下的動作。<br/>                                                                                                                                  |
| [**TDM \_ 按一下 \_ 單選 \_ 按鈕**](tdm-click-radio-button.md)                                     | 模擬選項按鈕在工作對話方塊中按一下的動作。<br/>                                                                                                                            |
| [**TDM \_ CLICK \_ 驗證**](tdm-click-verification.md)                                      | 模擬驗證核取方塊的動作在工作對話方塊中按一下。<br/>                                                                                                                   |
| [**[TDM \_ 啟用] \_ 按鈕**](tdm-enable-button.md)                                                | 啟用或停用工作對話方塊中的 [推送] 按鈕。<br/>                                                                                                                                       |
| [**TDM \_ 啟用 \_ 單選 \_ 按鈕**](tdm-enable-radio-button.md)                                   | 啟用或停用工作對話方塊中的選項按鈕。<br/>                                                                                                                                      |
| [**TDM \_ 流覽 \_ 頁面**](tdm-navigate-page.md)                                                | 以新的內容重新建立工作對話方塊，模擬多頁 wizard 的功能。<br/>                                                                                           |
| [**TDM \_ 設定 \_ 按鈕提高 \_ 許可權的 \_ \_ 狀態**](tdm-set-button-elevation-required-state.md) | 指定指定的工作對話方塊按鈕或命令連結是否應該有 (UAC) 盾牌圖示的使用者帳戶控制;亦即，按鈕叫用的動作是否需要提高許可權。 <br/> |
| [**TDM \_ 設定 \_ 元素 \_ 文字**](tdm-set-element-text.md)                                         | 更新工作對話方塊中的文字專案。<br/>                                                                                                                                                  |
| [**TDM \_ SET \_ 天棚 \_ 進度 \_ 列**](tdm-set-marquee-progress-bar.md)                        | 指出裝載的進度列是否應顯示在捲軸模式中。<br/>                                                                                                            |
| [**TDM \_ 設定 \_ 進度 \_ 列 \_ 捲軸**](tdm-set-progress-bar-marquee.md)                        | 啟動和停止進度列的字幕顯示，並設定捲軸的速度。<br/>                                                                                              |
| [**TDM \_ 設定 \_ 進度 \_ 列 \_ POS**](tdm-set-progress-bar-pos.md)                                | 設定進度列的目前位置。<br/>                                                                                                                                             |
| [**TDM \_ 設定 \_ 進度 \_ 列 \_ 範圍**](tdm-set-progress-bar-range.md)                            | 設定主控進度列的最小值和最大值。<br/>                                                                                                                          |
| [**TDM \_ 設定 \_ 進度 \_ 列 \_ 狀態**](tdm-set-progress-bar-state.md)                            | 設定進度列的目前狀態。<br/>                                                                                                                                               |
| [**TDM \_ UPDATE \_ 元素 \_ 文字**](tdm-update-element-text.md)                                   | 更新工作對話方塊中的文字專案。 <br/>                                                                                                                                                 |
| [**TDM \_ 更新 \_ 圖示**](tdm-update-icon.md)                                                    | 重新整理工作對話方塊的圖示。 <br/>                                                                                                                                                     |



 

### <a name="notifications"></a>通知



| 主題                                                           | 目錄                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [TDN 按鈕已按下 \_ \_](tdn-button-clicked.md)                  | 當使用者選取工作對話方塊中的按鈕或命令連結時，由工作對話方塊傳送。 此通知碼只會透過工作對話方塊回呼函式接收，此函式可以使用 [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) 方法來註冊。<br/>                                                                                                                                                                                                   |
| [TDN 已 \_ 建立](tdn-created.md)                                 | 在工作對話方塊建立之後和顯示之前，由工作對話方塊傳送。 此通知碼只會透過工作對話方塊回呼函式接收，此函式可以使用 [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) 方法來註冊。 <br/>                                                                                                                                                                                                  |
| [TDN \_ 損毀](tdn-destroyed.md)                             | 當工作對話方塊終結時傳送，而且其視窗控制碼不再有效。 此通知碼只會透過工作對話方塊回呼函式接收，此函式可以使用 [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) 方法來註冊。<br/>                                                                                                                                                                                                       |
| [TDN \_ 對話方塊已建立 \_](tdn-dialog-constructed.md)          | 在工作對話方塊建立之後和顯示之前，由工作對話方塊傳送。 此通知碼只會透過工作對話方塊回呼函式接收，此函式可以使用 [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) 方法來註冊。 <br/>                                                                                                                                                                                                  |
| [已 \_ 按一下 TDN EXPANDO \_ 按鈕 \_](tdn-expando-button-clicked.md) | 當使用者按一下工作對話方塊的 expando 按鈕時，由工作對話方塊傳送。 此通知碼只會透過工作對話方塊回呼函式接收，此函式可以使用 [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) 方法來註冊。<br/>                                                                                                                                                                                                            |
| [TDN \_ 說明](tdn-help.md)                                       | 當使用者在工作對話方塊具有焦點時按下鍵盤上的 F1 時，由工作對話方塊傳送。 此通知碼只會透過工作對話方塊回呼函式接收，此函式可以使用 [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) 方法來註冊。<br/>                                                                                                                                                                                            |
| [已 \_ 按一下的 TDN 超連結 \_](tdn-hyperlink-clicked.md)            | 當使用者按一下工作對話方塊內容中的超連結時，由工作對話方塊傳送。 此通知碼只會透過工作對話方塊回呼函式接收，此函式可以使用 [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) 方法來註冊。 <br/>                                                                                                                                                                                                        |
| [TDN \_ 流覽](tdn-navigated.md)                             | 在流覽發生時由工作對話方塊傳送。 此通知碼只會透過工作對話方塊回呼函式接收，此函式可以使用 [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) 方法來註冊。 <br/>                                                                                                                                                                                                                                     |
| [已 \_ 按一下 TDN 單選 \_ 按鈕 \_](tdn-radio-button-clicked.md)     | 當使用者選取工作對話方塊中的按鈕或命令連結時，由工作對話方塊傳送。 此通知碼只會透過工作對話方塊回呼函式接收，此函式可以使用 [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) 方法來註冊。 <br/>                                                                                                                                                                                                  |
| [TDN \_ 計時器](tdn-timer.md)                                     | 工作對話方塊大約每隔200毫秒傳送一次。 當已 \_ \_ 在傳遞給 [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)函式的 [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig)結構的 **dwFlags** 成員中設定 .tdf 回呼計時器旗標時，就會傳送此通知碼。 此通知碼只會透過工作對話方塊回呼函式接收，此函式可以使用 **TaskDialogIndirect** 方法來註冊。<br/> |
| [已 \_ 按一下 TDN 驗證 \_](tdn-verification-clicked.md)      | 當使用者按一下工作對話方塊驗證核取方塊時，由工作對話方塊傳送。 此通知碼只會透過工作對話方塊回呼函式接收，此函式可以使用 [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) 方法來註冊。<br/>                                                                                                                                                                                                       |



 

### <a name="structures"></a>結構



| 主題                                           | 目錄                                                                                                                                                   |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TASKDIALOG \_ 按鈕**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialog_button) | 包含用來在工作對話方塊中顯示按鈕的資訊。 [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig)結構會使用此結構。<br/> |
| [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig)    | 包含用來顯示工作對話方塊的資訊。 [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)函式會使用此結構。<br/>          |



 

 

