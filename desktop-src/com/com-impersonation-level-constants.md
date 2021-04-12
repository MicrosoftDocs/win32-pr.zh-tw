---
title: '模擬層級常數 (RpcDce .h) '
description: 指定模擬等級，指出當伺服器模擬用戶端時，提供給伺服器的授權數量。
ms.assetid: ea5a3b46-b607-4192-a3cc-b2ec55ca94a6
topic_type:
- apiref
api_name:
- RPC_C_IMP_LEVEL_DEFAULT
- RPC_C_IMP_LEVEL_ANONYMOUS
- RPC_C_IMP_LEVEL_IDENTIFY
- RPC_C_IMP_LEVEL_IMPERSONATE
- RPC_C_IMP_LEVEL_DELEGATE
api_location:
- RpcDce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9f16ed07235e52d9aefd7bffff9ce430c3978d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317280"
---
# <a name="impersonation-level-constants"></a><span data-ttu-id="0a4cc-103">模擬層級常數</span><span class="sxs-lookup"><span data-stu-id="0a4cc-103">Impersonation Level Constants</span></span>

<span data-ttu-id="0a4cc-104">指定模擬等級，指出當伺服器模擬用戶端時，提供給伺服器的授權數量。</span><span class="sxs-lookup"><span data-stu-id="0a4cc-104">Specifies an impersonation level, which indicates the amount of authority given to the server when it is impersonating the client.</span></span>



| <span data-ttu-id="0a4cc-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="0a4cc-105">Constant/value</span></span>                                                                                                                                                                                                                                                    | <span data-ttu-id="0a4cc-106">Description</span><span class="sxs-lookup"><span data-stu-id="0a4cc-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_IMP_LEVEL_DEFAULT"></span><span id="rpc_c_imp_level_default"></span><dl> <span data-ttu-id="0a4cc-107"><dt>**RPC \_C \_ IMP \_ 層級 \_ 預設值**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0a4cc-107"><dt>**RPC\_C\_IMP\_LEVEL\_DEFAULT**</dt> <dt>0</dt></span></span> </dl>             | <span data-ttu-id="0a4cc-108">DCOM 可以選擇使用其一般安全性整體協商演算法的模擬等級。</span><span class="sxs-lookup"><span data-stu-id="0a4cc-108">DCOM can choose the impersonation level using its normal security blanket negotiation algorithm.</span></span> <span data-ttu-id="0a4cc-109">如需詳細資訊，請參閱 [安全性綜合協商](security-blanket-negotiation.md)。</span><span class="sxs-lookup"><span data-stu-id="0a4cc-109">For more information, see [Security Blanket Negotiation](security-blanket-negotiation.md).</span></span><br/>                                                                                                                                                                                                                                                                           |
| <span id="RPC_C_IMP_LEVEL_ANONYMOUS"></span><span id="rpc_c_imp_level_anonymous"></span><dl> <span data-ttu-id="0a4cc-110"><dt>**RPC \_C \_ IMP \_ 層級 \_ 匿名**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0a4cc-110"><dt>**RPC\_C\_IMP\_LEVEL\_ANONYMOUS**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="0a4cc-111">用戶端對伺服器而言是匿名。</span><span class="sxs-lookup"><span data-stu-id="0a4cc-111">The client is anonymous to the server.</span></span> <span data-ttu-id="0a4cc-112">伺服器進程可以模擬用戶端，但模擬權杖將不會包含任何資訊，也無法使用。</span><span class="sxs-lookup"><span data-stu-id="0a4cc-112">The server process can impersonate the client, but the impersonation token will not contain any information and cannot be used.</span></span><br/>                                                                                                                                                                                                                                                                                                 |
| <span id="RPC_C_IMP_LEVEL_IDENTIFY"></span><span id="rpc_c_imp_level_identify"></span><dl> <span data-ttu-id="0a4cc-113"><dt>**RPC \_C \_ IMP \_ 層級 \_ 識別**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0a4cc-113"><dt>**RPC\_C\_IMP\_LEVEL\_IDENTIFY**</dt> <dt>2</dt></span></span> </dl>          | <span data-ttu-id="0a4cc-114">伺服器可以取得用戶端的身分識別。</span><span class="sxs-lookup"><span data-stu-id="0a4cc-114">The server can obtain the client's identity.</span></span> <span data-ttu-id="0a4cc-115">伺服器可以模擬用戶端進行 ACL 檢查，但是無法存取系統物件做為用戶端。</span><span class="sxs-lookup"><span data-stu-id="0a4cc-115">The server can impersonate the client for ACL checking, but it cannot access system objects as the client.</span></span> <br/>                                                                                                                                                                                                                                                                                                               |
| <span id="RPC_C_IMP_LEVEL_IMPERSONATE"></span><span id="rpc_c_imp_level_impersonate"></span><dl> <span data-ttu-id="0a4cc-116"><dt>**RPC \_C \_ IMP \_ 層 \_ 級**</dt>模擬 <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="0a4cc-116"><dt>**RPC\_C\_IMP\_LEVEL\_IMPERSONATE**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="0a4cc-117">伺服器進程可在代表用戶端時模擬用戶端的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="0a4cc-117">The server process can impersonate the client's security context while acting on behalf of the client.</span></span> <span data-ttu-id="0a4cc-118">此層級的模擬可用來存取本機資源，例如檔案。</span><span class="sxs-lookup"><span data-stu-id="0a4cc-118">This level of impersonation can be used to access local resources such as files.</span></span> <span data-ttu-id="0a4cc-119">模擬此層級時，模擬權杖只能跨一個電腦界限傳遞。</span><span class="sxs-lookup"><span data-stu-id="0a4cc-119">When impersonating at this level, the impersonation token can only be passed across one machine boundary.</span></span> <span data-ttu-id="0a4cc-120">[Schannel](schannel.md)驗證服務只支援此層級的模擬。</span><span class="sxs-lookup"><span data-stu-id="0a4cc-120">The [Schannel](schannel.md) authentication service only supports this level of impersonation.</span></span> <br/>                                                                      |
| <span id="RPC_C_IMP_LEVEL_DELEGATE"></span><span id="rpc_c_imp_level_delegate"></span><dl> <span data-ttu-id="0a4cc-121"><dt>**RPC \_C \_ IMP \_ 層級 \_ 委派**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="0a4cc-121"><dt>**RPC\_C\_IMP\_LEVEL\_DELEGATE**</dt> <dt>4</dt></span></span> </dl>          | <span data-ttu-id="0a4cc-122">伺服器進程可在代表用戶端時模擬用戶端的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="0a4cc-122">The server process can impersonate the client's security context while acting on behalf of the client.</span></span> <span data-ttu-id="0a4cc-123">伺服器進程也可以在代表用戶端的情況下，使用掩蓋來撥打電話給其他伺服器。</span><span class="sxs-lookup"><span data-stu-id="0a4cc-123">The server process can also make outgoing calls to other servers while acting on behalf of the client, using cloaking.</span></span> <span data-ttu-id="0a4cc-124">伺服器可能會在其他電腦上使用用戶端的安全性內容，以用戶端的形式存取本機和遠端資源。</span><span class="sxs-lookup"><span data-stu-id="0a4cc-124">The server may use the client's security context on other machines to access local and remote resources as the client.</span></span> <span data-ttu-id="0a4cc-125">當模擬此層級時，模擬權杖可以跨任意數目的電腦界限傳遞。</span><span class="sxs-lookup"><span data-stu-id="0a4cc-125">When impersonating at this level, the impersonation token can be passed across any number of computer boundaries.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0a4cc-126">備註</span><span class="sxs-lookup"><span data-stu-id="0a4cc-126">Remarks</span></span>

<span data-ttu-id="0a4cc-127">在識別層級進行模擬時， [**GetUserName**](/windows/desktop/api/winbase/nf-winbase-getusernamea)將會失敗。</span><span class="sxs-lookup"><span data-stu-id="0a4cc-127">[**GetUserName**](/windows/desktop/api/winbase/nf-winbase-getusernamea) will fail while impersonating at identify level.</span></span> <span data-ttu-id="0a4cc-128">解決方法是模擬、呼叫 [**OpenThreadToken**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken)、還原、呼叫 [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation)，最後呼叫 [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida)。</span><span class="sxs-lookup"><span data-stu-id="0a4cc-128">The workaround is to impersonate, call [**OpenThreadToken**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken), revert, call [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation), and finally, call [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida).</span></span> <span data-ttu-id="0a4cc-129">使用 [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)，用戶端會設定模擬等級</span><span class="sxs-lookup"><span data-stu-id="0a4cc-129">Using [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), the client sets the impersonation level</span></span>

<span data-ttu-id="0a4cc-130">用戶端會使用 [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)來設定模擬等級和 proxy 身分識別，以便在伺服器呼叫 [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)時使用。</span><span class="sxs-lookup"><span data-stu-id="0a4cc-130">Using [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), the client sets the impersonation level and proxy identity that will be available when a server calls [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient).</span></span> <span data-ttu-id="0a4cc-131">在進行模擬時，伺服器將會看到的身分識別會在 [掩蓋](cloaking.md)中描述。</span><span class="sxs-lookup"><span data-stu-id="0a4cc-131">The identity the server will see when impersonating takes place is described in [Cloaking](cloaking.md).</span></span> <span data-ttu-id="0a4cc-132">請注意，在模擬時進行呼叫時，被呼叫端通常會接收呼叫端的進程權杖，而不是呼叫端的模擬權杖。</span><span class="sxs-lookup"><span data-stu-id="0a4cc-132">Note that when making a call while impersonating, the callee will normally receive the caller's process token, not the caller's impersonation token.</span></span> <span data-ttu-id="0a4cc-133">若要接收呼叫端的模擬權杖，呼叫端必須啟用遮蓋。</span><span class="sxs-lookup"><span data-stu-id="0a4cc-133">To receive the caller's impersonation token, the caller must enable cloaking.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a4cc-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a4cc-134">Requirements</span></span>



| <span data-ttu-id="0a4cc-135">需求</span><span class="sxs-lookup"><span data-stu-id="0a4cc-135">Requirement</span></span> | <span data-ttu-id="0a4cc-136">值</span><span class="sxs-lookup"><span data-stu-id="0a4cc-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0a4cc-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0a4cc-137">Minimum supported client</span></span><br/> | <span data-ttu-id="0a4cc-138">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a4cc-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0a4cc-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0a4cc-139">Minimum supported server</span></span><br/> | <span data-ttu-id="0a4cc-140">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a4cc-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0a4cc-141">標頭</span><span class="sxs-lookup"><span data-stu-id="0a4cc-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a4cc-142"><dt>RpcDce。h</dt></span><span class="sxs-lookup"><span data-stu-id="0a4cc-142"><dt>RpcDce.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a4cc-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a4cc-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a4cc-144">隱形</span><span class="sxs-lookup"><span data-stu-id="0a4cc-144">Cloaking</span></span>](cloaking.md)
</dt> </dl>

 

