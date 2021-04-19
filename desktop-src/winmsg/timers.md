---
description: 本主題討論計時器。 計時器是一種內部常式，可重複測量指定的間隔（以毫秒為單位）。
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\timers.htm
title: 計時器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fa44be05acc09eafed550a200ed6bc61f79daa2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994540"
---
# <a name="timers"></a>計時器

計時器是一種內部常式，可重複測量指定的間隔（以毫秒為單位）。

### <a name="in-this-section"></a>本節內容



| Name                                   | 描述                                                                                                               |
|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [關於計時器](about-timers.md)       | 描述如何建立、識別、設定和刪除計時器。<br/>                                                     |
| [使用計時器](using-timers.md)       | 討論如何建立和終結計時器，以及如何使用計時器以指定的間隔來陷印滑鼠輸入。<br/> |
| [計時器參考](timer-reference.md) | 包含 API 參考。<br/>                                                                                    |



 

### <a name="timer-functions"></a>Timer 函數



| Name                           | 描述                                                                                                                                                                                                                                                              |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**KillTimer**](/windows/win32/api/winuser/nf-winuser-killtimer) | 終結指定的計時器。 <br/>                                                                                                                                                                                                                                |
| [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer)   | 使用指定的超時時間值建立計時器。<br/>                                                                                                                                                                                                            |
| [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc)   | 處理 [**WM \_ 計時器**](wm-timer.md) 訊息的應用程式定義回呼函數。 **TIMERPROC** 型別定義此回呼函數的指標。 [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) 是應用程式定義函數名稱的預留位置。 <br/> |



 

### <a name="timer-notifications"></a>計時器通知



| Name                          | 描述                                                                                                                                                                                     |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ 計時器**](wm-timer.md) | 當計時器到期時，張貼至安裝執行緒的訊息佇列。 此訊息是由 [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) 或 [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) 函數所張貼。 <br/> |



 

 

 
