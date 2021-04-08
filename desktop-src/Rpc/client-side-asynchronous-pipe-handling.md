---
title: 用戶端非同步管道處理
description: 在進行非同步遠端呼叫之前，用戶端必須先初始化非同步控制碼。
ms.assetid: 3d54b233-d8b0-45d1-b759-0d2d24c1e247
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ff503f80c77b2403d683c2b644d89836365956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840571"
---
# <a name="client-side-asynchronous-pipe-handling"></a><span data-ttu-id="e85f8-103">用戶端非同步管道處理</span><span class="sxs-lookup"><span data-stu-id="e85f8-103">Client-side Asynchronous Pipe Handling</span></span>

<span data-ttu-id="e85f8-104">在進行非同步遠端呼叫之前，用戶端必須先初始化非同步控制碼。</span><span class="sxs-lookup"><span data-stu-id="e85f8-104">Before making an asynchronous remote call, the client must first initialize the asynchronous handle.</span></span> <span data-ttu-id="e85f8-105">如同 nonpipe 程式，用戶端會呼叫非同步函式，並以非同步控制碼作為第一個參數，並使用非同步控制碼來傳送和接收管道資料、查詢呼叫的狀態，以及接收回複。</span><span class="sxs-lookup"><span data-stu-id="e85f8-105">As with nonpipe procedures, the client calls an asynchronous function with the asynchronous handle as the first parameter and uses the asynchronous handle to send and receive pipe data, query the status of the call, and receive the reply.</span></span>

<span data-ttu-id="e85f8-106">用戶端會以非同步控制碼做為第一個參數來進行非同步遠端程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="e85f8-106">The client makes the asynchronous remote procedure call with the asynchronous handle as the first parameter.</span></span> <span data-ttu-id="e85f8-107">用戶端可以使用此控制碼來查詢呼叫的狀態，並接收回複。</span><span class="sxs-lookup"><span data-stu-id="e85f8-107">The client can use this handle to query the status of the call and to receive the reply.</span></span> <span data-ttu-id="e85f8-108">非同步管道模型是對稱的。</span><span class="sxs-lookup"><span data-stu-id="e85f8-108">The asynchronous pipe model is symmetric.</span></span> <span data-ttu-id="e85f8-109">用戶端和伺服器應用程式都會主動 (傳送和接收管道資料，而不是同步 RPC，在這種情況下，管道資料會以被動) 傳送和接收。</span><span class="sxs-lookup"><span data-stu-id="e85f8-109">Both client and server applications send and receive pipe data actively (as opposed to synchronous RPC, where the pipe data is sent and received passively).</span></span>

<span data-ttu-id="e85f8-110">用戶端會藉由在適當的非同步管道上呼叫 **push** 函數，並以管道的狀態變數作為第一個參數，以傳送非同步管道資料。</span><span class="sxs-lookup"><span data-stu-id="e85f8-110">The client sends asynchronous pipe data by calling the **push** function on the appropriate asynchronous pipe, with the pipe's state variable as the first parameter.</span></span> <span data-ttu-id="e85f8-111">當 **push** 函數傳回時，用戶端可以修改或釋放傳送緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e85f8-111">When the **push** function returns, the client can modify or free the send buffer.</span></span>

<span data-ttu-id="e85f8-112">如果 \_ \_ \_ \_ 非同步控制碼中已設定 [傳送完成時的 RPC 非同步通知] \_ 旗標，而且如果使用 apc 做為通知機制，當管道傳送真的完成時，就會將 APC 排入佇列。</span><span class="sxs-lookup"><span data-stu-id="e85f8-112">If the RPC\_ASYNC\_NOTIFY\_ON\_SEND\_COMPLETE flag is set in the asynchronous handle, and if APCs are used as the notification mechanism, an APC is queued when the pipe send is actually complete.</span></span> <span data-ttu-id="e85f8-113">您可以利用這項機制來實行流程式控制制。</span><span class="sxs-lookup"><span data-stu-id="e85f8-113">You can take advantage of this mechanism to implement flow control.</span></span> <span data-ttu-id="e85f8-114">但是請注意，如果用戶端在先前的推送完成之前推入另一個緩衝區，用戶端可能會根據傳送作業的速度，只接收一個傳送完成通知，而不是每個緩衝區或每個 **推送** 作業的一個通知。</span><span class="sxs-lookup"><span data-stu-id="e85f8-114">Note, however, that if the client pushes another buffer before the previous push is complete, the client may, depending on the speed of the transfer operation, receive only one send-complete notification, rather than one notification for each buffer or each **push** operation.</span></span> <span data-ttu-id="e85f8-115">當用戶端傳送所有管道資料時，它會使用設定為0的專案數目進行最後一個 **推** 播呼叫。</span><span class="sxs-lookup"><span data-stu-id="e85f8-115">When the client has sent all of the pipe data, it makes one final **push** call with the number of elements set to 0.</span></span>

<span data-ttu-id="e85f8-116">用戶端程式會藉由在適當的非同步管道上呼叫 **提取** 函式，以管道的狀態變數作為第一個參數，來接收非同步管道資料。</span><span class="sxs-lookup"><span data-stu-id="e85f8-116">The client program receives asynchronous pipe data by calling the **pull** function on the appropriate asynchronous pipe, with the pipe's state variable as the first parameter.</span></span> <span data-ttu-id="e85f8-117">如果沒有可用的管道資料， **提取** 函數會傳回 RPC \_ S \_ 非同步 \_ 呼叫 \_ 擱置。</span><span class="sxs-lookup"><span data-stu-id="e85f8-117">If no pipe data is available, the **pull** function returns RPC\_S\_ASYNC\_CALL\_PENDING.</span></span>

<span data-ttu-id="e85f8-118">如果通知機制是 APC，且伺服器傳回 RPC \_ S \_ 非同步 \_ 呼叫 \_ 擱置，用戶端必須等到它從執行時間收到 **RpcReceiveComplete** 的 APC 之後，再呼叫 **pull** 。</span><span class="sxs-lookup"><span data-stu-id="e85f8-118">If the notification mechanism is APC, and the server returned RPC\_S\_ASYNC\_CALL\_PENDING, the client must wait until it receives the **RpcReceiveComplete** APC from run-time before calling **pull** again.</span></span>

 

 




