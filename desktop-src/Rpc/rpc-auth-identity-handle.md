---
title: 'RPC_AUTH_IDENTITY_HANDLE (Rpcdce) '
description: 「RPC \_ 驗證身分 \_ 識別 \_ 控制碼」資料類型會宣告指向結構的控制碼，該結構包含為遠端程序呼叫指定的用戶端驗證和授權認證。
ms.assetid: 06e45348-a392-45be-9f8a-e77ef887f26c
keywords:
- RPC_AUTH_IDENTITY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86559e7852172d34898d48f13bb2975ed792d85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106386"
---
# <a name="rpc_auth_identity_handle"></a><span data-ttu-id="4b649-104">RPC \_ 驗證身分 \_ 識別 \_ 控制碼</span><span class="sxs-lookup"><span data-stu-id="4b649-104">RPC\_AUTH\_IDENTITY\_HANDLE</span></span>

<span data-ttu-id="4b649-105">「 **RPC \_ 驗證身分 \_ 識別 \_ 控制碼** 」資料類型會宣告指向結構的控制碼，該結構包含為遠端程序呼叫指定的用戶端驗證和授權認證。</span><span class="sxs-lookup"><span data-stu-id="4b649-105">The **RPC\_AUTH\_IDENTITY\_HANDLE** data type declares a handle that points to a structure containing the client's authentication and authorization credentials specified for remote procedure calls.</span></span>


```C++
typedef void* RPC_AUTH_IDENTITY_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="4b649-106">規格需求</span><span class="sxs-lookup"><span data-stu-id="4b649-106">Requirements</span></span>



| <span data-ttu-id="4b649-107">需求</span><span class="sxs-lookup"><span data-stu-id="4b649-107">Requirement</span></span> | <span data-ttu-id="4b649-108">值</span><span class="sxs-lookup"><span data-stu-id="4b649-108">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b649-109">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4b649-109">Minimum supported client</span></span><br/> | <span data-ttu-id="4b649-110">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4b649-110">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4b649-111">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4b649-111">Minimum supported server</span></span><br/> | <span data-ttu-id="4b649-112">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4b649-112">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4b649-113">標頭</span><span class="sxs-lookup"><span data-stu-id="4b649-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b649-114"><dt>Rpcdce (包含 Rpc) </dt></span><span class="sxs-lookup"><span data-stu-id="4b649-114"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b649-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4b649-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b649-116">**RpcBindingInqAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="4b649-116">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[<span data-ttu-id="4b649-117">**RpcBindingSetAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="4b649-117">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> </dl>

 

 





