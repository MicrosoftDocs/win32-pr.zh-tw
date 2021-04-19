---
description: 本節討論視窗程式。 每個視窗都有相關聯的視窗程式，可處理所有傳送或張貼至類別之視窗的訊息。
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\windowprocedures.htm
title: 視窗程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92ae68ba9b64557a6dc70d5c83788b8337648a2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988996"
---
# <a name="window-procedures"></a>視窗程式

每個視窗都有相關聯的視窗程式，這個函式會處理所有傳送或張貼至類別之視窗的訊息。 視窗外觀和行為的所有層面都取決於視窗程式對這些訊息的回應。

### <a name="in-this-section"></a>本節內容



| Name                                                         | 描述                                                                                                                                                                                                    |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [關於視窗程式](about-window-procedures.md)       | 討論視窗程式。 每個視窗都是特定視窗類別的成員。 視窗類別會決定個別視窗用來處理其訊息的預設視窗程式。<br/> |
| [使用視窗程式](using-window-procedures.md)       | 涵蓋如何執行與視窗程式相關聯的下列工作。<br/>                                                                                                                        |
| [視窗程式參考](window-procedure-reference.md) | 包含 API 參考。<br/>                                                                                                                                                                         |



 

### <a name="functions"></a>函式



| Name                                     | 描述                                                                                                                                                                                                                                                                                                   |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) | 將訊息資訊傳遞給指定的視窗程式。 <br/>                                                                                                                                                                                                                                     |
| [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)   | 呼叫預設視窗程式，為應用程式未處理的任何視窗訊息提供預設處理。 這個函式可確保處理每個訊息。 呼叫 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)時所使用的參數，與視窗程式所收到的參數相同。 <br/> |
| [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))           | 處理傳送至視窗之訊息的應用程式定義函數。 **WNDPROC** 型別定義此回呼函數的指標。 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 是應用程式定義函數名稱的預留位置。 <br/>                                                            |



 

 

 
