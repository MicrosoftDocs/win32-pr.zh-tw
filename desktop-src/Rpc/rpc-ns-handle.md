---
title: 'RPC_NS_HANDLE (Rpcnsi) '
description: RPC \_ NS \_ 控制碼資料類型定義了名稱服務控制碼。
ms.assetid: d9c2a376-4972-4f16-aa8d-f0e43d5ddb8d
keywords:
- RPC_NS_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e72ee694e08be1b30a75dc1f5b986619043d592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509203"
---
# <a name="rpc_ns_handle"></a><span data-ttu-id="d796d-104">RPC \_ NS \_ 控制碼</span><span class="sxs-lookup"><span data-stu-id="d796d-104">RPC\_NS\_HANDLE</span></span>

<span data-ttu-id="d796d-105">**RPC \_ NS \_ 控制碼** 資料類型定義了名稱服務控制碼。</span><span class="sxs-lookup"><span data-stu-id="d796d-105">The data type **RPC\_NS\_HANDLE** defines a name-service handle.</span></span>


```C++
typedef void* RPC_NS_HANDLE;
```



## <a name="remarks"></a><span data-ttu-id="d796d-106">備註</span><span class="sxs-lookup"><span data-stu-id="d796d-106">Remarks</span></span>

<span data-ttu-id="d796d-107">名稱服務控制碼是一個不透明的變數，其中包含 RPC 執行時間程式庫用來從名稱-服務資料庫傳回下列 RPC 資料的資訊：</span><span class="sxs-lookup"><span data-stu-id="d796d-107">A name-service handle is an opaque variable containing information the RPC run-time library uses to return the following RPC data from the name-service database:</span></span>

-   <span data-ttu-id="d796d-108">伺服器系結控制碼</span><span class="sxs-lookup"><span data-stu-id="d796d-108">Server-binding handles</span></span>
-   <span data-ttu-id="d796d-109">伺服器設定檔成員所提供資源的 Uuid</span><span class="sxs-lookup"><span data-stu-id="d796d-109">UUIDs of resources offered by server profile members</span></span>
-   <span data-ttu-id="d796d-110">群組成員</span><span class="sxs-lookup"><span data-stu-id="d796d-110">Group members</span></span>

<span data-ttu-id="d796d-111">名稱服務控制碼的範圍是從「開始」常式到對應的「完成」常式。</span><span class="sxs-lookup"><span data-stu-id="d796d-111">The scope of a name-service handle is from a "Begin" routine through the corresponding "Done" routine.</span></span>

<span data-ttu-id="d796d-112">應用程式會負責並行控制跨執行緒的名稱服務控制碼。</span><span class="sxs-lookup"><span data-stu-id="d796d-112">Applications are responsible for concurrency control of name-service handles across threads.</span></span>

## <a name="requirements"></a><span data-ttu-id="d796d-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="d796d-113">Requirements</span></span>



| <span data-ttu-id="d796d-114">需求</span><span class="sxs-lookup"><span data-stu-id="d796d-114">Requirement</span></span> | <span data-ttu-id="d796d-115">值</span><span class="sxs-lookup"><span data-stu-id="d796d-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d796d-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d796d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d796d-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d796d-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d796d-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d796d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d796d-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d796d-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d796d-120">標頭</span><span class="sxs-lookup"><span data-stu-id="d796d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d796d-121"><dt>Rpcnsi (包含 Rpc) </dt></span><span class="sxs-lookup"><span data-stu-id="d796d-121"><dt>Rpcnsi.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d796d-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d796d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d796d-123">**RpcNsBindingImportBegin**</span><span class="sxs-lookup"><span data-stu-id="d796d-123">**RpcNsBindingImportBegin**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)
</dt> <dt>

[<span data-ttu-id="d796d-124">**RpcNsBindingImportDone**</span><span class="sxs-lookup"><span data-stu-id="d796d-124">**RpcNsBindingImportDone**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone)
</dt> <dt>

[<span data-ttu-id="d796d-125">**RpcNsBindingImportNext**</span><span class="sxs-lookup"><span data-stu-id="d796d-125">**RpcNsBindingImportNext**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)
</dt> <dt>

[<span data-ttu-id="d796d-126">**RpcNsBindingLookupBegin**</span><span class="sxs-lookup"><span data-stu-id="d796d-126">**RpcNsBindingLookupBegin**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina)
</dt> <dt>

[<span data-ttu-id="d796d-127">**RpcNsBindingLookupDone**</span><span class="sxs-lookup"><span data-stu-id="d796d-127">**RpcNsBindingLookupDone**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupdone)
</dt> <dt>

[<span data-ttu-id="d796d-128">**RpcNsBindingLookupNext**</span><span class="sxs-lookup"><span data-stu-id="d796d-128">**RpcNsBindingLookupNext**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)
</dt> </dl>

 

 





