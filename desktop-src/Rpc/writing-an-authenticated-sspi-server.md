---
title: 撰寫經過驗證的 SSPI 伺服器
description: 在用戶端和伺服器程式之間可以進行驗證通訊之前，伺服器必須註冊其驗證資訊。
ms.assetid: 723ae1ee-d729-4748-9ef1-062a0c6f60d0
keywords:
- 遠端程序呼叫 RPC、工作、撰寫經過驗證的 SSPI 伺服器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19b1cb06cfc626bc8130f3c4b0cee0a7b6d7893e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021399"
---
# <a name="writing-an-authenticated-sspi-server"></a><span data-ttu-id="b526f-104">撰寫經過驗證的 SSPI 伺服器</span><span class="sxs-lookup"><span data-stu-id="b526f-104">Writing an Authenticated SSPI Server</span></span>

<span data-ttu-id="b526f-105">在用戶端和伺服器程式之間可以進行驗證通訊之前，伺服器必須註冊其驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="b526f-105">Before authenticated communication can take place between the client and server programs, the server must register its authentication information.</span></span> <span data-ttu-id="b526f-106">尤其是，伺服器必須註冊其主體名稱，並指定它所使用的驗證服務。</span><span class="sxs-lookup"><span data-stu-id="b526f-106">In particular, the server must register its principal name and specify the authentication service it uses.</span></span> <span data-ttu-id="b526f-107">如需主體名稱的詳細資訊，請參閱 [主體名稱](principal-names.md)。</span><span class="sxs-lookup"><span data-stu-id="b526f-107">For more information on principal names, see [Principal Names](principal-names.md).</span></span> <span data-ttu-id="b526f-108">如需驗證服務的詳細資訊，請參閱 [驗證服務](authentication-services.md)。</span><span class="sxs-lookup"><span data-stu-id="b526f-108">For details about authentication services, see [Authentication Services](authentication-services.md).</span></span>

<span data-ttu-id="b526f-109">為了註冊其驗證資訊，伺服器會呼叫 [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) 函數。</span><span class="sxs-lookup"><span data-stu-id="b526f-109">To register its authentication information, servers call the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function.</span></span> <span data-ttu-id="b526f-110">將主體名稱的指標傳遞為第一個參數的值。</span><span class="sxs-lookup"><span data-stu-id="b526f-110">Pass a pointer to the principal name as the value of the first parameter.</span></span> <span data-ttu-id="b526f-111">將第二個參數設定為常數，表示應用程式將使用的驗證服務。</span><span class="sxs-lookup"><span data-stu-id="b526f-111">Set the second parameter to a constant indicating the authentication service that the application will use.</span></span> <span data-ttu-id="b526f-112">如需驗證服務的描述，請參閱 [驗證-服務常數](authentication-service-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="b526f-112">For a description of authentication services, see [Authentication-Service Constants](authentication-service-constants.md).</span></span>

<span data-ttu-id="b526f-113">伺服器也可以將金鑰取得函式的位址傳遞為第三個參數的值。</span><span class="sxs-lookup"><span data-stu-id="b526f-113">The server may also pass the address of a key acquisition function as the value of the third parameter.</span></span> <span data-ttu-id="b526f-114">請參閱 [金鑰](key-acquisition-functions.md)取得函式。</span><span class="sxs-lookup"><span data-stu-id="b526f-114">See [Key Acquisition Functions](key-acquisition-functions.md).</span></span> <span data-ttu-id="b526f-115">若要針對選取的驗證服務使用預設的金鑰取得函數，請將第三個參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b526f-115">To use the default key acquisition function for the selected authentication service, set the third parameter to **NULL**.</span></span> <span data-ttu-id="b526f-116">如果您提供金鑰取得函式， [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) 函式的最後一個參數是要傳遞至金鑰取得函式的指標資料。</span><span class="sxs-lookup"><span data-stu-id="b526f-116">The last parameter to the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function is a pointer data to pass to the key acquisition function, if you provide a key acquisition function.</span></span> <span data-ttu-id="b526f-117">**RpcServerRegisterAuthInfo** 的呼叫會顯示在下列程式碼片段中。</span><span class="sxs-lookup"><span data-stu-id="b526f-117">A call to **RpcServerRegisterAuthInfo** is shown in the following code fragment.</span></span>


```C++
dwStatus = DsMakeSpn(
    "ldap",
    "ServerName.domain.com",
    NULL,
    0,
    NULL,
    &pcSpnLength,
    pszSpn);

rpcStatus = RpcServerRegisterAuthInfo (
    psz,                                   // Server principal name
    RPC_C_AUTHN_GSS_NEGOTIATE,             // Authentication service
    NULL,                                  // Use default key function
    NULL);                                 // No arg for key function
```



<span data-ttu-id="b526f-118">此外，伺服器可能會提供具有授權功能的 RPC 執行時間程式庫。</span><span class="sxs-lookup"><span data-stu-id="b526f-118">In addition, the server may provide the RPC run-time library with an authorization function.</span></span> <span data-ttu-id="b526f-119">若要設定授權函數，請呼叫 [**RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) 函數。</span><span class="sxs-lookup"><span data-stu-id="b526f-119">To set an authorization function, call the [**RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) function.</span></span>

<span data-ttu-id="b526f-120">分散式應用程式的伺服器部分可以呼叫函數 [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) 或 [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) 來查詢驗證資訊的系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="b526f-120">The server portion of a distributed application can call the function [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) or [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) to query a binding handle for authentication information.</span></span>

<span data-ttu-id="b526f-121">如果您的伺服器向安全性支援提供者註冊，將不會分派具有無效認證的用戶端呼叫。</span><span class="sxs-lookup"><span data-stu-id="b526f-121">If your server registers with a security support provider, client calls with invalid credentials will not be dispatched.</span></span> <span data-ttu-id="b526f-122">但是，不會分派沒有認證的呼叫。</span><span class="sxs-lookup"><span data-stu-id="b526f-122">However, calls with no credentials will be dispatched.</span></span> <span data-ttu-id="b526f-123">有三種方式可以防止這種情況發生：</span><span class="sxs-lookup"><span data-stu-id="b526f-123">There are three ways to prevent this from happening:</span></span>

-   <span data-ttu-id="b526f-124">使用 [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)（具有安全性回呼函式）註冊介面;這會讓 RPC 執行時間程式庫自動拒絕對該介面的未經驗證呼叫。</span><span class="sxs-lookup"><span data-stu-id="b526f-124">Register the interface using [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex), with a security callback function; this will cause the RPC run-time library to automatically reject unauthenticated calls to that interface.</span></span> <span data-ttu-id="b526f-125">註冊回呼函數與其他檢查存取認證的方法相容;回呼函式本身可以呼叫 [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient)、 [**RpcGetAuthorizationCoNtextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient)或 [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) 函數或其他函式。</span><span class="sxs-lookup"><span data-stu-id="b526f-125">Registering a callback function is compatible with other methods of checking access credentials; the callback function can itself call the [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient), [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient), or [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) functions, or others.</span></span> <span data-ttu-id="b526f-126">不過，這些函式無法使用傳遞至函式的引數，因為它們不會在該時間點 unmarshalled。</span><span class="sxs-lookup"><span data-stu-id="b526f-126">However, these functions cannot use the arguments passed to the function, as they are not unmarshalled at that point.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b526f-127">使用具有安全性回呼函式的 [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) 來註冊介面，是檢查用戶端認證的最大建議方法。</span><span class="sxs-lookup"><span data-stu-id="b526f-127">Registering the interface using [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) with a security callback function is the most heavily recommended method of checking client credentials.</span></span>

 

-   <span data-ttu-id="b526f-128">呼叫 [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) 來判斷用戶端所使用的安全性層級。</span><span class="sxs-lookup"><span data-stu-id="b526f-128">Call [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) to determine the security level that the client is using.</span></span> <span data-ttu-id="b526f-129">如果用戶端未經驗證，則您的存根會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="b526f-129">Your stub can then return an error if the client is unauthenticated.</span></span>

 

 




