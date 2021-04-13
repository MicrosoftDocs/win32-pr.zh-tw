---
title: 概觀
description: 在 [總覽] 區段中 (RPC) 導覽頁面的遠端程序呼叫。
ms.assetid: 49dc35c3-efd7-45a2-bec0-cd68ac150754
keywords:
- 遠端程序呼叫 RPC，描述
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ea90c08dc075fdd90ae604b0d347ba6ac5baf9a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301560"
---
# <a name="overviews"></a>概觀

遠端程序呼叫的這個部分 (RPC) 程式設計人員指南和參考包含一系列主題，可協助您瞭解分散式應用程式的程式設計和 RPC，如下所示：

-   [MICROSOFT Rpc 模型](microsoft-rpc-model.md) 概述用戶端-伺服器程式設計模型、分散式應用程式程式設計的標準，以及 microsoft RPC 如何運作的說明。
-   [安裝 RPC 程式設計環境](installing-the-rpc-programming-environment.md) 會告訴您如何安裝使用 Microsoft RPC 開發分散式應用程式所需的檔案和工具。
-   [建立 RPC 應用程式](building-rpc-applications.md) 描述 MIDL 編譯器和必要的環境，以使用 Microsoft RPC 來建立分散式應用程式。
-   [連接用戶端和伺服器](connecting-the-client-and-the-server.md) 可提供初始化和執行分散式應用程式之程式的總覽。
-   [教學](tutorial.md) 課程概要說明小型分散式應用程式的開發。 此範例示範開發分散式應用程式的所有步驟、您使用的工具，以及組成可執行程式的元件。
-   [Idl 和 ACF](the-idl-and-acf-files.md) 檔會描述用來指定遠端程序呼叫之介面的 IDL 和 ACF 檔案，以及控制如何處理這些檔案的 MIDL 編譯器參數。
-   [資料和語言功能](data-and-language-features.md) 示範如何使用標準資料類型。
-   [陣列和指標](arrays-and-pointers.md) 說明如何將陣列指標做為參數傳遞。
-   [管道](pipes.md) 描述如何使用具名管道做為遠端程序呼叫的傳輸機制。
-   系結[和控制碼](binding-and-handles.md)描述系結控制碼，這是可讓開發人員將呼叫的應用程式系結至遠端程式的資料結構。
-   [記憶體管理](memory-management.md) 提供有關如何在執行遠端程序呼叫時管理用戶端和伺服器上記憶體的概念。
-   [序列化服務](serialization-services.md) 描述編碼或解碼資料的方法。
-   [安全性](security.md) 描述在分散式應用程式中執行安全性功能的方法。
-   [安裝和設定 RPC 應用程式](installing-and-configuring-rpc-applications.md) 會討論如何安裝用戶端和伺服器應用程式，並說明如何設定名稱服務提供者和安全性服務。 本節也包含 RPC 的網路傳輸資訊。
-   [非同步 rpc](asynchronous-rpc.md) 會向 RPC 定義提供 Microsoft 非同步擴充的資訊。 非同步遠端程序呼叫會立即傳回，而不會等候輸出。 當遠端程式完成在伺服器上執行時，它會將傳回的資料傳回到用戶端。
-   [RPC 訊息佇列](rpc-message-queuing.md) 會說明 (MSMQ) 使用訊息佇列服務，這可讓使用者在網路和系統之間進行通訊，而不論目前的通訊應用程式和系統狀態為何。
-   [使用 rpc OVER HTTP 的遠端程序呼叫](remote-procedure-calls-using-rpc-over-http.md) 可讓 rpc 用戶端能夠安全地透過網際網路連線到 rpc 伺服器程式，並執行遠端程序呼叫。
-   [RPC 負載平衡](rpc-load-balancing.md) 說明如何在伺服器陣列中的多部 rpc 伺服器之間散發大量 RPC over HTTP 流量。
-   [範例](examples.md) 包含 Microsoft 平臺軟體發展人員套件隨附的範例 RPC 程式說明。

 

 




