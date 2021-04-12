---
title: 'RPC_EP_INQ_HANDLE (Rpcasync) '
description: RPC \_ EP \_ INQ \_ 控制碼資料類型會宣告查詢內容的控制碼。 RPC 應用程式會使用它來查看端點對應中儲存的伺服器位址資訊。
ms.assetid: e18ce800-0110-4450-9a1b-a3f777d00f2d
keywords:
- RPC_EP_INQ_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c34c64b5601b31485808924fc57dbe3412b6009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385134"
---
# <a name="rpc_ep_inq_handle"></a><span data-ttu-id="bff5c-105">RPC \_ EP \_ INQ \_ 控制碼</span><span class="sxs-lookup"><span data-stu-id="bff5c-105">RPC\_EP\_INQ\_HANDLE</span></span>

<span data-ttu-id="bff5c-106">**RPC \_ EP \_ INQ \_ 控制碼** 資料類型會宣告查詢內容的控制碼。</span><span class="sxs-lookup"><span data-stu-id="bff5c-106">The **RPC\_EP\_INQ\_HANDLE** data type declares a handle for an inquiry context.</span></span> <span data-ttu-id="bff5c-107">RPC 應用程式會使用它來查看端點對應中儲存的伺服器位址資訊。</span><span class="sxs-lookup"><span data-stu-id="bff5c-107">RPC applications use it to view server address information stored in the endpoint map.</span></span>


```C++
typedef I_RPC_HANDLE* RPC_EP_INQ_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="bff5c-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="bff5c-108">Requirements</span></span>



| <span data-ttu-id="bff5c-109">需求</span><span class="sxs-lookup"><span data-stu-id="bff5c-109">Requirement</span></span> | <span data-ttu-id="bff5c-110">值</span><span class="sxs-lookup"><span data-stu-id="bff5c-110">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bff5c-111">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bff5c-111">Minimum supported client</span></span><br/> | <span data-ttu-id="bff5c-112">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bff5c-112">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="bff5c-113">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bff5c-113">Minimum supported server</span></span><br/> | <span data-ttu-id="bff5c-114">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bff5c-114">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="bff5c-115">標頭</span><span class="sxs-lookup"><span data-stu-id="bff5c-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="bff5c-116"><dt>Rpcasync (包含 Rpc) </dt></span><span class="sxs-lookup"><span data-stu-id="bff5c-116"><dt>Rpcasync.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bff5c-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bff5c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bff5c-118">**RpcMgmtEpEltInqBegin**</span><span class="sxs-lookup"><span data-stu-id="bff5c-118">**RpcMgmtEpEltInqBegin**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin)
</dt> <dt>

[<span data-ttu-id="bff5c-119">**RpcMgmtEpEltInqNext**</span><span class="sxs-lookup"><span data-stu-id="bff5c-119">**RpcMgmtEpEltInqNext**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqnext)
</dt> <dt>

[<span data-ttu-id="bff5c-120">**RpcMgmtEpEltInqDone**</span><span class="sxs-lookup"><span data-stu-id="bff5c-120">**RpcMgmtEpEltInqDone**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqdone)
</dt> </dl>

 

 





