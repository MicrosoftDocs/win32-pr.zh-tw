---
title: RPC)  (範例
description: 示範遠端程序呼叫 (RPC) 概念的範例。
ms.assetid: d5db3085-6df0-4539-a605-d60055f4f4ec
keywords:
- 遠端程序呼叫 RPC，範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e6a814d78afbfc7fefa979c890cbbb8c3d4ce0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106968126"
---
# <a name="examples-rpc"></a><span data-ttu-id="09de5-104">RPC)  (範例</span><span class="sxs-lookup"><span data-stu-id="09de5-104">Examples (RPC)</span></span>

<span data-ttu-id="09de5-105">平臺軟體發展工具組 (SDK) 包含的範例會示範各種不同的遠端程序呼叫， (RPC) 概念，如下所示：</span><span class="sxs-lookup"><span data-stu-id="09de5-105">The Platform Software Development Kit (SDK) includes examples that demonstrate a variety of Remote Procedure Call (RPC) concepts, as follows:</span></span>

-   <span data-ttu-id="09de5-106">ASYNCRPC 說明使用非同步遠端程序呼叫的 RPC 應用程式結構。</span><span class="sxs-lookup"><span data-stu-id="09de5-106">ASYNCRPC illustrates the structure of an RPC application that uses asynchronous remote procedure calls.</span></span> <span data-ttu-id="09de5-107">它也會示範呼叫完成的各種通知方法。</span><span class="sxs-lookup"><span data-stu-id="09de5-107">It also demonstrates various methods of notification of the call's completion.</span></span>
-   <span data-ttu-id="09de5-108">CLUUID 示範如何使用用戶端物件 UUID，讓用戶端從遠端程式的多個執行中進行選取。</span><span class="sxs-lookup"><span data-stu-id="09de5-108">CLUUID demonstrates use of the client-object UUID to enable a client to select from multiple implementations of a remote procedure.</span></span>
-   <span data-ttu-id="09de5-109">資料目錄包含四個程式： DUNION 說明區分 (nonencapsulated) 等位的差異;INOUT 示範[ \[ in \] ](../midl/in.md)、 [ \[ out \] ](../midl/out-idl.md)參數;REPAS 示範[代表 \_ as](/windows/desktop/Midl/represent-as)屬性;XMIT 示範[傳輸 \_ 為](/windows/desktop/Midl/transmit-as)屬性。</span><span class="sxs-lookup"><span data-stu-id="09de5-109">DATA directory contains four programs: DUNION illustrates discriminated (nonencapsulated) unions; INOUT demonstrates [\[in\]](../midl/in.md), [\[out\]](../midl/out-idl.md) parameters; REPAS demonstrates the [represent\_as](/windows/desktop/Midl/represent-as) attribute; XMIT demonstrates the [transmit\_as](/windows/desktop/Midl/transmit-as) attribute.</span></span>
-   <span data-ttu-id="09de5-110">DYNEPT 示範用戶端應用程式透過動態端點管理其與伺服器的連線。</span><span class="sxs-lookup"><span data-stu-id="09de5-110">DYNEPT demonstrates a client application managing its connection to the server through dynamic endpoints.</span></span>
-   <span data-ttu-id="09de5-111">FILEREP 目錄包含四個範例，說明開發人員如何撰寫簡單的檔案複寫服務、多重使用者檔案複寫服務、支援安全性功能的服務，以及使用 RPC 非同步管道的服務。</span><span class="sxs-lookup"><span data-stu-id="09de5-111">FILEREP directory contains four samples illustrating how developers can write a simple file replication service, a multi-user file replication service, a service supporting security features, and a service using RPC asynchronous pipes.</span></span>
-   <span data-ttu-id="09de5-112">控制碼目錄包含三個程式： AUTO、CXHNDL、USRDEF，分別示範 [自動 \_ 處理](/windows/desktop/Midl/auto-handle)、 \[ 內容 \_ 控制碼 \] 和泛型 (使用者定義的) 控制碼。</span><span class="sxs-lookup"><span data-stu-id="09de5-112">HANDLES directory contains three programs, AUTO, CXHNDL, USRDEF, which demonstrate [auto\_handle](/windows/desktop/Midl/auto-handle), \[context\_handle\], and generic (user-defined) handles, respectively.</span></span>
-   <span data-ttu-id="09de5-113">HELLO 是 "Hello，world" 的用戶端/伺服器執行。</span><span class="sxs-lookup"><span data-stu-id="09de5-113">HELLO is a client/server implementation of "Hello, world."</span></span>
-   <span data-ttu-id="09de5-114">PICKLE 目錄包含兩個程式： PICKLP 示範資料程式序列化;PICKLT 示範資料類型序列化;這兩個程式都使用[ \[ 編碼 \] ](../midl/encode.md)和[ \[ \] 解碼](../midl/decode.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="09de5-114">PICKLE directory contains two programs: PICKLP demonstrates data procedure serialization; PICKLT demonstrates data type serialization; both programs use the [\[encode\]](../midl/encode.md) and [\[decode\]](../midl/decode.md) attributes.</span></span>
-   <span data-ttu-id="09de5-115">管道示範如何使用管道類型的函式。</span><span class="sxs-lookup"><span data-stu-id="09de5-115">PIPES demonstrates the use of the pipe-type constructor.</span></span>
-   <span data-ttu-id="09de5-116">RPCSVC 示範如何使用 RPC 來執行服務。</span><span class="sxs-lookup"><span data-stu-id="09de5-116">RPCSVC demonstrates the implementation of a service with RPC.</span></span>
-   <span data-ttu-id="09de5-117">STROUT 示範如何在伺服器上為 () 指標陣列的二維物件配置記憶體，並將其以 out 參數的形式傳遞回用戶端 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="09de5-117">STROUT demonstrates how to allocate memory at a server for a two-dimensional object (an array of pointers) and pass it back to the client as an \[out\]-only parameter.</span></span> <span data-ttu-id="09de5-118">然後，用戶端就會釋出記憶體。</span><span class="sxs-lookup"><span data-stu-id="09de5-118">The client then frees the memory.</span></span> <span data-ttu-id="09de5-119">這項技術可讓存根呼叫伺服器，而不需事先知道將傳回多少資料。</span><span class="sxs-lookup"><span data-stu-id="09de5-119">This technique allows the stub to call the server without knowing in advance how much data will be returned.</span></span>

    <span data-ttu-id="09de5-120">此程式也可讓使用者針對 UNICODE 或 ANSI 進行編譯。</span><span class="sxs-lookup"><span data-stu-id="09de5-120">This program also allows the user to compile either for UNICODE or ANSI.</span></span>

<span data-ttu-id="09de5-121">這些程式的所有原始程式檔和 makefile 都位於 Platform SDK 中。</span><span class="sxs-lookup"><span data-stu-id="09de5-121">All of the source files and makefiles for these programs are located in the Platform SDK.</span></span>

<span data-ttu-id="09de5-122">如需基本的 RPC 應用程式開發和更簡單的範例，請參閱 [教學](tutorial.md) 課程主題。</span><span class="sxs-lookup"><span data-stu-id="09de5-122">For basic RPC application development and simpler examples, please see the [Tutorial](tutorial.md) topics.</span></span>

 

 
