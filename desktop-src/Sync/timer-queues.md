---
description: CreateTimerQueue 函式會建立計時器的佇列。
ms.assetid: ee85a6c3-3a1d-4f94-9112-cb8247b2a189
title: 計時器佇列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ad2f94612c234b3ec0d1d75fa723c4e86e6fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986957"
---
# <a name="timer-queues"></a><span data-ttu-id="d5ed1-103">計時器佇列</span><span class="sxs-lookup"><span data-stu-id="d5ed1-103">Timer Queues</span></span>

<span data-ttu-id="d5ed1-104">[**CreateTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue)函式會建立計時器的佇列。</span><span class="sxs-lookup"><span data-stu-id="d5ed1-104">The [**CreateTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue) function creates a queue for timers.</span></span> <span data-ttu-id="d5ed1-105">此佇列中的計時器（稱為 *計時器佇列計時器*）是輕量物件，可讓您指定在指定的到期時間到達時要呼叫的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="d5ed1-105">Timers in this queue, known as *timer-queue timers*, are lightweight objects that enable you to specify a callback function to be called when the specified due time arrives.</span></span> <span data-ttu-id="d5ed1-106">等候作業是由 [執行緒集](../procthread/thread-pooling.md)區中的執行緒執行。</span><span class="sxs-lookup"><span data-stu-id="d5ed1-106">The wait operation is performed by a thread in the [thread pool](../procthread/thread-pooling.md).</span></span>

<span data-ttu-id="d5ed1-107">若要將計時器加入至佇列，請呼叫 [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) 函數。</span><span class="sxs-lookup"><span data-stu-id="d5ed1-107">To add a timer to the queue, call the [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) function.</span></span> <span data-ttu-id="d5ed1-108">若要更新計時器佇列計時器，請呼叫 [**ChangeTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-changetimerqueuetimer) 函數。</span><span class="sxs-lookup"><span data-stu-id="d5ed1-108">To update a timer-queue timer, call the [**ChangeTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-changetimerqueuetimer) function.</span></span> <span data-ttu-id="d5ed1-109">當計時器到期時，您可以指定要由執行緒集區中的工作者執行緒執行的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="d5ed1-109">You can specify a callback function to be executed by a worker thread from the thread pool when the timer expires.</span></span>

<span data-ttu-id="d5ed1-110">若要取消暫止的計時器，請呼叫 [**DeleteTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer) 函數。</span><span class="sxs-lookup"><span data-stu-id="d5ed1-110">To cancel a pending timer, call the [**DeleteTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer) function.</span></span> <span data-ttu-id="d5ed1-111">當您完成計時器佇列時，請呼叫 [**DeleteTimerQueueEx**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex) 函數來刪除計時器佇列。</span><span class="sxs-lookup"><span data-stu-id="d5ed1-111">When you are finished with the queue of timers, call the [**DeleteTimerQueueEx**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex) function to delete the timer queue.</span></span> <span data-ttu-id="d5ed1-112">佇列中的任何暫止計時器都已取消及刪除。</span><span class="sxs-lookup"><span data-stu-id="d5ed1-112">Any pending timers in the queue are canceled and deleted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5ed1-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="d5ed1-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5ed1-114">使用計時器佇列</span><span class="sxs-lookup"><span data-stu-id="d5ed1-114">Using Timer Queues</span></span>](using-timer-queues.md)
</dt> </dl>

 

 
