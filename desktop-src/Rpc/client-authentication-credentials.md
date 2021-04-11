---
title: 用戶端驗證認證
description: 每個已驗證的用戶端都必須提供驗證認證給伺服器。
ms.assetid: d567e944-8d68-4d95-be6a-840e30f57ba9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3704663411fc33340a462d8e3b356041b6061468
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022025"
---
# <a name="client-authentication-credentials"></a><span data-ttu-id="bd789-103">用戶端驗證認證</span><span class="sxs-lookup"><span data-stu-id="bd789-103">Client Authentication Credentials</span></span>

<span data-ttu-id="bd789-104">每個已驗證的用戶端都必須提供驗證認證給伺服器。</span><span class="sxs-lookup"><span data-stu-id="bd789-104">Each authenticated client must provide authentication credentials to the server.</span></span> <span data-ttu-id="bd789-105">在 RPC 下，用戶端會將其驗證認證儲存在用戶端與伺服器之間的系結中。</span><span class="sxs-lookup"><span data-stu-id="bd789-105">Under RPC, the client stores its authentication credentials in the binding between the client and the server.</span></span> <span data-ttu-id="bd789-106">若要這樣做，用戶端會呼叫 [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) 或 [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)。</span><span class="sxs-lookup"><span data-stu-id="bd789-106">To do this, the client calls [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) or [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa).</span></span>

<span data-ttu-id="bd789-107">有兩種類型的認證，隱含和明確：</span><span class="sxs-lookup"><span data-stu-id="bd789-107">There are two types of credentials—implicit and explicit:</span></span>

-   <span data-ttu-id="bd789-108">當用戶端提供使用者名稱、密碼和網域時，會有明確的認證。</span><span class="sxs-lookup"><span data-stu-id="bd789-108">Explicit credentials exist when the client supplies username, password, and domain.</span></span>
-   <span data-ttu-id="bd789-109">當用戶端使用來自呼叫 **RpcBindingSetAuthInfo** 或 **RpcBindingSetAuthInfoEx** 函式之執行緒或進程權杖的認證時，就會有隱含的認證。</span><span class="sxs-lookup"><span data-stu-id="bd789-109">Implicit credentials exist when the client uses credentials from the thread or process token calling the **RpcBindingSetAuthInfo** or **RpcBindingSetAuthInfoEx** functions.</span></span>

<span data-ttu-id="bd789-110">用戶端應該避免提供明確的認證，因為如果使用了明確的認證，儲存、操作及取出使用者密碼可能會導致分散式系統產生安全性弱點。</span><span class="sxs-lookup"><span data-stu-id="bd789-110">Clients should refrain from supplying explicit credentials because storing, manipulating, and retrieving a user password can introduce a security vulnerability into a distributed system if explicit credentials are used.</span></span>

<span data-ttu-id="bd789-111">若要使用隱含認證，用戶端會呼叫 **RpcBindingSetAuthInfo** (*例如*) 。</span><span class="sxs-lookup"><span data-stu-id="bd789-111">To use implicit credentials, the client calls **RpcBindingSetAuthInfo**(*Ex*).</span></span> <span data-ttu-id="bd789-112">安全性系統和 RPC 會從執行緒或進程權杖取得認證，以便用於驗證會話中。</span><span class="sxs-lookup"><span data-stu-id="bd789-112">The security system and RPC obtain credentials from the thread or process token for use in the authentication session.</span></span>

<span data-ttu-id="bd789-113">如果用戶端使用明確的認證，則這兩個函式的第五個參數屬於 [**RPC \_ AUTH 身分 \_ 識別 \_ 控制碼**](rpc-auth-identity-handle.md)類型。</span><span class="sxs-lookup"><span data-stu-id="bd789-113">If the client uses explicit credentials, the fifth parameter of these two functions is of type [**RPC\_AUTH\_IDENTITY\_HANDLE**](rpc-auth-identity-handle.md).</span></span> <span data-ttu-id="bd789-114">這是一種彈性類型，也就是資料結構的指標。</span><span class="sxs-lookup"><span data-stu-id="bd789-114">This is a flexible type that is a pointer to a data structure.</span></span> <span data-ttu-id="bd789-115">資料結構的內容可以與每個驗證服務不同。</span><span class="sxs-lookup"><span data-stu-id="bd789-115">The contents of the data structure can differ with each authentication service.</span></span> <span data-ttu-id="bd789-116">目前，RPC 支援的 Ssp 要求您的應用程式將 **rpc \_ 驗證身分 \_ 識別 \_ 控制碼** 設定為指向 [**SEC 的 \_ WINNT \_ AUTH \_ identity**](/windows/desktop/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a) 結構。</span><span class="sxs-lookup"><span data-stu-id="bd789-116">Currently, the SSPs that RPC supports require that your application set **RPC\_AUTH\_IDENTITY\_HANDLE** to point to a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/desktop/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a) structure.</span></span> <span data-ttu-id="bd789-117">**每秒的 \_ WINNT 驗證身分 \_ \_ 識別** 結構包含使用者名稱、網域和密碼的欄位。</span><span class="sxs-lookup"><span data-stu-id="bd789-117">The **SEC\_WINNT\_AUTH\_IDENTITY** structure contains fields for a user name, domain, and password.</span></span>

 

 




