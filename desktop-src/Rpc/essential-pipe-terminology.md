---
title: 基本管道術語
description: 如同遠端程序呼叫的其他參數類型，管道可以是 \ 或 \t 參數。
ms.assetid: 377fb65a-e819-4e96-a5b7-9850afd97b73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3df183d18d7962ad0c63ecaa0d350006a4144f23
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508068"
---
# <a name="essential-pipe-terminology"></a><span data-ttu-id="a6ab0-103">基本管道術語</span><span class="sxs-lookup"><span data-stu-id="a6ab0-103">Essential Pipe Terminology</span></span>

<span data-ttu-id="a6ab0-104">如同遠端程序呼叫的其他參數類型，管道可以是 \[ [**in**](/windows/desktop/Midl/in) \] 或 \[ [**out**](/windows/desktop/Midl/out-idl) \] 參數。</span><span class="sxs-lookup"><span data-stu-id="a6ab0-104">Like other types of parameters to remote procedure calls, pipes can be \[ [**in**](/windows/desktop/Midl/in)\] or \[ [**out**](/windows/desktop/Midl/out-idl)\] parameters.</span></span> <span data-ttu-id="a6ab0-105">由於伺服器會控制透過管道傳送資料的方式，因此會將具有 \[ **in** \] 屬性的管道 *提取* 至伺服器。</span><span class="sxs-lookup"><span data-stu-id="a6ab0-105">Since the server controls the transfer of data through a pipe, pipes with the \[**in**\] attribute are said to *pull* data to the server.</span></span> <span data-ttu-id="a6ab0-106">同樣地，輸出管道會從伺服器將資料 *推送* 至用戶端。</span><span class="sxs-lookup"><span data-stu-id="a6ab0-106">Similarly, output pipes *push* data from the server to the client.</span></span> <span data-ttu-id="a6ab0-107">進行資料傳輸的程式分別稱為 *提取* 程式和 *推送* 程式。</span><span class="sxs-lookup"><span data-stu-id="a6ab0-107">The procedures that do the data transfer are called the *pull procedure* and the *push procedure*, respectively.</span></span>

<span data-ttu-id="a6ab0-108">MIDL 編譯器會產生伺服器的推播和提取程式。</span><span class="sxs-lookup"><span data-stu-id="a6ab0-108">The MIDL compiler generates the push and pull procedures for the server.</span></span> <span data-ttu-id="a6ab0-109">此外，它也會管理記憶體中資料緩衝區的配置。</span><span class="sxs-lookup"><span data-stu-id="a6ab0-109">In addition, it manages the allocation of data buffers in memory.</span></span> <span data-ttu-id="a6ab0-110">不過，用戶端必須提供自己的推播和提取程式。</span><span class="sxs-lookup"><span data-stu-id="a6ab0-110">However, the client must provide its own push and pull procedures.</span></span> <span data-ttu-id="a6ab0-111">它也必須提供程式來配置管道所使用的記憶體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a6ab0-111">It must also provide a procedure for allocating the memory buffers used by the pipe.</span></span> <span data-ttu-id="a6ab0-112">用戶端 stub 會在適當的時間自動呼叫這些。</span><span class="sxs-lookup"><span data-stu-id="a6ab0-112">These are automatically called at the appropriate time by the client stub.</span></span> <span data-ttu-id="a6ab0-113">配置程式通常稱為配置程式或配置函數。</span><span class="sxs-lookup"><span data-stu-id="a6ab0-113">The allocation procedure is often called the alloc procedure or the alloc function.</span></span>

 

 