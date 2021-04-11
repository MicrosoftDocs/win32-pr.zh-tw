---
description: 多工作業系統會將可用的處理器時間分割在需要它的進程或執行緒之間。
ms.assetid: ac45bef6-f078-40ac-95f4-06bd61ff46c4
title: 多工
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d06c1d8d44f397f06923c793971bcb20f35b2b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319163"
---
# <a name="multitasking"></a><span data-ttu-id="75630-103">多工</span><span class="sxs-lookup"><span data-stu-id="75630-103">Multitasking</span></span>

<span data-ttu-id="75630-104">多工作業系統會將可用的處理器時間分割在需要它的進程或執行緒之間。</span><span class="sxs-lookup"><span data-stu-id="75630-104">A multitasking operating system divides the available processor time among the processes or threads that need it.</span></span> <span data-ttu-id="75630-105">系統是針對優先處理的多工而設計它會將處理器 *時間* 配量配置給它所執行的每個執行緒。</span><span class="sxs-lookup"><span data-stu-id="75630-105">The system is designed for preemptive multitasking; it allocates a processor *time slice* to each thread it executes.</span></span> <span data-ttu-id="75630-106">目前執行中的執行緒會在其時間配量過期時暫停，讓另一個執行緒執行。</span><span class="sxs-lookup"><span data-stu-id="75630-106">The currently executing thread is suspended when its time slice elapses, allowing another thread to run.</span></span> <span data-ttu-id="75630-107">當系統從某個執行緒切換至另一個執行緒時，會儲存佔用的執行緒內容，並還原佇列中下一個執行緒的已儲存內容。</span><span class="sxs-lookup"><span data-stu-id="75630-107">When the system switches from one thread to another, it saves the context of the preempted thread and restores the saved context of the next thread in the queue.</span></span>

<span data-ttu-id="75630-108">時間配量的長短取決於作業系統和處理器。</span><span class="sxs-lookup"><span data-stu-id="75630-108">The length of the time slice depends on the operating system and the processor.</span></span> <span data-ttu-id="75630-109">由於每個時間配量都很小 (大約20毫秒的) ，因此多個執行緒會同時執行。</span><span class="sxs-lookup"><span data-stu-id="75630-109">Because each time slice is small (approximately 20 milliseconds), multiple threads appear to be executing at the same time.</span></span> <span data-ttu-id="75630-110">這實際上就是多處理器系統上的情況，其中會在可用的處理器之間分配可執行的執行緒。</span><span class="sxs-lookup"><span data-stu-id="75630-110">This is actually the case on multiprocessor systems, where the executable threads are distributed among the available processors.</span></span> <span data-ttu-id="75630-111">但是，當您在應用程式中使用多個執行緒時，必須特別小心，因為如果有太多執行緒，系統效能可能會降低。</span><span class="sxs-lookup"><span data-stu-id="75630-111">However, you must use caution when using multiple threads in an application, because system performance can decrease if there are too many threads.</span></span>

<span data-ttu-id="75630-112">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="75630-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="75630-113">多工處理的優點</span><span class="sxs-lookup"><span data-stu-id="75630-113">Advantages of Multitasking</span></span>](advantages-of-multitasking.md)
-   [<span data-ttu-id="75630-114">使用多工的時機</span><span class="sxs-lookup"><span data-stu-id="75630-114">When to Use Multitasking</span></span>](when-to-use-multitasking.md)
-   [<span data-ttu-id="75630-115">多工考慮</span><span class="sxs-lookup"><span data-stu-id="75630-115">Multitasking Considerations</span></span>](multitasking-considerations.md)

 

 



