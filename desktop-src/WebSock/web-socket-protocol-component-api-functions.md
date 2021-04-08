---
title: WebSocket 通訊協定元件 API 函數
description: WebSocket 通訊協定元件 API 會定義這些函式。
ms.assetid: B833D18D-286C-4D32-A9C7-D5D5806EC306
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d778fef6680112007b0f4a459787a51eb20bfe0d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682728"
---
# <a name="websocket-protocol-component-api-functions"></a>WebSocket 通訊協定元件 API 函數

WebSocket 通訊協定元件 API 會定義這些函式。

## <a name="in-this-section"></a>本節內容



| 主題                                                                             | 描述                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WebSocketAbortHandle**](/windows/desktop/api/Websocket/nf-websocket-websocketaborthandle)<br/>                   | 中止 [**WebSocketCreateClientHandle**](/windows/desktop/api/websocket/nf-websocket-websocketcreateclienthandle) 或 [**WebSocketCreateServerHandle**](/windows/desktop/api/websocket/nf-websocket-websocketcreateserverhandle)所建立的 WebSocket 會話控制碼。<br/>   |
| [**WebSocketBeginClientHandshake**](/windows/desktop/api/Websocket/nf-websocket-websocketbeginclienthandshake)<br/> | 開始用戶端交握。<br/>                                                                                                                                                                |
| [**WebSocketBeginServerHandshake**](/windows/desktop/api/Websocket/nf-websocket-websocketbeginserverhandshake)<br/> | 開始伺服器端信號交換。<br/>                                                                                                                                                                |
| [**WebSocketCompleteAction**](/windows/desktop/api/Websocket/nf-websocket-websocketcompleteaction)<br/>             | 完成 [**WebSocketGetAction**](/windows/desktop/api/websocket/nf-websocket-websocketgetaction)啟動的動作。<br/>                                                                                                             |
| [**WebSocketCreateClientHandle**](/windows/desktop/api/Websocket/nf-websocket-websocketcreateclienthandle)<br/>     | 建立用戶端 WebSocket 會話控制碼。<br/>                                                                                                                                                  |
| [**WebSocketCreateServerHandle**](/windows/desktop/api/Websocket/nf-websocket-websocketcreateserverhandle)<br/>     | 建立伺服器端 WebSocket 會話控制碼。<br/>                                                                                                                                                  |
| [**WebSocketDeleteHandle**](/windows/desktop/api/Websocket/nf-websocket-websocketdeletehandle)<br/>                 | 刪除由 [**WebSocketCreateClientHandle**](/windows/desktop/api/websocket/nf-websocket-websocketcreateclienthandle) 或 [**WebSocketCreateServerHandle**](/windows/desktop/api/websocket/nf-websocket-websocketcreateserverhandle)所建立的 WebSocket 會話控制碼。<br/>  |
| [**WebSocketEndClientHandshake**](/windows/desktop/api/Websocket/nf-websocket-websocketendclienthandshake)<br/>     | 完成用戶端交握。<br/>                                                                                                                                                             |
| [**WebSocketEndServerHandshake**](/windows/desktop/api/Websocket/nf-websocket-websocketendserverhandshake)<br/>     | 完成伺服器端信號交換。<br/>                                                                                                                                                             |
| [**WebSocketGetAction**](/windows/desktop/api/Websocket/nf-websocket-websocketgetaction)<br/>                       | 傳回 [**WebSocketSend**](/windows/desktop/api/websocket/nf-websocket-websocketsend)、 [**WebSocketReceive**](/windows/desktop/api/websocket/nf-websocket-websocketreceive) 或 [**WebSocketCompleteAction**](/windows/desktop/api/websocket/nf-websocket-websocketcompleteaction)呼叫的動作。<br/> |
| [**WebSocketGetGlobalProperty**](/windows/desktop/api/Websocket/nf-websocket-websocketgetglobalproperty)<br/>       | 取得單一 WebSocket 屬性。<br/>                                                                                                                                                                |
| [**WebSocketReceive**](/windows/desktop/api/Websocket/nf-websocket-websocketreceive)<br/>                           | 將接收作業加入至通訊協定元件作業佇列。<br/>                                                                                                                              |
| [**WebSocketSend**](/windows/desktop/api/Websocket/nf-websocket-websocketsend)<br/>                                 | 將傳送作業加入至通訊協定元件作業佇列。<br/>                                                                                                                                 |



 

 

