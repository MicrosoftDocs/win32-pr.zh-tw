---
title: RPC 訊息佇列
description: 訊息佇列 (MSMQ) 可讓使用者在網路和系統之間進行通訊，而不論目前的通訊應用程式和系統狀態為何。
ms.assetid: f1c8665b-3754-4c2e-b3ac-bba1f4b329e1
keywords:
- 遠端程序呼叫 RPC、描述、訊息佇列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b72e9e35ec2aa1cc440c0d0356c681c4fe8548c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021862"
---
# <a name="rpc-message-queuing"></a>RPC 訊息佇列

訊息佇列 (MSMQ) 可讓使用者在網路和系統之間進行通訊，而不論目前的通訊應用程式和系統狀態為何。 應用程式會透過 MSMQ 維護的訊息佇列來傳送和接收訊息。 即使用戶端或伺服器應用程式不在執行中，訊息佇列仍會繼續運作。 訊息佇列提供：

-   **非同步通訊。** 透過 MSMQ 非同步通訊，用戶端應用程式可以將訊息傳送至伺服器，並立即傳回，即使目的電腦或伺服器程式沒有回應。
-   **保證訊息傳遞。** 當應用程式透過 MSMQ 傳送訊息時，即使目的地應用程式未同時執行，或者網路和系統離線，訊息還是會到達其目的地。
-   **路由及動態設定。** MSMQ 可透過異類網路提供彈性的路由。 您可以動態變更這類網路的設定，而不需要對系統和網路本身進行任何重大變更。
-   **未連接的訊息。** 使用 MSMQ 的應用程式不需要設定目標應用程式的直接會話。
-   [安全性](security.md)。 MSMQ 提供以 Windows 安全性為基礎的安全通訊，以及加密和數位簽章 (CryptoAPI) 的密碼編譯 API。
-   **排定優先順序的訊息。** MSMQ 會根據優先順序將訊息傳送到網路上，讓重要的應用程式更快進行通訊。

Microsoft RPC 將開放式 Software Foundation –資料通訊設備 (憑證-DCE) 模型，藉由允許分散式應用程式使用 MSMQ 做為傳輸，並控制其許多功能，來進行遠端程序呼叫。 這項功能可用於傳統的 RPC 應用程式，以及透過 **IRPCOptions** 介面，到 COM 應用程式。

> [!Note]  
> RPC 訊息佇列僅適用于 Windows 2000。 較新版本的 Windows 不支援 RPC 訊息佇列。

 

下列主題提供訊息佇列的總覽：

-   [訊息佇列服務架構總覽](overview-of-message-queuing-services-architecture.md)
-   [訊息和訊息佇列屬性](message-and-message-queue-properties.md)
-   [使用 MSMQ 做為 RPC 傳輸](using-msmq-as-an-rpc-transport.md)
-   [RPC 消息 \_ 佇列應用程式的系統需求](system-requirements-for-rpc-message-queuing-applications.md)
-   [開發 RPC-Message 佇列應用程式](developing-rpc-message-queuing-applications.md)
-   [MSMQ 安全性服務](msmq-security-services.md)

 

 




