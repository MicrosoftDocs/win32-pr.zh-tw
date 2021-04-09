---
title: 用戶端建立連接的方式
description: 若要與伺服器程式建立用戶端/伺服器通訊會話，具有明確控制碼的用戶端應用程式必須建立系結控制碼。
ms.assetid: c67c9b1a-084f-4b85-ac6c-8cf25a6b0cca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c5fd8437fb5821c2b52240256a1938e8de31c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021565"
---
# <a name="how-the-client-establishes-a-connection"></a><span data-ttu-id="03e0d-103">用戶端建立連接的方式</span><span class="sxs-lookup"><span data-stu-id="03e0d-103">How the Client Establishes a Connection</span></span>

<span data-ttu-id="03e0d-104">若要與伺服器程式建立用戶端/伺服器通訊會話，具有明確控制碼的用戶端應用程式必須建立系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="03e0d-104">To establish a client/server communication session with a server program, client applications with explicit handles need to create a binding handle.</span></span> <span data-ttu-id="03e0d-105">在這些情況下，RPC 執行時間程式庫會尋找裝載伺服器程式的電腦。</span><span class="sxs-lookup"><span data-stu-id="03e0d-105">After they do, the RPC run-time library finds the computer that hosts the server program.</span></span> <span data-ttu-id="03e0d-106">然後，它會尋找伺服器程式正在接聽的端點，並將呼叫導向該端點。</span><span class="sxs-lookup"><span data-stu-id="03e0d-106">It then finds the endpoint that the server program is listening to and directs the call to it.</span></span> <span data-ttu-id="03e0d-107">下圖說明此程序。</span><span class="sxs-lookup"><span data-stu-id="03e0d-107">The following diagram illustrates this process.</span></span>

![rpc 用戶端建立與 rpc 伺服器的連接](images/clntcon.png)

<span data-ttu-id="03e0d-109">本節會提供有關用戶端如何連接到伺服器程式，以及如何執行它所提供之遠端程式的資訊。</span><span class="sxs-lookup"><span data-stu-id="03e0d-109">This section presents information about how the client connects to the server program and executes remote procedures that it offers.</span></span> <span data-ttu-id="03e0d-110">有許多方法可完成這些步驟;視選擇的設計而定，應用程式可能會選擇一組不同的步驟。</span><span class="sxs-lookup"><span data-stu-id="03e0d-110">There are many approaches to completing these steps; depending on the design chosen, an application may choose a different set of steps.</span></span> <span data-ttu-id="03e0d-111">這個範例只是其中一種方法。</span><span class="sxs-lookup"><span data-stu-id="03e0d-111">This example is simply one way of doing so.</span></span>

<span data-ttu-id="03e0d-112">討論區分為下列各節：</span><span class="sxs-lookup"><span data-stu-id="03e0d-112">The discussion is divided into the following sections:</span></span>

-   [<span data-ttu-id="03e0d-113">建立系結控制碼</span><span class="sxs-lookup"><span data-stu-id="03e0d-113">Creating a Binding Handle</span></span>](creating-a-binding-handle.md)
-   [<span data-ttu-id="03e0d-114">進行遠端程序呼叫</span><span class="sxs-lookup"><span data-stu-id="03e0d-114">Making a Remote Procedure Call</span></span>](making-a-remote-procedure-call.md)
-   [<span data-ttu-id="03e0d-115">尋找伺服器程式</span><span class="sxs-lookup"><span data-stu-id="03e0d-115">Finding the Server Program</span></span>](finding-the-server-program.md)
-   [<span data-ttu-id="03e0d-116">傳送呼叫給伺服器程式</span><span class="sxs-lookup"><span data-stu-id="03e0d-116">Sending the Call to the Server Program</span></span>](sending-the-call-to-the-server-program.md)

 

 




