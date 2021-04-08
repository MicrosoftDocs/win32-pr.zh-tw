---
title: 使用 RPC 名稱服務發行
description: RPC 服務可以使用 RPC 名稱服務在命名空間中發佈其識別碼， (RpcNs) Api。
ms.assetid: 0c8e1207-daeb-4dc8-b83a-a54cd59a46a7
ms.tgt_platform: multiple
keywords:
- 使用 RPC 名稱服務 AD 進行發佈
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b672eec6308d709fe2f4cbc64ad22ecf0d6edd
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023228"
---
# <a name="publishing-with-the-rpc-name-service"></a><span data-ttu-id="8e000-104">使用 RPC 名稱服務發行</span><span class="sxs-lookup"><span data-stu-id="8e000-104">Publishing with the RPC Name Service</span></span>

<span data-ttu-id="8e000-105">RPC 服務可以使用 RPC 名稱服務在命名空間中發佈其識別碼， (RpcNs) Api。</span><span class="sxs-lookup"><span data-stu-id="8e000-105">RPC services can publish their identifiers in a namespace using the RPC name service (RpcNs) APIs.</span></span> <span data-ttu-id="8e000-106">Windows 2000 中的 RpcNs Api 會將 Active Directory Domain Services 中的 RPC 專案發佈。</span><span class="sxs-lookup"><span data-stu-id="8e000-106">The RpcNs APIs in Windows 2000 publish the RPC entries in Active Directory Domain Services.</span></span> <span data-ttu-id="8e000-107">服務會建立 RPC 系結，並在命名空間中將它們發佈為具有屬性的命名空間，其中包含唯一的介面識別碼，也就是用戶端所能辨識的 GUID。</span><span class="sxs-lookup"><span data-stu-id="8e000-107">Services create RPC bindings and publish them in the namespace as named RPC Server entries with attributes including the unique interface ID, a GUID that is recognized by clients.</span></span> <span data-ttu-id="8e000-108">接著，用戶端可以搜尋提供所需介面的 RPC 伺服器、匯入系結，然後連接到伺服器。</span><span class="sxs-lookup"><span data-stu-id="8e000-108">A client can then search for RPC Servers offering the desired interface, import the binding, and connect to the server.</span></span>

<span data-ttu-id="8e000-109">如需發行 RPC 服務的詳細資訊，請參閱 [伺服器端](/windows/desktop/Rpc/server-side-binding)系結。</span><span class="sxs-lookup"><span data-stu-id="8e000-109">For more information about publishing an RPC service, see [Server-side Binding](/windows/desktop/Rpc/server-side-binding).</span></span>

 

 