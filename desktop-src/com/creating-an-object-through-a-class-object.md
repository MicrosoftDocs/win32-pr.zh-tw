---
title: 透過類別物件建立物件
description: 透過類別物件建立物件
ms.assetid: cecf21b0-e509-425f-8dd6-ca6b1ac04f5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38787e7bc32151446cda6ff0a4cfe3f23a0f6eda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932565"
---
# <a name="creating-an-object-through-a-class-object"></a><span data-ttu-id="70ee6-103">透過類別物件建立物件</span><span class="sxs-lookup"><span data-stu-id="70ee6-103">Creating an Object Through a Class Object</span></span>

<span data-ttu-id="70ee6-104">隨著電腦網路的重要性日益增加，用戶端和伺服器都必須能夠輕鬆且有效率地進行互動，不論它們是位於同一部電腦或網路上。</span><span class="sxs-lookup"><span data-stu-id="70ee6-104">With the increasing importance of computer networks, it has become necessary for clients and servers to interact easily and efficiently, whether they reside on the same machine or across a network.</span></span> <span data-ttu-id="70ee6-105">重要的是，用戶端可以啟動伺服器、建立伺服器物件的實例，並且可以存取物件上的介面方法。</span><span class="sxs-lookup"><span data-stu-id="70ee6-105">Crucial to this is a client's ability to launch a server, create an instance of the server's object, and have access to the methods of the interfaces on the object.</span></span>

<span data-ttu-id="70ee6-106">COM 提供此基本 COM 進程的延伸模組，讓它在網路上幾乎順暢。</span><span class="sxs-lookup"><span data-stu-id="70ee6-106">COM provides extensions to this basic COM process that make it virtually seamless across a network.</span></span> <span data-ttu-id="70ee6-107">如果用戶端能夠透過 CLSID 來識別伺服器，則呼叫一些簡單的函式會允許 COM 執行所有尋找和啟動伺服器的工作，以及啟始物件。</span><span class="sxs-lookup"><span data-stu-id="70ee6-107">If a client is able to identify the server through its CLSID, calling a few simple functions permit COM to do all the work of locating and launching the server and activating the object.</span></span> <span data-ttu-id="70ee6-108">登錄中的子機碼可讓遠端伺服器註冊其位置，因此用戶端不需要該資訊。</span><span class="sxs-lookup"><span data-stu-id="70ee6-108">Subkeys in the registry allow remote servers to register their location, so the client does not require that information.</span></span> <span data-ttu-id="70ee6-109">對於想要利用網路功能的應用程式，COM 物件建立功能可提供更大的彈性和效率。</span><span class="sxs-lookup"><span data-stu-id="70ee6-109">For applications that want to take advantage of networking features, the COM object creation functions allow more flexibility and efficiency.</span></span>

<span data-ttu-id="70ee6-110">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="70ee6-110">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="70ee6-111">COM 類別物件和 Clsid</span><span class="sxs-lookup"><span data-stu-id="70ee6-111">COM Class Objects and CLSIDs</span></span>](com-class-objects-and-clsids.md)
-   [<span data-ttu-id="70ee6-112">尋找遠端物件</span><span class="sxs-lookup"><span data-stu-id="70ee6-112">Locating a Remote Object</span></span>](locating-a-remote-object.md)
-   [<span data-ttu-id="70ee6-113">實例建立 Helper 函數</span><span class="sxs-lookup"><span data-stu-id="70ee6-113">Instance Creation Helper Functions</span></span>](instance-creation-helper-functions.md)

## <a name="related-topics"></a><span data-ttu-id="70ee6-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="70ee6-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70ee6-115">COM 用戶端和伺服器</span><span class="sxs-lookup"><span data-stu-id="70ee6-115">COM Clients and Servers</span></span>](com-clients-and-servers.md)
</dt> </dl>

 

 




