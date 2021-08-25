---
title: IAgentNotifySink
description: IAgentNotifySink
ms.assetid: vs|msagent|~\paface_2xet.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b43a092ddd9c50ff7aacb0254c4773a43005759ab23b6682aaf6484d5aef4839
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725778"
---
# <a name="iagentnotifysink"></a>IAgentNotifySink

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

IAgentNotifySink 會在發生特定狀態變更時通知用戶端。 這些函數也可從 [IAgentNotifySinkEx](iagentnotifysinkex.md)取得。

**依照 Vtable 順序的方法**



| IAgentNotifySink                                                      | 描述                                                                              |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**命令**](command-method.md)                                     | 當伺服器處理用戶端定義的命令時發生。                               |
| [**ActivateInputState**](iagentnotifysink--activateinputstate.md)    | 當字元變成或停止輸入-主動時發生。                            |
| [**BalloonVisibleState**](iagentnotifysink---balloonvisiblestate.md) | 當字元的 **可見** 狀態變更時發生。                                   |
| [**點選事件**](click-event.md)                                    | 發生于按一下字元時。                                                      |
| [**DblClick 事件**](dblclick-event.md)                              | 發生于按兩下字元時。                                               |
| [**DragStart**](/windows/desktop/lwef/dragstart-event)                                | 發生于使用者開始拖曳字元時。                                          |
| [**DragComplete**](https://www.bing.com/search?q=**DragComplete**)                          | 發生于使用者停止拖曳字元時。                                           |
| [**RequestStart**](iagentnotifysink--requeststart.md)                | 當伺服器開始處理 [**要求**](/windows/desktop/lwef/the-request-object) 物件時發生。    |
| [**RequestComplete**](iagentnotifysink--requestcomplete.md)          | 當伺服器完成處理 [**要求**](/windows/desktop/lwef/the-request-object) 物件時發生。 |
| [**書籤**](iagentnotifysink--bookmark.md)                        | 當伺服器處理書簽時發生。                                             |
| [**閒置**](iagentnotifysink--idle.md)                                | 當伺服器啟動或結束閒置處理時發生。                                   |
| [**移動**](iagentnotifysink--move.md)                                | 發生于移動字元時。                                                  |
| [**大小**](iagentnotifysink---size.md)                               | 當字元已調整大小時發生。                                                |
| [**BalloonVisibleState**](iagentnotifysink---balloonvisiblestate.md) | 發生于字元字組氣球的可見度狀態變更時。                  |



 

舊版 Microsoft Agent 支援的 IAgentNotifySink：： Restart 和 IAgentNotifySink：： Shutdown 事件現在已過時。 雖然支援回溯相容性，但伺服器不會再傳送這些事件。

 

 