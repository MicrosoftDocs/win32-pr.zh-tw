---
title: " (RpcDce 的授權常數) "
description: 定義伺服器授權的內容。
ms.assetid: a0bc9337-b7e4-41c5-ae36-4843fa7d98ce
topic_type:
- apiref
api_name:
- RPC_C_AUTHZ_NONE
- RPC_C_AUTHZ_NAME
- RPC_C_AUTHZ_DCE
- RPC_C_AUTHZ_DEFAULT
api_location:
- RpcDce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed2c46ad729e02fd63eb9b8088d31f05515c2ef8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686532"
---
# <a name="authorization-constants"></a><span data-ttu-id="09fb6-103">授權常數</span><span class="sxs-lookup"><span data-stu-id="09fb6-103">Authorization Constants</span></span>

<span data-ttu-id="09fb6-104">定義伺服器授權的內容。</span><span class="sxs-lookup"><span data-stu-id="09fb6-104">Defines what the server authorizes.</span></span>



| <span data-ttu-id="09fb6-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="09fb6-105">Constant/value</span></span>                                                                                                                                                                                                                                    | <span data-ttu-id="09fb6-106">Description</span><span class="sxs-lookup"><span data-stu-id="09fb6-106">Description</span></span>                                                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHZ_NONE"></span><span id="rpc_c_authz_none"></span><dl> <span data-ttu-id="09fb6-107"><dt>**RPC \_C \_ AUTHZ \_ 無**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="09fb6-107"><dt>**RPC\_C\_AUTHZ\_NONE**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="09fb6-108">伺服器不會執行任何授權。</span><span class="sxs-lookup"><span data-stu-id="09fb6-108">The server performs no authorization.</span></span> <span data-ttu-id="09fb6-109">目前，RPC \_ c \_ 驗證 \_ WINNT、rpc \_ c \_ 驗證 \_ gss \_ SCHANNEL 和 rpc \_ c \_ 驗證 \_ GSS \_ KERBEROS 全都只使用 rpc \_ c \_ 授權 \_ 無。</span><span class="sxs-lookup"><span data-stu-id="09fb6-109">Currently, RPC\_C\_AUTHN\_WINNT, RPC\_C\_AUTHN\_GSS\_SCHANNEL, and RPC\_C\_AUTHN\_GSS\_KERBEROS all use only RPC\_C\_AUTHZ\_NONE.</span></span><br/>                                                                                                                |
| <span id="RPC_C_AUTHZ_NAME"></span><span id="rpc_c_authz_name"></span><dl> <span data-ttu-id="09fb6-110"><dt>**RPC \_C \_ AUTHZ \_ 名稱**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="09fb6-110"><dt>**RPC\_C\_AUTHZ\_NAME**</dt> <dt>1</dt></span></span> </dl>                   | <span data-ttu-id="09fb6-111">伺服器會根據用戶端的主體名稱執行授權。</span><span class="sxs-lookup"><span data-stu-id="09fb6-111">The server performs authorization based on the client's principal name.</span></span> <br/>                                                                                                                                                                                                               |
| <span id="RPC_C_AUTHZ_DCE"></span><span id="rpc_c_authz_dce"></span><dl> <span data-ttu-id="09fb6-112"><dt>**RPC \_C \_ AUTHZ \_ DCE**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="09fb6-112"><dt>**RPC\_C\_AUTHZ\_DCE**</dt> <dt>2</dt></span></span> </dl>                      | <span data-ttu-id="09fb6-113">伺服器會使用用戶端的 DCE 許可權屬性憑證來執行授權檢查 (PAC) 資訊，此資訊會透過使用系結控制碼的每個遠端程序呼叫傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="09fb6-113">The server performs authorization checking using the client's DCE privilege attribute certificate (PAC) information, which is sent to the server with each remote procedure call made using the binding handle.</span></span> <span data-ttu-id="09fb6-114">一般而言，會根據 (Acl) 的 DCE 存取控制清單來檢查存取權。</span><span class="sxs-lookup"><span data-stu-id="09fb6-114">Generally, access is checked against DCE access control lists (ACLs).</span></span> <br/> |
| <span id="RPC_C_AUTHZ_DEFAULT"></span><span id="rpc_c_authz_default"></span><dl> <span data-ttu-id="09fb6-115"><dt>**RPC \_C \_ 授權 \_ 預設**</dt>為 <dt>0xffffffff</dt></span><span class="sxs-lookup"><span data-stu-id="09fb6-115"><dt>**RPC\_C\_AUTHZ\_DEFAULT**</dt> <dt>0xffffffff</dt></span></span> </dl> | <span data-ttu-id="09fb6-116">DCOM 可以選擇使用其一般安全性整體協商演算法的授權層級。</span><span class="sxs-lookup"><span data-stu-id="09fb6-116">DCOM can choose the authorization level using its normal security blanket negotiation algorithm.</span></span> <span data-ttu-id="09fb6-117">如需詳細資訊，請參閱 [安全性綜合協商](security-blanket-negotiation.md)。</span><span class="sxs-lookup"><span data-stu-id="09fb6-117">For more information, see [Security Blanket Negotiation](security-blanket-negotiation.md).</span></span><br/>                                                                                           |



## <a name="remarks"></a><span data-ttu-id="09fb6-118">備註</span><span class="sxs-lookup"><span data-stu-id="09fb6-118">Remarks</span></span>

<span data-ttu-id="09fb6-119">[**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity)介面的方法會使用這些常數。</span><span class="sxs-lookup"><span data-stu-id="09fb6-119">These constants are used by methods of the [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) interface.</span></span> <span data-ttu-id="09fb6-120">它們是在 [**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices)函式所取出的 [**唯一 \_ 驗證 \_ 服務**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service)結構中使用。</span><span class="sxs-lookup"><span data-stu-id="09fb6-120">They are used in the [**SOLE\_AUTHENTICATION\_SERVICE**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) structure, which is retrieved by the [**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) function.</span></span> <span data-ttu-id="09fb6-121">它們也會用在 [**唯一的 \_ 驗證 \_ 資訊**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) 結構中，而後者又是 [**唯一 \_ 驗證 \_ 清單**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="09fb6-121">They are also used in the [**SOLE\_AUTHENTICATION\_INFO**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) structure, which in turn is a member of the [**SOLE\_AUTHENTICATION\_LIST**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list) structure.</span></span> <span data-ttu-id="09fb6-122">此結構是驗證服務的清單、他們執行的授權服務，以及每個服務的驗證資訊，都會傳遞至 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 函式和 [**IClientSecurity：： SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) 方法。</span><span class="sxs-lookup"><span data-stu-id="09fb6-122">This structure, which is a list of authentication services, the authorization services they perform, and the authentication information for each service, is passed to the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) function and the [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="09fb6-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="09fb6-123">Requirements</span></span>



| <span data-ttu-id="09fb6-124">需求</span><span class="sxs-lookup"><span data-stu-id="09fb6-124">Requirement</span></span> | <span data-ttu-id="09fb6-125">值</span><span class="sxs-lookup"><span data-stu-id="09fb6-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="09fb6-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="09fb6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="09fb6-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09fb6-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="09fb6-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="09fb6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="09fb6-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09fb6-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="09fb6-130">標頭</span><span class="sxs-lookup"><span data-stu-id="09fb6-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="09fb6-131"><dt>RpcDce。h</dt></span><span class="sxs-lookup"><span data-stu-id="09fb6-131"><dt>RpcDce.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09fb6-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="09fb6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09fb6-133">**CoInitializeSecurity**</span><span class="sxs-lookup"><span data-stu-id="09fb6-133">**CoInitializeSecurity**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[<span data-ttu-id="09fb6-134">**CoQueryAuthenticationServices**</span><span class="sxs-lookup"><span data-stu-id="09fb6-134">**CoQueryAuthenticationServices**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices)
</dt> <dt>

[<span data-ttu-id="09fb6-135">**IClientSecurity**</span><span class="sxs-lookup"><span data-stu-id="09fb6-135">**IClientSecurity**</span></span>](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity)
</dt> <dt>

[<span data-ttu-id="09fb6-136">**唯一 \_ 驗證 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="09fb6-136">**SOLE\_AUTHENTICATION\_INFO**</span></span>](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info)
</dt> <dt>

[<span data-ttu-id="09fb6-137">**唯一 \_ 驗證 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="09fb6-137">**SOLE\_AUTHENTICATION\_SERVICE**</span></span>](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service)
</dt> </dl>

 

