---
title: 控制用戶端驗證
description: 驗證用戶端的最佳方法是使用 RpcServerRegisterIf2 或 RpcServerRegisterIfEx 函式安裝安全性回呼函數;接受安全性回呼函數做為引數。
ms.assetid: 3e858a71-9190-44a3-bc63-08cfbd02d443
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3508e99b351cd57fb67a3727710b60562ffe25dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839888"
---
# <a name="controlling-client-authentication"></a><span data-ttu-id="4f477-103">控制用戶端驗證</span><span class="sxs-lookup"><span data-stu-id="4f477-103">Controlling Client Authentication</span></span>

<span data-ttu-id="4f477-104">驗證用戶端的最佳方法是使用 [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) 或 [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) 函式安裝安全性回呼函數;接受安全性回呼函數做為引數。</span><span class="sxs-lookup"><span data-stu-id="4f477-104">The best method for authenticating a client is installing a security callback function using the [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) or [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) function; either accepts a security callback function as an argument.</span></span> <span data-ttu-id="4f477-105">呼叫安全性回呼函式時，請進行必要的檢查。</span><span class="sxs-lookup"><span data-stu-id="4f477-105">When the security callback function is called, make the necessary checks.</span></span> <span data-ttu-id="4f477-106">您可以檢查連接上的屬性、呼叫端的身分識別，或兩者都有。</span><span class="sxs-lookup"><span data-stu-id="4f477-106">The attributes on the connection, identity of the caller, or both, can be checked.</span></span> <span data-ttu-id="4f477-107">若要檢查連接的屬性，請呼叫 [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) 或 [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) 函數。</span><span class="sxs-lookup"><span data-stu-id="4f477-107">To check the attributes of a connection, call the [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) or [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) function.</span></span> <span data-ttu-id="4f477-108">這可讓您篩選未經過驗證的用戶端、使用特定安全性提供者的用戶端，或未使用強式保護的用戶端 (例如隱私權) 。</span><span class="sxs-lookup"><span data-stu-id="4f477-108">This enables the filtering of clients that are not authenticated, clients that use a specific security provider, or clients that do not use strong enough protection (like privacy).</span></span>

<span data-ttu-id="4f477-109">若要允許存取已驗證的使用者子集，請使用 [**RpcGetAuthorizationCoNtextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient)。</span><span class="sxs-lookup"><span data-stu-id="4f477-109">To allow access to a subset of the authenticated users, use [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient).</span></span> <span data-ttu-id="4f477-110">此函數會傳回可用於進行非常複雜之存取檢查的 Authz 用戶端內容。</span><span class="sxs-lookup"><span data-stu-id="4f477-110">This function returns an Authz client context that can be used to make very sophisticated access checks.</span></span> <span data-ttu-id="4f477-111">例如，您可以使用此方法，在正常上班時間內只允許存取組織中的副總裁，以及使用 Active Directory 服務將使用者名稱對應至其標題的任何小時。</span><span class="sxs-lookup"><span data-stu-id="4f477-111">For example, this method could be used to allow access only to the vice presidents in an organization during normal business hours, and to the CEO during any hour using Active Directory services to map a user name to their title.</span></span> <span data-ttu-id="4f477-112">使用者可以模擬，並取得其名稱。</span><span class="sxs-lookup"><span data-stu-id="4f477-112">The user can be impersonated, and their name obtained.</span></span> <span data-ttu-id="4f477-113">知道他們的身分識別之後，就可以進行任何所需的檢查。</span><span class="sxs-lookup"><span data-stu-id="4f477-113">Once their identity is known, any desired checks can be made.</span></span>

 

 




