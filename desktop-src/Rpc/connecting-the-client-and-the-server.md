---
title: 連接用戶端和伺服器
description: 若要進行通訊，用戶端和伺服器程式必須在連線的網路或網路之間建立通訊會話。
ms.assetid: 1164252a-7615-4958-9d2f-cf35c0db513a
keywords:
- 遠端程序呼叫 RPC、工作、連接用戶端和伺服器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98a22ea7a9a6dd30f2b9495b6d2ee868aac217f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462281"
---
# <a name="connecting-the-client-and-the-server"></a><span data-ttu-id="4c40f-104">連接用戶端和伺服器</span><span class="sxs-lookup"><span data-stu-id="4c40f-104">Connecting the Client and the Server</span></span>

<span data-ttu-id="4c40f-105">若要進行通訊，用戶端和伺服器程式必須在連線的網路或網路之間建立通訊會話。</span><span class="sxs-lookup"><span data-stu-id="4c40f-105">To communicate, client and server programs must establish a communication session across the network or networks that connect them.</span></span> <span data-ttu-id="4c40f-106">一旦建立連線之後，用戶端就可以呼叫伺服器程式中的遠端程式，就好像它們是用戶端程式的本機程式一樣。</span><span class="sxs-lookup"><span data-stu-id="4c40f-106">Once they establish the connection, the client can call remote procedures in the server program as if they were local to the client program.</span></span>

<span data-ttu-id="4c40f-107">本節提供有關如何在用戶端與伺服器之間建立遠端程序呼叫之連接的概念。</span><span class="sxs-lookup"><span data-stu-id="4c40f-107">This section provides a conceptual overview of how to establish a connection between clients and servers for remote procedure calls.</span></span> <span data-ttu-id="4c40f-108">它不會提供本主題的深入討論。</span><span class="sxs-lookup"><span data-stu-id="4c40f-108">It does not provide an in-depth discussion of this topic.</span></span> <span data-ttu-id="4c40f-109">本章節中的所有概念將在稍後的章節和 RPC 函數參考一節中詳細說明。</span><span class="sxs-lookup"><span data-stu-id="4c40f-109">All of the concepts in this section are presented in detail in later chapters and in the RPC Function Reference section.</span></span>

<span data-ttu-id="4c40f-110">本節中的討論區分為下列主題：</span><span class="sxs-lookup"><span data-stu-id="4c40f-110">The discussion presented in this section is divided into the following topics:</span></span>

-   [<span data-ttu-id="4c40f-111">基本 RPC 系結術語</span><span class="sxs-lookup"><span data-stu-id="4c40f-111">Essential RPC Binding Terminology</span></span>](essential-rpc-binding-terminology.md)
-   [<span data-ttu-id="4c40f-112">伺服器如何準備連接</span><span class="sxs-lookup"><span data-stu-id="4c40f-112">How the Server Prepares for a Connection</span></span>](how-the-server-prepares-for-a-connection.md)
-   [<span data-ttu-id="4c40f-113">用戶端建立連接的方式</span><span class="sxs-lookup"><span data-stu-id="4c40f-113">How the Client Establishes a Connection</span></span>](how-the-client-establishes-a-connection.md)

<span data-ttu-id="4c40f-114">請注意，討論會假設明確的系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="4c40f-114">Note that the discussion assumes explicit binding handles.</span></span> <span data-ttu-id="4c40f-115">但是，如果您的應用程式使用其他類型的系結控制碼，您可能必須修改本節所述的步驟。</span><span class="sxs-lookup"><span data-stu-id="4c40f-115">However, if your application uses other types of binding handles, you may have to modify the steps presented in this section.</span></span> <span data-ttu-id="4c40f-116">如需詳細資訊，請參閱系結 [和控制碼](binding-and-handles.md)。</span><span class="sxs-lookup"><span data-stu-id="4c40f-116">For more information, see [Binding and Handles](binding-and-handles.md).</span></span>

 

 




