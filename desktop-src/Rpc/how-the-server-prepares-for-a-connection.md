---
title: 伺服器如何準備連接
description: 當伺服器程式開始執行時，它必須先向 RPC 執行時間程式庫註冊它所包含的介面或介面。
ms.assetid: 3e78e095-f4a4-4ce7-b4a9-936a6c10316b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9787cc0f4a10da99f1401843450a6e00073e135b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301191"
---
# <a name="how-the-server-prepares-for-a-connection"></a><span data-ttu-id="58423-103">伺服器如何準備連接</span><span class="sxs-lookup"><span data-stu-id="58423-103">How the Server Prepares for a Connection</span></span>

<span data-ttu-id="58423-104">當伺服器程式開始執行時，它必須先向 RPC 執行時間程式庫註冊它所包含的介面或介面。</span><span class="sxs-lookup"><span data-stu-id="58423-104">When a server program begins execution, it must first register the interface or interfaces it contains with the RPC run-time library.</span></span> <span data-ttu-id="58423-105">然後，它會建立必要的系結資訊。</span><span class="sxs-lookup"><span data-stu-id="58423-105">It then creates the necessary binding information.</span></span> <span data-ttu-id="58423-106">伺服器程式也必須註冊端點或接聽的端點。</span><span class="sxs-lookup"><span data-stu-id="58423-106">The server program must also register the endpoint or endpoints it listens to.</span></span> <span data-ttu-id="58423-107">然後，它就可以開始接聽用戶端呼叫。</span><span class="sxs-lookup"><span data-stu-id="58423-107">It can then begin listening for client calls.</span></span> <span data-ttu-id="58423-108">下圖說明此程式。</span><span class="sxs-lookup"><span data-stu-id="58423-108">This process is illustrated in the following diagram.</span></span>

![rpc 伺服器應用程式準備進行用戶端連接](images/srvrcon.png)

<span data-ttu-id="58423-110">根據選擇的設計，伺服器應用程式可以選擇一組不同的步驟;先前的範例和圖例提供了一種方法。</span><span class="sxs-lookup"><span data-stu-id="58423-110">Depending on the design chosen, a server application may choose a different set of steps; the previous example and illustration provides one approach.</span></span>

<span data-ttu-id="58423-111">本節提供伺服器進程為了準備連接所必須採取的步驟資訊。</span><span class="sxs-lookup"><span data-stu-id="58423-111">This section presents information on the steps that a server process must take to prepare for a connection.</span></span> <span data-ttu-id="58423-112">討論區分為下列各節：</span><span class="sxs-lookup"><span data-stu-id="58423-112">The discussion is divided into the following sections:</span></span>

-   [<span data-ttu-id="58423-113">註冊介面</span><span class="sxs-lookup"><span data-stu-id="58423-113">Registering the Interface</span></span>](registering-the-interface.md)
-   [<span data-ttu-id="58423-114">讓伺服器可在網路上使用</span><span class="sxs-lookup"><span data-stu-id="58423-114">Making the Server Available on the Network</span></span>](making-the-server-available-on-the-network.md)
-   [<span data-ttu-id="58423-115">註冊端點</span><span class="sxs-lookup"><span data-stu-id="58423-115">Registering Endpoints</span></span>](registering-endpoints.md)
-   [<span data-ttu-id="58423-116">接聽用戶端呼叫</span><span class="sxs-lookup"><span data-stu-id="58423-116">Listening for Client Calls</span></span>](listening-for-client-calls.md)

 

 




