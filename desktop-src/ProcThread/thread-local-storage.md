---
description: 利用執行緒區域儲存 (TLS) ，您可以使用全域索引，為進程可以存取的每個執行緒提供唯一的資料。 一個執行緒會配置索引，其他執行緒可以使用此索引來抓取與索引相關聯的唯一資料。
ms.assetid: 40df7410-64d6-4edd-8009-d9c3d2aca920
title: 執行緒區域儲存區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e17d2ff7a1ff253ce5a20b3921cc9605bf2989f6
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/03/2021
ms.locfileid: "104550768"
---
# <a name="thread-local-storage"></a><span data-ttu-id="d13ea-104">執行緒區域儲存區</span><span class="sxs-lookup"><span data-stu-id="d13ea-104">Thread Local Storage</span></span>

<span data-ttu-id="d13ea-105">一個處理序的所有執行緒都共用該處理序的虛擬位址空間。</span><span class="sxs-lookup"><span data-stu-id="d13ea-105">All threads of a process share its virtual address space.</span></span> <span data-ttu-id="d13ea-106">函式的區域變數對執行函式的每個執行緒都是唯一的。</span><span class="sxs-lookup"><span data-stu-id="d13ea-106">The local variables of a function are unique to each thread that runs the function.</span></span> <span data-ttu-id="d13ea-107">不過，靜態和全域變數會由進程中的所有線程所共用。</span><span class="sxs-lookup"><span data-stu-id="d13ea-107">However, the static and global variables are shared by all threads in the process.</span></span> <span data-ttu-id="d13ea-108">利用 *執行緒區域儲存* (TLS) ，您可以使用全域索引，為進程可以存取的每個執行緒提供唯一的資料。</span><span class="sxs-lookup"><span data-stu-id="d13ea-108">With *thread local storage* (TLS), you can provide unique data for each thread that the process can access using a global index.</span></span> <span data-ttu-id="d13ea-109">一個執行緒會配置索引，其他執行緒可以使用此索引來抓取與索引相關聯的唯一資料。</span><span class="sxs-lookup"><span data-stu-id="d13ea-109">One thread allocates the index, which can be used by the other threads to retrieve the unique data associated with the index.</span></span>

<span data-ttu-id="d13ea-110">可用的最小 TLS \_ 最小值會 \_ 定義每個進程中可用的最小 tls 索引數目。</span><span class="sxs-lookup"><span data-stu-id="d13ea-110">The constant TLS\_MINIMUM\_AVAILABLE defines the minimum number of TLS indexes available in each process.</span></span> <span data-ttu-id="d13ea-111">所有系統的最小值保證至少為64。</span><span class="sxs-lookup"><span data-stu-id="d13ea-111">This minimum is guaranteed to be at least 64 for all systems.</span></span> <span data-ttu-id="d13ea-112">每個進程的最大索引數目是1088。</span><span class="sxs-lookup"><span data-stu-id="d13ea-112">The maximum number of indexes per process is 1,088.</span></span>

<span data-ttu-id="d13ea-113">建立執行緒時，系統會為 TLS 配置 **LPVOID** 值的陣列，這些值會初始化為 Null。</span><span class="sxs-lookup"><span data-stu-id="d13ea-113">When the threads are created, the system allocates an array of **LPVOID** values for TLS, which are initialized to NULL.</span></span> <span data-ttu-id="d13ea-114">在可以使用索引之前，必須先由其中一個執行緒配置。</span><span class="sxs-lookup"><span data-stu-id="d13ea-114">Before an index can be used, it must be allocated by one of the threads.</span></span> <span data-ttu-id="d13ea-115">每個執行緒都會將 TLS 索引的資料儲存在陣列的 *tls 插槽* 中。</span><span class="sxs-lookup"><span data-stu-id="d13ea-115">Each thread stores its data for a TLS index in a *TLS slot* in the array.</span></span> <span data-ttu-id="d13ea-116">如果與索引相關聯的資料會符合 **LPVOID** 值，您可以將資料直接儲存在 TLS 位置中。</span><span class="sxs-lookup"><span data-stu-id="d13ea-116">If the data associated with an index will fit in an **LPVOID** value, you can store the data directly in the TLS slot.</span></span> <span data-ttu-id="d13ea-117">但是，如果您以這種方式使用大量的索引，最好是配置個別的儲存體、合併資料，並將使用中的 TLS 插槽數目降至最低。</span><span class="sxs-lookup"><span data-stu-id="d13ea-117">However, if you are using a large number of indexes in this way, it is better to allocate separate storage, consolidate the data, and minimize the number of TLS slots in use.</span></span>

<span data-ttu-id="d13ea-118">下圖說明 TLS 的運作方式。</span><span class="sxs-lookup"><span data-stu-id="d13ea-118">The following diagram illustrates how TLS works.</span></span> <span data-ttu-id="d13ea-119">如需說明如何使用執行緒區域儲存區的程式碼範例，請參閱 [使用執行緒區域儲存區](using-thread-local-storage.md)。</span><span class="sxs-lookup"><span data-stu-id="d13ea-119">For a code example illustrating the use of thread local storage, see [Using Thread Local Storage](using-thread-local-storage.md).</span></span>

![此圖顯示 T L S 進程的運作方式。](images/tls.png)

<span data-ttu-id="d13ea-121">此處理程式有兩個執行緒，執行緒1和執行緒2。</span><span class="sxs-lookup"><span data-stu-id="d13ea-121">The process has two threads, Thread 1 and Thread 2.</span></span> <span data-ttu-id="d13ea-122">它會配置兩個可搭配 TLS、gdwTlsIndex1 和 gdwTlsIndex2 使用的索引。</span><span class="sxs-lookup"><span data-stu-id="d13ea-122">It allocates two indexes for use with TLS, gdwTlsIndex1 and gdwTlsIndex2.</span></span> <span data-ttu-id="d13ea-123">每個執行緒都會配置兩個記憶體區塊 (一個用於儲存資料的每個索引) ，然後將這些記憶體區塊的指標儲存在對應的 TLS 位置中。</span><span class="sxs-lookup"><span data-stu-id="d13ea-123">Each thread allocates two memory blocks (one for each index) in which to store the data, and stores the pointers to these memory blocks in the corresponding TLS slots.</span></span> <span data-ttu-id="d13ea-124">為了存取與索引相關聯的資料，執行緒會從 TLS 位置抓取記憶體區塊的指標，並將其儲存在 lpvData 區域變數中。</span><span class="sxs-lookup"><span data-stu-id="d13ea-124">To access the data associated with an index, the thread retrieves the pointer to the memory block from the TLS slot and stores it in the lpvData local variable.</span></span>

<span data-ttu-id="d13ea-125">在動態連結程式庫中使用 TLS 是很理想的 (DLL) 。</span><span class="sxs-lookup"><span data-stu-id="d13ea-125">It is ideal to use TLS in a dynamic-link library (DLL).</span></span> <span data-ttu-id="d13ea-126">如需範例，請參閱 [使用動態連結程式庫中的執行緒區域儲存區](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md)。</span><span class="sxs-lookup"><span data-stu-id="d13ea-126">For an example, see [Using Thread Local Storage in a Dynamic Link Library](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d13ea-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="d13ea-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d13ea-128">執行緒區域儲存 (Visual C++) </span><span class="sxs-lookup"><span data-stu-id="d13ea-128">Thread Local Storage (Visual C++)</span></span>](/cpp/parallel/thread-local-storage-tls?view=vs-2019)
</dt> <dt>

[<span data-ttu-id="d13ea-129">使用執行緒區域儲存區</span><span class="sxs-lookup"><span data-stu-id="d13ea-129">Using Thread Local Storage</span></span>](using-thread-local-storage.md)
</dt> <dt>

[<span data-ttu-id="d13ea-130">使用動態連結程式庫中的執行緒區域儲存區</span><span class="sxs-lookup"><span data-stu-id="d13ea-130">Using Thread Local Storage in a Dynamic Link Library</span></span>](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md)
</dt> </dl>

 

 
