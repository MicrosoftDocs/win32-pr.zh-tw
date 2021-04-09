---
title: 非同步管道
description: 使用具有非同步 RPC 的管道參數，可讓您以累加方式傳送資料，因為它可供使用，而不會佔用用戶端和伺服器。
ms.assetid: e5c466b8-c0b0-4fa8-8867-d0715fd614b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be9d6dd5a3e8de7d5c4ad233a577187a49d04ed8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682890"
---
# <a name="asynchronous-pipes"></a><span data-ttu-id="dd055-103">非同步管道</span><span class="sxs-lookup"><span data-stu-id="dd055-103">Asynchronous Pipes</span></span>

<span data-ttu-id="dd055-104">使用具有非同步 RPC 的 [管道](/windows/desktop/Midl/pipe) 參數，可讓您以累加方式傳送資料，因為它可供使用，而不會佔用用戶端和伺服器。</span><span class="sxs-lookup"><span data-stu-id="dd055-104">Using [pipe](/windows/desktop/Midl/pipe) parameters with asynchronous RPC allows you to transmit data incrementally, as it becomes available, without tying up the client and server.</span></span> <span data-ttu-id="dd055-105">當您有大量的資料要傳輸、與緩慢的用戶端、緩慢的伺服器或慢速網路合併時，這項功能特別有用。</span><span class="sxs-lookup"><span data-stu-id="dd055-105">This is particularly useful when you have a large amount of data to transfer, combined with a slow client, a slow server, or a slow network.</span></span> <span data-ttu-id="dd055-106">如果您在非同步函式呼叫中使用管道，則會以非同步管道的定義來進行。</span><span class="sxs-lookup"><span data-stu-id="dd055-106">If you use a pipe in an asynchronous function call, it is, by definition, an asynchronous pipe.</span></span> <span data-ttu-id="dd055-107">同步管道不支援與非同步函式一起使用。</span><span class="sxs-lookup"><span data-stu-id="dd055-107">Synchronous pipes are not supported in conjunction with asynchronous functions.</span></span>

<span data-ttu-id="dd055-108">不同于傳統 (同步) 管道，伺服器會在其中處理傳送和接收管道資料的所有詳細資料，非同步管道是對稱的。</span><span class="sxs-lookup"><span data-stu-id="dd055-108">Unlike conventional (synchronous) pipes where the server handles all the details of sending and receiving pipe data, asynchronous pipes are symmetrical.</span></span> <span data-ttu-id="dd055-109">亦即，用戶端和伺服器都可以透過管道推送和提取資料。</span><span class="sxs-lookup"><span data-stu-id="dd055-109">That is, both the client and the server can push and pull data through the pipe.</span></span>

> [!Note]  
> <span data-ttu-id="dd055-110">只能以傳址方式傳遞管道參數。</span><span class="sxs-lookup"><span data-stu-id="dd055-110">Pipe parameters can only be passed by reference.</span></span> <span data-ttu-id="dd055-111">即使 IDL 檔案顯示以傳值方式傳遞的 [管道](/windows/desktop/Midl/pipe) 參數，產生的存根還是只會以傳址方式接受管道參數。</span><span class="sxs-lookup"><span data-stu-id="dd055-111">Even if the IDL file shows [pipe](/windows/desktop/Midl/pipe) parameters being passed by value, the generated stubs will accept pipe parameters by reference only.</span></span>

 

<span data-ttu-id="dd055-112">在下列非同步管道的討論中，會假設您熟悉管道類型的函式。</span><span class="sxs-lookup"><span data-stu-id="dd055-112">In the following discussion of asynchronous pipes, familiarity with the pipe type constructor is assumed.</span></span> <span data-ttu-id="dd055-113">如需有關這些主題所述之管道程式的詳細資訊，請參閱 [管道](pipes.md)。</span><span class="sxs-lookup"><span data-stu-id="dd055-113">For more information on the pipe procedures described in these topics, see [Pipes](pipes.md).</span></span>

 

 