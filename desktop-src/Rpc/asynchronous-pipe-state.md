---
title: 非同步管道狀態
description: 此頁面描述 RPC 呼叫的非同步管道狀態。
ms.assetid: af937eba-6b70-447a-af76-a8e27f5754e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a35e54d9f86228cb4c957f53411c105e20e2109
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468165"
---
# <a name="asynchronous-pipe-state"></a>非同步管道狀態

此頁面描述 RPC 呼叫的非同步管道狀態。

## <a name="in-pipe"></a>在管線中

用戶端行為


| 狀態 | 狀態名稱 | 動作 | 
|-------|------------|--------|
| C | 進行呼叫 | 讓 RPC<ul><li>成功時移至狀態 WS</li><li>發生例外狀況時移至結尾</li></ul>失敗：前往 [可以]<br /> | 
| P | 發送 | 進行推送<ul><li>失敗時移至結尾</li><li>成功時移至 WS</li></ul>失敗：前往 [可以]<br /> | 
| WS | 等候傳送 | 等候通知<ul><li>若無法取得通知，請前往</li><li>如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> ，且需要傳送更多資料，請移至 P</li><li>如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> ，且不需要傳送更多資料，請移至 NP</li><li>如果接收到失敗 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> ，請使用 go Comp</li></ul>失敗：前往 [可以]<br /> | 
| NP | Null 推送 | 將0個位元組推 (null 推送) <ul><li>失敗時移至結尾</li><li>成功移至 WComp</li></ul>失敗：前往 [可以]<br /> | 
| 可以 | 取消呼叫 | 呼叫 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>前往 WComp<br /> | 
| WComp | 等候完成 | 應會收到 notificationCall 的等候通知。<br /> 移至 [複合]<br /> | 
| Comp | Completion | 問題 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>移至結尾<br /> | 
| 結束 | 




 

伺服器行為


| 狀態 | 狀態名稱 | 動作 | 
|-------|------------|--------|
| D | 分派 | RPC 執行時間會將呼叫分派至 P<br /> 若要在 RPC 執行緒上執行時失敗嚴重 () ：引發例外狀況;移至結尾<br /> 若要正常地失敗：請移至<br /> | 
| P | 提取 | 進行提取<ul><li>失敗時移至結尾</li><li>在成功和同步完成時，若有非零位元組讀取，請移至 P</li><li>在成功和同步完成時，讀取零個位元組 (null 提取) 移至複合</li><li>成功和非同步完成 (ERROR_IO_PENDING 會傳回) 移至 WP</li></ul>失敗：前往<br /> | 
| WP | 等候提取 | 等候通知<ul><li>當無法完成時，請移至</li><li>如果收到失敗 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，請移至</li><li>如果以非零位元組接收成功 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，請移至 P</li><li>如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，但讀取了零個位元組 (null 提取) 移至複合</li><li>如果收到失敗，請移至</li></ul>失敗：前往<br /> | 
| A | 中止呼叫 | 呼叫 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>Go to End<br /> | 
| Comp | Completion | 呼叫 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End<br /> | 
| 結束 | 




 

## <a name="out-pipe"></a>輸出管道

用戶端行為


| 狀態 | 狀態名稱 | 動作 | 
|-------|------------|--------|
| C | 進行呼叫 | 讓 RPC<ul><li>成功時移至 P</li><li>失敗時移至複合</li></ul>失敗：前往 [可以]<br /> | 
| P | 提取 | 進行提取<ul><li>失敗時移至結尾</li><li>在成功和同步完成時，若有非零位元組讀取，請移至 P</li><li>在成功和同步完成時，讀取零個位元組 (null 提取) 移至 WComp</li><li>成功和非同步完成 (ERROR_IO_PENDING 會傳回) 移至 WP</li></ul>失敗：前往 [可以]<br /> | 
| WP | 等候提取 | 等候通知<ul><li>若無法取得完成，請移至</li><li>如果收到失敗 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，請移至 [可以]</li><li>如果以非零位元組接收成功 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，請移至 P</li><li>如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，但讀取了零個位元組 (null 提取) 移至複合</li><li>如果收到失敗，可以</li></ul>失敗：前往 [可以]<br /> | 
| 可以 | 取消呼叫 | 呼叫 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>前往 WComp<br /> | 
| WComp | 等候完成 | 等候通知。 應會收到呼叫完成通知。<br /> 移至 [複合]<br /> | 
| Comp | Completion | 問題 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>移至結尾<br /> | 
| 結束 | 




 

伺服器行為


| 狀態 | 狀態名稱 | 動作 | 
|-------|------------|--------|
| D | 分派 | RPC 執行時間會將呼叫分派至 P<br /> 若要在 RPC 執行緒上執行時失敗嚴重 () ：引發例外狀況;移至結尾<br /> 若要正常地失敗：請移至<br /> | 
| P | 發送 | 進行推送<ul><li>成功移至 WP</li><li>失敗時移至結尾</li></ul>失敗：前往<br /> | 
| WP | 等候推播 | 等候通知<ul><li>當無法完成時，請移至</li><li>如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> ，且需要傳送更多資料，請移至 P</li><li>如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> ，且不需要傳送更多資料，請移至 NP</li><li>如果發生失敗，請使用 < 複合</li></ul>失敗：前往<br /> | 
| NP | Null 推送 | 推播0位元組<ul><li>成功移至 WNP</li><li>失敗時移至複合</li></ul>失敗：前往<br /> | 
| WNP | 等候 Null 推送 | 等候通知<ul><li>當無法完成時，請移至</li><li>如果發生失敗，請使用 < 複合</li><li>如果成功收到 go Comp</li></ul> | 
| A | 中止呼叫 | 呼叫 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>;移至結尾 | 
| Comp | Completion | 問題 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>;移至結尾 | 
| 結束 | 




 

## <a name="in-out-pipe"></a>輸出管道

用戶端行為


| 狀態 | 狀態名稱 | 動作 | 
|-------|------------|--------|
| C | 進行呼叫 | 讓 RPC<ul><li>成功時移至 WS</li><li>發生例外狀況時移至結尾</li></ul>失敗：前往 [可以]<br /> | 
| PS | 發送 | 進行推送<ul><li>失敗時移至結尾</li><li>成功時移至 WS</li></ul>失敗：前往 [可以]<br /> | 
| WS | 等候傳送 | 等候通知<ul><li>若無法取得通知，請前往</li><li>如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> ，且需要傳送更多資料，請前往 PS</li><li>如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> ，且不需要傳送更多資料，請移至 NP</li><li>如果接收到失敗 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> ，請使用 go Comp</li></ul>失敗：前往 [可以]<br /> | 
| NP | Null 推送 | 將0個位元組推 (null 推送) <ul><li>失敗時移至結尾</li><li>成功前往 PL</li></ul>失敗：前往 [可以]<br /> | 
| PL | 提取 | 進行提取<ul><li>失敗時移至結尾</li><li>在成功和同步完成時，若有非零位元組，請前往 PL</li><li>在成功和同步完成時，讀取零個位元組 (null 提取) 移至 WComp</li><li>成功和非同步完成 (ERROR_IO_PENDING 會傳回) 移至 .WPL</li></ul>失敗：前往 [可以]<br /> | 
| .WPL | 等候提取 | 等候通知<ul><li>若無法取得完成，請移至</li><li>如果收到失敗 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，請移至 [可以]</li><li>如果以非零位元組接收成功 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，請前往 PL</li><li>如果接收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，且讀取了零個位元組，則會移至複合</li><li>如果收到失敗，可以</li></ul>失敗：前往 [可以]<br /> | 
| 可以 | 取消呼叫 | 呼叫 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>前往 WComp<br /> | 
| WComp | 等候完成 | 等候通知。 應會收到 CallComplete 通知。<br /> 移至 [複合]<br /> | 
| Comp | Completion | 問題 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>移至結尾<br /> | 
| 結束 | 




 

伺服器行為


| 狀態 | 狀態名稱 | 動作 | 
|-------|------------|--------|
| D | 分派 | RPC runtimeGo 將呼叫分派給 PL<br /> 若要在 RPC 執行緒上執行時失敗嚴重 () ：引發例外狀況;移至結尾<br /> 若要正常地失敗：請移至<br /> | 
| PL | 提取 | 進行提取<ul><li>失敗時移至結尾</li><li>在成功和同步完成時，若有非零位元組，請前往 PL</li><li>在成功和同步完成時，讀取零個位元組 (null 提取) 前往 PS</li><li>成功和非同步完成 (ERROR_IO_PENDING 會傳回) 移至 .WPL</li></ul>失敗：前往<br /> | 
| .WPL | 等候提取 | 等候通知<ul><li>當無法完成時，請移至</li><li>如果收到失敗 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，請移至</li><li>如果以非零位元組接收成功 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，請前往 PL</li><li>如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> ，則讀取的位元組為零，讀取前往 PS</li><li>如果收到失敗，請移至</li></ul>失敗：前往<br /> | 
| PS | 發送 | 進行推送<ul><li>成功移至 WPS</li><li>失敗時移至結尾</li></ul>失敗：前往<br /> | 
| WPS | 等候推播 | 等候通知<ul><li>當無法完成時，請移至</li><li>如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> ，且需要傳送更多資料，請前往 PS</li><li>如果收到成功的 <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> ，且不需要傳送更多資料，請移至 NP</li><li>如果發生失敗，請使用 < 複合</li></ul>失敗：前往<br /> | 
| NP | Null 推送 | 推播0位元組<ul><li>成功移至 WNP</li><li>失敗時移至複合</li></ul>失敗：前往<br /> | 
| WNP | 等候 Null 推送 | 等候通知<ul><li>當無法完成時，請移至</li><li>如果發生失敗，請使用 < 複合</li><li>如果成功收到 go Comp</li></ul><br /> | 
| A | 中止呼叫 | 呼叫 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>;移至結尾 | 
| Comp | Completion | 問題 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>;移至結尾 | 
| 結束 | 




 

 

 





