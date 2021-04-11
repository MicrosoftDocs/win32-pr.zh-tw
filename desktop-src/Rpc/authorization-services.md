---
title: 授權服務
description: 授權服務是 SSP 用來授權遠端程式存取權的方法。 Ssp 可以提供一個以上的授權服務。 不過，它們通常會選取一個做為預設值。
ms.assetid: 5ea3cde9-96e9-4208-bb61-d0f98f23b90c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 548f834c69726425a52a033e0dbb08bf6f1f3a38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021758"
---
# <a name="authorization-services"></a><span data-ttu-id="fc561-105">授權服務</span><span class="sxs-lookup"><span data-stu-id="fc561-105">Authorization Services</span></span>

<span data-ttu-id="fc561-106">授權服務是 SSP 用來授權遠端程式存取權的方法。</span><span class="sxs-lookup"><span data-stu-id="fc561-106">An authorization service is the method that the SSP uses to authorize access to a remote procedure.</span></span> <span data-ttu-id="fc561-107">Ssp 可以提供一個以上的授權服務。</span><span class="sxs-lookup"><span data-stu-id="fc561-107">SSPs can provide more than one authorization service.</span></span> <span data-ttu-id="fc561-108">不過，它們通常會選取一個做為預設值。</span><span class="sxs-lookup"><span data-stu-id="fc561-108">However, they usually select one as a default.</span></span>

<span data-ttu-id="fc561-109">您的應用程式可以使用目前 SSP 的預設授權方法，也可以指定一個。</span><span class="sxs-lookup"><span data-stu-id="fc561-109">Your application can use the default authorization method for the current SSP, or it can specify one.</span></span> <span data-ttu-id="fc561-110">目前，Microsoft RPC 支援兩種授權方法。</span><span class="sxs-lookup"><span data-stu-id="fc561-110">At present, Microsoft RPC supports two methods of authorization.</span></span> <span data-ttu-id="fc561-111">其中一個是讓伺服器根據用戶端程式的名稱提供授權。</span><span class="sxs-lookup"><span data-stu-id="fc561-111">One is for the server to provide authorization based on the name of the client program.</span></span> <span data-ttu-id="fc561-112">另一種是讓伺服器將用戶端的驗證認證與伺服器的存取控制清單進行比較 (ACL) 。</span><span class="sxs-lookup"><span data-stu-id="fc561-112">The other is for the server to compare the client's authentication credentials against the server's access control list (ACL).</span></span>

<span data-ttu-id="fc561-113">如需授權服務的清單，請參閱授權服務的 [常數](authorization-service-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="fc561-113">For a list of authorization services, see [Authorization-Service Constants](authorization-service-constants.md).</span></span>

> [!Note]  
> <span data-ttu-id="fc561-114">建議開發人員使用 RPC \_ C \_ 授權 \_ 無。</span><span class="sxs-lookup"><span data-stu-id="fc561-114">It is recommended that developers use RPC\_C\_AUTHZ\_NONE.</span></span>

 

 

 




