---
title: 非同步撥號狀態
description: 此頁面描述 RPC 呼叫的非同步撥號狀態。
ms.assetid: 4a594dad-a8a1-44e9-8648-ddc2539c234c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96331a18b267b2e44072840727c8fd06afd11d6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840855"
---
# <a name="asynchronous-call-state"></a><span data-ttu-id="c9afd-103">非同步撥號狀態</span><span class="sxs-lookup"><span data-stu-id="c9afd-103">Asynchronous Call State</span></span>

<span data-ttu-id="c9afd-104">此頁面描述 RPC 呼叫的非同步撥號狀態。</span><span class="sxs-lookup"><span data-stu-id="c9afd-104">This page describes the Asynchronous Call State for RPC calls.</span></span>

## <a name="client-behavior"></a><span data-ttu-id="c9afd-105">用戶端行為</span><span class="sxs-lookup"><span data-stu-id="c9afd-105">Client Behavior</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c9afd-106">狀態</span><span class="sxs-lookup"><span data-stu-id="c9afd-106">State</span></span></th>
<th><span data-ttu-id="c9afd-107">狀態名稱</span><span class="sxs-lookup"><span data-stu-id="c9afd-107">State name</span></span></th>
<th><span data-ttu-id="c9afd-108">動作</span><span class="sxs-lookup"><span data-stu-id="c9afd-108">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c9afd-109">C</span><span class="sxs-lookup"><span data-stu-id="c9afd-109">C</span></span></td>
<td><span data-ttu-id="c9afd-110">進行呼叫</span><span class="sxs-lookup"><span data-stu-id="c9afd-110">Make the call</span></span></td>
<td><span data-ttu-id="c9afd-111">讓 RPC</span><span class="sxs-lookup"><span data-stu-id="c9afd-111">Make the RPC</span></span>
<ul>
<li><span data-ttu-id="c9afd-112">成功時移至狀態 WComp</span><span class="sxs-lookup"><span data-stu-id="c9afd-112">On success go to state WComp</span></span></li>
<li><span data-ttu-id="c9afd-113">發生例外狀況時移至結尾</span><span class="sxs-lookup"><span data-stu-id="c9afd-113">On exception go to End</span></span></li>
</ul>
<span data-ttu-id="c9afd-114">失敗：前往 [可以]</span><span class="sxs-lookup"><span data-stu-id="c9afd-114">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9afd-115">可以</span><span class="sxs-lookup"><span data-stu-id="c9afd-115">Can</span></span></td>
<td><span data-ttu-id="c9afd-116">取消呼叫</span><span class="sxs-lookup"><span data-stu-id="c9afd-116">Cancel the call</span></span></td>
<td><span data-ttu-id="c9afd-117">呼叫 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>前往 WComp</span><span class="sxs-lookup"><span data-stu-id="c9afd-117">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go to WComp</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9afd-118">WComp</span><span class="sxs-lookup"><span data-stu-id="c9afd-118">WComp</span></span></td>
<td><span data-ttu-id="c9afd-119">等候完成</span><span class="sxs-lookup"><span data-stu-id="c9afd-119">Wait for completion</span></span></td>
<td><span data-ttu-id="c9afd-120">等候 notificationCall-應會收到完整通知</span><span class="sxs-lookup"><span data-stu-id="c9afd-120">Wait for notificationCall-complete notification should be received</span></span><br/> <span data-ttu-id="c9afd-121">移至 [複合]</span><span class="sxs-lookup"><span data-stu-id="c9afd-121">Go to Comp</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9afd-122">Comp</span><span class="sxs-lookup"><span data-stu-id="c9afd-122">Comp</span></span></td>
<td><span data-ttu-id="c9afd-123">Completion</span><span class="sxs-lookup"><span data-stu-id="c9afd-123">Completion</span></span></td>
<td><span data-ttu-id="c9afd-124">問題 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>移至結尾</span><span class="sxs-lookup"><span data-stu-id="c9afd-124">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9afd-125">結束</span><span class="sxs-lookup"><span data-stu-id="c9afd-125">End</span></span></td>


</tr>
</tbody>
</table>



 

## <a name="server-behavior"></a><span data-ttu-id="c9afd-126">伺服器行為</span><span class="sxs-lookup"><span data-stu-id="c9afd-126">Server Behavior</span></span>



| <span data-ttu-id="c9afd-127">狀態</span><span class="sxs-lookup"><span data-stu-id="c9afd-127">State</span></span> | <span data-ttu-id="c9afd-128">狀態名稱</span><span class="sxs-lookup"><span data-stu-id="c9afd-128">State name</span></span>     | <span data-ttu-id="c9afd-129">動作</span><span class="sxs-lookup"><span data-stu-id="c9afd-129">Action</span></span>                                                                                                                                                                                                              |
|-------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9afd-130">D</span><span class="sxs-lookup"><span data-stu-id="c9afd-130">D</span></span>     | <span data-ttu-id="c9afd-131">分派</span><span class="sxs-lookup"><span data-stu-id="c9afd-131">Dispatch</span></span>       | <span data-ttu-id="c9afd-132">呼叫是由 RPC runtimeProcess 分派</span><span class="sxs-lookup"><span data-stu-id="c9afd-132">The call is dispatched by the RPC runtimeProcess</span></span><br/> <span data-ttu-id="c9afd-133">移至 [複合]</span><span class="sxs-lookup"><span data-stu-id="c9afd-133">Go to Comp</span></span><br/> <span data-ttu-id="c9afd-134">若要在 RPC 執行緒上執行時失敗嚴重 () ：引發例外狀況;移至結尾</span><span class="sxs-lookup"><span data-stu-id="c9afd-134">To fail fatally (while executing on the RPC thread): Raise exception; go to End</span></span><br/> <span data-ttu-id="c9afd-135">若要正常地失敗：請移至</span><span class="sxs-lookup"><span data-stu-id="c9afd-135">To fail gracefully: go to A</span></span><br/> |
| <span data-ttu-id="c9afd-136">A</span><span class="sxs-lookup"><span data-stu-id="c9afd-136">A</span></span>     | <span data-ttu-id="c9afd-137">中止呼叫</span><span class="sxs-lookup"><span data-stu-id="c9afd-137">Abort the call</span></span> | <span data-ttu-id="c9afd-138">呼叫 [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)Go to End</span><span class="sxs-lookup"><span data-stu-id="c9afd-138">Call [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)Go to End</span></span><br/>                                                                                                                                             |
| <span data-ttu-id="c9afd-139">Comp</span><span class="sxs-lookup"><span data-stu-id="c9afd-139">Comp</span></span>  | <span data-ttu-id="c9afd-140">Completion</span><span class="sxs-lookup"><span data-stu-id="c9afd-140">Completion</span></span>     | <span data-ttu-id="c9afd-141">問題 [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)移至結尾</span><span class="sxs-lookup"><span data-stu-id="c9afd-141">Issue [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)Go to End</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="c9afd-142">結束</span><span class="sxs-lookup"><span data-stu-id="c9afd-142">End</span></span>   |                |                                                                                                                                                                                                                     |



 

 

 





