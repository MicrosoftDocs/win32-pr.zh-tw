---
title: 非同步 RPC
description: 非同步遠端程序呼叫 (RPC) 是 Microsoft 擴充功能，可解決 Open Software Foundation \ 8211; 分散式運算環境 (憑證-DCE) 所定義的傳統 RPC 模型的數項限制。
ms.assetid: 2586c10e-8284-419f-a200-4f6b11953688
keywords:
- 遠端程序呼叫 RPC、說明、非同步 RPC
- 非同步 RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e36ac79a30fd01aeba1efb3cbd2b7cc741f26238
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093087"
---
# <a name="asynchronous-rpc"></a>非同步 RPC

非同步遠端程序呼叫 (RPC) 是 Microsoft 擴充功能，可解決開放式 Software Foundation –分散式運算環境 (憑證-DCE) 所定義的傳統 RPC 模型的數項限制。 非同步 RPC 會將遠端程序呼叫與其傳回值分隔開來，以解析傳統、同步 RPC 的下列限制：

-   **單一執行緒用戶端的多個未完成呼叫。** 在傳統的 RPC 模型中，遠端程序呼叫會封鎖用戶端，直到呼叫傳回為止。 這可防止用戶端有多個未完成的呼叫，同時仍然讓執行緒可以執行其他工作。
-   **較慢或延遲的用戶端。** 產生資料緩慢的用戶端可能會想要使用初始資料進行遠端程序呼叫，然後在產生時提供其他資料。 這與傳統的 (同步) RPC 不可行。
-   **慢或延遲的伺服器。** 需要很長時間才能完成的遠端程序呼叫，將會在工作的持續時間內結合分派執行緒。 使用非同步 RPC 時，伺服器可以啟動個別的 (非同步) 作業來處理要求，並在有可用的回復時將其傳回。 伺服器也可以在結果變成可用時，以累加方式傳送回復，而不需要在遠端呼叫期間系結分派執行緒。 藉由讓用戶端應用程式變成非同步，您可以防止較慢的伺服器不必要地將用戶端應用程式上傳。
-   **傳輸大量資料。** 在用戶端與伺服器之間傳輸大量資料（尤其是透過低速連結）會在傳輸期間，結合用戶端執行緒和伺服器管理員執行緒。 使用非同步 RPC 和管道時，資料傳輸可以累加方式進行，而不會封鎖用戶端或伺服器執行其他工作。

您可以利用 async 屬性來宣告函式，以利用非同步 RPC 機制 \[ [](/windows/desktop/Midl/async) \] 。 因為您會在屬性設定檔中進行此宣告 (ACF) ，所以不需要對介面定義語言進行任何變更 (IDL) 檔;非同步 RPC 對網路通訊協定沒有任何影響， (在用戶端和伺服器) 之間傳輸資料的方式。 這表示同步和非同步用戶端都可以與非同步伺服器應用程式進行通訊。

本節提供如何使用非同步 RPC 開發分散式應用程式的總覽。 下列各節會提供總覽：

-   [宣告非同步函式](declaring-asynchronous-functions.md)
-   [用戶端非同步 RPC](client-side-asynchronous-rpc.md)
-   [伺服器端非同步 RPC](server-side-asynchronous-rpc.md)
-   [非同步呼叫的因果順序](causal-ordering-of-asynchronous-calls.md)
-   [錯誤處理](error-handling.md)
-   [具名管道通訊協定上的非同步 RPC](asynchronous-rpc-over-the-named-pipe-protocol.md)
-   [使用具有 DCE 管道的非同步 RPC](using-asynchronous-rpc-with-dce-pipes.md)
-   [非同步 DCOM](asynchronous-dcom.md)

 

 