---
title: 取消
description: WWSAPI 中的大部分作業都可以在執行期間取消。
ms.assetid: d73d76e1-bd78-40ce-9f92-e282b6b127ce
keywords:
- 取消 Windows 的 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf75bd8d07d8f78ddf0a5750e6f4f96feb073dc15b8e63ed23ab8ceb061de145
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841778"
---
# <a name="cancellation"></a>取消

WWSAPI 中的大部分作業都可以在執行期間取消。

您用來取消作業的函式取決於受影響的物件。

| 函式                                           | 描述                                                                                                            |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel)           | 取消指定通道上所有暫止的輸入和輸出，並將通道狀態設定為 WS \_ 通道狀態發生錯誤 \_ \_ 。 |
| [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)         | 取消指定接聽程式上所有暫止的輸入和輸出。                                                          |
| [**WsAbortServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy) | 取消指定的服務 proxy 上所有暫止的輸入和輸出。                                                     |
| [**WsAbortServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)   | 中斷並中止服務主機上的目前作業。                                                    |
| [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)             | 放棄呼叫，在指定的服務 proxy 上呼叫指定的呼叫。                                                        |



 

如需影響 [伺服器端服務作業](server-side-service-operations.md) 和服務模型回呼之取消的詳細資訊，請參閱 [呼叫取消](call-cancellation.md)。


 

 




