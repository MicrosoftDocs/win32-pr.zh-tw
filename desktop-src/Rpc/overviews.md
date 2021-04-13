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
# <a name="overviews"></a><span data-ttu-id="1c6b4-104">概觀</span><span class="sxs-lookup"><span data-stu-id="1c6b4-104">Overviews</span></span>

<span data-ttu-id="1c6b4-105">遠端程序呼叫的這個部分 (RPC) 程式設計人員指南和參考包含一系列主題，可協助您瞭解分散式應用程式的程式設計和 RPC，如下所示：</span><span class="sxs-lookup"><span data-stu-id="1c6b4-105">This portion of the Remote Procedure Call (RPC) Programmer's Guide and Reference consists of a sequence of topics that will help you understand distributed application programming and RPC as follows:</span></span>

-   <span data-ttu-id="1c6b4-106">[MICROSOFT Rpc 模型](microsoft-rpc-model.md) 概述用戶端-伺服器程式設計模型、分散式應用程式程式設計的標準，以及 microsoft RPC 如何運作的說明。</span><span class="sxs-lookup"><span data-stu-id="1c6b4-106">[Microsoft RPC Model](microsoft-rpc-model.md) provides an overview of the client-server programming model, standards for distributed application programming, and a description of how Microsoft RPC works.</span></span>
-   <span data-ttu-id="1c6b4-107">[安裝 RPC 程式設計環境](installing-the-rpc-programming-environment.md) 會告訴您如何安裝使用 Microsoft RPC 開發分散式應用程式所需的檔案和工具。</span><span class="sxs-lookup"><span data-stu-id="1c6b4-107">[Installing The RPC Programming Environment](installing-the-rpc-programming-environment.md) tells how to install the files and tools needed to develop distributed applications with Microsoft RPC.</span></span>
-   <span data-ttu-id="1c6b4-108">[建立 RPC 應用程式](building-rpc-applications.md) 描述 MIDL 編譯器和必要的環境，以使用 Microsoft RPC 來建立分散式應用程式。</span><span class="sxs-lookup"><span data-stu-id="1c6b4-108">[Building RPC Applications](building-rpc-applications.md) describes the MIDL compiler and the necessary environment for building distributed applications with Microsoft RPC.</span></span>
-   <span data-ttu-id="1c6b4-109">[連接用戶端和伺服器](connecting-the-client-and-the-server.md) 可提供初始化和執行分散式應用程式之程式的總覽。</span><span class="sxs-lookup"><span data-stu-id="1c6b4-109">[Connecting the Client and the Server](connecting-the-client-and-the-server.md) provides an overview of the process of initializing and running distributed applications.</span></span>
-   <span data-ttu-id="1c6b4-110">[教學](tutorial.md) 課程概要說明小型分散式應用程式的開發。</span><span class="sxs-lookup"><span data-stu-id="1c6b4-110">[Tutorial](tutorial.md) provides an overview of the development of a small distributed application.</span></span> <span data-ttu-id="1c6b4-111">此範例示範開發分散式應用程式的所有步驟、您使用的工具，以及組成可執行程式的元件。</span><span class="sxs-lookup"><span data-stu-id="1c6b4-111">This example demonstrates all the steps in developing a distributed application, the tools you use, and the components that make up the executable programs.</span></span>
-   <span data-ttu-id="1c6b4-112">[Idl 和 ACF](the-idl-and-acf-files.md) 檔會描述用來指定遠端程序呼叫之介面的 IDL 和 ACF 檔案，以及控制如何處理這些檔案的 MIDL 編譯器參數。</span><span class="sxs-lookup"><span data-stu-id="1c6b4-112">[IDL and ACF Files](the-idl-and-acf-files.md) describes the IDL and ACF files used to specify the interface to the remote procedure call and the MIDL compiler switches that control how these files are processed.</span></span>
-   <span data-ttu-id="1c6b4-113">[資料和語言功能](data-and-language-features.md) 示範如何使用標準資料類型。</span><span class="sxs-lookup"><span data-stu-id="1c6b4-113">[Data and Language Features](data-and-language-features.md) demonstrates the use of standard data types.</span></span>
-   <span data-ttu-id="1c6b4-114">[陣列和指標](arrays-and-pointers.md) 說明如何將陣列指標做為參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="1c6b4-114">[Arrays and Pointers](arrays-and-pointers.md) explains how to pass arrays pointers as parameters.</span></span>
-   <span data-ttu-id="1c6b4-115">[管道](pipes.md) 描述如何使用具名管道做為遠端程序呼叫的傳輸機制。</span><span class="sxs-lookup"><span data-stu-id="1c6b4-115">[Pipes](pipes.md) describes how to use named pipes as the transport mechanism for remote procedure calls.</span></span>
-   <span data-ttu-id="1c6b4-116">系結[和控制碼](binding-and-handles.md)描述系結控制碼，這是可讓開發人員將呼叫的應用程式系結至遠端程式的資料結構。</span><span class="sxs-lookup"><span data-stu-id="1c6b4-116">[Binding and Handles](binding-and-handles.md) describes the binding handle — the data structure that allows the developer to bind the calling application to the remote procedure.</span></span>
-   <span data-ttu-id="1c6b4-117">[記憶體管理](memory-management.md) 提供有關如何在執行遠端程序呼叫時管理用戶端和伺服器上記憶體的概念。</span><span class="sxs-lookup"><span data-stu-id="1c6b4-117">[Memory Management](memory-management.md) offers ideas about how to manage memory on the client and server when performing remote procedure calls.</span></span>
-   <span data-ttu-id="1c6b4-118">[序列化服務](serialization-services.md) 描述編碼或解碼資料的方法。</span><span class="sxs-lookup"><span data-stu-id="1c6b4-118">[Serialization Services](serialization-services.md) describes the methods for encoding or decoding data.</span></span>
-   <span data-ttu-id="1c6b4-119">[安全性](security.md) 描述在分散式應用程式中執行安全性功能的方法。</span><span class="sxs-lookup"><span data-stu-id="1c6b4-119">[Security](security.md) describes the methods for implementing security features in your distributed applications.</span></span>
-   <span data-ttu-id="1c6b4-120">[安裝和設定 RPC 應用程式](installing-and-configuring-rpc-applications.md) 會討論如何安裝用戶端和伺服器應用程式，並說明如何設定名稱服務提供者和安全性服務。</span><span class="sxs-lookup"><span data-stu-id="1c6b4-120">[Installing and Configuring RPC Applications](installing-and-configuring-rpc-applications.md) discusses installing your client and server applications, describes how to configure the name service provider and the security service.</span></span> <span data-ttu-id="1c6b4-121">本節也包含 RPC 的網路傳輸資訊。</span><span class="sxs-lookup"><span data-stu-id="1c6b4-121">This section also contains network transport information for RPC.</span></span>
-   <span data-ttu-id="1c6b4-122">[非同步 rpc](asynchronous-rpc.md) 會向 RPC 定義提供 Microsoft 非同步擴充的資訊。</span><span class="sxs-lookup"><span data-stu-id="1c6b4-122">[Asynchronous RPC](asynchronous-rpc.md) presents information on the Microsoft asynchronous extensions to the RPC definition.</span></span> <span data-ttu-id="1c6b4-123">非同步遠端程序呼叫會立即傳回，而不會等候輸出。</span><span class="sxs-lookup"><span data-stu-id="1c6b4-123">Asynchronous remote procedure calls return immediately without waiting for output.</span></span> <span data-ttu-id="1c6b4-124">當遠端程式完成在伺服器上執行時，它會將傳回的資料傳回到用戶端。</span><span class="sxs-lookup"><span data-stu-id="1c6b4-124">When the remote procedure finishes executing on the server, it transfers return data to the client.</span></span>
-   <span data-ttu-id="1c6b4-125">[RPC 訊息佇列](rpc-message-queuing.md) 會說明 (MSMQ) 使用訊息佇列服務，這可讓使用者在網路和系統之間進行通訊，而不論目前的通訊應用程式和系統狀態為何。</span><span class="sxs-lookup"><span data-stu-id="1c6b4-125">[RPC Message Queuing](rpc-message-queuing.md) describes the use of the Message Queuing Service (MSMQ), which lets users communicate across networks and systems regardless of the current state of the communicating applications and systems.</span></span>
-   <span data-ttu-id="1c6b4-126">[使用 rpc OVER HTTP 的遠端程序呼叫](remote-procedure-calls-using-rpc-over-http.md) 可讓 rpc 用戶端能夠安全地透過網際網路連線到 rpc 伺服器程式，並執行遠端程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="1c6b4-126">[Remote Procedure Calls Using RPC over HTTP](remote-procedure-calls-using-rpc-over-http.md) provides RPC clients with the ability to securely connect across the Internet to RPC server programs and execute remote procedure calls.</span></span>
-   <span data-ttu-id="1c6b4-127">[RPC 負載平衡](rpc-load-balancing.md) 說明如何在伺服器陣列中的多部 rpc 伺服器之間散發大量 RPC over HTTP 流量。</span><span class="sxs-lookup"><span data-stu-id="1c6b4-127">[RPC Load Balancing](rpc-load-balancing.md) describes distributing high volumes of RPC over HTTP traffic among numerous RPC servers within a server farm.</span></span>
-   <span data-ttu-id="1c6b4-128">[範例](examples.md) 包含 Microsoft 平臺軟體發展人員套件隨附的範例 RPC 程式說明。</span><span class="sxs-lookup"><span data-stu-id="1c6b4-128">[Samples](examples.md) contains a description of the example RPC programs shipped with the Microsoft Platform Software Developer's Kit.</span></span>

 

 




