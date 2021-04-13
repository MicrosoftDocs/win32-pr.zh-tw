---
title: 'Authentication-Level 常數 (Rpcdce) '
description: 驗證層級常數代表傳遞給各種執行時間函數的驗證層級。
ms.assetid: b8bb2517-e1a0-4607-a672-259f8686fc3e
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_LEVEL_DEFAULT
- RPC_C_AUTHN_LEVEL_NONE
- RPC_C_AUTHN_LEVEL_CONNECT
- RPC_C_AUTHN_LEVEL_CALL
- RPC_C_AUTHN_LEVEL_PKT
- RPC_C_AUTHN_LEVEL_PKT_INTEGRITY
- RPC_C_AUTHN_LEVEL_PKT_PRIVACY
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 114e5624b2cbc8af0b86a29daff2c1761f6fee39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509208"
---
# <a name="authentication-level-constants"></a><span data-ttu-id="9f1ba-103">驗證層級常數</span><span class="sxs-lookup"><span data-stu-id="9f1ba-103">Authentication-Level Constants</span></span>

<span data-ttu-id="9f1ba-104">驗證層級常數代表傳遞給各種執行時間函數的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="9f1ba-104">The authentication-level constants represent authentication levels passed to various run-time functions.</span></span> <span data-ttu-id="9f1ba-105">這些層級會依提高驗證順序列出。</span><span class="sxs-lookup"><span data-stu-id="9f1ba-105">These levels are listed in order of increasing authentication.</span></span> <span data-ttu-id="9f1ba-106">每個新層級都會加入至上一個層級所提供的驗證。</span><span class="sxs-lookup"><span data-stu-id="9f1ba-106">Each new level adds to the authentication provided by the previous level.</span></span> <span data-ttu-id="9f1ba-107">如果 RPC 執行時間程式庫不支援指定的層級，則會自動升級至下一個較高的支援層級。</span><span class="sxs-lookup"><span data-stu-id="9f1ba-107">If the RPC run-time library does not support the specified level, it automatically upgrades to the next higher supported level.</span></span>



| <span data-ttu-id="9f1ba-108">常數</span><span class="sxs-lookup"><span data-stu-id="9f1ba-108">Constant</span></span>                                                                                                                                                                                                                | <span data-ttu-id="9f1ba-109">描述</span><span class="sxs-lookup"><span data-stu-id="9f1ba-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_LEVEL_DEFAULT"></span><span id="rpc_c_authn_level_default"></span><dl> <span data-ttu-id="9f1ba-110"><dt>**RPC \_ C \_ 驗證 \_ 層級 \_ 預設值**</dt></span><span class="sxs-lookup"><span data-stu-id="9f1ba-110"><dt>**RPC\_C\_AUTHN\_LEVEL\_DEFAULT**</dt></span></span> </dl>                    | <span data-ttu-id="9f1ba-111">使用指定驗證服務的預設驗證層級。</span><span class="sxs-lookup"><span data-stu-id="9f1ba-111">Uses the default authentication level for the specified authentication service.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_LEVEL_NONE"></span><span id="rpc_c_authn_level_none"></span><dl> <span data-ttu-id="9f1ba-112"><dt>**RPC \_ C \_ 驗證 \_ 層級 \_ 無**</dt></span><span class="sxs-lookup"><span data-stu-id="9f1ba-112"><dt>**RPC\_C\_AUTHN\_LEVEL\_NONE**</dt></span></span> </dl>                             | <span data-ttu-id="9f1ba-113">不執行任何驗證。</span><span class="sxs-lookup"><span data-stu-id="9f1ba-113">Performs no authentication.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="RPC_C_AUTHN_LEVEL_CONNECT"></span><span id="rpc_c_authn_level_connect"></span><dl> <span data-ttu-id="9f1ba-114"><dt>**RPC \_ C \_ 驗證 \_ LEVEL \_ CONNECT**</dt></span><span class="sxs-lookup"><span data-stu-id="9f1ba-114"><dt>**RPC\_C\_AUTHN\_LEVEL\_CONNECT**</dt></span></span> </dl>                    | <span data-ttu-id="9f1ba-115">只有在用戶端與伺服器建立關聯性時才會驗證。</span><span class="sxs-lookup"><span data-stu-id="9f1ba-115">Authenticates only when the client establishes a relationship with a server.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="RPC_C_AUTHN_LEVEL_CALL"></span><span id="rpc_c_authn_level_call"></span><dl> <span data-ttu-id="9f1ba-116"><dt>**RPC \_ C \_ 驗證 \_ 層級 \_ 呼叫**</dt></span><span class="sxs-lookup"><span data-stu-id="9f1ba-116"><dt>**RPC\_C\_AUTHN\_LEVEL\_CALL**</dt></span></span> </dl>                             | <span data-ttu-id="9f1ba-117">當伺服器收到要求時，只會在每個遠端程序呼叫的開頭進行驗證。</span><span class="sxs-lookup"><span data-stu-id="9f1ba-117">Authenticates only at the beginning of each remote procedure call when the server receives the request.</span></span> <span data-ttu-id="9f1ba-118">不會套用至使用以連線為基礎的通訊協定順序所建立的遠端程序呼叫， (開頭為 "ncacn" 前置詞的 ) 。</span><span class="sxs-lookup"><span data-stu-id="9f1ba-118">Does not apply to remote procedure calls made using the connection-based protocol sequences (those that start with the prefix "ncacn").</span></span> <span data-ttu-id="9f1ba-119">如果系結控制碼中的通訊協定順序是以連線為基礎的通訊協定順序，而您指定此層級，則此常式會改為使用 RPC \_ C \_ 驗證 \_ 層級的 \_ PKT 常數。</span><span class="sxs-lookup"><span data-stu-id="9f1ba-119">If the protocol sequence in a binding handle is a connection-based protocol sequence and you specify this level, this routine instead uses the RPC\_C\_AUTHN\_LEVEL\_PKT constant.</span></span><br/> |
| <span id="RPC_C_AUTHN_LEVEL_PKT"></span><span id="rpc_c_authn_level_pkt"></span><dl> <span data-ttu-id="9f1ba-120"><dt>**RPC \_ C \_ 驗證 \_ 層級 \_ PKT**</dt></span><span class="sxs-lookup"><span data-stu-id="9f1ba-120"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT**</dt></span></span> </dl>                                | <span data-ttu-id="9f1ba-121">只會驗證收到的所有資料來自預期的用戶端。</span><span class="sxs-lookup"><span data-stu-id="9f1ba-121">Authenticates only that all data received is from the expected client.</span></span> <span data-ttu-id="9f1ba-122">不會驗證資料本身。</span><span class="sxs-lookup"><span data-stu-id="9f1ba-122">Does not validate the data itself.</span></span><br/>                                                                                                                                                                                                                                                                                                                          |
| <span id="RPC_C_AUTHN_LEVEL_PKT_INTEGRITY"></span><span id="rpc_c_authn_level_pkt_integrity"></span><dl> <span data-ttu-id="9f1ba-123"><dt>**RPC \_ C \_ 驗證 \_ 層級 \_ PKT \_ 完整性**</dt></span><span class="sxs-lookup"><span data-stu-id="9f1ba-123"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY**</dt></span></span> </dl> | <span data-ttu-id="9f1ba-124">驗證並確認在用戶端與伺服器之間傳送的資料都沒有修改。</span><span class="sxs-lookup"><span data-stu-id="9f1ba-124">Authenticates and verifies that none of the data transferred between client and server has been modified.</span></span><br/>                                                                                                                                                                                                                                                                                                                          |
| <span id="RPC_C_AUTHN_LEVEL_PKT_PRIVACY"></span><span id="rpc_c_authn_level_pkt_privacy"></span><dl> <span data-ttu-id="9f1ba-125"><dt>**RPC \_ C \_ 驗證 \_ LEVEL \_ PKT \_ 隱私權**</dt></span><span class="sxs-lookup"><span data-stu-id="9f1ba-125"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**</dt></span></span> </dl>       | <span data-ttu-id="9f1ba-126">包含所有先前的層級，並確保只有寄件者和接收者可以看到純文字資料。</span><span class="sxs-lookup"><span data-stu-id="9f1ba-126">Includes all previous levels, and ensures clear text data can only be seen by the sender and the receiver.</span></span> <span data-ttu-id="9f1ba-127">在本機案例中，這牽涉到使用安全通道。</span><span class="sxs-lookup"><span data-stu-id="9f1ba-127">In the local case, this involves using a secure channel.</span></span> <span data-ttu-id="9f1ba-128">在遠端案例中，這牽涉到加密每個遠端程序呼叫的引數值。</span><span class="sxs-lookup"><span data-stu-id="9f1ba-128">In the remote case, this involves encrypting the argument value of each remote procedure call.</span></span><br/>                                                                                                                                                                 |



## <a name="remarks"></a><span data-ttu-id="9f1ba-129">備註</span><span class="sxs-lookup"><span data-stu-id="9f1ba-129">Remarks</span></span>

<span data-ttu-id="9f1ba-130">無論常數所指定的值為何， **ncalrpc** 一律會使用 RPC \_ C \_ 驗證 \_ 層 \_ 級 \_ 的 PKT 隱私權。</span><span class="sxs-lookup"><span data-stu-id="9f1ba-130">Regardless of the value specified by the constant, **ncalrpc** always uses RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f1ba-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f1ba-131">Requirements</span></span>



| <span data-ttu-id="9f1ba-132">需求</span><span class="sxs-lookup"><span data-stu-id="9f1ba-132">Requirement</span></span> | <span data-ttu-id="9f1ba-133">值</span><span class="sxs-lookup"><span data-stu-id="9f1ba-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9f1ba-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9f1ba-134">Minimum supported client</span></span><br/> | <span data-ttu-id="9f1ba-135">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f1ba-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9f1ba-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9f1ba-136">Minimum supported server</span></span><br/> | <span data-ttu-id="9f1ba-137">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f1ba-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9f1ba-138">標頭</span><span class="sxs-lookup"><span data-stu-id="9f1ba-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f1ba-139"><dt>Rpcdce。h</dt></span><span class="sxs-lookup"><span data-stu-id="9f1ba-139"><dt>Rpcdce.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f1ba-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9f1ba-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f1ba-141">**RpcBindingInqAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="9f1ba-141">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[<span data-ttu-id="9f1ba-142">**RpcBindingSetAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="9f1ba-142">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> <dt>

[<span data-ttu-id="9f1ba-143">**RpcMgmtInqDefaultProtectLevel**</span><span class="sxs-lookup"><span data-stu-id="9f1ba-143">**RpcMgmtInqDefaultProtectLevel**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqdefaultprotectlevel)
</dt> <dt>

[<span data-ttu-id="9f1ba-144">**RpcBindingInqAuthClient**</span><span class="sxs-lookup"><span data-stu-id="9f1ba-144">**RpcBindingInqAuthClient**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[<span data-ttu-id="9f1ba-145">**RpcBindingInqAuthClientEx**</span><span class="sxs-lookup"><span data-stu-id="9f1ba-145">**RpcBindingInqAuthClientEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[<span data-ttu-id="9f1ba-146">**RpcBindingSetAuthInfoEx**</span><span class="sxs-lookup"><span data-stu-id="9f1ba-146">**RpcBindingSetAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[<span data-ttu-id="9f1ba-147">**RpcBindingInqAuthInfoEx**</span><span class="sxs-lookup"><span data-stu-id="9f1ba-147">**RpcBindingInqAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> </dl>

 

 





