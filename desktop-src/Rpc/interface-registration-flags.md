---
title: '介面註冊旗標 (Rpcdce .h) '
description: RpcServerRegisterIf2 和 RpcServerRegisterIfEx 函數的 Flags 參數中會使用下列常數。
ms.assetid: 387311c0-13df-4497-a0ac-ce6aec0e726c
topic_type:
- apiref
api_name:
- RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH
- RPC_IF_ALLOW_LOCAL_ONLY
- RPC_IF_AUTOLISTEN
- RPC_IF_OLE
- RPC_IF_ALLOW_UNKNOWN_AUTHORITY
- RPC_IF_ALLOW_SECURE_ONLY
- RPC_IF_SEC_NO_CACHE
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af938038d2bc7000d80268fb4cb00941f6b282b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105701"
---
# <a name="interface-registration-flags"></a><span data-ttu-id="b0a54-103">介面註冊旗標</span><span class="sxs-lookup"><span data-stu-id="b0a54-103">Interface Registration Flags</span></span>

<span data-ttu-id="b0a54-104">[**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)和 [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)函數的 *Flags* 參數中會使用下列常數。</span><span class="sxs-lookup"><span data-stu-id="b0a54-104">The following constants are used in the *Flags* parameter of the [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) and [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) functions.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="b0a54-105">常數</span><span class="sxs-lookup"><span data-stu-id="b0a54-105">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="b0a54-106">描述</span><span class="sxs-lookup"><span data-stu-id="b0a54-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="0"></span><dl> <span data-ttu-id="b0a54-107"><dt><strong>0</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b0a54-107"><dt><strong>0</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b0a54-108">標準介面語義。</span><span class="sxs-lookup"><span data-stu-id="b0a54-108">Standard interface semantics.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH"></span><span id="rpc_if_allow_callbacks_with_no_auth"></span><dl> <span data-ttu-id="b0a54-109"><dt><strong>RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b0a54-109"><dt><strong>RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b0a54-110">註冊這個介面旗標時，RPC 執行時間會叫用所有呼叫的已註冊安全性回呼，而不論身分識別、通訊協定順序或用戶端的驗證層級為何。</span><span class="sxs-lookup"><span data-stu-id="b0a54-110">When this interface flag is registered, the RPC runtime invokes the registered security callback for all calls, regardless of identity, protocol sequence, or authentication level of the client.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b0a54-111">從 Windows XP SP2 和 Windows Server 2003 SP1 開始提供此旗標。</span><span class="sxs-lookup"><span data-stu-id="b0a54-111">This flag is available starting with Windows XP with SP2 and Windows Server 2003 with SP1.</span></span> <span data-ttu-id="b0a54-112">如果未設定此旗標，RPC 會在所有未經驗證的呼叫到達安全性回呼之前自動進行篩選。</span><span class="sxs-lookup"><span data-stu-id="b0a54-112">When this flag is not set, RPC automatically filters all unauthenticated calls before they reach the security callback.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_LOCAL_ONLY"></span><span id="rpc_if_allow_local_only"></span><dl> <span data-ttu-id="b0a54-113"><dt><strong>RPC_IF_ALLOW_LOCAL_ONLY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b0a54-113"><dt><strong>RPC_IF_ALLOW_LOCAL_ONLY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b0a54-114">註冊這個介面旗標時，RPC 執行時間會拒絕遠端用戶端所發出的呼叫。</span><span class="sxs-lookup"><span data-stu-id="b0a54-114">When this interface flag is registered, the RPC runtime rejects calls made by remote clients.</span></span> <span data-ttu-id="b0a54-115">使用 ncadg_ \* 和 ncacn_ \* 通訊協定序列的所有本機呼叫也會被拒絕，但 ncacn_np 除外。</span><span class="sxs-lookup"><span data-stu-id="b0a54-115">All local calls using ncadg_\* and ncacn_\* protocol sequences are also rejected, with the exception of ncacn_np.</span></span> <span data-ttu-id="b0a54-116">RPC 只在呼叫不是來自 SRV 時，才允許 ncacn_NP 呼叫。</span><span class="sxs-lookup"><span data-stu-id="b0a54-116">RPC allows ncacn_NP calls only if the call does not come from SRV.</span></span> <span data-ttu-id="b0a54-117">一律會處理來自 ncalrpc 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="b0a54-117">Calls from ncalrpc are always processed.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b0a54-118">從 Windows XP SP2 和 Windows Server 2003 SP1 開始提供此旗標。</span><span class="sxs-lookup"><span data-stu-id="b0a54-118">This flag is available starting with Windows XP with SP2 and Windows Server 2003 with SP1.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_AUTOLISTEN"></span><span id="rpc_if_autolisten"></span><dl> <span data-ttu-id="b0a54-119"><dt><strong>RPC_IF_AUTOLISTEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b0a54-119"><dt><strong>RPC_IF_AUTOLISTEN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b0a54-120">這是 <strong>自動接聽</strong> 介面。</span><span class="sxs-lookup"><span data-stu-id="b0a54-120">This is an <strong>auto-listen</strong> interface.</span></span> <span data-ttu-id="b0a54-121">當第一個 autolisten 介面註冊之後，執行時間就會開始接聽呼叫，並在上一次 autolisten 介面未註冊時停止接聽。</span><span class="sxs-lookup"><span data-stu-id="b0a54-121">The run time begins listening for calls as soon as the first autolisten interface is registered, and stops listening when the last autolisten interface is unregistered.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_OLE"></span><span id="rpc_if_ole"></span><dl> <span data-ttu-id="b0a54-122"><dt><strong>RPC_IF_OLE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b0a54-122"><dt><strong>RPC_IF_OLE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b0a54-123">保留給 OLE。</span><span class="sxs-lookup"><span data-stu-id="b0a54-123">Reserved for OLE.</span></span> <span data-ttu-id="b0a54-124">請勿使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="b0a54-124">Do not use this flag.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_UNKNOWN_AUTHORITY"></span><span id="rpc_if_allow_unknown_authority"></span><dl> <span data-ttu-id="b0a54-125"><dt><strong>RPC_IF_ALLOW_UNKNOWN_AUTHORITY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b0a54-125"><dt><strong>RPC_IF_ALLOW_UNKNOWN_AUTHORITY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b0a54-126">目前尚未實作。</span><span class="sxs-lookup"><span data-stu-id="b0a54-126">Currently not implemented.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_SECURE_ONLY"></span><span id="rpc_if_allow_secure_only"></span><dl> <span data-ttu-id="b0a54-127"><dt><strong>RPC_IF_ALLOW_SECURE_ONLY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b0a54-127"><dt><strong>RPC_IF_ALLOW_SECURE_ONLY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b0a54-128">限制使用高於 RPC_C_AUTHN_LEVEL_NONE 的授權等級之用戶端的連接。</span><span class="sxs-lookup"><span data-stu-id="b0a54-128">Limits connections to clients that use an authorization level higher than RPC_C_AUTHN_LEVEL_NONE.</span></span> <span data-ttu-id="b0a54-129">指定這個旗標可讓用戶端在 <strong>Null</strong> 會話上進行。</span><span class="sxs-lookup"><span data-stu-id="b0a54-129">Specifying this flag allows clients to come through on the <strong>NULL</strong> session.</span></span> <span data-ttu-id="b0a54-130">在 Windows XP 與 Windows Server 2003 上，不允許這類用戶端。</span><span class="sxs-lookup"><span data-stu-id="b0a54-130">On Windows XP and Windows Server 2003, such clients are not allowed.</span></span> <span data-ttu-id="b0a54-131">RPC_IF_ALLOW_SECURE_ONLY 測試失敗的用戶端會收到 RPC_S_ACCESS_DENIED 錯誤。</span><span class="sxs-lookup"><span data-stu-id="b0a54-131">Clients that fail the RPC_IF_ALLOW_SECURE_ONLY test receive an RPC_S_ACCESS_DENIED error.</span></span> <span data-ttu-id="b0a54-132">使用 RPC_IF_ALLOW_SECURE_ONLY 旗標並不代表或保證呼叫使用者的部分具有高階許可權。</span><span class="sxs-lookup"><span data-stu-id="b0a54-132">Using the RPC_IF_ALLOW_SECURE_ONLY flag does not imply or guarantee a high level of privilege on the part of the calling user.</span></span> <span data-ttu-id="b0a54-133">RPC 只會檢查使用者是否擁有有效的認證;呼叫的使用者可能使用 guest 帳戶或其他低許可權帳戶。</span><span class="sxs-lookup"><span data-stu-id="b0a54-133">RPC only checks that the user has valid credentials; the calling user may be using the guest account or other low privileged accounts.</span></span> <span data-ttu-id="b0a54-134">使用 RPC_IF_ALLOW_SECURE_ONLY 時，請勿採用高許可權。</span><span class="sxs-lookup"><span data-stu-id="b0a54-134">Do not assume high privilege when RPC_IF_ALLOW_SECURE_ONLY is used.</span></span><br/> <span data-ttu-id="b0a54-135"><strong>Windows NT 4.0 和 Windows Me/98/95：  </strong></span><span class="sxs-lookup"><span data-stu-id="b0a54-135"><strong>Windows NT 4.0 and Windows Me/98/95:  </strong></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_SEC_NO_CACHE"></span><span id="rpc_if_sec_no_cache"></span><dl> <span data-ttu-id="b0a54-136"><dt><strong>RPC_IF_SEC_NO_CACHE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b0a54-136"><dt><strong>RPC_IF_SEC_NO_CACHE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b0a54-137">停用安全性回呼快取，針對指定介面上的每個 RPC 呼叫強制執行安全性回呼。</span><span class="sxs-lookup"><span data-stu-id="b0a54-137">Disables security callback caching, forcing a security callback for each RPC call on a given interface.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b0a54-138">從 Windows XP SP2 和 Windows Server 2003 SP1 開始提供此旗標。</span><span class="sxs-lookup"><span data-stu-id="b0a54-138">This flag is available starting with Windows XP with SP2 and Windows Server 2003 with SP1.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="b0a54-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0a54-139">Requirements</span></span>



| <span data-ttu-id="b0a54-140">需求</span><span class="sxs-lookup"><span data-stu-id="b0a54-140">Requirement</span></span> | <span data-ttu-id="b0a54-141">值</span><span class="sxs-lookup"><span data-stu-id="b0a54-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b0a54-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b0a54-142">Minimum supported client</span></span><br/> | <span data-ttu-id="b0a54-143">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0a54-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b0a54-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b0a54-144">Minimum supported server</span></span><br/> | <span data-ttu-id="b0a54-145">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0a54-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b0a54-146">標頭</span><span class="sxs-lookup"><span data-stu-id="b0a54-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0a54-147"><dt>Rpcdce。h</dt></span><span class="sxs-lookup"><span data-stu-id="b0a54-147"><dt>Rpcdce.h</dt></span></span> </dl> |



 

 





