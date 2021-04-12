---
title: 動畫控制項
description: 本章節包含與動畫控制項搭配使用之程式設計項目的相關資訊。
ms.assetid: 16994f93-e0fd-4c71-9c8a-15642408b8de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2a3fc7377c7258ba49b5a4188e6074270b5862
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463793"
---
# <a name="animation-control"></a>動畫控制項

本章節包含與動畫控制項搭配使用之程式設計項目的相關資訊。

### <a name="overviews"></a>概觀



| 主題                                                      | 目錄                                                                                                                                                                                                                           |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [關於動畫控制項](animation-control-overview.md) | *動畫控制項* 是顯示 Audio-Video 交錯 (AVI) 剪輯的視窗。 AVI 剪輯是一系列的點陣圖框架，例如電影。 動畫控制項只能顯示不包含音訊的 AVI 剪輯。<br/> |
| [使用動畫控制項](using-animation-control.md)    | 本節提供動畫控制項的執行詳細資料與範例程式碼。<br/>                                                                                                                                      |



 

### <a name="macros"></a>巨集



| 主題                                           | 目錄                                                                                                                                                                                                                                                          |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**動畫 \_ 關閉**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close)         | 關閉 AVI 剪輯。 您可以使用這個宏，或明確地傳送未傳遞的 [**\_ 開啟**](acm-open.md) 訊息，傳遞 **Null** 參數。 <br/>                                                                                                              |
| [**\_建立動畫**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create)       | 建立動畫控制項。 [**動畫 \_Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) 會呼叫 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) 函數來建立動畫控制項。 <br/>                                                                                   |
| [**動畫 \_ >isplaying**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) | 檢查是否現正播放 AVI 剪輯。 您可以使用此宏或傳送進行中的 [**\_ >isplaying**](acm-isplaying.md) 訊息。<br/>                                                                                                                            |
| [**\_開啟動畫**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open)           | 開啟 AVI 剪輯，並在動畫控制項中顯示其第一個畫面格。 您可以使用這個宏，或明確地傳送未執行的 [**\_ 開啟**](acm-open.md) 訊息。 <br/>                                                                                          |
| [**動畫 \_ OpenEx**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex)       | 從指定模組中的資源開啟 AVI 剪輯，並在動畫控制項中顯示其第一個畫面格。 您可以使用這個宏，或明確地傳送未執行的 [**\_ 開啟**](acm-open.md) 訊息。 <br/>                                                    |
| [**動畫 \_ 播放**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play)           | 在動畫控制項中播放 AVI 剪輯。 當執行緒繼續執行時，控制項會在背景中播放剪輯。 您可以使用這個宏，或明確地傳送未執行的 [**\_ 播放**](acm-play.md) 訊息。 <br/>                                    |
| [**建立 \_ 搜尋動畫**](/windows/desktop/api/Commctrl/nf-commctrl-animate_seek)           | 指示動畫控制項顯示 AVI 剪輯的特定框架。 當執行緒繼續執行時，控制項會在背景中顯示剪輯。 您可以使用這個宏，或明確地傳送未執行的 [**\_ 播放**](acm-play.md) 訊息。 <br/> |
| [**動畫 \_ 停止**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop)           | 停止在動畫控制項中播放 AVI 剪輯。 您可以使用這個宏，或明確地傳送未進行的「執行的 [**\_ 停止**](acm-stop.md) 」訊息。 <br/>                                                                                                               |



 

### <a name="messages"></a>訊息



| 主題                                   | 目錄                                                                                                                                                                                                                                   |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_>ISPLAYING**](acm-isplaying.md) | 檢查是否現正播放 AVI 剪輯。 您可以明確地傳送此訊息，或使用 [**動畫 \_ >isplaying**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) 宏。<br/>                                                                                   |
| [**\_開啟的狀態**](acm-open.md)           | 開啟 AVI 剪輯，並在動畫控制項中顯示其第一個畫面格。 您可以明確地傳送此訊息，或使用 [**動畫 \_ 開啟**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) 或 [**\_ OpenEx**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) 宏的動畫。 <br/>              |
| [**未通過的 \_ PLAY**](acm-play.md)           | 在動畫控制項中播放 AVI 剪輯。 當執行緒繼續執行時，控制項會在背景中播放剪輯。 您可以明確地傳送此訊息，或使用 [**動畫 \_ 播放**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play) 宏。<br/> |
| [**進行中的 \_ 停止**](acm-stop.md)           | 停止在動畫控制項中播放 AVI 剪輯。 您可以明確地傳送此訊息，或使用 [**動畫 \_ 停**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop) 用宏來傳送。<br/>                                                                            |



 

### <a name="notifications"></a>通知



| 主題                           | 目錄                                                                                                                                                                                                       |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ACN \_ 開始**](acn-start.md) | 通知動畫控制項的父視窗，相關聯的 AVI 剪輯已開始播放。 此通知碼會以 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息的形式傳送。 <br/>      |
| [**ACN \_ 停止**](acn-stop.md)   | 通知動畫控制項的父視窗，相關聯的 AVI 剪輯已停止播放。 此通知碼會以 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息的形式傳送。 <br/> |



 

### <a name="constants"></a>常數



| 主題                                                        | 目錄                                                                      |
|--------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**動畫控制項樣式**](animation-control-styles.md) | 此區段會列出與動畫控制項搭配使用的視窗樣式。<br/> |



 

 

