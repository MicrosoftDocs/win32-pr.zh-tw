---
title: 'RPC_AUTHZ_HANDLE (Rpcdce) '
description: RPC \_ AUTHZ \_ 控制碼資料類型宣告了授權控制碼。 這個控制碼會指向進行遠端程序呼叫之用戶端應用程式的許可權資訊。
ms.assetid: 35b6a3f4-1703-4244-98fd-fad7de48b262
keywords:
- RPC_AUTHZ_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b095100e1e224590ef6a285785da632e198e1b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106385"
---
# <a name="rpc_authz_handle"></a><span data-ttu-id="e2919-105">RPC \_ 授權 \_ 控制碼</span><span class="sxs-lookup"><span data-stu-id="e2919-105">RPC\_AUTHZ\_HANDLE</span></span>

<span data-ttu-id="e2919-106">**RPC \_ AUTHZ \_ 控制碼** 資料類型宣告了授權控制碼。</span><span class="sxs-lookup"><span data-stu-id="e2919-106">The **RPC\_AUTHZ\_HANDLE** data type declares an authorization handle.</span></span> <span data-ttu-id="e2919-107">這個控制碼會指向進行遠端程序呼叫之用戶端應用程式的許可權資訊。</span><span class="sxs-lookup"><span data-stu-id="e2919-107">This handle points to the privileges information for the client application that made the remote procedure call.</span></span>


```C++
typedef void* RPC_AUTHZ_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="e2919-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2919-108">Requirements</span></span>



| <span data-ttu-id="e2919-109">需求</span><span class="sxs-lookup"><span data-stu-id="e2919-109">Requirement</span></span> | <span data-ttu-id="e2919-110">值</span><span class="sxs-lookup"><span data-stu-id="e2919-110">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2919-111">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e2919-111">Minimum supported client</span></span><br/> | <span data-ttu-id="e2919-112">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2919-112">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e2919-113">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e2919-113">Minimum supported server</span></span><br/> | <span data-ttu-id="e2919-114">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2919-114">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e2919-115">標頭</span><span class="sxs-lookup"><span data-stu-id="e2919-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2919-116"><dt>Rpcdce (包含 Rpc) </dt></span><span class="sxs-lookup"><span data-stu-id="e2919-116"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2919-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2919-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2919-118">**RpcBindingInqAuthClient**</span><span class="sxs-lookup"><span data-stu-id="e2919-118">**RpcBindingInqAuthClient**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> </dl>

 

 





