---
title: 'RPC_BINDING_HANDLE (Rpcdce) '
description: RPC 系結 \_ 控制碼資料類型會宣告一個系結控制碼，其中包含 RPC 執行時間程式庫用來存取系結資訊的資訊。
ms.assetid: 3e07d9e9-04d8-4f94-8104-cd0ee89a9407
keywords:
- RPC_BINDING_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e37d14bc5186f05815c10f538b0c90bdddd353
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686572"
---
# <a name="rpc_binding_handle"></a><span data-ttu-id="559c7-104">RPC 系結 \_ \_ 控制碼</span><span class="sxs-lookup"><span data-stu-id="559c7-104">RPC\_BINDING\_HANDLE</span></span>

<span data-ttu-id="559c7-105">Rpc 系結 **\_ 控制碼** 資料類型會宣告一個系結控制碼，其中包含 RPC 執行時間程式庫用來存取系結資訊的資訊。</span><span class="sxs-lookup"><span data-stu-id="559c7-105">The **RPC\_BINDING HANDLE** data type declares a binding handle containing information that the RPC run-time library uses to access binding information.</span></span>


```C++
typedef I_RPC_HANDLE RPC_BINDING_HANDLE;
```



## <a name="remarks"></a><span data-ttu-id="559c7-106">備註</span><span class="sxs-lookup"><span data-stu-id="559c7-106">Remarks</span></span>

<span data-ttu-id="559c7-107">執行時間程式庫會使用系結資訊來建立允許遠端程序呼叫執行的用戶端-伺服器關聯性。</span><span class="sxs-lookup"><span data-stu-id="559c7-107">The run-time library uses binding information to establish a client-server relationship that allows the execution of remote procedure calls.</span></span> <span data-ttu-id="559c7-108">根據建立系結控制碼的內容，它會被視為伺服器系結控制碼或用戶端系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="559c7-108">Based on the context in which a binding handle is created, it is considered a server-binding handle or a client-binding handle.</span></span>

<span data-ttu-id="559c7-109">伺服器系結控制碼包含用戶端建立與特定伺服器之關聯性所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="559c7-109">A server-binding handle contains the information necessary for a client to establish a relationship with a specific server.</span></span> <span data-ttu-id="559c7-110">任何數目的 RPC API 執行時間常式都會傳回伺服器系結控制碼，可用來進行遠端程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="559c7-110">Any number of RPC API run-time routines return a server-binding handle that can be used for making a remote procedure call.</span></span>

<span data-ttu-id="559c7-111">用戶端系結控制碼不能用來進行遠端程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="559c7-111">A client-binding handle cannot be used to make a remote procedure call.</span></span> <span data-ttu-id="559c7-112">RPC 執行時間程式庫會建立並提供用戶端系結控制碼給被呼叫的伺服器程式， (也稱為伺服器管理員常式) 做為 RPC 系結 \_ \_ 控制碼參數。</span><span class="sxs-lookup"><span data-stu-id="559c7-112">The RPC run-time library creates and provides a client-binding handle to a called-server procedure (also called a server-manager routine) as the RPC\_BINDING\_HANDLE parameter.</span></span> <span data-ttu-id="559c7-113">用戶端系結控制碼包含呼叫用戶端的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="559c7-113">The client-binding handle contains information about the calling client.</span></span>

<span data-ttu-id="559c7-114">*\** _*\**_ \_ \_ \_ \_ \_ 當應用程式提供錯誤的系結控制碼類型時，\* RpcBinding _ 和 RpcNsBinding 函式會傳回狀態碼 RPC S 錯誤的系結類型。</span><span class="sxs-lookup"><span data-stu-id="559c7-114">The **RpcBinding\** _ and _*RpcNsBinding\*\*_ functions return the status code RPC\_S\_WRONG\_KIND\_OF\_BINDING when an application provides the incorrect binding-handle type.</span></span>

<span data-ttu-id="559c7-115">應用程式可以跨多個執行執行緒共用單一系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="559c7-115">An application can share a single binding handle across multiple threads of execution.</span></span> <span data-ttu-id="559c7-116">RPC 執行時間程式庫會管理使用單一系結控制碼的並行遠端程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="559c7-116">The RPC run-time library manages concurrent remote procedure calls that use a single binding handle.</span></span> <span data-ttu-id="559c7-117">但是，應用程式負責系結控制碼並行控制，以進行修改系結控制碼的作業。</span><span class="sxs-lookup"><span data-stu-id="559c7-117">However, the application is responsible for binding handle concurrency control for operations that modify a binding handle.</span></span> <span data-ttu-id="559c7-118">這些作業包括下列常式：</span><span class="sxs-lookup"><span data-stu-id="559c7-118">These operations include the following routines:</span></span>

-   [<span data-ttu-id="559c7-119">_ *RpcBindingFree*\*</span><span class="sxs-lookup"><span data-stu-id="559c7-119">_ *RpcBindingFree*\*</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree)
-   [<span data-ttu-id="559c7-120">**RpcBindingReset**</span><span class="sxs-lookup"><span data-stu-id="559c7-120">**RpcBindingReset**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset)
-   [<span data-ttu-id="559c7-121">**RpcBindingSetAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="559c7-121">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
-   [<span data-ttu-id="559c7-122">**RpcBindingSetObject**</span><span class="sxs-lookup"><span data-stu-id="559c7-122">**RpcBindingSetObject**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)

<span data-ttu-id="559c7-123">例如，如果應用程式在兩個執行執行緒之間共用系結控制碼，並藉由呼叫 [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset)在其中一個執行緒中重設系結控制碼端點，則結果為未定義。</span><span class="sxs-lookup"><span data-stu-id="559c7-123">For example, if an application shares a binding handle across two threads of execution and resets the binding-handle endpoint in one of the threads by calling [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset), the results are undefined.</span></span> <span data-ttu-id="559c7-124">另一個執行緒上的系結控制碼也可以重設，或作業可能會失敗，或是進程可能會損毀。</span><span class="sxs-lookup"><span data-stu-id="559c7-124">The binding handle on the other thread may also be reset, or the operation may fail, or the process may crash.</span></span> <span data-ttu-id="559c7-125">常見的錯誤是在其進行呼叫時釋放系結控制碼;這通常會導致呼叫進程損毀。</span><span class="sxs-lookup"><span data-stu-id="559c7-125">A common error is freeing a binding handle while a call on it is in progress; this usually crashes the calling process.</span></span>

<span data-ttu-id="559c7-126">如果您不想要平行存取，您可以藉由呼叫 [**RpcBindingCopy**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy)來設計應用程式，以建立系結控制碼的複本。</span><span class="sxs-lookup"><span data-stu-id="559c7-126">If you do not want concurrency, you can design an application to create a copy of a binding handle by calling [**RpcBindingCopy**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy).</span></span> <span data-ttu-id="559c7-127">在這種情況下，第一個系結控制碼的作業對第二個系結控制碼沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="559c7-127">In this case, an operation to the first binding handle has no effect on the second binding handle.</span></span>

<span data-ttu-id="559c7-128">需要系結控制碼作為參數的常式會顯示 RPC 系 **結 \_ \_ 控制碼** 的資料類型。</span><span class="sxs-lookup"><span data-stu-id="559c7-128">Routines requiring a binding handle as a parameter show a data type of **RPC\_BINDING\_HANDLE**.</span></span> <span data-ttu-id="559c7-129">系結控制碼參數會以傳值方式傳遞。</span><span class="sxs-lookup"><span data-stu-id="559c7-129">Binding-handle parameters are passed by value.</span></span>

## <a name="requirements"></a><span data-ttu-id="559c7-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="559c7-130">Requirements</span></span>



| <span data-ttu-id="559c7-131">需求</span><span class="sxs-lookup"><span data-stu-id="559c7-131">Requirement</span></span> | <span data-ttu-id="559c7-132">值</span><span class="sxs-lookup"><span data-stu-id="559c7-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="559c7-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="559c7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="559c7-134">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="559c7-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="559c7-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="559c7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="559c7-136">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="559c7-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="559c7-137">標頭</span><span class="sxs-lookup"><span data-stu-id="559c7-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="559c7-138"><dt>Rpcdce (包含 Rpc) </dt></span><span class="sxs-lookup"><span data-stu-id="559c7-138"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



 

 





