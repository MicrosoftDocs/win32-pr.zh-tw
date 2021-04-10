---
title: 撰寫經過驗證的 SSPI 用戶端
description: 將已驗證的 SSPI 用戶端和遠端程序呼叫寫入 (RPC) 。
ms.assetid: db39d3bf-84fa-466e-9ba1-ba17f64c8f8d
keywords:
- 遠端程序呼叫 RPC、工作、撰寫已驗證的 SSPI 用戶端
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8476772a2ed652f6646b078c2876234cbcc0d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092987"
---
# <a name="writing-an-authenticated-sspi-client"></a><span data-ttu-id="ee55f-104">撰寫經過驗證的 SSPI 用戶端</span><span class="sxs-lookup"><span data-stu-id="ee55f-104">Writing an Authenticated SSPI Client</span></span>

<span data-ttu-id="ee55f-105">所有 RPC 用戶端/伺服器會話都需要用戶端與伺服器之間的系結。</span><span class="sxs-lookup"><span data-stu-id="ee55f-105">All RPC client/server sessions require a binding between the client and the server.</span></span> <span data-ttu-id="ee55f-106">若要將安全性新增至用戶端/伺服器應用程式，程式必須使用已驗證的系結。</span><span class="sxs-lookup"><span data-stu-id="ee55f-106">To add security to client/server applications, the programs must use an authenticated binding.</span></span> <span data-ttu-id="ee55f-107">本節說明在用戶端與伺服器之間建立已驗證系結的程式。</span><span class="sxs-lookup"><span data-stu-id="ee55f-107">This section describes the process of creating an authenticated binding between the client and the server.</span></span>

-   [<span data-ttu-id="ee55f-108">建立用戶端系結控制碼</span><span class="sxs-lookup"><span data-stu-id="ee55f-108">Creating Client-side Binding Handles</span></span>](#creating-client-side-binding-handles)
-   [<span data-ttu-id="ee55f-109">提供用戶端認證給伺服器</span><span class="sxs-lookup"><span data-stu-id="ee55f-109">Providing Client Credentials to the Server</span></span>](#providing-client-credentials-to-the-server)

<span data-ttu-id="ee55f-110">如需相關資訊，請參閱平臺軟體發展工具組中 [與大部分安全性套件和通訊協定搭配使用的程式](/windows/desktop/SecAuthN/procedures-used-with-most-security-packages-and-protocols) (SDK) 。</span><span class="sxs-lookup"><span data-stu-id="ee55f-110">For related information, see [Procedures Used with Most Security Packages and Protocols](/windows/desktop/SecAuthN/procedures-used-with-most-security-packages-and-protocols) in the Platform Software Development Kit (SDK).</span></span>

## <a name="creating-client-side-binding-handles"></a><span data-ttu-id="ee55f-111">建立用戶端系結控制碼</span><span class="sxs-lookup"><span data-stu-id="ee55f-111">Creating Client-side Binding Handles</span></span>

<span data-ttu-id="ee55f-112">若要使用伺服器程式建立已驗證的會話，用戶端應用程式必須使用其系結控制碼提供驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="ee55f-112">To create an authenticated session with a server program, client applications must provide authentication information with their binding handle.</span></span> <span data-ttu-id="ee55f-113">若要設定已驗證的系結控制碼，用戶端會叫用 [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) 或 [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) 函數。</span><span class="sxs-lookup"><span data-stu-id="ee55f-113">To set up an authenticated binding handle, clients invoke the [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) or [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) function.</span></span> <span data-ttu-id="ee55f-114">這兩個函數幾乎完全相同。</span><span class="sxs-lookup"><span data-stu-id="ee55f-114">These two functions are nearly identical.</span></span> <span data-ttu-id="ee55f-115">兩者之間唯一的差異在於，用戶端可以使用 **RpcBindingSetAuthInfoEx** 函式來指定服務品質。</span><span class="sxs-lookup"><span data-stu-id="ee55f-115">The only difference between them is that the client can specify the quality of service with the **RpcBindingSetAuthInfoEx** function.</span></span>

<span data-ttu-id="ee55f-116">下列程式碼片段顯示 [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) 呼叫的方式。</span><span class="sxs-lookup"><span data-stu-id="ee55f-116">The following code fragment shows how a call to [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) might look.</span></span>


```C++
// This code fragment assumes that rpcBinding is a valid binding 
// handle between the client and the server. It also assumes that
// pAuthCredentials is a valid pointer to a data structure which
// contains the user's authentication credentials.

dwStatus = DsMakeSpn(
    "ldap",
    "ServerName.domain.com",
    NULL,
    0,
    NULL,
    &pcSpnLength,
    pszSpn);

//...

rpcStatus = RpcBindingSetAuthInfo(
    rpcBinding,                       // Valid binding handle
    pszSpn,                           // Principal name 
    RPC_C_AUTHN_LEVEL_PKT_INTEGRITY,  // Authentication level
    RPC_C_AUTHN_GSS_NEGOTIATE,        // Use Negotiate SSP
    NULL,                             // Authentication credentials <entity type="ndash"/> use current thread credentials
    RPC_C_AUTHZ_NAME);                // Authorization service
```



<span data-ttu-id="ee55f-117">在用戶端成功呼叫 [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) 或 [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) 函式之後，rpc 執行時間程式庫會自動驗證系結上的所有 RPC 呼叫。</span><span class="sxs-lookup"><span data-stu-id="ee55f-117">After the client successfully calls the [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) or [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) functions, the RPC run-time library automatically authenticates all RPC calls on the binding.</span></span> <span data-ttu-id="ee55f-118">用戶端選取的安全性和驗證層級僅適用于該系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="ee55f-118">The level of security and authentication that the client selects applies only to that binding handle.</span></span> <span data-ttu-id="ee55f-119">衍生自系結控制碼的內容控制碼將使用相同的安全性資訊，但是對系結控制碼的後續修改不會反映在內容控制碼中。</span><span class="sxs-lookup"><span data-stu-id="ee55f-119">Context handles derived from the binding handle will use the same security information, but subsequent modifications to the binding handle will not be reflected in the context handles.</span></span> <span data-ttu-id="ee55f-120">如需詳細資訊，請參閱 [內容控制碼](context-handles.md)。</span><span class="sxs-lookup"><span data-stu-id="ee55f-120">For more information, see [Context Handles](context-handles.md).</span></span>

<span data-ttu-id="ee55f-121">在用戶端選擇另一個層級，或直到進程終止之前，驗證等級會保持有效。</span><span class="sxs-lookup"><span data-stu-id="ee55f-121">The authentication level stays in effect until the client chooses another level, or until the process terminates.</span></span> <span data-ttu-id="ee55f-122">大部分的應用程式都不需要變更安全性層級。</span><span class="sxs-lookup"><span data-stu-id="ee55f-122">Most applications will not require a change in the security level.</span></span> <span data-ttu-id="ee55f-123">用戶端可以藉由叫用 [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) 並傳遞系結控制碼來查詢任何系結控制碼，以取得其授權資訊。</span><span class="sxs-lookup"><span data-stu-id="ee55f-123">The client can query any binding handle to obtain its authorization information by invoking [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) and passing it the binding handle.</span></span>

## <a name="providing-client-credentials-to-the-server"></a><span data-ttu-id="ee55f-124">提供用戶端認證給伺服器</span><span class="sxs-lookup"><span data-stu-id="ee55f-124">Providing Client Credentials to the Server</span></span>

<span data-ttu-id="ee55f-125">伺服器會使用用戶端的系結資訊來強制執行安全性。</span><span class="sxs-lookup"><span data-stu-id="ee55f-125">Servers use the client's binding information to enforce security.</span></span> <span data-ttu-id="ee55f-126">用戶端一律會傳遞系結控制碼做為遠端程序呼叫的第一個參數。</span><span class="sxs-lookup"><span data-stu-id="ee55f-126">Clients always pass a binding handle as the first parameter of a remote procedure call.</span></span> <span data-ttu-id="ee55f-127">不過，伺服器無法使用控制碼，除非它被宣告為 IDL 檔案或伺服器應用程式佈建檔中遠端程式的第一個參數， (ACF) 。</span><span class="sxs-lookup"><span data-stu-id="ee55f-127">However, servers cannot use the handle unless it is declared as the first parameter to remote procedures in either the IDL file or in the server's application configuration file (ACF).</span></span> <span data-ttu-id="ee55f-128">您可以選擇在 IDL 檔案中列出系結控制碼，但這會強制所有用戶端宣告和操作系結控制碼，而不是使用自動或隱含系結。</span><span class="sxs-lookup"><span data-stu-id="ee55f-128">You can choose to list the binding handle in the IDL file, but this forces all clients to declare and manipulate the binding handle rather than using automatic or implicit binding.</span></span> <span data-ttu-id="ee55f-129">如需詳細資訊，請參閱 [IDL 和 ACF](the-idl-and-acf-files.md)檔。</span><span class="sxs-lookup"><span data-stu-id="ee55f-129">For further information, see [The IDL and ACF Files](the-idl-and-acf-files.md).</span></span>

<span data-ttu-id="ee55f-130">另一種方法是讓系結控制碼離開 IDL 檔案，並將 **明確的 \_ 控制碼** 屬性放入伺服器的 ACF 中。</span><span class="sxs-lookup"><span data-stu-id="ee55f-130">Another method is to leave the binding handles out of the IDL file and to place the **explicit\_handle** attribute into the server's ACF.</span></span> <span data-ttu-id="ee55f-131">如此一來，用戶端就可以使用最適合應用程式的系結類型，而伺服器則使用系結控制碼，就好像是明確宣告一樣。</span><span class="sxs-lookup"><span data-stu-id="ee55f-131">In this way, the client can use the type of binding best suited to the application, while the server uses the binding handle as though it were declared explicitly.</span></span>

<span data-ttu-id="ee55f-132">從系結控制碼解壓縮用戶端認證的程式會如下所示：</span><span class="sxs-lookup"><span data-stu-id="ee55f-132">The process of extracting the client credentials from the binding handle occurs as follows:</span></span>

-   <span data-ttu-id="ee55f-133">RPC 用戶端會呼叫 [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) ，並在傳遞至伺服器的系結資訊中包含其驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="ee55f-133">RPC clients call [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) and include their authentication information as part of the binding information passed to the server.</span></span>
-   <span data-ttu-id="ee55f-134">通常，伺服器會呼叫 [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) ，以便如同用戶端一樣運作。</span><span class="sxs-lookup"><span data-stu-id="ee55f-134">Usually, the server calls [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) in order to behave as though it were the client.</span></span> <span data-ttu-id="ee55f-135">如果系結控制碼未經過驗證，則呼叫會失敗，而且 RPC \_ S \_ 沒有 \_ 內容 \_ 可用。</span><span class="sxs-lookup"><span data-stu-id="ee55f-135">If the binding handle is not authenticated, the call fails with RPC\_S\_NO\_CONTEXT\_AVAILABLE.</span></span> <span data-ttu-id="ee55f-136">若要取得用戶端的使用者名稱，請在模擬時呼叫 [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) ，或是在 windows XP 或更新版本的 windows 上呼叫 [**RpcGetAuthorizationCoNtextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) 來取得授權內容，然後使用 Authz 函式來取得名稱。</span><span class="sxs-lookup"><span data-stu-id="ee55f-136">To obtain the client's user name, call [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) while impersonating, or on Windows XP or later versions of Windows, call [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) to get the authorization context, then use Authz functions to retrieve the name.</span></span>
-   <span data-ttu-id="ee55f-137">伺服器通常會呼叫 [**CreatePrivateObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity) 來建立具有 acl 的物件。</span><span class="sxs-lookup"><span data-stu-id="ee55f-137">The server will normally call [**CreatePrivateObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity) to create objects with ACLs.</span></span> <span data-ttu-id="ee55f-138">完成這項作業之後，稍後的安全性檢查就會變成自動。</span><span class="sxs-lookup"><span data-stu-id="ee55f-138">After this is accomplished, later security checks become automatic.</span></span>

 

 