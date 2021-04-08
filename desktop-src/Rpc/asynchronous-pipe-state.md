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
# <a name="asynchronous-pipe-state"></a><span data-ttu-id="b291f-103">非同步管道狀態</span><span class="sxs-lookup"><span data-stu-id="b291f-103">Asynchronous Pipe State</span></span>

<span data-ttu-id="b291f-104">此頁面描述 RPC 呼叫的非同步管道狀態。</span><span class="sxs-lookup"><span data-stu-id="b291f-104">This page describes the Asynchronous Pipe State for RPC calls.</span></span>

## <a name="in-pipe"></a><span data-ttu-id="b291f-105">在管線中</span><span class="sxs-lookup"><span data-stu-id="b291f-105">IN Pipe</span></span>

<span data-ttu-id="b291f-106">用戶端行為</span><span class="sxs-lookup"><span data-stu-id="b291f-106">Client Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b291f-107">狀態</span><span class="sxs-lookup"><span data-stu-id="b291f-107">State</span></span></th>
<th><span data-ttu-id="b291f-108">狀態名稱</span><span class="sxs-lookup"><span data-stu-id="b291f-108">State Name</span></span></th>
<th><span data-ttu-id="b291f-109">動作</span><span class="sxs-lookup"><span data-stu-id="b291f-109">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b291f-110">C</span><span class="sxs-lookup"><span data-stu-id="b291f-110">C</span></span></td>
<td><span data-ttu-id="b291f-111">進行呼叫</span><span class="sxs-lookup"><span data-stu-id="b291f-111">Make the call</span></span></td>
<td><span data-ttu-id="b291f-112">讓 RPC</span><span class="sxs-lookup"><span data-stu-id="b291f-112">Make the RPC</span></span>
<ul>
<li><span data-ttu-id="b291f-113">成功時移至狀態 WS</span><span class="sxs-lookup"><span data-stu-id="b291f-113">On success go to state WS</span></span></li>
<li><span data-ttu-id="b291f-114">發生例外狀況時移至結尾</span><span class="sxs-lookup"><span data-stu-id="b291f-114">On exception go to End</span></span></li>
</ul>
<span data-ttu-id="b291f-115">失敗：前往 [可以]</span><span class="sxs-lookup"><span data-stu-id="b291f-115">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b291f-116">P</span><span class="sxs-lookup"><span data-stu-id="b291f-116">P</span></span></td>
<td><span data-ttu-id="b291f-117">發送</span><span class="sxs-lookup"><span data-stu-id="b291f-117">Push</span></span></td>
<td><span data-ttu-id="b291f-118">進行推送</span><span class="sxs-lookup"><span data-stu-id="b291f-118">Make a push</span></span>
<ul>
<li><span data-ttu-id="b291f-119">失敗時移至結尾</span><span class="sxs-lookup"><span data-stu-id="b291f-119">On failure go to End</span></span></li>
<li><span data-ttu-id="b291f-120">成功時移至 WS</span><span class="sxs-lookup"><span data-stu-id="b291f-120">On success go to WS</span></span></li>
</ul>
<span data-ttu-id="b291f-121">失敗：前往 [可以]</span><span class="sxs-lookup"><span data-stu-id="b291f-121">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b291f-122">WS</span><span class="sxs-lookup"><span data-stu-id="b291f-122">WS</span></span></td>
<td><span data-ttu-id="b291f-123">等候傳送</span><span class="sxs-lookup"><span data-stu-id="b291f-123">Wait for Send</span></span></td>
<td><span data-ttu-id="b291f-124">等候通知</span><span class="sxs-lookup"><span data-stu-id="b291f-124">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="b291f-125">若無法取得通知，請前往</span><span class="sxs-lookup"><span data-stu-id="b291f-125">On failure to get a notification go to Can</span></span></li>
<li><span data-ttu-id="b291f-126">如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> ，且需要傳送更多資料，請移至 P</span><span class="sxs-lookup"><span data-stu-id="b291f-126">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data needs to be sent go to P</span></span></li>
<li><span data-ttu-id="b291f-127">如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> ，且不需要傳送更多資料，請移至 NP</span><span class="sxs-lookup"><span data-stu-id="b291f-127">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data does not need to be sent go to NP</span></span></li>
<li><span data-ttu-id="b291f-128">如果接收到失敗 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> ，請使用 go Comp</span><span class="sxs-lookup"><span data-stu-id="b291f-128">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> is received go Comp</span></span></li>
</ul>
<span data-ttu-id="b291f-129">失敗：前往 [可以]</span><span class="sxs-lookup"><span data-stu-id="b291f-129">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b291f-130">NP</span><span class="sxs-lookup"><span data-stu-id="b291f-130">NP</span></span></td>
<td><span data-ttu-id="b291f-131">Null 推送</span><span class="sxs-lookup"><span data-stu-id="b291f-131">Null Push</span></span></td>
<td><span data-ttu-id="b291f-132">將0個位元組推 (null 推送) </span><span class="sxs-lookup"><span data-stu-id="b291f-132">Push 0 bytes (null push)</span></span>
<ul>
<li><span data-ttu-id="b291f-133">失敗時移至結尾</span><span class="sxs-lookup"><span data-stu-id="b291f-133">On failure go to End</span></span></li>
<li><span data-ttu-id="b291f-134">成功移至 WComp</span><span class="sxs-lookup"><span data-stu-id="b291f-134">On success go to WComp</span></span></li>
</ul>
<span data-ttu-id="b291f-135">失敗：前往 [可以]</span><span class="sxs-lookup"><span data-stu-id="b291f-135">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b291f-136">可以</span><span class="sxs-lookup"><span data-stu-id="b291f-136">Can</span></span></td>
<td><span data-ttu-id="b291f-137">取消呼叫</span><span class="sxs-lookup"><span data-stu-id="b291f-137">Cancel the Call</span></span></td>
<td><span data-ttu-id="b291f-138">呼叫 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>前往 WComp</span><span class="sxs-lookup"><span data-stu-id="b291f-138">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go to WComp</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b291f-139">WComp</span><span class="sxs-lookup"><span data-stu-id="b291f-139">WComp</span></span></td>
<td><span data-ttu-id="b291f-140">等候完成</span><span class="sxs-lookup"><span data-stu-id="b291f-140">Wait for Completion</span></span></td>
<td><span data-ttu-id="b291f-141">應會收到 notificationCall 的等候通知。</span><span class="sxs-lookup"><span data-stu-id="b291f-141">Wait for notificationCall-complete notification should be received.</span></span><br/> <span data-ttu-id="b291f-142">移至 [複合]</span><span class="sxs-lookup"><span data-stu-id="b291f-142">Go to Comp</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b291f-143">Comp</span><span class="sxs-lookup"><span data-stu-id="b291f-143">Comp</span></span></td>
<td><span data-ttu-id="b291f-144">Completion</span><span class="sxs-lookup"><span data-stu-id="b291f-144">Completion</span></span></td>
<td><span data-ttu-id="b291f-145">問題 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>移至結尾</span><span class="sxs-lookup"><span data-stu-id="b291f-145">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b291f-146">結束</span><span class="sxs-lookup"><span data-stu-id="b291f-146">End</span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="b291f-147">伺服器行為</span><span class="sxs-lookup"><span data-stu-id="b291f-147">Server Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b291f-148">狀態</span><span class="sxs-lookup"><span data-stu-id="b291f-148">State</span></span></th>
<th><span data-ttu-id="b291f-149">狀態名稱</span><span class="sxs-lookup"><span data-stu-id="b291f-149">State Name</span></span></th>
<th><span data-ttu-id="b291f-150">動作</span><span class="sxs-lookup"><span data-stu-id="b291f-150">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b291f-151">D</span><span class="sxs-lookup"><span data-stu-id="b291f-151">D</span></span></td>
<td><span data-ttu-id="b291f-152">分派</span><span class="sxs-lookup"><span data-stu-id="b291f-152">Dispatch</span></span></td>
<td><span data-ttu-id="b291f-153">RPC 執行時間會將呼叫分派至 P</span><span class="sxs-lookup"><span data-stu-id="b291f-153">The call is dispatched by the RPC runtime Go to P</span></span><br/> <span data-ttu-id="b291f-154">若要在 RPC 執行緒上執行時失敗嚴重 () ：引發例外狀況;移至結尾</span><span class="sxs-lookup"><span data-stu-id="b291f-154">To fail fatally (while executing on the RPC thread): Raise exception; go to End</span></span><br/> <span data-ttu-id="b291f-155">若要正常地失敗：請移至</span><span class="sxs-lookup"><span data-stu-id="b291f-155">To fail gracefully: Go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b291f-156">P</span><span class="sxs-lookup"><span data-stu-id="b291f-156">P</span></span></td>
<td><span data-ttu-id="b291f-157">提取</span><span class="sxs-lookup"><span data-stu-id="b291f-157">Pull</span></span></td>
<td><span data-ttu-id="b291f-158">進行提取</span><span class="sxs-lookup"><span data-stu-id="b291f-158">Make a pull</span></span>
<ul>
<li><span data-ttu-id="b291f-159">失敗時移至結尾</span><span class="sxs-lookup"><span data-stu-id="b291f-159">On failure go to End</span></span></li>
<li><span data-ttu-id="b291f-160">在成功和同步完成時，若有非零位元組讀取，請移至 P</span><span class="sxs-lookup"><span data-stu-id="b291f-160">On success and synchronous completion with non-zero bytes read go to P</span></span></li>
<li><span data-ttu-id="b291f-161">在成功和同步完成時，讀取零個位元組 (null 提取) 移至複合</span><span class="sxs-lookup"><span data-stu-id="b291f-161">On success and synchronous completion with zero bytes read (null pull) go to Comp</span></span></li>
<li><span data-ttu-id="b291f-162">成功和非同步完成 (ERROR_IO_PENDING 會傳回) 移至 WP</span><span class="sxs-lookup"><span data-stu-id="b291f-162">On success and asynchronous completion (ERROR_IO_PENDING is returned) go to WP</span></span></li>
</ul>
<span data-ttu-id="b291f-163">失敗：前往</span><span class="sxs-lookup"><span data-stu-id="b291f-163">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b291f-164">WP</span><span class="sxs-lookup"><span data-stu-id="b291f-164">WP</span></span></td>
<td><span data-ttu-id="b291f-165">等候提取</span><span class="sxs-lookup"><span data-stu-id="b291f-165">Wait for Pull</span></span></td>
<td><span data-ttu-id="b291f-166">等候通知</span><span class="sxs-lookup"><span data-stu-id="b291f-166">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="b291f-167">當無法完成時，請移至</span><span class="sxs-lookup"><span data-stu-id="b291f-167">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="b291f-168">如果收到失敗 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，請移至</span><span class="sxs-lookup"><span data-stu-id="b291f-168">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received go to A</span></span></li>
<li><span data-ttu-id="b291f-169">如果以非零位元組接收成功 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，請移至 P</span><span class="sxs-lookup"><span data-stu-id="b291f-169">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with non-zero bytes read go to P</span></span></li>
<li><span data-ttu-id="b291f-170">如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，但讀取了零個位元組 (null 提取) 移至複合</span><span class="sxs-lookup"><span data-stu-id="b291f-170">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with zero bytes read (null pull) go to Comp</span></span></li>
<li><span data-ttu-id="b291f-171">如果收到失敗，請移至</span><span class="sxs-lookup"><span data-stu-id="b291f-171">If a failure is received go to A</span></span></li>
</ul>
<span data-ttu-id="b291f-172">失敗：前往</span><span class="sxs-lookup"><span data-stu-id="b291f-172">To fail: go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b291f-173">A</span><span class="sxs-lookup"><span data-stu-id="b291f-173">A</span></span></td>
<td><span data-ttu-id="b291f-174">中止呼叫</span><span class="sxs-lookup"><span data-stu-id="b291f-174">Abort the Call</span></span></td>
<td><span data-ttu-id="b291f-175">呼叫 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>Go to End</span><span class="sxs-lookup"><span data-stu-id="b291f-175">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b291f-176">Comp</span><span class="sxs-lookup"><span data-stu-id="b291f-176">Comp</span></span></td>
<td><span data-ttu-id="b291f-177">Completion</span><span class="sxs-lookup"><span data-stu-id="b291f-177">Completion</span></span></td>
<td><span data-ttu-id="b291f-178">呼叫 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span><span class="sxs-lookup"><span data-stu-id="b291f-178">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b291f-179">結束</span><span class="sxs-lookup"><span data-stu-id="b291f-179">End</span></span></td>


</tr>
</tbody>
</table>



 

## <a name="out-pipe"></a><span data-ttu-id="b291f-180">輸出管道</span><span class="sxs-lookup"><span data-stu-id="b291f-180">OUT Pipe</span></span>

<span data-ttu-id="b291f-181">用戶端行為</span><span class="sxs-lookup"><span data-stu-id="b291f-181">Client Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b291f-182">狀態</span><span class="sxs-lookup"><span data-stu-id="b291f-182">State</span></span></th>
<th><span data-ttu-id="b291f-183">狀態名稱</span><span class="sxs-lookup"><span data-stu-id="b291f-183">State Name</span></span></th>
<th><span data-ttu-id="b291f-184">動作</span><span class="sxs-lookup"><span data-stu-id="b291f-184">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b291f-185">C</span><span class="sxs-lookup"><span data-stu-id="b291f-185">C</span></span></td>
<td><span data-ttu-id="b291f-186">進行呼叫</span><span class="sxs-lookup"><span data-stu-id="b291f-186">Make the call</span></span></td>
<td><span data-ttu-id="b291f-187">讓 RPC</span><span class="sxs-lookup"><span data-stu-id="b291f-187">Make the RPC</span></span>
<ul>
<li><span data-ttu-id="b291f-188">成功時移至 P</span><span class="sxs-lookup"><span data-stu-id="b291f-188">On success go to P</span></span></li>
<li><span data-ttu-id="b291f-189">失敗時移至複合</span><span class="sxs-lookup"><span data-stu-id="b291f-189">On failure go to Comp</span></span></li>
</ul>
<span data-ttu-id="b291f-190">失敗：前往 [可以]</span><span class="sxs-lookup"><span data-stu-id="b291f-190">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b291f-191">P</span><span class="sxs-lookup"><span data-stu-id="b291f-191">P</span></span></td>
<td><span data-ttu-id="b291f-192">提取</span><span class="sxs-lookup"><span data-stu-id="b291f-192">Pull</span></span></td>
<td><span data-ttu-id="b291f-193">進行提取</span><span class="sxs-lookup"><span data-stu-id="b291f-193">Make a pull</span></span>
<ul>
<li><span data-ttu-id="b291f-194">失敗時移至結尾</span><span class="sxs-lookup"><span data-stu-id="b291f-194">On failure go to End</span></span></li>
<li><span data-ttu-id="b291f-195">在成功和同步完成時，若有非零位元組讀取，請移至 P</span><span class="sxs-lookup"><span data-stu-id="b291f-195">On success and synchronous completion with non-zero bytes read go to P</span></span></li>
<li><span data-ttu-id="b291f-196">在成功和同步完成時，讀取零個位元組 (null 提取) 移至 WComp</span><span class="sxs-lookup"><span data-stu-id="b291f-196">On success and synchronous completion with zero bytes read (null pull) go to WComp</span></span></li>
<li><span data-ttu-id="b291f-197">成功和非同步完成 (ERROR_IO_PENDING 會傳回) 移至 WP</span><span class="sxs-lookup"><span data-stu-id="b291f-197">On success and asynchronous completion (ERROR_IO_PENDING is returned) go to WP</span></span></li>
</ul>
<span data-ttu-id="b291f-198">失敗：前往 [可以]</span><span class="sxs-lookup"><span data-stu-id="b291f-198">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b291f-199">WP</span><span class="sxs-lookup"><span data-stu-id="b291f-199">WP</span></span></td>
<td><span data-ttu-id="b291f-200">等候提取</span><span class="sxs-lookup"><span data-stu-id="b291f-200">Wait for Pull</span></span></td>
<td><span data-ttu-id="b291f-201">等候通知</span><span class="sxs-lookup"><span data-stu-id="b291f-201">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="b291f-202">若無法取得完成，請移至</span><span class="sxs-lookup"><span data-stu-id="b291f-202">On failure to get a completion go to Can</span></span></li>
<li><span data-ttu-id="b291f-203">如果收到失敗 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，請移至 [可以]</span><span class="sxs-lookup"><span data-stu-id="b291f-203">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received go to Can</span></span></li>
<li><span data-ttu-id="b291f-204">如果以非零位元組接收成功 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，請移至 P</span><span class="sxs-lookup"><span data-stu-id="b291f-204">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with non-zero bytes read go to P</span></span></li>
<li><span data-ttu-id="b291f-205">如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，但讀取了零個位元組 (null 提取) 移至複合</span><span class="sxs-lookup"><span data-stu-id="b291f-205">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with zero bytes read (null pull) go to Comp</span></span></li>
<li><span data-ttu-id="b291f-206">如果收到失敗，可以</span><span class="sxs-lookup"><span data-stu-id="b291f-206">If a failure is received go Can</span></span></li>
</ul>
<span data-ttu-id="b291f-207">失敗：前往 [可以]</span><span class="sxs-lookup"><span data-stu-id="b291f-207">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b291f-208">可以</span><span class="sxs-lookup"><span data-stu-id="b291f-208">Can</span></span></td>
<td><span data-ttu-id="b291f-209">取消呼叫</span><span class="sxs-lookup"><span data-stu-id="b291f-209">Cancel the Call</span></span></td>
<td><span data-ttu-id="b291f-210">呼叫 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>前往 WComp</span><span class="sxs-lookup"><span data-stu-id="b291f-210">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go to WComp</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b291f-211">WComp</span><span class="sxs-lookup"><span data-stu-id="b291f-211">WComp</span></span></td>
<td><span data-ttu-id="b291f-212">等候完成</span><span class="sxs-lookup"><span data-stu-id="b291f-212">Wait for Completion</span></span></td>
<td><span data-ttu-id="b291f-213">等候通知。</span><span class="sxs-lookup"><span data-stu-id="b291f-213">Wait for notification.</span></span> <span data-ttu-id="b291f-214">應會收到呼叫完成通知。</span><span class="sxs-lookup"><span data-stu-id="b291f-214">Call-complete notification should be received.</span></span><br/> <span data-ttu-id="b291f-215">移至 [複合]</span><span class="sxs-lookup"><span data-stu-id="b291f-215">Go to Comp</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b291f-216">Comp</span><span class="sxs-lookup"><span data-stu-id="b291f-216">Comp</span></span></td>
<td><span data-ttu-id="b291f-217">Completion</span><span class="sxs-lookup"><span data-stu-id="b291f-217">Completion</span></span></td>
<td><span data-ttu-id="b291f-218">問題 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>移至結尾</span><span class="sxs-lookup"><span data-stu-id="b291f-218">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b291f-219">結束</span><span class="sxs-lookup"><span data-stu-id="b291f-219">End</span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="b291f-220">伺服器行為</span><span class="sxs-lookup"><span data-stu-id="b291f-220">Server Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b291f-221">狀態</span><span class="sxs-lookup"><span data-stu-id="b291f-221">State</span></span></th>
<th><span data-ttu-id="b291f-222">狀態名稱</span><span class="sxs-lookup"><span data-stu-id="b291f-222">State Name</span></span></th>
<th><span data-ttu-id="b291f-223">動作</span><span class="sxs-lookup"><span data-stu-id="b291f-223">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b291f-224">D</span><span class="sxs-lookup"><span data-stu-id="b291f-224">D</span></span></td>
<td><span data-ttu-id="b291f-225">分派</span><span class="sxs-lookup"><span data-stu-id="b291f-225">Dispatch</span></span></td>
<td><span data-ttu-id="b291f-226">RPC 執行時間會將呼叫分派至 P</span><span class="sxs-lookup"><span data-stu-id="b291f-226">The call is dispatched by the RPC runtime Go to P</span></span><br/> <span data-ttu-id="b291f-227">若要在 RPC 執行緒上執行時失敗嚴重 () ：引發例外狀況;移至結尾</span><span class="sxs-lookup"><span data-stu-id="b291f-227">To fail fatally (while executing on the RPC thread): Raise exception; go to End</span></span><br/> <span data-ttu-id="b291f-228">若要正常地失敗：請移至</span><span class="sxs-lookup"><span data-stu-id="b291f-228">To fail gracefully: Go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b291f-229">P</span><span class="sxs-lookup"><span data-stu-id="b291f-229">P</span></span></td>
<td><span data-ttu-id="b291f-230">發送</span><span class="sxs-lookup"><span data-stu-id="b291f-230">Push</span></span></td>
<td><span data-ttu-id="b291f-231">進行推送</span><span class="sxs-lookup"><span data-stu-id="b291f-231">Make a push</span></span>
<ul>
<li><span data-ttu-id="b291f-232">成功移至 WP</span><span class="sxs-lookup"><span data-stu-id="b291f-232">On success go to WP</span></span></li>
<li><span data-ttu-id="b291f-233">失敗時移至結尾</span><span class="sxs-lookup"><span data-stu-id="b291f-233">On failure go to End</span></span></li>
</ul>
<span data-ttu-id="b291f-234">失敗：前往</span><span class="sxs-lookup"><span data-stu-id="b291f-234">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b291f-235">WP</span><span class="sxs-lookup"><span data-stu-id="b291f-235">WP</span></span></td>
<td><span data-ttu-id="b291f-236">等候推播</span><span class="sxs-lookup"><span data-stu-id="b291f-236">Wait for Push</span></span></td>
<td><span data-ttu-id="b291f-237">等候通知</span><span class="sxs-lookup"><span data-stu-id="b291f-237">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="b291f-238">當無法完成時，請移至</span><span class="sxs-lookup"><span data-stu-id="b291f-238">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="b291f-239">如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> ，且需要傳送更多資料，請移至 P</span><span class="sxs-lookup"><span data-stu-id="b291f-239">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data needs to be sent go to P</span></span></li>
<li><span data-ttu-id="b291f-240">如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> ，且不需要傳送更多資料，請移至 NP</span><span class="sxs-lookup"><span data-stu-id="b291f-240">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data does not need to be sent go to NP</span></span></li>
<li><span data-ttu-id="b291f-241">如果發生失敗，請使用 < 複合</span><span class="sxs-lookup"><span data-stu-id="b291f-241">If a failure is received go Comp</span></span></li>
</ul>
<span data-ttu-id="b291f-242">失敗：前往</span><span class="sxs-lookup"><span data-stu-id="b291f-242">To fail: go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b291f-243">NP</span><span class="sxs-lookup"><span data-stu-id="b291f-243">NP</span></span></td>
<td><span data-ttu-id="b291f-244">Null 推送</span><span class="sxs-lookup"><span data-stu-id="b291f-244">Null Push</span></span></td>
<td><span data-ttu-id="b291f-245">推播0位元組</span><span class="sxs-lookup"><span data-stu-id="b291f-245">Push 0 bytes</span></span>
<ul>
<li><span data-ttu-id="b291f-246">成功移至 WNP</span><span class="sxs-lookup"><span data-stu-id="b291f-246">on success go to WNP</span></span></li>
<li><span data-ttu-id="b291f-247">失敗時移至複合</span><span class="sxs-lookup"><span data-stu-id="b291f-247">on failure go to Comp</span></span></li>
</ul>
<span data-ttu-id="b291f-248">失敗：前往</span><span class="sxs-lookup"><span data-stu-id="b291f-248">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b291f-249">WNP</span><span class="sxs-lookup"><span data-stu-id="b291f-249">WNP</span></span></td>
<td><span data-ttu-id="b291f-250">等候 Null 推送</span><span class="sxs-lookup"><span data-stu-id="b291f-250">Wait for Null Push</span></span></td>
<td><span data-ttu-id="b291f-251">等候通知</span><span class="sxs-lookup"><span data-stu-id="b291f-251">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="b291f-252">當無法完成時，請移至</span><span class="sxs-lookup"><span data-stu-id="b291f-252">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="b291f-253">如果發生失敗，請使用 < 複合</span><span class="sxs-lookup"><span data-stu-id="b291f-253">If a failure is received go Comp</span></span></li>
<li><span data-ttu-id="b291f-254">如果成功收到 go Comp</span><span class="sxs-lookup"><span data-stu-id="b291f-254">If a success is received go Comp</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b291f-255">A</span><span class="sxs-lookup"><span data-stu-id="b291f-255">A</span></span></td>
<td><span data-ttu-id="b291f-256">中止呼叫</span><span class="sxs-lookup"><span data-stu-id="b291f-256">Abort the Call</span></span></td>
<td><span data-ttu-id="b291f-257">呼叫 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>;移至結尾</span><span class="sxs-lookup"><span data-stu-id="b291f-257">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; go to End</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b291f-258">Comp</span><span class="sxs-lookup"><span data-stu-id="b291f-258">Comp</span></span></td>
<td><span data-ttu-id="b291f-259">Completion</span><span class="sxs-lookup"><span data-stu-id="b291f-259">Completion</span></span></td>
<td><span data-ttu-id="b291f-260">問題 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>;移至結尾</span><span class="sxs-lookup"><span data-stu-id="b291f-260">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; go to End</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b291f-261">結束</span><span class="sxs-lookup"><span data-stu-id="b291f-261">End</span></span></td>


</tr>
</tbody>
</table>



 

## <a name="in-out-pipe"></a><span data-ttu-id="b291f-262">輸出管道</span><span class="sxs-lookup"><span data-stu-id="b291f-262">IN-OUT Pipe</span></span>

<span data-ttu-id="b291f-263">用戶端行為</span><span class="sxs-lookup"><span data-stu-id="b291f-263">Client Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b291f-264">狀態</span><span class="sxs-lookup"><span data-stu-id="b291f-264">State</span></span></th>
<th><span data-ttu-id="b291f-265">狀態名稱</span><span class="sxs-lookup"><span data-stu-id="b291f-265">State Name</span></span></th>
<th><span data-ttu-id="b291f-266">動作</span><span class="sxs-lookup"><span data-stu-id="b291f-266">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b291f-267">C</span><span class="sxs-lookup"><span data-stu-id="b291f-267">C</span></span></td>
<td><span data-ttu-id="b291f-268">進行呼叫</span><span class="sxs-lookup"><span data-stu-id="b291f-268">Make the call</span></span></td>
<td><span data-ttu-id="b291f-269">讓 RPC</span><span class="sxs-lookup"><span data-stu-id="b291f-269">Make the RPC</span></span>
<ul>
<li><span data-ttu-id="b291f-270">成功時移至 WS</span><span class="sxs-lookup"><span data-stu-id="b291f-270">On success go to WS</span></span></li>
<li><span data-ttu-id="b291f-271">發生例外狀況時移至結尾</span><span class="sxs-lookup"><span data-stu-id="b291f-271">On exception go to End</span></span></li>
</ul>
<span data-ttu-id="b291f-272">失敗：前往 [可以]</span><span class="sxs-lookup"><span data-stu-id="b291f-272">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b291f-273">PS</span><span class="sxs-lookup"><span data-stu-id="b291f-273">PS</span></span></td>
<td><span data-ttu-id="b291f-274">發送</span><span class="sxs-lookup"><span data-stu-id="b291f-274">Push</span></span></td>
<td><span data-ttu-id="b291f-275">進行推送</span><span class="sxs-lookup"><span data-stu-id="b291f-275">Make a push</span></span>
<ul>
<li><span data-ttu-id="b291f-276">失敗時移至結尾</span><span class="sxs-lookup"><span data-stu-id="b291f-276">On failure go to End</span></span></li>
<li><span data-ttu-id="b291f-277">成功時移至 WS</span><span class="sxs-lookup"><span data-stu-id="b291f-277">On success go to WS</span></span></li>
</ul>
<span data-ttu-id="b291f-278">失敗：前往 [可以]</span><span class="sxs-lookup"><span data-stu-id="b291f-278">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b291f-279">WS</span><span class="sxs-lookup"><span data-stu-id="b291f-279">WS</span></span></td>
<td><span data-ttu-id="b291f-280">等候傳送</span><span class="sxs-lookup"><span data-stu-id="b291f-280">Wait for Send</span></span></td>
<td><span data-ttu-id="b291f-281">等候通知</span><span class="sxs-lookup"><span data-stu-id="b291f-281">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="b291f-282">若無法取得通知，請前往</span><span class="sxs-lookup"><span data-stu-id="b291f-282">On failure to get a notification go to Can</span></span></li>
<li><span data-ttu-id="b291f-283">如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> ，且需要傳送更多資料，請前往 PS</span><span class="sxs-lookup"><span data-stu-id="b291f-283">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data needs to be sent go to PS</span></span></li>
<li><span data-ttu-id="b291f-284">如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> ，且不需要傳送更多資料，請移至 NP</span><span class="sxs-lookup"><span data-stu-id="b291f-284">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data does not need to be sent go to NP</span></span></li>
<li><span data-ttu-id="b291f-285">如果接收到失敗 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> ，請使用 go Comp</span><span class="sxs-lookup"><span data-stu-id="b291f-285">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> is received go Comp</span></span></li>
</ul>
<span data-ttu-id="b291f-286">失敗：前往 [可以]</span><span class="sxs-lookup"><span data-stu-id="b291f-286">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b291f-287">NP</span><span class="sxs-lookup"><span data-stu-id="b291f-287">NP</span></span></td>
<td><span data-ttu-id="b291f-288">Null 推送</span><span class="sxs-lookup"><span data-stu-id="b291f-288">Null Push</span></span></td>
<td><span data-ttu-id="b291f-289">將0個位元組推 (null 推送) </span><span class="sxs-lookup"><span data-stu-id="b291f-289">Push 0 bytes (null push)</span></span>
<ul>
<li><span data-ttu-id="b291f-290">失敗時移至結尾</span><span class="sxs-lookup"><span data-stu-id="b291f-290">On failure go to End</span></span></li>
<li><span data-ttu-id="b291f-291">成功前往 PL</span><span class="sxs-lookup"><span data-stu-id="b291f-291">On success go to PL</span></span></li>
</ul>
<span data-ttu-id="b291f-292">失敗：前往 [可以]</span><span class="sxs-lookup"><span data-stu-id="b291f-292">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b291f-293">PL</span><span class="sxs-lookup"><span data-stu-id="b291f-293">PL</span></span></td>
<td><span data-ttu-id="b291f-294">提取</span><span class="sxs-lookup"><span data-stu-id="b291f-294">Pull</span></span></td>
<td><span data-ttu-id="b291f-295">進行提取</span><span class="sxs-lookup"><span data-stu-id="b291f-295">Make a pull</span></span>
<ul>
<li><span data-ttu-id="b291f-296">失敗時移至結尾</span><span class="sxs-lookup"><span data-stu-id="b291f-296">On failure go to End</span></span></li>
<li><span data-ttu-id="b291f-297">在成功和同步完成時，若有非零位元組，請前往 PL</span><span class="sxs-lookup"><span data-stu-id="b291f-297">On success and synchronous completion with non-zero bytes read go to PL</span></span></li>
<li><span data-ttu-id="b291f-298">在成功和同步完成時，讀取零個位元組 (null 提取) 移至 WComp</span><span class="sxs-lookup"><span data-stu-id="b291f-298">On success and synchronous completion with zero bytes read (null pull) go to WComp</span></span></li>
<li><span data-ttu-id="b291f-299">成功和非同步完成 (ERROR_IO_PENDING 會傳回) 移至 .WPL</span><span class="sxs-lookup"><span data-stu-id="b291f-299">On success and asynchronous completion (ERROR_IO_PENDING is returned) go to WPL</span></span></li>
</ul>
<span data-ttu-id="b291f-300">失敗：前往 [可以]</span><span class="sxs-lookup"><span data-stu-id="b291f-300">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b291f-301">.WPL</span><span class="sxs-lookup"><span data-stu-id="b291f-301">WPL</span></span></td>
<td><span data-ttu-id="b291f-302">等候提取</span><span class="sxs-lookup"><span data-stu-id="b291f-302">Wait for Pull</span></span></td>
<td><span data-ttu-id="b291f-303">等候通知</span><span class="sxs-lookup"><span data-stu-id="b291f-303">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="b291f-304">若無法取得完成，請移至</span><span class="sxs-lookup"><span data-stu-id="b291f-304">On failure to get a completion go to Can</span></span></li>
<li><span data-ttu-id="b291f-305">如果收到失敗 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，請移至 [可以]</span><span class="sxs-lookup"><span data-stu-id="b291f-305">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received go to Can</span></span></li>
<li><span data-ttu-id="b291f-306">如果以非零位元組接收成功 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，請前往 PL</span><span class="sxs-lookup"><span data-stu-id="b291f-306">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with non-zero bytes read go to PL</span></span></li>
<li><span data-ttu-id="b291f-307">如果接收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，且讀取了零個位元組，則會移至複合</span><span class="sxs-lookup"><span data-stu-id="b291f-307">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with zero bytes read go to Comp</span></span></li>
<li><span data-ttu-id="b291f-308">如果收到失敗，可以</span><span class="sxs-lookup"><span data-stu-id="b291f-308">If a failure is received go Can</span></span></li>
</ul>
<span data-ttu-id="b291f-309">失敗：前往 [可以]</span><span class="sxs-lookup"><span data-stu-id="b291f-309">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b291f-310">可以</span><span class="sxs-lookup"><span data-stu-id="b291f-310">Can</span></span></td>
<td><span data-ttu-id="b291f-311">取消呼叫</span><span class="sxs-lookup"><span data-stu-id="b291f-311">Cancel the Call</span></span></td>
<td><span data-ttu-id="b291f-312">呼叫 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>前往 WComp</span><span class="sxs-lookup"><span data-stu-id="b291f-312">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go to WComp</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b291f-313">WComp</span><span class="sxs-lookup"><span data-stu-id="b291f-313">WComp</span></span></td>
<td><span data-ttu-id="b291f-314">等候完成</span><span class="sxs-lookup"><span data-stu-id="b291f-314">Wait for Completion</span></span></td>
<td><span data-ttu-id="b291f-315">等候通知。</span><span class="sxs-lookup"><span data-stu-id="b291f-315">Wait for notification.</span></span> <span data-ttu-id="b291f-316">應會收到 CallComplete 通知。</span><span class="sxs-lookup"><span data-stu-id="b291f-316">CallComplete notification should be received.</span></span><br/> <span data-ttu-id="b291f-317">移至 [複合]</span><span class="sxs-lookup"><span data-stu-id="b291f-317">Go to Comp</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b291f-318">Comp</span><span class="sxs-lookup"><span data-stu-id="b291f-318">Comp</span></span></td>
<td><span data-ttu-id="b291f-319">Completion</span><span class="sxs-lookup"><span data-stu-id="b291f-319">Completion</span></span></td>
<td><span data-ttu-id="b291f-320">問題 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>移至結尾</span><span class="sxs-lookup"><span data-stu-id="b291f-320">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b291f-321">結束</span><span class="sxs-lookup"><span data-stu-id="b291f-321">End</span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="b291f-322">伺服器行為</span><span class="sxs-lookup"><span data-stu-id="b291f-322">Server Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b291f-323">狀態</span><span class="sxs-lookup"><span data-stu-id="b291f-323">State</span></span></th>
<th><span data-ttu-id="b291f-324">狀態名稱</span><span class="sxs-lookup"><span data-stu-id="b291f-324">State Name</span></span></th>
<th><span data-ttu-id="b291f-325">動作</span><span class="sxs-lookup"><span data-stu-id="b291f-325">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b291f-326">D</span><span class="sxs-lookup"><span data-stu-id="b291f-326">D</span></span></td>
<td><span data-ttu-id="b291f-327">分派</span><span class="sxs-lookup"><span data-stu-id="b291f-327">Dispatch</span></span></td>
<td><span data-ttu-id="b291f-328">RPC runtimeGo 將呼叫分派給 PL</span><span class="sxs-lookup"><span data-stu-id="b291f-328">The call is dispatched by the RPC runtimeGo to PL</span></span><br/> <span data-ttu-id="b291f-329">若要在 RPC 執行緒上執行時失敗嚴重 () ：引發例外狀況;移至結尾</span><span class="sxs-lookup"><span data-stu-id="b291f-329">To fail fatally (while executing on the RPC thread): Raise exception; go to End</span></span><br/> <span data-ttu-id="b291f-330">若要正常地失敗：請移至</span><span class="sxs-lookup"><span data-stu-id="b291f-330">To fail gracefully: Go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b291f-331">PL</span><span class="sxs-lookup"><span data-stu-id="b291f-331">PL</span></span></td>
<td><span data-ttu-id="b291f-332">提取</span><span class="sxs-lookup"><span data-stu-id="b291f-332">Pull</span></span></td>
<td><span data-ttu-id="b291f-333">進行提取</span><span class="sxs-lookup"><span data-stu-id="b291f-333">Make a pull</span></span>
<ul>
<li><span data-ttu-id="b291f-334">失敗時移至結尾</span><span class="sxs-lookup"><span data-stu-id="b291f-334">On failure go to End</span></span></li>
<li><span data-ttu-id="b291f-335">在成功和同步完成時，若有非零位元組，請前往 PL</span><span class="sxs-lookup"><span data-stu-id="b291f-335">On success and synchronous completion with non-zero bytes read go to PL</span></span></li>
<li><span data-ttu-id="b291f-336">在成功和同步完成時，讀取零個位元組 (null 提取) 前往 PS</span><span class="sxs-lookup"><span data-stu-id="b291f-336">On success and synchronous completion with zero bytes read (null pull) go to PS</span></span></li>
<li><span data-ttu-id="b291f-337">成功和非同步完成 (ERROR_IO_PENDING 會傳回) 移至 .WPL</span><span class="sxs-lookup"><span data-stu-id="b291f-337">On success and asynchronous completion (ERROR_IO_PENDING is returned) go to WPL</span></span></li>
</ul>
<span data-ttu-id="b291f-338">失敗：前往</span><span class="sxs-lookup"><span data-stu-id="b291f-338">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b291f-339">.WPL</span><span class="sxs-lookup"><span data-stu-id="b291f-339">WPL</span></span></td>
<td><span data-ttu-id="b291f-340">等候提取</span><span class="sxs-lookup"><span data-stu-id="b291f-340">Wait for Pull</span></span></td>
<td><span data-ttu-id="b291f-341">等候通知</span><span class="sxs-lookup"><span data-stu-id="b291f-341">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="b291f-342">當無法完成時，請移至</span><span class="sxs-lookup"><span data-stu-id="b291f-342">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="b291f-343">如果收到失敗 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，請移至</span><span class="sxs-lookup"><span data-stu-id="b291f-343">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received go to A</span></span></li>
<li><span data-ttu-id="b291f-344">如果以非零位元組接收成功 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，請前往 PL</span><span class="sxs-lookup"><span data-stu-id="b291f-344">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with non-zero bytes read go to PL</span></span></li>
<li><span data-ttu-id="b291f-345">如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，則讀取的位元組為零，讀取前往 PS</span><span class="sxs-lookup"><span data-stu-id="b291f-345">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with zero bytes read go to PS</span></span></li>
<li><span data-ttu-id="b291f-346">如果收到失敗，請移至</span><span class="sxs-lookup"><span data-stu-id="b291f-346">If a failure is received go A</span></span></li>
</ul>
<span data-ttu-id="b291f-347">失敗：前往</span><span class="sxs-lookup"><span data-stu-id="b291f-347">To fail: go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b291f-348">PS</span><span class="sxs-lookup"><span data-stu-id="b291f-348">PS</span></span></td>
<td><span data-ttu-id="b291f-349">發送</span><span class="sxs-lookup"><span data-stu-id="b291f-349">Push</span></span></td>
<td><span data-ttu-id="b291f-350">進行推送</span><span class="sxs-lookup"><span data-stu-id="b291f-350">Make a push</span></span>
<ul>
<li><span data-ttu-id="b291f-351">成功移至 WPS</span><span class="sxs-lookup"><span data-stu-id="b291f-351">On success go to WPS</span></span></li>
<li><span data-ttu-id="b291f-352">失敗時移至結尾</span><span class="sxs-lookup"><span data-stu-id="b291f-352">On failure go to End</span></span></li>
</ul>
<span data-ttu-id="b291f-353">失敗：前往</span><span class="sxs-lookup"><span data-stu-id="b291f-353">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b291f-354">Wps</span><span class="sxs-lookup"><span data-stu-id="b291f-354">WPS</span></span></td>
<td><span data-ttu-id="b291f-355">等候推播</span><span class="sxs-lookup"><span data-stu-id="b291f-355">Wait for Push</span></span></td>
<td><span data-ttu-id="b291f-356">等候通知</span><span class="sxs-lookup"><span data-stu-id="b291f-356">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="b291f-357">當無法完成時，請移至</span><span class="sxs-lookup"><span data-stu-id="b291f-357">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="b291f-358">如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> ，且需要傳送更多資料，請前往 PS</span><span class="sxs-lookup"><span data-stu-id="b291f-358">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data needs to be sent go to PS</span></span></li>
<li><span data-ttu-id="b291f-359">如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> ，且不需要傳送更多資料，請移至 NP</span><span class="sxs-lookup"><span data-stu-id="b291f-359">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data does not need to be sent go to NP</span></span></li>
<li><span data-ttu-id="b291f-360">如果發生失敗，請使用 < 複合</span><span class="sxs-lookup"><span data-stu-id="b291f-360">If a failure is received go Comp</span></span></li>
</ul>
<span data-ttu-id="b291f-361">失敗：前往</span><span class="sxs-lookup"><span data-stu-id="b291f-361">To fail: go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b291f-362">NP</span><span class="sxs-lookup"><span data-stu-id="b291f-362">NP</span></span></td>
<td><span data-ttu-id="b291f-363">Null 推送</span><span class="sxs-lookup"><span data-stu-id="b291f-363">Null Push</span></span></td>
<td><span data-ttu-id="b291f-364">推播0位元組</span><span class="sxs-lookup"><span data-stu-id="b291f-364">Push 0 bytes</span></span>
<ul>
<li><span data-ttu-id="b291f-365">成功移至 WNP</span><span class="sxs-lookup"><span data-stu-id="b291f-365">on success go to WNP</span></span></li>
<li><span data-ttu-id="b291f-366">失敗時移至複合</span><span class="sxs-lookup"><span data-stu-id="b291f-366">on failure go to Comp</span></span></li>
</ul>
<span data-ttu-id="b291f-367">失敗：前往</span><span class="sxs-lookup"><span data-stu-id="b291f-367">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b291f-368">WNP</span><span class="sxs-lookup"><span data-stu-id="b291f-368">WNP</span></span></td>
<td><span data-ttu-id="b291f-369">等候 Null 推送</span><span class="sxs-lookup"><span data-stu-id="b291f-369">Wait for Null Push</span></span></td>
<td><span data-ttu-id="b291f-370">等候通知</span><span class="sxs-lookup"><span data-stu-id="b291f-370">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="b291f-371">當無法完成時，請移至</span><span class="sxs-lookup"><span data-stu-id="b291f-371">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="b291f-372">如果發生失敗，請使用 < 複合</span><span class="sxs-lookup"><span data-stu-id="b291f-372">If a failure is received go Comp</span></span></li>
<li><span data-ttu-id="b291f-373">如果成功收到 go Comp</span><span class="sxs-lookup"><span data-stu-id="b291f-373">If a success is received go Comp</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b291f-374">A</span><span class="sxs-lookup"><span data-stu-id="b291f-374">A</span></span></td>
<td><span data-ttu-id="b291f-375">中止呼叫</span><span class="sxs-lookup"><span data-stu-id="b291f-375">Abort the Call</span></span></td>
<td><span data-ttu-id="b291f-376">呼叫 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>;移至結尾</span><span class="sxs-lookup"><span data-stu-id="b291f-376">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; go to End</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b291f-377">Comp</span><span class="sxs-lookup"><span data-stu-id="b291f-377">Comp</span></span></td>
<td><span data-ttu-id="b291f-378">Completion</span><span class="sxs-lookup"><span data-stu-id="b291f-378">Completion</span></span></td>
<td><span data-ttu-id="b291f-379">問題 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>;移至結尾</span><span class="sxs-lookup"><span data-stu-id="b291f-379">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; go to End</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b291f-380">結束</span><span class="sxs-lookup"><span data-stu-id="b291f-380">End</span></span></td>


</tr>
</tbody>
</table>



 

 

 





