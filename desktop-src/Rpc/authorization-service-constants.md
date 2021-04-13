---
title: 'Authorization-Service 常數 (Rpcdce) '
description: 授權服務常數代表傳遞給各種執行時間函數的授權服務。
ms.assetid: b773bb51-7af0-4eb3-9438-fe3ef9a350db
topic_type:
- apiref
api_name:
- RPC_C_AUTHZ_NONE
- RPC_C_AUTHZ_NAME
- RPC_C_AUTHZ_DCE
- RPC_C_AUTHZ_DEFAULT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0394163e97a822126e71eeda3cf8382f1dcc20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509478"
---
# <a name="authorization-service-constants"></a><span data-ttu-id="29316-103">Authorization-Service 常數</span><span class="sxs-lookup"><span data-stu-id="29316-103">Authorization-Service Constants</span></span>

<span data-ttu-id="29316-104">授權服務常數代表傳遞給各種執行時間函數的授權服務。</span><span class="sxs-lookup"><span data-stu-id="29316-104">The authorization service constants represent the authorization services passed to various run-time functions.</span></span>

<span data-ttu-id="29316-105">下列常數是 *AuthzSvc* 參數的有效值。</span><span class="sxs-lookup"><span data-stu-id="29316-105">The following constants are valid values for the *AuthzSvc* parameter.</span></span> <span data-ttu-id="29316-106">大部分的應用程式都發現 RPC \_ C \_ AUTHZ \_ 沒有足夠的許可權。</span><span class="sxs-lookup"><span data-stu-id="29316-106">Most applications find RPC\_C\_AUTHZ\_NON sufficient.</span></span>



| <span data-ttu-id="29316-107">常數/值</span><span class="sxs-lookup"><span data-stu-id="29316-107">Constant/value</span></span>                                                                                                                                                                                                                                    | <span data-ttu-id="29316-108">Description</span><span class="sxs-lookup"><span data-stu-id="29316-108">Description</span></span>                                                                                                                                                                                                                                                                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHZ_NONE"></span><span id="rpc_c_authz_none"></span><dl> <span data-ttu-id="29316-109"><dt>**RPC \_C \_ AUTHZ \_ 無**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="29316-109"><dt>**RPC\_C\_AUTHZ\_NONE**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="29316-110">伺服器不會執行任何授權。</span><span class="sxs-lookup"><span data-stu-id="29316-110">Server performs no authorization.</span></span><br/>                                                                                                                                                                                                                                                                 |
| <span id="RPC_C_AUTHZ_NAME"></span><span id="rpc_c_authz_name"></span><dl> <span data-ttu-id="29316-111"><dt>**RPC \_C \_ AUTHZ \_ 名稱**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="29316-111"><dt>**RPC\_C\_AUTHZ\_NAME**</dt> <dt>1</dt></span></span> </dl>                   | <span data-ttu-id="29316-112">伺服器會根據用戶端的主體名稱執行授權。</span><span class="sxs-lookup"><span data-stu-id="29316-112">Server performs authorization based on the client's principal name.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="RPC_C_AUTHZ_DCE"></span><span id="rpc_c_authz_dce"></span><dl> <span data-ttu-id="29316-113"><dt>**RPC \_C \_ AUTHZ \_ DCE**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="29316-113"><dt>**RPC\_C\_AUTHZ\_DCE**</dt> <dt>2</dt></span></span> </dl>                      | <span data-ttu-id="29316-114">伺服器會使用用戶端的 DCE 許可權屬性憑證來執行授權檢查 (PAC) 資訊，此資訊會透過使用系結控制碼的每個遠端程序呼叫傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="29316-114">Server performs authorization checking using the client's DCE privilege attribute certificate (PAC) information, which is sent to the server with each remote procedure call made using the binding handle.</span></span> <span data-ttu-id="29316-115">一般而言，會根據 ([acl](/windows/desktop/api/winnt/ns-winnt-acl)) 的 DCE 存取控制清單來檢查存取權。</span><span class="sxs-lookup"><span data-stu-id="29316-115">Generally, access is checked against DCE access control lists ([ACLs](/windows/desktop/api/winnt/ns-winnt-acl)).</span></span><br/> |
| <span id="RPC_C_AUTHZ_DEFAULT"></span><span id="rpc_c_authz_default"></span><dl> <span data-ttu-id="29316-116"><dt>**RPC \_C \_ 授權 \_ 預設**</dt>為 <dt>0xffffffff</dt></span><span class="sxs-lookup"><span data-stu-id="29316-116"><dt>**RPC\_C\_AUTHZ\_DEFAULT**</dt> <dt>0xffffffff</dt></span></span> </dl> | <span data-ttu-id="29316-117">伺服器使用目前 SSP 的預設授權服務。</span><span class="sxs-lookup"><span data-stu-id="29316-117">Server uses the default authorization service for the current SSP.</span></span><br/>                                                                                                                                                                                                                                |



## <a name="requirements"></a><span data-ttu-id="29316-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="29316-118">Requirements</span></span>



| <span data-ttu-id="29316-119">需求</span><span class="sxs-lookup"><span data-stu-id="29316-119">Requirement</span></span> | <span data-ttu-id="29316-120">值</span><span class="sxs-lookup"><span data-stu-id="29316-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="29316-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="29316-121">Minimum supported client</span></span><br/> | <span data-ttu-id="29316-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29316-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="29316-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="29316-123">Minimum supported server</span></span><br/> | <span data-ttu-id="29316-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29316-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="29316-125">標頭</span><span class="sxs-lookup"><span data-stu-id="29316-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="29316-126"><dt>Rpcdce。h</dt></span><span class="sxs-lookup"><span data-stu-id="29316-126"><dt>Rpcdce.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29316-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="29316-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29316-128">**RpcBindingInqAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="29316-128">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[<span data-ttu-id="29316-129">**RpcBindingSetAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="29316-129">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> <dt>

[<span data-ttu-id="29316-130">**RpcBindingInqAuthClient**</span><span class="sxs-lookup"><span data-stu-id="29316-130">**RpcBindingInqAuthClient**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[<span data-ttu-id="29316-131">**RpcBindingInqAuthClientEx**</span><span class="sxs-lookup"><span data-stu-id="29316-131">**RpcBindingInqAuthClientEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[<span data-ttu-id="29316-132">**RpcBindingSetAuthInfoEx**</span><span class="sxs-lookup"><span data-stu-id="29316-132">**RpcBindingSetAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[<span data-ttu-id="29316-133">**RpcBindingInqAuthInfoEx**</span><span class="sxs-lookup"><span data-stu-id="29316-133">**RpcBindingInqAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> <dt>

[<span data-ttu-id="29316-134">**RpcMgmtInqDefaultProtectLevel**</span><span class="sxs-lookup"><span data-stu-id="29316-134">**RpcMgmtInqDefaultProtectLevel**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqdefaultprotectlevel)
</dt> </dl>

 

