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
# <a name="asynchronous-pipe-state"></a>非同步管道狀態

此頁面描述 RPC 呼叫的非同步管道狀態。

## <a name="in-pipe"></a>在管線中

用戶端行為

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>狀態</th>
<th>狀態名稱</th>
<th>動作</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>C</td>
<td>進行呼叫</td>
<td>讓 RPC
<ul>
<li>成功時移至狀態 WS</li>
<li>發生例外狀況時移至結尾</li>
</ul>
失敗：前往 [可以]<br/></td>
</tr>
<tr class="even">
<td>P</td>
<td>發送</td>
<td>進行推送
<ul>
<li>失敗時移至結尾</li>
<li>成功時移至 WS</li>
</ul>
失敗：前往 [可以]<br/></td>
</tr>
<tr class="odd">
<td>WS</td>
<td>等候傳送</td>
<td>等候通知
<ul>
<li>若無法取得通知，請前往</li>
<li>如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> ，且需要傳送更多資料，請移至 P</li>
<li>如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> ，且不需要傳送更多資料，請移至 NP</li>
<li>如果接收到失敗 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> ，請使用 go Comp</li>
</ul>
失敗：前往 [可以]<br/></td>
</tr>
<tr class="even">
<td>NP</td>
<td>Null 推送</td>
<td>將0個位元組推 (null 推送) 
<ul>
<li>失敗時移至結尾</li>
<li>成功移至 WComp</li>
</ul>
失敗：前往 [可以]<br/></td>
</tr>
<tr class="odd">
<td>可以</td>
<td>取消呼叫</td>
<td>呼叫 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>前往 WComp<br/></td>
</tr>
<tr class="even">
<td>WComp</td>
<td>等候完成</td>
<td>應會收到 notificationCall 的等候通知。<br/> 移至 [複合]<br/></td>
</tr>
<tr class="odd">
<td>Comp</td>
<td>Completion</td>
<td>問題 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>移至結尾<br/></td>
</tr>
<tr class="even">
<td>結束</td>


</tr>
</tbody>
</table>



 

伺服器行為

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>狀態</th>
<th>狀態名稱</th>
<th>動作</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D</td>
<td>分派</td>
<td>RPC 執行時間會將呼叫分派至 P<br/> 若要在 RPC 執行緒上執行時失敗嚴重 () ：引發例外狀況;移至結尾<br/> 若要正常地失敗：請移至<br/></td>
</tr>
<tr class="even">
<td>P</td>
<td>提取</td>
<td>進行提取
<ul>
<li>失敗時移至結尾</li>
<li>在成功和同步完成時，若有非零位元組讀取，請移至 P</li>
<li>在成功和同步完成時，讀取零個位元組 (null 提取) 移至複合</li>
<li>成功和非同步完成 (ERROR_IO_PENDING 會傳回) 移至 WP</li>
</ul>
失敗：前往<br/></td>
</tr>
<tr class="odd">
<td>WP</td>
<td>等候提取</td>
<td>等候通知
<ul>
<li>當無法完成時，請移至</li>
<li>如果收到失敗 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，請移至</li>
<li>如果以非零位元組接收成功 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，請移至 P</li>
<li>如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，但讀取了零個位元組 (null 提取) 移至複合</li>
<li>如果收到失敗，請移至</li>
</ul>
失敗：前往<br/></td>
</tr>
<tr class="even">
<td>A</td>
<td>中止呼叫</td>
<td>呼叫 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>Go to End<br/></td>
</tr>
<tr class="odd">
<td>Comp</td>
<td>Completion</td>
<td>呼叫 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End<br/></td>
</tr>
<tr class="even">
<td>結束</td>


</tr>
</tbody>
</table>



 

## <a name="out-pipe"></a>輸出管道

用戶端行為

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>狀態</th>
<th>狀態名稱</th>
<th>動作</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>C</td>
<td>進行呼叫</td>
<td>讓 RPC
<ul>
<li>成功時移至 P</li>
<li>失敗時移至複合</li>
</ul>
失敗：前往 [可以]<br/></td>
</tr>
<tr class="even">
<td>P</td>
<td>提取</td>
<td>進行提取
<ul>
<li>失敗時移至結尾</li>
<li>在成功和同步完成時，若有非零位元組讀取，請移至 P</li>
<li>在成功和同步完成時，讀取零個位元組 (null 提取) 移至 WComp</li>
<li>成功和非同步完成 (ERROR_IO_PENDING 會傳回) 移至 WP</li>
</ul>
失敗：前往 [可以]<br/></td>
</tr>
<tr class="odd">
<td>WP</td>
<td>等候提取</td>
<td>等候通知
<ul>
<li>若無法取得完成，請移至</li>
<li>如果收到失敗 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，請移至 [可以]</li>
<li>如果以非零位元組接收成功 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，請移至 P</li>
<li>如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，但讀取了零個位元組 (null 提取) 移至複合</li>
<li>如果收到失敗，可以</li>
</ul>
失敗：前往 [可以]<br/></td>
</tr>
<tr class="even">
<td>可以</td>
<td>取消呼叫</td>
<td>呼叫 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>前往 WComp<br/></td>
</tr>
<tr class="odd">
<td>WComp</td>
<td>等候完成</td>
<td>等候通知。 應會收到呼叫完成通知。<br/> 移至 [複合]<br/></td>
</tr>
<tr class="even">
<td>Comp</td>
<td>Completion</td>
<td>問題 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>移至結尾<br/></td>
</tr>
<tr class="odd">
<td>結束</td>


</tr>
</tbody>
</table>



 

伺服器行為

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>狀態</th>
<th>狀態名稱</th>
<th>動作</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D</td>
<td>分派</td>
<td>RPC 執行時間會將呼叫分派至 P<br/> 若要在 RPC 執行緒上執行時失敗嚴重 () ：引發例外狀況;移至結尾<br/> 若要正常地失敗：請移至<br/></td>
</tr>
<tr class="even">
<td>P</td>
<td>發送</td>
<td>進行推送
<ul>
<li>成功移至 WP</li>
<li>失敗時移至結尾</li>
</ul>
失敗：前往<br/></td>
</tr>
<tr class="odd">
<td>WP</td>
<td>等候推播</td>
<td>等候通知
<ul>
<li>當無法完成時，請移至</li>
<li>如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> ，且需要傳送更多資料，請移至 P</li>
<li>如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> ，且不需要傳送更多資料，請移至 NP</li>
<li>如果發生失敗，請使用 < 複合</li>
</ul>
失敗：前往<br/></td>
</tr>
<tr class="even">
<td>NP</td>
<td>Null 推送</td>
<td>推播0位元組
<ul>
<li>成功移至 WNP</li>
<li>失敗時移至複合</li>
</ul>
失敗：前往<br/></td>
</tr>
<tr class="odd">
<td>WNP</td>
<td>等候 Null 推送</td>
<td>等候通知
<ul>
<li>當無法完成時，請移至</li>
<li>如果發生失敗，請使用 < 複合</li>
<li>如果成功收到 go Comp</li>
</ul></td>
</tr>
<tr class="even">
<td>A</td>
<td>中止呼叫</td>
<td>呼叫 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>;移至結尾</td>
</tr>
<tr class="odd">
<td>Comp</td>
<td>Completion</td>
<td>問題 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>;移至結尾</td>
</tr>
<tr class="even">
<td>結束</td>


</tr>
</tbody>
</table>



 

## <a name="in-out-pipe"></a>輸出管道

用戶端行為

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>狀態</th>
<th>狀態名稱</th>
<th>動作</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>C</td>
<td>進行呼叫</td>
<td>讓 RPC
<ul>
<li>成功時移至 WS</li>
<li>發生例外狀況時移至結尾</li>
</ul>
失敗：前往 [可以]<br/></td>
</tr>
<tr class="even">
<td>PS</td>
<td>發送</td>
<td>進行推送
<ul>
<li>失敗時移至結尾</li>
<li>成功時移至 WS</li>
</ul>
失敗：前往 [可以]<br/></td>
</tr>
<tr class="odd">
<td>WS</td>
<td>等候傳送</td>
<td>等候通知
<ul>
<li>若無法取得通知，請前往</li>
<li>如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> ，且需要傳送更多資料，請前往 PS</li>
<li>如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> ，且不需要傳送更多資料，請移至 NP</li>
<li>如果接收到失敗 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> ，請使用 go Comp</li>
</ul>
失敗：前往 [可以]<br/></td>
</tr>
<tr class="even">
<td>NP</td>
<td>Null 推送</td>
<td>將0個位元組推 (null 推送) 
<ul>
<li>失敗時移至結尾</li>
<li>成功前往 PL</li>
</ul>
失敗：前往 [可以]<br/></td>
</tr>
<tr class="odd">
<td>PL</td>
<td>提取</td>
<td>進行提取
<ul>
<li>失敗時移至結尾</li>
<li>在成功和同步完成時，若有非零位元組，請前往 PL</li>
<li>在成功和同步完成時，讀取零個位元組 (null 提取) 移至 WComp</li>
<li>成功和非同步完成 (ERROR_IO_PENDING 會傳回) 移至 .WPL</li>
</ul>
失敗：前往 [可以]<br/></td>
</tr>
<tr class="even">
<td>.WPL</td>
<td>等候提取</td>
<td>等候通知
<ul>
<li>若無法取得完成，請移至</li>
<li>如果收到失敗 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，請移至 [可以]</li>
<li>如果以非零位元組接收成功 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，請前往 PL</li>
<li>如果接收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，且讀取了零個位元組，則會移至複合</li>
<li>如果收到失敗，可以</li>
</ul>
失敗：前往 [可以]<br/></td>
</tr>
<tr class="odd">
<td>可以</td>
<td>取消呼叫</td>
<td>呼叫 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>前往 WComp<br/></td>
</tr>
<tr class="even">
<td>WComp</td>
<td>等候完成</td>
<td>等候通知。 應會收到 CallComplete 通知。<br/> 移至 [複合]<br/></td>
</tr>
<tr class="odd">
<td>Comp</td>
<td>Completion</td>
<td>問題 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>移至結尾<br/></td>
</tr>
<tr class="even">
<td>結束</td>


</tr>
</tbody>
</table>



 

伺服器行為

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>狀態</th>
<th>狀態名稱</th>
<th>動作</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D</td>
<td>分派</td>
<td>RPC runtimeGo 將呼叫分派給 PL<br/> 若要在 RPC 執行緒上執行時失敗嚴重 () ：引發例外狀況;移至結尾<br/> 若要正常地失敗：請移至<br/></td>
</tr>
<tr class="even">
<td>PL</td>
<td>提取</td>
<td>進行提取
<ul>
<li>失敗時移至結尾</li>
<li>在成功和同步完成時，若有非零位元組，請前往 PL</li>
<li>在成功和同步完成時，讀取零個位元組 (null 提取) 前往 PS</li>
<li>成功和非同步完成 (ERROR_IO_PENDING 會傳回) 移至 .WPL</li>
</ul>
失敗：前往<br/></td>
</tr>
<tr class="odd">
<td>.WPL</td>
<td>等候提取</td>
<td>等候通知
<ul>
<li>當無法完成時，請移至</li>
<li>如果收到失敗 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，請移至</li>
<li>如果以非零位元組接收成功 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，請前往 PL</li>
<li>如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，則讀取的位元組為零，讀取前往 PS</li>
<li>如果收到失敗，請移至</li>
</ul>
失敗：前往<br/></td>
</tr>
<tr class="even">
<td>PS</td>
<td>發送</td>
<td>進行推送
<ul>
<li>成功移至 WPS</li>
<li>失敗時移至結尾</li>
</ul>
失敗：前往<br/></td>
</tr>
<tr class="odd">
<td>Wps</td>
<td>等候推播</td>
<td>等候通知
<ul>
<li>當無法完成時，請移至</li>
<li>如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> ，且需要傳送更多資料，請前往 PS</li>
<li>如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> ，且不需要傳送更多資料，請移至 NP</li>
<li>如果發生失敗，請使用 < 複合</li>
</ul>
失敗：前往<br/></td>
</tr>
<tr class="even">
<td>NP</td>
<td>Null 推送</td>
<td>推播0位元組
<ul>
<li>成功移至 WNP</li>
<li>失敗時移至複合</li>
</ul>
失敗：前往<br/></td>
</tr>
<tr class="odd">
<td>WNP</td>
<td>等候 Null 推送</td>
<td>等候通知
<ul>
<li>當無法完成時，請移至</li>
<li>如果發生失敗，請使用 < 複合</li>
<li>如果成功收到 go Comp</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>A</td>
<td>中止呼叫</td>
<td>呼叫 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>;移至結尾</td>
</tr>
<tr class="odd">
<td>Comp</td>
<td>Completion</td>
<td>問題 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>;移至結尾</td>
</tr>
<tr class="even">
<td>結束</td>


</tr>
</tbody>
</table>



 

 

 





