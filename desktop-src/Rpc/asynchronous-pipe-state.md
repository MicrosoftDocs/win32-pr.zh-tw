---
title: 非同步管道狀態
description: 此頁面描述 RPC 呼叫的非同步管道狀態。
ms.assetid: af937eba-6b70-447a-af76-a8e27f5754e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8396b08c7ef7b8152457d9426883645fab39bdef
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023051"
---
# <a name="asynchronous-pipe-state"></a><span data-ttu-id="425ba-103">非同步管道狀態</span><span class="sxs-lookup"><span data-stu-id="425ba-103">Asynchronous Pipe State</span></span>

<span data-ttu-id="425ba-104">此頁面描述 RPC 呼叫的非同步管道狀態。</span><span class="sxs-lookup"><span data-stu-id="425ba-104">This page describes the Asynchronous Pipe State for RPC calls.</span></span>

## <a name="in-pipe"></a><span data-ttu-id="425ba-105">在管線中</span><span class="sxs-lookup"><span data-stu-id="425ba-105">IN Pipe</span></span>

<span data-ttu-id="425ba-106">用戶端行為</span><span class="sxs-lookup"><span data-stu-id="425ba-106">Client Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="425ba-107">狀態</span><span class="sxs-lookup"><span data-stu-id="425ba-107">State</span></span></th>
<th><span data-ttu-id="425ba-108">狀態名稱</span><span class="sxs-lookup"><span data-stu-id="425ba-108">State Name</span></span></th>
<th><span data-ttu-id="425ba-109">動作</span><span class="sxs-lookup"><span data-stu-id="425ba-109">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="425ba-110">C</span><span class="sxs-lookup"><span data-stu-id="425ba-110">C</span></span></td>
<td><span data-ttu-id="425ba-111">進行呼叫</span><span class="sxs-lookup"><span data-stu-id="425ba-111">Make the call</span></span></td>
<td><span data-ttu-id="425ba-112">讓 RPC</span><span class="sxs-lookup"><span data-stu-id="425ba-112">Make the RPC</span></span>
<ul>
<li><span data-ttu-id="425ba-113">成功時移至狀態 WS</span><span class="sxs-lookup"><span data-stu-id="425ba-113">On success go to state WS</span></span></li>
<li><span data-ttu-id="425ba-114">發生例外狀況時移至結尾</span><span class="sxs-lookup"><span data-stu-id="425ba-114">On exception go to End</span></span></li>
</ul>
<span data-ttu-id="425ba-115">失敗：前往 [可以]</span><span class="sxs-lookup"><span data-stu-id="425ba-115">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="425ba-116">P</span><span class="sxs-lookup"><span data-stu-id="425ba-116">P</span></span></td>
<td><span data-ttu-id="425ba-117">發送</span><span class="sxs-lookup"><span data-stu-id="425ba-117">Push</span></span></td>
<td><span data-ttu-id="425ba-118">進行推送</span><span class="sxs-lookup"><span data-stu-id="425ba-118">Make a push</span></span>
<ul>
<li><span data-ttu-id="425ba-119">失敗時移至結尾</span><span class="sxs-lookup"><span data-stu-id="425ba-119">On failure go to End</span></span></li>
<li><span data-ttu-id="425ba-120">成功時移至 WS</span><span class="sxs-lookup"><span data-stu-id="425ba-120">On success go to WS</span></span></li>
</ul>
<span data-ttu-id="425ba-121">失敗：前往 [可以]</span><span class="sxs-lookup"><span data-stu-id="425ba-121">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="425ba-122">WS</span><span class="sxs-lookup"><span data-stu-id="425ba-122">WS</span></span></td>
<td><span data-ttu-id="425ba-123">等候傳送</span><span class="sxs-lookup"><span data-stu-id="425ba-123">Wait for Send</span></span></td>
<td><span data-ttu-id="425ba-124">等候通知</span><span class="sxs-lookup"><span data-stu-id="425ba-124">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="425ba-125">若無法取得通知，請前往</span><span class="sxs-lookup"><span data-stu-id="425ba-125">On failure to get a notification go to Can</span></span></li>
<li><span data-ttu-id="425ba-126">如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> ，且需要傳送更多資料，請移至 P</span><span class="sxs-lookup"><span data-stu-id="425ba-126">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data needs to be sent go to P</span></span></li>
<li><span data-ttu-id="425ba-127">如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> ，且不需要傳送更多資料，請移至 NP</span><span class="sxs-lookup"><span data-stu-id="425ba-127">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data does not need to be sent go to NP</span></span></li>
<li><span data-ttu-id="425ba-128">如果接收到失敗 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> ，請使用 go Comp</span><span class="sxs-lookup"><span data-stu-id="425ba-128">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> is received go Comp</span></span></li>
</ul>
<span data-ttu-id="425ba-129">失敗：前往 [可以]</span><span class="sxs-lookup"><span data-stu-id="425ba-129">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="425ba-130">NP</span><span class="sxs-lookup"><span data-stu-id="425ba-130">NP</span></span></td>
<td><span data-ttu-id="425ba-131">Null 推送</span><span class="sxs-lookup"><span data-stu-id="425ba-131">Null Push</span></span></td>
<td><span data-ttu-id="425ba-132">將0個位元組推 (null 推送) </span><span class="sxs-lookup"><span data-stu-id="425ba-132">Push 0 bytes (null push)</span></span>
<ul>
<li><span data-ttu-id="425ba-133">失敗時移至結尾</span><span class="sxs-lookup"><span data-stu-id="425ba-133">On failure go to End</span></span></li>
<li><span data-ttu-id="425ba-134">成功移至 WComp</span><span class="sxs-lookup"><span data-stu-id="425ba-134">On success go to WComp</span></span></li>
</ul>
<span data-ttu-id="425ba-135">失敗：前往 [可以]</span><span class="sxs-lookup"><span data-stu-id="425ba-135">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="425ba-136">可以</span><span class="sxs-lookup"><span data-stu-id="425ba-136">Can</span></span></td>
<td><span data-ttu-id="425ba-137">取消呼叫</span><span class="sxs-lookup"><span data-stu-id="425ba-137">Cancel the Call</span></span></td>
<td><span data-ttu-id="425ba-138">呼叫 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>前往 WComp</span><span class="sxs-lookup"><span data-stu-id="425ba-138">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go to WComp</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="425ba-139">WComp</span><span class="sxs-lookup"><span data-stu-id="425ba-139">WComp</span></span></td>
<td><span data-ttu-id="425ba-140">等候完成</span><span class="sxs-lookup"><span data-stu-id="425ba-140">Wait for Completion</span></span></td>
<td><span data-ttu-id="425ba-141">應會收到 notificationCall 的等候通知。</span><span class="sxs-lookup"><span data-stu-id="425ba-141">Wait for notificationCall-complete notification should be received.</span></span><br/> <span data-ttu-id="425ba-142">移至 [複合]</span><span class="sxs-lookup"><span data-stu-id="425ba-142">Go to Comp</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="425ba-143">Comp</span><span class="sxs-lookup"><span data-stu-id="425ba-143">Comp</span></span></td>
<td><span data-ttu-id="425ba-144">Completion</span><span class="sxs-lookup"><span data-stu-id="425ba-144">Completion</span></span></td>
<td><span data-ttu-id="425ba-145">問題 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>移至結尾</span><span class="sxs-lookup"><span data-stu-id="425ba-145">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="425ba-146">結束</span><span class="sxs-lookup"><span data-stu-id="425ba-146">End</span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="425ba-147">伺服器行為</span><span class="sxs-lookup"><span data-stu-id="425ba-147">Server Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="425ba-148">狀態</span><span class="sxs-lookup"><span data-stu-id="425ba-148">State</span></span></th>
<th><span data-ttu-id="425ba-149">狀態名稱</span><span class="sxs-lookup"><span data-stu-id="425ba-149">State Name</span></span></th>
<th><span data-ttu-id="425ba-150">動作</span><span class="sxs-lookup"><span data-stu-id="425ba-150">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="425ba-151">D</span><span class="sxs-lookup"><span data-stu-id="425ba-151">D</span></span></td>
<td><span data-ttu-id="425ba-152">分派</span><span class="sxs-lookup"><span data-stu-id="425ba-152">Dispatch</span></span></td>
<td><span data-ttu-id="425ba-153">RPC 執行時間會將呼叫分派至 P</span><span class="sxs-lookup"><span data-stu-id="425ba-153">The call is dispatched by the RPC runtime Go to P</span></span><br/> <span data-ttu-id="425ba-154">若要在 RPC 執行緒上執行時失敗嚴重 () ：引發例外狀況;移至結尾</span><span class="sxs-lookup"><span data-stu-id="425ba-154">To fail fatally (while executing on the RPC thread): Raise exception; go to End</span></span><br/> <span data-ttu-id="425ba-155">若要正常地失敗：請移至</span><span class="sxs-lookup"><span data-stu-id="425ba-155">To fail gracefully: Go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="425ba-156">P</span><span class="sxs-lookup"><span data-stu-id="425ba-156">P</span></span></td>
<td><span data-ttu-id="425ba-157">提取</span><span class="sxs-lookup"><span data-stu-id="425ba-157">Pull</span></span></td>
<td><span data-ttu-id="425ba-158">進行提取</span><span class="sxs-lookup"><span data-stu-id="425ba-158">Make a pull</span></span>
<ul>
<li><span data-ttu-id="425ba-159">失敗時移至結尾</span><span class="sxs-lookup"><span data-stu-id="425ba-159">On failure go to End</span></span></li>
<li><span data-ttu-id="425ba-160">在成功和同步完成時，若有非零位元組讀取，請移至 P</span><span class="sxs-lookup"><span data-stu-id="425ba-160">On success and synchronous completion with non-zero bytes read go to P</span></span></li>
<li><span data-ttu-id="425ba-161">在成功和同步完成時，讀取零個位元組 (null 提取) 移至複合</span><span class="sxs-lookup"><span data-stu-id="425ba-161">On success and synchronous completion with zero bytes read (null pull) go to Comp</span></span></li>
<li><span data-ttu-id="425ba-162">成功和非同步完成 (ERROR_IO_PENDING 會傳回) 移至 WP</span><span class="sxs-lookup"><span data-stu-id="425ba-162">On success and asynchronous completion (ERROR_IO_PENDING is returned) go to WP</span></span></li>
</ul>
<span data-ttu-id="425ba-163">失敗：前往</span><span class="sxs-lookup"><span data-stu-id="425ba-163">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="425ba-164">WP</span><span class="sxs-lookup"><span data-stu-id="425ba-164">WP</span></span></td>
<td><span data-ttu-id="425ba-165">等候提取</span><span class="sxs-lookup"><span data-stu-id="425ba-165">Wait for Pull</span></span></td>
<td><span data-ttu-id="425ba-166">等候通知</span><span class="sxs-lookup"><span data-stu-id="425ba-166">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="425ba-167">當無法完成時，請移至</span><span class="sxs-lookup"><span data-stu-id="425ba-167">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="425ba-168">如果收到失敗 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，請移至</span><span class="sxs-lookup"><span data-stu-id="425ba-168">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received go to A</span></span></li>
<li><span data-ttu-id="425ba-169">如果以非零位元組接收成功 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，請移至 P</span><span class="sxs-lookup"><span data-stu-id="425ba-169">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with non-zero bytes read go to P</span></span></li>
<li><span data-ttu-id="425ba-170">如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，但讀取了零個位元組 (null 提取) 移至複合</span><span class="sxs-lookup"><span data-stu-id="425ba-170">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with zero bytes read (null pull) go to Comp</span></span></li>
<li><span data-ttu-id="425ba-171">如果收到失敗，請移至</span><span class="sxs-lookup"><span data-stu-id="425ba-171">If a failure is received go to A</span></span></li>
</ul>
<span data-ttu-id="425ba-172">失敗：前往</span><span class="sxs-lookup"><span data-stu-id="425ba-172">To fail: go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="425ba-173">A</span><span class="sxs-lookup"><span data-stu-id="425ba-173">A</span></span></td>
<td><span data-ttu-id="425ba-174">中止呼叫</span><span class="sxs-lookup"><span data-stu-id="425ba-174">Abort the Call</span></span></td>
<td><span data-ttu-id="425ba-175">呼叫 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>Go to End</span><span class="sxs-lookup"><span data-stu-id="425ba-175">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="425ba-176">Comp</span><span class="sxs-lookup"><span data-stu-id="425ba-176">Comp</span></span></td>
<td><span data-ttu-id="425ba-177">Completion</span><span class="sxs-lookup"><span data-stu-id="425ba-177">Completion</span></span></td>
<td><span data-ttu-id="425ba-178">呼叫 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span><span class="sxs-lookup"><span data-stu-id="425ba-178">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="425ba-179">結束</span><span class="sxs-lookup"><span data-stu-id="425ba-179">End</span></span></td>


</tr>
</tbody>
</table>



 

## <a name="out-pipe"></a><span data-ttu-id="425ba-180">輸出管道</span><span class="sxs-lookup"><span data-stu-id="425ba-180">OUT Pipe</span></span>

<span data-ttu-id="425ba-181">用戶端行為</span><span class="sxs-lookup"><span data-stu-id="425ba-181">Client Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="425ba-182">狀態</span><span class="sxs-lookup"><span data-stu-id="425ba-182">State</span></span></th>
<th><span data-ttu-id="425ba-183">狀態名稱</span><span class="sxs-lookup"><span data-stu-id="425ba-183">State Name</span></span></th>
<th><span data-ttu-id="425ba-184">動作</span><span class="sxs-lookup"><span data-stu-id="425ba-184">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="425ba-185">C</span><span class="sxs-lookup"><span data-stu-id="425ba-185">C</span></span></td>
<td><span data-ttu-id="425ba-186">進行呼叫</span><span class="sxs-lookup"><span data-stu-id="425ba-186">Make the call</span></span></td>
<td><span data-ttu-id="425ba-187">讓 RPC</span><span class="sxs-lookup"><span data-stu-id="425ba-187">Make the RPC</span></span>
<ul>
<li><span data-ttu-id="425ba-188">成功時移至 P</span><span class="sxs-lookup"><span data-stu-id="425ba-188">On success go to P</span></span></li>
<li><span data-ttu-id="425ba-189">失敗時移至複合</span><span class="sxs-lookup"><span data-stu-id="425ba-189">On failure go to Comp</span></span></li>
</ul>
<span data-ttu-id="425ba-190">失敗：前往 [可以]</span><span class="sxs-lookup"><span data-stu-id="425ba-190">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="425ba-191">P</span><span class="sxs-lookup"><span data-stu-id="425ba-191">P</span></span></td>
<td><span data-ttu-id="425ba-192">提取</span><span class="sxs-lookup"><span data-stu-id="425ba-192">Pull</span></span></td>
<td><span data-ttu-id="425ba-193">進行提取</span><span class="sxs-lookup"><span data-stu-id="425ba-193">Make a pull</span></span>
<ul>
<li><span data-ttu-id="425ba-194">失敗時移至結尾</span><span class="sxs-lookup"><span data-stu-id="425ba-194">On failure go to End</span></span></li>
<li><span data-ttu-id="425ba-195">在成功和同步完成時，若有非零位元組讀取，請移至 P</span><span class="sxs-lookup"><span data-stu-id="425ba-195">On success and synchronous completion with non-zero bytes read go to P</span></span></li>
<li><span data-ttu-id="425ba-196">在成功和同步完成時，讀取零個位元組 (null 提取) 移至 WComp</span><span class="sxs-lookup"><span data-stu-id="425ba-196">On success and synchronous completion with zero bytes read (null pull) go to WComp</span></span></li>
<li><span data-ttu-id="425ba-197">成功和非同步完成 (ERROR_IO_PENDING 會傳回) 移至 WP</span><span class="sxs-lookup"><span data-stu-id="425ba-197">On success and asynchronous completion (ERROR_IO_PENDING is returned) go to WP</span></span></li>
</ul>
<span data-ttu-id="425ba-198">失敗：前往 [可以]</span><span class="sxs-lookup"><span data-stu-id="425ba-198">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="425ba-199">WP</span><span class="sxs-lookup"><span data-stu-id="425ba-199">WP</span></span></td>
<td><span data-ttu-id="425ba-200">等候提取</span><span class="sxs-lookup"><span data-stu-id="425ba-200">Wait for Pull</span></span></td>
<td><span data-ttu-id="425ba-201">等候通知</span><span class="sxs-lookup"><span data-stu-id="425ba-201">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="425ba-202">若無法取得完成，請移至</span><span class="sxs-lookup"><span data-stu-id="425ba-202">On failure to get a completion go to Can</span></span></li>
<li><span data-ttu-id="425ba-203">如果收到失敗 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，請移至 [可以]</span><span class="sxs-lookup"><span data-stu-id="425ba-203">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received go to Can</span></span></li>
<li><span data-ttu-id="425ba-204">如果以非零位元組接收成功 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，請移至 P</span><span class="sxs-lookup"><span data-stu-id="425ba-204">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with non-zero bytes read go to P</span></span></li>
<li><span data-ttu-id="425ba-205">如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，但讀取了零個位元組 (null 提取) 移至複合</span><span class="sxs-lookup"><span data-stu-id="425ba-205">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with zero bytes read (null pull) go to Comp</span></span></li>
<li><span data-ttu-id="425ba-206">如果收到失敗，可以</span><span class="sxs-lookup"><span data-stu-id="425ba-206">If a failure is received go Can</span></span></li>
</ul>
<span data-ttu-id="425ba-207">失敗：前往 [可以]</span><span class="sxs-lookup"><span data-stu-id="425ba-207">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="425ba-208">可以</span><span class="sxs-lookup"><span data-stu-id="425ba-208">Can</span></span></td>
<td><span data-ttu-id="425ba-209">取消呼叫</span><span class="sxs-lookup"><span data-stu-id="425ba-209">Cancel the Call</span></span></td>
<td><span data-ttu-id="425ba-210">呼叫 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>前往 WComp</span><span class="sxs-lookup"><span data-stu-id="425ba-210">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go to WComp</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="425ba-211">WComp</span><span class="sxs-lookup"><span data-stu-id="425ba-211">WComp</span></span></td>
<td><span data-ttu-id="425ba-212">等候完成</span><span class="sxs-lookup"><span data-stu-id="425ba-212">Wait for Completion</span></span></td>
<td><span data-ttu-id="425ba-213">等候通知。</span><span class="sxs-lookup"><span data-stu-id="425ba-213">Wait for notification.</span></span> <span data-ttu-id="425ba-214">應會收到呼叫完成通知。</span><span class="sxs-lookup"><span data-stu-id="425ba-214">Call-complete notification should be received.</span></span><br/> <span data-ttu-id="425ba-215">移至 [複合]</span><span class="sxs-lookup"><span data-stu-id="425ba-215">Go to Comp</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="425ba-216">Comp</span><span class="sxs-lookup"><span data-stu-id="425ba-216">Comp</span></span></td>
<td><span data-ttu-id="425ba-217">Completion</span><span class="sxs-lookup"><span data-stu-id="425ba-217">Completion</span></span></td>
<td><span data-ttu-id="425ba-218">問題 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>移至結尾</span><span class="sxs-lookup"><span data-stu-id="425ba-218">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="425ba-219">結束</span><span class="sxs-lookup"><span data-stu-id="425ba-219">End</span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="425ba-220">伺服器行為</span><span class="sxs-lookup"><span data-stu-id="425ba-220">Server Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="425ba-221">狀態</span><span class="sxs-lookup"><span data-stu-id="425ba-221">State</span></span></th>
<th><span data-ttu-id="425ba-222">狀態名稱</span><span class="sxs-lookup"><span data-stu-id="425ba-222">State Name</span></span></th>
<th><span data-ttu-id="425ba-223">動作</span><span class="sxs-lookup"><span data-stu-id="425ba-223">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="425ba-224">D</span><span class="sxs-lookup"><span data-stu-id="425ba-224">D</span></span></td>
<td><span data-ttu-id="425ba-225">分派</span><span class="sxs-lookup"><span data-stu-id="425ba-225">Dispatch</span></span></td>
<td><span data-ttu-id="425ba-226">RPC 執行時間會將呼叫分派至 P</span><span class="sxs-lookup"><span data-stu-id="425ba-226">The call is dispatched by the RPC runtime Go to P</span></span><br/> <span data-ttu-id="425ba-227">若要在 RPC 執行緒上執行時失敗嚴重 () ：引發例外狀況;移至結尾</span><span class="sxs-lookup"><span data-stu-id="425ba-227">To fail fatally (while executing on the RPC thread): Raise exception; go to End</span></span><br/> <span data-ttu-id="425ba-228">若要正常地失敗：請移至</span><span class="sxs-lookup"><span data-stu-id="425ba-228">To fail gracefully: Go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="425ba-229">P</span><span class="sxs-lookup"><span data-stu-id="425ba-229">P</span></span></td>
<td><span data-ttu-id="425ba-230">發送</span><span class="sxs-lookup"><span data-stu-id="425ba-230">Push</span></span></td>
<td><span data-ttu-id="425ba-231">進行推送</span><span class="sxs-lookup"><span data-stu-id="425ba-231">Make a push</span></span>
<ul>
<li><span data-ttu-id="425ba-232">成功移至 WP</span><span class="sxs-lookup"><span data-stu-id="425ba-232">On success go to WP</span></span></li>
<li><span data-ttu-id="425ba-233">失敗時移至結尾</span><span class="sxs-lookup"><span data-stu-id="425ba-233">On failure go to End</span></span></li>
</ul>
<span data-ttu-id="425ba-234">失敗：前往</span><span class="sxs-lookup"><span data-stu-id="425ba-234">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="425ba-235">WP</span><span class="sxs-lookup"><span data-stu-id="425ba-235">WP</span></span></td>
<td><span data-ttu-id="425ba-236">等候推播</span><span class="sxs-lookup"><span data-stu-id="425ba-236">Wait for Push</span></span></td>
<td><span data-ttu-id="425ba-237">等候通知</span><span class="sxs-lookup"><span data-stu-id="425ba-237">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="425ba-238">當無法完成時，請移至</span><span class="sxs-lookup"><span data-stu-id="425ba-238">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="425ba-239">如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> ，且需要傳送更多資料，請移至 P</span><span class="sxs-lookup"><span data-stu-id="425ba-239">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data needs to be sent go to P</span></span></li>
<li><span data-ttu-id="425ba-240">如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> ，且不需要傳送更多資料，請移至 NP</span><span class="sxs-lookup"><span data-stu-id="425ba-240">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data does not need to be sent go to NP</span></span></li>
<li><span data-ttu-id="425ba-241">如果發生失敗，請使用 < 複合</span><span class="sxs-lookup"><span data-stu-id="425ba-241">If a failure is received go Comp</span></span></li>
</ul>
<span data-ttu-id="425ba-242">失敗：前往</span><span class="sxs-lookup"><span data-stu-id="425ba-242">To fail: go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="425ba-243">NP</span><span class="sxs-lookup"><span data-stu-id="425ba-243">NP</span></span></td>
<td><span data-ttu-id="425ba-244">Null 推送</span><span class="sxs-lookup"><span data-stu-id="425ba-244">Null Push</span></span></td>
<td><span data-ttu-id="425ba-245">推播0位元組</span><span class="sxs-lookup"><span data-stu-id="425ba-245">Push 0 bytes</span></span>
<ul>
<li><span data-ttu-id="425ba-246">成功移至 WNP</span><span class="sxs-lookup"><span data-stu-id="425ba-246">on success go to WNP</span></span></li>
<li><span data-ttu-id="425ba-247">失敗時移至複合</span><span class="sxs-lookup"><span data-stu-id="425ba-247">on failure go to Comp</span></span></li>
</ul>
<span data-ttu-id="425ba-248">失敗：前往</span><span class="sxs-lookup"><span data-stu-id="425ba-248">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="425ba-249">WNP</span><span class="sxs-lookup"><span data-stu-id="425ba-249">WNP</span></span></td>
<td><span data-ttu-id="425ba-250">等候 Null 推送</span><span class="sxs-lookup"><span data-stu-id="425ba-250">Wait for Null Push</span></span></td>
<td><span data-ttu-id="425ba-251">等候通知</span><span class="sxs-lookup"><span data-stu-id="425ba-251">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="425ba-252">當無法完成時，請移至</span><span class="sxs-lookup"><span data-stu-id="425ba-252">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="425ba-253">如果發生失敗，請使用 < 複合</span><span class="sxs-lookup"><span data-stu-id="425ba-253">If a failure is received go Comp</span></span></li>
<li><span data-ttu-id="425ba-254">如果成功收到 go Comp</span><span class="sxs-lookup"><span data-stu-id="425ba-254">If a success is received go Comp</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="425ba-255">A</span><span class="sxs-lookup"><span data-stu-id="425ba-255">A</span></span></td>
<td><span data-ttu-id="425ba-256">中止呼叫</span><span class="sxs-lookup"><span data-stu-id="425ba-256">Abort the Call</span></span></td>
<td><span data-ttu-id="425ba-257">呼叫 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>;移至結尾</span><span class="sxs-lookup"><span data-stu-id="425ba-257">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; go to End</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="425ba-258">Comp</span><span class="sxs-lookup"><span data-stu-id="425ba-258">Comp</span></span></td>
<td><span data-ttu-id="425ba-259">Completion</span><span class="sxs-lookup"><span data-stu-id="425ba-259">Completion</span></span></td>
<td><span data-ttu-id="425ba-260">問題 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>;移至結尾</span><span class="sxs-lookup"><span data-stu-id="425ba-260">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; go to End</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="425ba-261">結束</span><span class="sxs-lookup"><span data-stu-id="425ba-261">End</span></span></td>


</tr>
</tbody>
</table>



 

## <a name="in-out-pipe"></a><span data-ttu-id="425ba-262">輸出管道</span><span class="sxs-lookup"><span data-stu-id="425ba-262">IN-OUT Pipe</span></span>

<span data-ttu-id="425ba-263">用戶端行為</span><span class="sxs-lookup"><span data-stu-id="425ba-263">Client Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="425ba-264">狀態</span><span class="sxs-lookup"><span data-stu-id="425ba-264">State</span></span></th>
<th><span data-ttu-id="425ba-265">狀態名稱</span><span class="sxs-lookup"><span data-stu-id="425ba-265">State Name</span></span></th>
<th><span data-ttu-id="425ba-266">動作</span><span class="sxs-lookup"><span data-stu-id="425ba-266">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="425ba-267">C</span><span class="sxs-lookup"><span data-stu-id="425ba-267">C</span></span></td>
<td><span data-ttu-id="425ba-268">進行呼叫</span><span class="sxs-lookup"><span data-stu-id="425ba-268">Make the call</span></span></td>
<td><span data-ttu-id="425ba-269">讓 RPC</span><span class="sxs-lookup"><span data-stu-id="425ba-269">Make the RPC</span></span>
<ul>
<li><span data-ttu-id="425ba-270">成功時移至 WS</span><span class="sxs-lookup"><span data-stu-id="425ba-270">On success go to WS</span></span></li>
<li><span data-ttu-id="425ba-271">發生例外狀況時移至結尾</span><span class="sxs-lookup"><span data-stu-id="425ba-271">On exception go to End</span></span></li>
</ul>
<span data-ttu-id="425ba-272">失敗：前往 [可以]</span><span class="sxs-lookup"><span data-stu-id="425ba-272">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="425ba-273">PS</span><span class="sxs-lookup"><span data-stu-id="425ba-273">PS</span></span></td>
<td><span data-ttu-id="425ba-274">發送</span><span class="sxs-lookup"><span data-stu-id="425ba-274">Push</span></span></td>
<td><span data-ttu-id="425ba-275">進行推送</span><span class="sxs-lookup"><span data-stu-id="425ba-275">Make a push</span></span>
<ul>
<li><span data-ttu-id="425ba-276">失敗時移至結尾</span><span class="sxs-lookup"><span data-stu-id="425ba-276">On failure go to End</span></span></li>
<li><span data-ttu-id="425ba-277">成功時移至 WS</span><span class="sxs-lookup"><span data-stu-id="425ba-277">On success go to WS</span></span></li>
</ul>
<span data-ttu-id="425ba-278">失敗：前往 [可以]</span><span class="sxs-lookup"><span data-stu-id="425ba-278">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="425ba-279">WS</span><span class="sxs-lookup"><span data-stu-id="425ba-279">WS</span></span></td>
<td><span data-ttu-id="425ba-280">等候傳送</span><span class="sxs-lookup"><span data-stu-id="425ba-280">Wait for Send</span></span></td>
<td><span data-ttu-id="425ba-281">等候通知</span><span class="sxs-lookup"><span data-stu-id="425ba-281">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="425ba-282">若無法取得通知，請前往</span><span class="sxs-lookup"><span data-stu-id="425ba-282">On failure to get a notification go to Can</span></span></li>
<li><span data-ttu-id="425ba-283">如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> ，且需要傳送更多資料，請前往 PS</span><span class="sxs-lookup"><span data-stu-id="425ba-283">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data needs to be sent go to PS</span></span></li>
<li><span data-ttu-id="425ba-284">如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> ，且不需要傳送更多資料，請移至 NP</span><span class="sxs-lookup"><span data-stu-id="425ba-284">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data does not need to be sent go to NP</span></span></li>
<li><span data-ttu-id="425ba-285">如果接收到失敗 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> ，請使用 go Comp</span><span class="sxs-lookup"><span data-stu-id="425ba-285">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> is received go Comp</span></span></li>
</ul>
<span data-ttu-id="425ba-286">失敗：前往 [可以]</span><span class="sxs-lookup"><span data-stu-id="425ba-286">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="425ba-287">NP</span><span class="sxs-lookup"><span data-stu-id="425ba-287">NP</span></span></td>
<td><span data-ttu-id="425ba-288">Null 推送</span><span class="sxs-lookup"><span data-stu-id="425ba-288">Null Push</span></span></td>
<td><span data-ttu-id="425ba-289">將0個位元組推 (null 推送) </span><span class="sxs-lookup"><span data-stu-id="425ba-289">Push 0 bytes (null push)</span></span>
<ul>
<li><span data-ttu-id="425ba-290">失敗時移至結尾</span><span class="sxs-lookup"><span data-stu-id="425ba-290">On failure go to End</span></span></li>
<li><span data-ttu-id="425ba-291">成功前往 PL</span><span class="sxs-lookup"><span data-stu-id="425ba-291">On success go to PL</span></span></li>
</ul>
<span data-ttu-id="425ba-292">失敗：前往 [可以]</span><span class="sxs-lookup"><span data-stu-id="425ba-292">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="425ba-293">PL</span><span class="sxs-lookup"><span data-stu-id="425ba-293">PL</span></span></td>
<td><span data-ttu-id="425ba-294">提取</span><span class="sxs-lookup"><span data-stu-id="425ba-294">Pull</span></span></td>
<td><span data-ttu-id="425ba-295">進行提取</span><span class="sxs-lookup"><span data-stu-id="425ba-295">Make a pull</span></span>
<ul>
<li><span data-ttu-id="425ba-296">失敗時移至結尾</span><span class="sxs-lookup"><span data-stu-id="425ba-296">On failure go to End</span></span></li>
<li><span data-ttu-id="425ba-297">在成功和同步完成時，若有非零位元組，請前往 PL</span><span class="sxs-lookup"><span data-stu-id="425ba-297">On success and synchronous completion with non-zero bytes read go to PL</span></span></li>
<li><span data-ttu-id="425ba-298">在成功和同步完成時，讀取零個位元組 (null 提取) 移至 WComp</span><span class="sxs-lookup"><span data-stu-id="425ba-298">On success and synchronous completion with zero bytes read (null pull) go to WComp</span></span></li>
<li><span data-ttu-id="425ba-299">成功和非同步完成 (ERROR_IO_PENDING 會傳回) 移至 .WPL</span><span class="sxs-lookup"><span data-stu-id="425ba-299">On success and asynchronous completion (ERROR_IO_PENDING is returned) go to WPL</span></span></li>
</ul>
<span data-ttu-id="425ba-300">失敗：前往 [可以]</span><span class="sxs-lookup"><span data-stu-id="425ba-300">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="425ba-301">.WPL</span><span class="sxs-lookup"><span data-stu-id="425ba-301">WPL</span></span></td>
<td><span data-ttu-id="425ba-302">等候提取</span><span class="sxs-lookup"><span data-stu-id="425ba-302">Wait for Pull</span></span></td>
<td><span data-ttu-id="425ba-303">等候通知</span><span class="sxs-lookup"><span data-stu-id="425ba-303">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="425ba-304">若無法取得完成，請移至</span><span class="sxs-lookup"><span data-stu-id="425ba-304">On failure to get a completion go to Can</span></span></li>
<li><span data-ttu-id="425ba-305">如果收到失敗 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，請移至 [可以]</span><span class="sxs-lookup"><span data-stu-id="425ba-305">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received go to Can</span></span></li>
<li><span data-ttu-id="425ba-306">如果以非零位元組接收成功 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，請前往 PL</span><span class="sxs-lookup"><span data-stu-id="425ba-306">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with non-zero bytes read go to PL</span></span></li>
<li><span data-ttu-id="425ba-307">如果接收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，且讀取了零個位元組，則會移至複合</span><span class="sxs-lookup"><span data-stu-id="425ba-307">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with zero bytes read go to Comp</span></span></li>
<li><span data-ttu-id="425ba-308">如果收到失敗，可以</span><span class="sxs-lookup"><span data-stu-id="425ba-308">If a failure is received go Can</span></span></li>
</ul>
<span data-ttu-id="425ba-309">失敗：前往 [可以]</span><span class="sxs-lookup"><span data-stu-id="425ba-309">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="425ba-310">可以</span><span class="sxs-lookup"><span data-stu-id="425ba-310">Can</span></span></td>
<td><span data-ttu-id="425ba-311">取消呼叫</span><span class="sxs-lookup"><span data-stu-id="425ba-311">Cancel the Call</span></span></td>
<td><span data-ttu-id="425ba-312">呼叫 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>前往 WComp</span><span class="sxs-lookup"><span data-stu-id="425ba-312">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go to WComp</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="425ba-313">WComp</span><span class="sxs-lookup"><span data-stu-id="425ba-313">WComp</span></span></td>
<td><span data-ttu-id="425ba-314">等候完成</span><span class="sxs-lookup"><span data-stu-id="425ba-314">Wait for Completion</span></span></td>
<td><span data-ttu-id="425ba-315">等候通知。</span><span class="sxs-lookup"><span data-stu-id="425ba-315">Wait for notification.</span></span> <span data-ttu-id="425ba-316">應會收到 CallComplete 通知。</span><span class="sxs-lookup"><span data-stu-id="425ba-316">CallComplete notification should be received.</span></span><br/> <span data-ttu-id="425ba-317">移至 [複合]</span><span class="sxs-lookup"><span data-stu-id="425ba-317">Go to Comp</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="425ba-318">Comp</span><span class="sxs-lookup"><span data-stu-id="425ba-318">Comp</span></span></td>
<td><span data-ttu-id="425ba-319">Completion</span><span class="sxs-lookup"><span data-stu-id="425ba-319">Completion</span></span></td>
<td><span data-ttu-id="425ba-320">問題 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>移至結尾</span><span class="sxs-lookup"><span data-stu-id="425ba-320">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="425ba-321">結束</span><span class="sxs-lookup"><span data-stu-id="425ba-321">End</span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="425ba-322">伺服器行為</span><span class="sxs-lookup"><span data-stu-id="425ba-322">Server Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="425ba-323">狀態</span><span class="sxs-lookup"><span data-stu-id="425ba-323">State</span></span></th>
<th><span data-ttu-id="425ba-324">狀態名稱</span><span class="sxs-lookup"><span data-stu-id="425ba-324">State Name</span></span></th>
<th><span data-ttu-id="425ba-325">動作</span><span class="sxs-lookup"><span data-stu-id="425ba-325">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="425ba-326">D</span><span class="sxs-lookup"><span data-stu-id="425ba-326">D</span></span></td>
<td><span data-ttu-id="425ba-327">分派</span><span class="sxs-lookup"><span data-stu-id="425ba-327">Dispatch</span></span></td>
<td><span data-ttu-id="425ba-328">RPC runtimeGo 將呼叫分派給 PL</span><span class="sxs-lookup"><span data-stu-id="425ba-328">The call is dispatched by the RPC runtimeGo to PL</span></span><br/> <span data-ttu-id="425ba-329">若要在 RPC 執行緒上執行時失敗嚴重 () ：引發例外狀況;移至結尾</span><span class="sxs-lookup"><span data-stu-id="425ba-329">To fail fatally (while executing on the RPC thread): Raise exception; go to End</span></span><br/> <span data-ttu-id="425ba-330">若要正常地失敗：請移至</span><span class="sxs-lookup"><span data-stu-id="425ba-330">To fail gracefully: Go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="425ba-331">PL</span><span class="sxs-lookup"><span data-stu-id="425ba-331">PL</span></span></td>
<td><span data-ttu-id="425ba-332">提取</span><span class="sxs-lookup"><span data-stu-id="425ba-332">Pull</span></span></td>
<td><span data-ttu-id="425ba-333">進行提取</span><span class="sxs-lookup"><span data-stu-id="425ba-333">Make a pull</span></span>
<ul>
<li><span data-ttu-id="425ba-334">失敗時移至結尾</span><span class="sxs-lookup"><span data-stu-id="425ba-334">On failure go to End</span></span></li>
<li><span data-ttu-id="425ba-335">在成功和同步完成時，若有非零位元組，請前往 PL</span><span class="sxs-lookup"><span data-stu-id="425ba-335">On success and synchronous completion with non-zero bytes read go to PL</span></span></li>
<li><span data-ttu-id="425ba-336">在成功和同步完成時，讀取零個位元組 (null 提取) 前往 PS</span><span class="sxs-lookup"><span data-stu-id="425ba-336">On success and synchronous completion with zero bytes read (null pull) go to PS</span></span></li>
<li><span data-ttu-id="425ba-337">成功和非同步完成 (ERROR_IO_PENDING 會傳回) 移至 .WPL</span><span class="sxs-lookup"><span data-stu-id="425ba-337">On success and asynchronous completion (ERROR_IO_PENDING is returned) go to WPL</span></span></li>
</ul>
<span data-ttu-id="425ba-338">失敗：前往</span><span class="sxs-lookup"><span data-stu-id="425ba-338">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="425ba-339">.WPL</span><span class="sxs-lookup"><span data-stu-id="425ba-339">WPL</span></span></td>
<td><span data-ttu-id="425ba-340">等候提取</span><span class="sxs-lookup"><span data-stu-id="425ba-340">Wait for Pull</span></span></td>
<td><span data-ttu-id="425ba-341">等候通知</span><span class="sxs-lookup"><span data-stu-id="425ba-341">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="425ba-342">當無法完成時，請移至</span><span class="sxs-lookup"><span data-stu-id="425ba-342">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="425ba-343">如果收到失敗 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，請移至</span><span class="sxs-lookup"><span data-stu-id="425ba-343">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received go to A</span></span></li>
<li><span data-ttu-id="425ba-344">如果以非零位元組接收成功 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，請前往 PL</span><span class="sxs-lookup"><span data-stu-id="425ba-344">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with non-zero bytes read go to PL</span></span></li>
<li><span data-ttu-id="425ba-345">如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，則讀取的位元組為零，讀取前往 PS</span><span class="sxs-lookup"><span data-stu-id="425ba-345">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with zero bytes read go to PS</span></span></li>
<li><span data-ttu-id="425ba-346">如果收到失敗，請移至</span><span class="sxs-lookup"><span data-stu-id="425ba-346">If a failure is received go A</span></span></li>
</ul>
<span data-ttu-id="425ba-347">失敗：前往</span><span class="sxs-lookup"><span data-stu-id="425ba-347">To fail: go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="425ba-348">PS</span><span class="sxs-lookup"><span data-stu-id="425ba-348">PS</span></span></td>
<td><span data-ttu-id="425ba-349">發送</span><span class="sxs-lookup"><span data-stu-id="425ba-349">Push</span></span></td>
<td><span data-ttu-id="425ba-350">進行推送</span><span class="sxs-lookup"><span data-stu-id="425ba-350">Make a push</span></span>
<ul>
<li><span data-ttu-id="425ba-351">成功移至 WPS</span><span class="sxs-lookup"><span data-stu-id="425ba-351">On success go to WPS</span></span></li>
<li><span data-ttu-id="425ba-352">失敗時移至結尾</span><span class="sxs-lookup"><span data-stu-id="425ba-352">On failure go to End</span></span></li>
</ul>
<span data-ttu-id="425ba-353">失敗：前往</span><span class="sxs-lookup"><span data-stu-id="425ba-353">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="425ba-354">Wps</span><span class="sxs-lookup"><span data-stu-id="425ba-354">WPS</span></span></td>
<td><span data-ttu-id="425ba-355">等候推播</span><span class="sxs-lookup"><span data-stu-id="425ba-355">Wait for Push</span></span></td>
<td><span data-ttu-id="425ba-356">等候通知</span><span class="sxs-lookup"><span data-stu-id="425ba-356">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="425ba-357">當無法完成時，請移至</span><span class="sxs-lookup"><span data-stu-id="425ba-357">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="425ba-358">如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> ，且需要傳送更多資料，請前往 PS</span><span class="sxs-lookup"><span data-stu-id="425ba-358">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data needs to be sent go to PS</span></span></li>
<li><span data-ttu-id="425ba-359">如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> ，且不需要傳送更多資料，請移至 NP</span><span class="sxs-lookup"><span data-stu-id="425ba-359">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data does not need to be sent go to NP</span></span></li>
<li><span data-ttu-id="425ba-360">如果發生失敗，請使用 < 複合</span><span class="sxs-lookup"><span data-stu-id="425ba-360">If a failure is received go Comp</span></span></li>
</ul>
<span data-ttu-id="425ba-361">失敗：前往</span><span class="sxs-lookup"><span data-stu-id="425ba-361">To fail: go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="425ba-362">NP</span><span class="sxs-lookup"><span data-stu-id="425ba-362">NP</span></span></td>
<td><span data-ttu-id="425ba-363">Null 推送</span><span class="sxs-lookup"><span data-stu-id="425ba-363">Null Push</span></span></td>
<td><span data-ttu-id="425ba-364">推播0位元組</span><span class="sxs-lookup"><span data-stu-id="425ba-364">Push 0 bytes</span></span>
<ul>
<li><span data-ttu-id="425ba-365">成功移至 WNP</span><span class="sxs-lookup"><span data-stu-id="425ba-365">on success go to WNP</span></span></li>
<li><span data-ttu-id="425ba-366">失敗時移至複合</span><span class="sxs-lookup"><span data-stu-id="425ba-366">on failure go to Comp</span></span></li>
</ul>
<span data-ttu-id="425ba-367">失敗：前往</span><span class="sxs-lookup"><span data-stu-id="425ba-367">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="425ba-368">WNP</span><span class="sxs-lookup"><span data-stu-id="425ba-368">WNP</span></span></td>
<td><span data-ttu-id="425ba-369">等候 Null 推送</span><span class="sxs-lookup"><span data-stu-id="425ba-369">Wait for Null Push</span></span></td>
<td><span data-ttu-id="425ba-370">等候通知</span><span class="sxs-lookup"><span data-stu-id="425ba-370">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="425ba-371">當無法完成時，請移至</span><span class="sxs-lookup"><span data-stu-id="425ba-371">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="425ba-372">如果發生失敗，請使用 < 複合</span><span class="sxs-lookup"><span data-stu-id="425ba-372">If a failure is received go Comp</span></span></li>
<li><span data-ttu-id="425ba-373">如果成功收到 go Comp</span><span class="sxs-lookup"><span data-stu-id="425ba-373">If a success is received go Comp</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="425ba-374">A</span><span class="sxs-lookup"><span data-stu-id="425ba-374">A</span></span></td>
<td><span data-ttu-id="425ba-375">中止呼叫</span><span class="sxs-lookup"><span data-stu-id="425ba-375">Abort the Call</span></span></td>
<td><span data-ttu-id="425ba-376">呼叫 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>;移至結尾</span><span class="sxs-lookup"><span data-stu-id="425ba-376">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; go to End</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="425ba-377">Comp</span><span class="sxs-lookup"><span data-stu-id="425ba-377">Comp</span></span></td>
<td><span data-ttu-id="425ba-378">Completion</span><span class="sxs-lookup"><span data-stu-id="425ba-378">Completion</span></span></td>
<td><span data-ttu-id="425ba-379">問題 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>;移至結尾</span><span class="sxs-lookup"><span data-stu-id="425ba-379">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; go to End</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="425ba-380">結束</span><span class="sxs-lookup"><span data-stu-id="425ba-380">End</span></span></td>


</tr>
</tbody>
</table>



 

 

 





