---
title: IStream 複合檔案執行
description: IStream 介面支援對資料流程物件讀取和寫入資料。 在結構化儲存物件中，資料流程物件包含資料和儲存體提供結構。
ms.assetid: 52474e37-0e14-4dcc-8e04-4442cfd26eb3
keywords:
- IStream Strctd Stg.，複合檔案執行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d15e671521f4a1e81b78579bc1225eccb48898
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "106974743"
---
# <a name="istream---compound-file-implementation"></a><span data-ttu-id="27892-105">IStream 複合檔案執行</span><span class="sxs-lookup"><span data-stu-id="27892-105">IStream - Compound File Implementation</span></span>

<span data-ttu-id="27892-106">[**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)介面支援對資料流程物件讀取和寫入資料。</span><span class="sxs-lookup"><span data-stu-id="27892-106">The [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) interface supports reading and writing data to stream objects.</span></span> <span data-ttu-id="27892-107">在結構化儲存物件中，資料流程物件包含資料和儲存體提供結構。</span><span class="sxs-lookup"><span data-stu-id="27892-107">In a structured storage object, stream objects contain the data and storages provide the structure.</span></span> <span data-ttu-id="27892-108">簡單的資料可以直接寫入資料流程，但更頻繁的是，資料流程是在儲存物件中嵌套的元素。</span><span class="sxs-lookup"><span data-stu-id="27892-108">Simple data can be written directly to a stream, but more frequently, streams are elements nested within a storage object.</span></span> <span data-ttu-id="27892-109">它們類似于標準檔案。</span><span class="sxs-lookup"><span data-stu-id="27892-109">They are similar to standard files.</span></span>

<span data-ttu-id="27892-110">[**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)的規格定義了比 COM 執行所支援的功能更多的功能。</span><span class="sxs-lookup"><span data-stu-id="27892-110">The specification of [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) defines more functionality than the COM implementation supports.</span></span> <span data-ttu-id="27892-111">例如， **IStream** 介面會定義最多2個⁶⁴位元組的資料流程，而其長度需要64位的 seek 指標。</span><span class="sxs-lookup"><span data-stu-id="27892-111">For example, the **IStream** interface defines streams up to 2⁶⁴ bytes in length requiring a 64-bit seek pointer.</span></span> <span data-ttu-id="27892-112">不過，COM 執行只支援最多2個³²位元組的資料流程， (4 GB) ，而且讀取和寫入作業一次一律會限制為2個³²位元組。</span><span class="sxs-lookup"><span data-stu-id="27892-112">However, the COM implementation only supports streams up to 2³² bytes in length (4 GB) and read and write operations are always limited to 2³² bytes at a time.</span></span> <span data-ttu-id="27892-113">COM 執行也不支援資料流程 transactioning 或區域鎖定。</span><span class="sxs-lookup"><span data-stu-id="27892-113">The COM implementation also does not support stream transactioning or region locking.</span></span>

<span data-ttu-id="27892-114">若要根據全域記憶體建立簡單的資料流程，請呼叫 API 函數 [**CreateStreamOnHGlobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal)來取得 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)指標。</span><span class="sxs-lookup"><span data-stu-id="27892-114">To create a simple stream based on global memory, get an [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) pointer by calling the API function [**CreateStreamOnHGlobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal).</span></span> <span data-ttu-id="27892-115">若要取得複合檔案物件內的 **IStream** 指標，請呼叫 [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) 或 [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)。</span><span class="sxs-lookup"><span data-stu-id="27892-115">To get an **IStream** pointer within a compound file object, call either [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) or [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage).</span></span> <span data-ttu-id="27892-116">這些函式會 [**取出 IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)指標，您接著可以針對 **IStream** 指標呼叫 [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)或 [**OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) 。</span><span class="sxs-lookup"><span data-stu-id="27892-116">These functions retrieve an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) pointer, with which you can then call [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) or [**OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) for an **IStream** pointer.</span></span> <span data-ttu-id="27892-117">在任一種情況下，都會使用相同的 **IStream** 執行程式碼。</span><span class="sxs-lookup"><span data-stu-id="27892-117">In either case, the same **IStream** implementation code is used.</span></span>

> [!Note]  
> <span data-ttu-id="27892-118">結構化儲存區的複合檔案執行不會在 [**ISequentialStream**](/windows/desktop/api/Objidl/nn-objidl-isequentialstream)的 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))方法上成功，但它包含透過 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)介面指標的 [**讀取**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)和 [**寫入**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write)方法。</span><span class="sxs-lookup"><span data-stu-id="27892-118">The compound file implementation of structured storage does not succeed on a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method for [**ISequentialStream**](/windows/desktop/api/Objidl/nn-objidl-isequentialstream), but it includes the [**Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) and [**Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) methods through the [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) interface pointer.</span></span>

 

## <a name="when-to-use"></a><span data-ttu-id="27892-119">使用時機</span><span class="sxs-lookup"><span data-stu-id="27892-119">When to Use</span></span>

<span data-ttu-id="27892-120">呼叫 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) 的方法以讀取資料，並將資料寫入資料流程。</span><span class="sxs-lookup"><span data-stu-id="27892-120">Call the methods of [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) to read and write data to a stream.</span></span>

<span data-ttu-id="27892-121">由於資料流程物件可以封送處理至其他進程，因此應用程式可以共用儲存物件中的資料，而不需要使用全域記憶體。</span><span class="sxs-lookup"><span data-stu-id="27892-121">Because stream objects can be marshaled to other processes, applications can share the data in storage objects without having to use global memory.</span></span> <span data-ttu-id="27892-122">在資料流程物件的 COM 複合檔案執行中，當兩個進程具有共用記憶體存取權時，COM 中的自訂封送處理功能會在新的進程中建立原始物件的遠端版本。</span><span class="sxs-lookup"><span data-stu-id="27892-122">In the COM compound file implementation of stream objects, the custom marshaling facilities in COM create a remote version of the original object in the new process when the two processes have shared-memory access.</span></span> <span data-ttu-id="27892-123">因此，遠端版本不需要與原始進程通訊來執行其功能。</span><span class="sxs-lookup"><span data-stu-id="27892-123">Thus, the remote version does not need to communicate with the original process to carry out its functions.</span></span>

<span data-ttu-id="27892-124">資料流程物件的遠端版本與原始資料流程共用相同的 seek 指標。</span><span class="sxs-lookup"><span data-stu-id="27892-124">The remote version of the stream object shares the same seek pointer as the original stream.</span></span> <span data-ttu-id="27892-125">如果您不想要共用搜尋指標，請使用 [**IStream：： Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) 方法為遠端進程提供資料流程物件的複本。</span><span class="sxs-lookup"><span data-stu-id="27892-125">If you do not want to share the seek pointer, use the [**IStream::Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) method to provide a copy of the stream object for the remote process.</span></span>

> [!Note]
> <span data-ttu-id="27892-126">如果您在電腦的記憶體中建立大於堆積的資料流程物件，並使用全域記憶體物件的 **HGLOBAL** 控制碼，資料流程物件就會在內部呼叫 [**GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) 方法當它需要更多的記憶體。</span><span class="sxs-lookup"><span data-stu-id="27892-126">If creating a stream object that is larger than the heap in your computer's memory and you are using an **HGLOBAL** handle to a global memory object, the stream object calls the [**GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) method internally whe it requires more memory.</span></span> <span data-ttu-id="27892-127">由於 **GlobalRealloc** 一律會將資料從來源複製到目的地，因此將資料流程物件從 20 mb 增加至 25 mb 會需要很長的時間。</span><span class="sxs-lookup"><span data-stu-id="27892-127">Because **GlobalRealloc** always copies data from the source to the destination, increasing a stream object from 20 MB to 25 MB, for example, requires large amounts of time.</span></span> <span data-ttu-id="27892-128">這是因為複製的增量大小，如果電腦上的記憶體少於 45 MB，而且因為磁片交換，則會惡化。</span><span class="sxs-lookup"><span data-stu-id="27892-128">This is due to the size of the increments copied and is worsened if there is less than 45 MB of memory on the computer because of disk swapping.</span></span>
>
> <span data-ttu-id="27892-129">慣用的解決方法是使用 [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) （而非 [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc)）所配置的記憶體，來執行 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)方法。</span><span class="sxs-lookup"><span data-stu-id="27892-129">The preferred solution is to implement an [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) method that uses memory allocated by [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) instead of [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc).</span></span> <span data-ttu-id="27892-130">這可以保留大量的虛擬位址空間，然後視需要在該位址空間內認可記憶體。</span><span class="sxs-lookup"><span data-stu-id="27892-130">This can reserve a large chunk of virtual address space and then commit memory within that address space as required.</span></span> <span data-ttu-id="27892-131">不會進行資料複製，而且只有在需要時才會認可記憶體。</span><span class="sxs-lookup"><span data-stu-id="27892-131">No data copying occurs and memory is committed only as it is required.</span></span>
>
> <span data-ttu-id="27892-132">[**GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc)的替代方法是在資料流程物件上呼叫 [**IStream：： SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize)方法，以預先增加記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="27892-132">An alternative to [**GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) is to call the [**IStream::SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) method on the stream object to increase the memory allocation in advance.</span></span> <span data-ttu-id="27892-133">不過，這並不是像使用 [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc)一樣有效率，如上面所述。</span><span class="sxs-lookup"><span data-stu-id="27892-133">This is not, however, as efficient as using [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc), as described above.</span></span>

 

## <a name="methods"></a><span data-ttu-id="27892-134">方法</span><span class="sxs-lookup"><span data-stu-id="27892-134">Methods</span></span>

<dl> <dt>

<span data-ttu-id="27892-135"><span id="ISequentialStream__Read"></span><span id="isequentialstream__read"></span><span id="ISEQUENTIALSTREAM__READ"></span>[**ISequentialStream：： Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)</span><span class="sxs-lookup"><span data-stu-id="27892-135"><span id="ISequentialStream__Read"></span><span id="isequentialstream__read"></span><span id="ISEQUENTIALSTREAM__READ"></span>[**ISequentialStream::Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)</span></span>
</dt> <dd>

<span data-ttu-id="27892-136">從資料流物件中將指定的位元組數目讀入記憶體中目前搜尋指標開始處。</span><span class="sxs-lookup"><span data-stu-id="27892-136">Reads a specified number of bytes from the stream object into memory starting at the current seek pointer.</span></span> <span data-ttu-id="27892-137">\_如果在讀取期間到達資料流程的結尾，則此實作為「確定」。</span><span class="sxs-lookup"><span data-stu-id="27892-137">This implementation returns S\_OK if the end of the stream was reached during the read.</span></span> <span data-ttu-id="27892-138"> (這與在 MS-DOS FAT 檔案系統中找到的「檔案結尾」行為相同。 ) </span><span class="sxs-lookup"><span data-stu-id="27892-138">(This is the same as the "end of file" behavior found in the MS-DOS FAT file system.)</span></span>

</dd> <dt>

<span data-ttu-id="27892-139"><span id="ISequentialStream__Write"></span><span id="isequentialstream__write"></span><span id="ISEQUENTIALSTREAM__WRITE"></span>[**ISequentialStream：： Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write)</span><span class="sxs-lookup"><span data-stu-id="27892-139"><span id="ISequentialStream__Write"></span><span id="isequentialstream__write"></span><span id="ISEQUENTIALSTREAM__WRITE"></span>[**ISequentialStream::Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write)</span></span>
</dt> <dd>

<span data-ttu-id="27892-140">從目前的 seek 指標開始，將指定的數位從位元組寫入資料流程物件。</span><span class="sxs-lookup"><span data-stu-id="27892-140">Writes a specified number from bytes into the stream object starting at the current seek pointer.</span></span> <span data-ttu-id="27892-141">在這個執行中，資料流程物件不是稀疏的。</span><span class="sxs-lookup"><span data-stu-id="27892-141">In this implementation, stream objects are not sparse.</span></span> <span data-ttu-id="27892-142">任何填滿的位元組最後都會配置在磁片上，並指派給串流。</span><span class="sxs-lookup"><span data-stu-id="27892-142">Any fill bytes are eventually allocated on the disk and assigned to the stream.</span></span>

</dd> <dt>

<span data-ttu-id="27892-143"><span id="IStream__Seek"></span><span id="istream__seek"></span><span id="ISTREAM__SEEK"></span>[**IStream：： Seek**](/windows/desktop/api/Objidl/nf-objidl-istream-seek)</span><span class="sxs-lookup"><span data-stu-id="27892-143"><span id="IStream__Seek"></span><span id="istream__seek"></span><span id="ISTREAM__SEEK"></span>[**IStream::Seek**](/windows/desktop/api/Objidl/nf-objidl-istream-seek)</span></span>
</dt> <dd>

<span data-ttu-id="27892-144">將搜尋指標變更為相對於資料流開頭、資料流結尾或目前搜尋指標的新位置。</span><span class="sxs-lookup"><span data-stu-id="27892-144">Changes the seek pointer to a new location relative to the beginning of the stream, to the end of the stream, or to the current seek pointer.</span></span>

</dd> <dt>

<span data-ttu-id="27892-145"><span id="IStream__SetSize"></span><span id="istream__setsize"></span><span id="ISTREAM__SETSIZE"></span>[**IStream：： SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize)</span><span class="sxs-lookup"><span data-stu-id="27892-145"><span id="IStream__SetSize"></span><span id="istream__setsize"></span><span id="ISTREAM__SETSIZE"></span>[**IStream::SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize)</span></span>
</dt> <dd>

<span data-ttu-id="27892-146">變更資料流物件的大小。</span><span class="sxs-lookup"><span data-stu-id="27892-146">Changes the size of the stream object.</span></span> <span data-ttu-id="27892-147">在這種情況下，並不保證配置的空間將會是連續的。</span><span class="sxs-lookup"><span data-stu-id="27892-147">In this implementation, there is no guarantee that the space allocated will be contiguous.</span></span>

</dd> <dt>

<span data-ttu-id="27892-148"><span id="IStream__CopyTo"></span><span id="istream__copyto"></span><span id="ISTREAM__COPYTO"></span>[**IStream：： CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto)</span><span class="sxs-lookup"><span data-stu-id="27892-148"><span id="IStream__CopyTo"></span><span id="istream__copyto"></span><span id="ISTREAM__COPYTO"></span>[**IStream::CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto)</span></span>
</dt> <dd>

<span data-ttu-id="27892-149">從資料流中目前的搜尋指標將指定的位元組數目複製到另一個資料流中目前的搜尋指標。</span><span class="sxs-lookup"><span data-stu-id="27892-149">Copies a specified number of bytes from the current seek pointer in the stream to the current seek pointer in another stream.</span></span>

</dd> <dt>

<span data-ttu-id="27892-150"><span id="IStream__Commit"></span><span id="istream__commit"></span><span id="ISTREAM__COMMIT"></span>[**IStream：： Commit**](/windows/desktop/api/Objidl/nf-objidl-istream-commit)</span><span class="sxs-lookup"><span data-stu-id="27892-150"><span id="IStream__Commit"></span><span id="istream__commit"></span><span id="ISTREAM__COMMIT"></span>[**IStream::Commit**](/windows/desktop/api/Objidl/nf-objidl-istream-commit)</span></span>
</dt> <dd>

<span data-ttu-id="27892-151">[**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)的複合檔案執行僅支援在直接模式下開啟資料流程，而不支援交易模式。</span><span class="sxs-lookup"><span data-stu-id="27892-151">The compound file implementation of [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) supports opening streams only in direct mode, not transacted mode.</span></span> <span data-ttu-id="27892-152">因此，除了將所有記憶體緩衝區排清至下一個儲存層級以外，方法不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="27892-152">Therefore, the method has no effect when called other than to flush all memory buffers to the next storage level.</span></span>

<span data-ttu-id="27892-153">在這種情況下，如果您將變更認可至資料流程，就不需要認可儲存物件的變更。</span><span class="sxs-lookup"><span data-stu-id="27892-153">In this implementation, it does not matter if you commit changes to streams, you need only commit changes for storage objects.</span></span>

</dd> <dt>

<span data-ttu-id="27892-154"><span id="IStream__Revert"></span><span id="istream__revert"></span><span id="ISTREAM__REVERT"></span>[**IStream：： Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert)</span><span class="sxs-lookup"><span data-stu-id="27892-154"><span id="IStream__Revert"></span><span id="istream__revert"></span><span id="ISTREAM__REVERT"></span>[**IStream::Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert)</span></span>
</dt> <dd>

<span data-ttu-id="27892-155">此執行不支援交易資料流程，因此呼叫這個方法不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="27892-155">This implementation does not support transacted streams, so a call to this method has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="27892-156"><span id="IStream__LockRegion"></span><span id="istream__lockregion"></span><span id="ISTREAM__LOCKREGION"></span>[**IStream：： LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion)</span><span class="sxs-lookup"><span data-stu-id="27892-156"><span id="IStream__LockRegion"></span><span id="istream__lockregion"></span><span id="ISTREAM__LOCKREGION"></span>[**IStream::LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion)</span></span>
</dt> <dd>

<span data-ttu-id="27892-157">此執行不支援範圍鎖定，因此呼叫這個方法不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="27892-157">Range-locking is not supported by this implementation, so a call to this method has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="27892-158"><span id="IStream__UnlockRegion"></span><span id="istream__unlockregion"></span><span id="ISTREAM__UNLOCKREGION"></span>[**IStream：： UnlockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-unlockregion)</span><span class="sxs-lookup"><span data-stu-id="27892-158"><span id="IStream__UnlockRegion"></span><span id="istream__unlockregion"></span><span id="ISTREAM__UNLOCKREGION"></span>[**IStream::UnlockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-unlockregion)</span></span>
</dt> <dd>

<span data-ttu-id="27892-159">移除先前以 [**IStream：： LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion)限制之位元組範圍的存取限制。</span><span class="sxs-lookup"><span data-stu-id="27892-159">Removes the access restriction on a range of bytes previously restricted with [**IStream::LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion).</span></span>

</dd> <dt>

<span data-ttu-id="27892-160"><span id="IStream__Stat"></span><span id="istream__stat"></span><span id="ISTREAM__STAT"></span>[**IStream：： Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)</span><span class="sxs-lookup"><span data-stu-id="27892-160"><span id="IStream__Stat"></span><span id="istream__stat"></span><span id="ISTREAM__STAT"></span>[**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)</span></span>
</dt> <dd>

<span data-ttu-id="27892-161">抓取此資料流程的 [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) 結構</span><span class="sxs-lookup"><span data-stu-id="27892-161">Retrieves the [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) structure for this stream</span></span>

</dd> <dt>

<span data-ttu-id="27892-162"><span id="IStream__Clone"></span><span id="istream__clone"></span><span id="ISTREAM__CLONE"></span>[**IStream：： Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone)</span><span class="sxs-lookup"><span data-stu-id="27892-162"><span id="IStream__Clone"></span><span id="istream__clone"></span><span id="ISTREAM__CLONE"></span>[**IStream::Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone)</span></span>
</dt> <dd>

<span data-ttu-id="27892-163">建立新的資料流物件，其搜尋指標會參考與原始資料流相同的位元組。</span><span class="sxs-lookup"><span data-stu-id="27892-163">Creates a new stream object with its own seek pointer that references the same bytes as the original stream.</span></span>

</dd> </dl>

<span data-ttu-id="27892-164">簡單模式的 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) 受限於下列條件約束。</span><span class="sxs-lookup"><span data-stu-id="27892-164">A simple-mode [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) is subject to the following constraints.</span></span>

-   <span data-ttu-id="27892-165">如果資料流程是在簡單模式的儲存體中建立或開啟，則為簡單模式。</span><span class="sxs-lookup"><span data-stu-id="27892-165">A stream is simple mode if it was created or opened from a simple-mode storage.</span></span> <span data-ttu-id="27892-166">如果使用 \_ *grfMode* 參數中所設定的 STGM simple 旗標來建立或開啟儲存體，則儲存體是簡單模式。</span><span class="sxs-lookup"><span data-stu-id="27892-166">A storage is simple mode if it is created or opened with the STGM\_SIMPLE flag set in the *grfMode* parameter.</span></span>
-   <span data-ttu-id="27892-167">不支援 [**複製**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) 和 [**CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto) 方法。</span><span class="sxs-lookup"><span data-stu-id="27892-167">The [**Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) and [**CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto) methods are not supported.</span></span>
-   <span data-ttu-id="27892-168">支援 [**Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) 方法，但 \_ 必須指定 STATFLAG NONAME 值。</span><span class="sxs-lookup"><span data-stu-id="27892-168">The [**Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) method is supported, but the STATFLAG\_NONAME value must be specified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27892-169">相關主題</span><span class="sxs-lookup"><span data-stu-id="27892-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27892-170">**IStream**</span><span class="sxs-lookup"><span data-stu-id="27892-170">**IStream**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> <dt>

[<span data-ttu-id="27892-171">**IStorage**</span><span class="sxs-lookup"><span data-stu-id="27892-171">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[<span data-ttu-id="27892-172">**CreateStreamOnHGlobal**</span><span class="sxs-lookup"><span data-stu-id="27892-172">**CreateStreamOnHGlobal**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal)
</dt> <dt>

[<span data-ttu-id="27892-173">**StgCreateDocfile**</span><span class="sxs-lookup"><span data-stu-id="27892-173">**StgCreateDocfile**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[<span data-ttu-id="27892-174">**StgOpenStorage**</span><span class="sxs-lookup"><span data-stu-id="27892-174">**StgOpenStorage**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> </dl>

 

 