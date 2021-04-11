---
description: 執行緒可以暫停和繼續執行另一個執行緒。 當執行緒暫停時，不會排定在處理器上的時間。
ms.assetid: b76d7af7-e3ec-4663-a9e7-832c01733c8c
title: 暫停執行緒執行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3688b0327ecf5fd21f07e9be6be6ecab17d64617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944224"
---
# <a name="suspending-thread-execution"></a><span data-ttu-id="842ca-104">暫停執行緒執行</span><span class="sxs-lookup"><span data-stu-id="842ca-104">Suspending Thread Execution</span></span>

<span data-ttu-id="842ca-105">執行緒可以暫停和繼續執行另一個執行緒。</span><span class="sxs-lookup"><span data-stu-id="842ca-105">A thread can suspend and resume the execution of another thread.</span></span> <span data-ttu-id="842ca-106">當執行緒暫停時，不會排定在處理器上的時間。</span><span class="sxs-lookup"><span data-stu-id="842ca-106">While a thread is suspended, it is not scheduled for time on the processor.</span></span>

<span data-ttu-id="842ca-107">如果以暫停狀態建立執行緒 (使用 [ [**建立 \_ 擱置**](process-creation-flags.md) ] 旗標) ，則在另一個執行緒呼叫 [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) 函式時，將不會開始執行，直到另一個執行緒呼叫已暫止執行緒的控制碼為止。</span><span class="sxs-lookup"><span data-stu-id="842ca-107">If a thread is created in a suspended state (with the [**CREATE\_SUSPENDED**](process-creation-flags.md) flag), it does not begin to execute until another thread calls the [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) function with a handle to the suspended thread.</span></span> <span data-ttu-id="842ca-108">這有助於線上程開始執行之前初始化執行緒的狀態。</span><span class="sxs-lookup"><span data-stu-id="842ca-108">This can be useful for initializing the thread's state before it begins to execute.</span></span> <span data-ttu-id="842ca-109">在建立時暫停執行緒可能有助於單次同步處理，因為這樣可確保當您呼叫 **ResumeThread** 時，暫停的執行緒將會執行其程式碼的起始點。</span><span class="sxs-lookup"><span data-stu-id="842ca-109">Suspending a thread at creation can be useful for one-time synchronization, because this ensures that the suspended thread will execute the starting point of its code when you call **ResumeThread**.</span></span>

<span data-ttu-id="842ca-110">[**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread)函式不適合用于執行緒同步處理，因為它不會控制在程式碼中暫停執行緒執行的時間點。</span><span class="sxs-lookup"><span data-stu-id="842ca-110">The [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) function is not intended to be used for thread synchronization because it does not control the point in the code at which the thread's execution is suspended.</span></span> <span data-ttu-id="842ca-111">這項功能主要是設計來供偵錯工具使用。</span><span class="sxs-lookup"><span data-stu-id="842ca-111">This function is primarily designed for use by debuggers.</span></span>

<span data-ttu-id="842ca-112">執行緒可能會藉由呼叫 [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) 或 [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) 函式來暫時產生其執行，這線上程回應使用者互動的情況下特別有用，因為它可能會順延強制的時間足以讓使用者觀察其動作的結果。</span><span class="sxs-lookup"><span data-stu-id="842ca-112">A thread can temporarily yield its execution for a specified interval by calling the [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) or [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) functions This is useful particularly in cases where the thread responds to user interaction, because it can delay execution long enough to allow users to observe the results of their actions.</span></span> <span data-ttu-id="842ca-113">在睡眠間隔期間，執行緒不會排定在處理器上的時間。</span><span class="sxs-lookup"><span data-stu-id="842ca-113">During the sleep interval, the thread is not scheduled for time on the processor.</span></span>

<span data-ttu-id="842ca-114">[**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread)函式類似于 [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep)和 [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex)，不同之處在于您無法指定間隔。</span><span class="sxs-lookup"><span data-stu-id="842ca-114">The [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) function is similar to [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) and [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex), except that you cannot specify the interval.</span></span> <span data-ttu-id="842ca-115">**SwitchToThread** 可讓執行緒產生其時間配量。</span><span class="sxs-lookup"><span data-stu-id="842ca-115">**SwitchToThread** allows the thread to give up its time slice.</span></span>

 

 
