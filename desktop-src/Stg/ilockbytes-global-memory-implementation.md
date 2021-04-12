---
title: ILockBytes-全域記憶體執行
description: ILockBytes global memory 實作為 COM 複合檔案儲存物件基礎的位元組陣列物件，並設計為可直接讀取和寫入全域記憶體。
ms.assetid: 6ab019b0-34d7-4b6e-ba77-6b6881fabd29
keywords:
- ILockBytes Strctd Stg.、、global memory
- ILockBytes Strctd Stg.，實施
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9d7cae82c1503fcb53d2cfd8fee39095eb60801
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300311"
---
# <a name="ilockbytes---global-memory-implementation"></a><span data-ttu-id="82130-105">ILockBytes-全域記憶體執行</span><span class="sxs-lookup"><span data-stu-id="82130-105">ILockBytes - Global Memory Implementation</span></span>

<span data-ttu-id="82130-106">ILockBytes global memory 實作為 COM 複合檔案儲存物件基礎的位元組陣列物件，並設計為可直接讀取和寫入全域記憶體。</span><span class="sxs-lookup"><span data-stu-id="82130-106">The ILockBytes global memory implementation is implemented on a byte array object underlying a COM compound file storage object, and designed to read and write directly to global memory.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="82130-107">使用時機</span><span class="sxs-lookup"><span data-stu-id="82130-107">When to Use</span></span>

<span data-ttu-id="82130-108">[**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)的方法是從透過呼叫 [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)所建立的複合檔案儲存物件上， [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)和 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)的複合檔案執行所呼叫。</span><span class="sxs-lookup"><span data-stu-id="82130-108">Methods of [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) are called from the compound file implementations of [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) and [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) on the compound file storage object created through a call to [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile).</span></span>

## <a name="remarks"></a><span data-ttu-id="82130-109">備註</span><span class="sxs-lookup"><span data-stu-id="82130-109">Remarks</span></span>

<span data-ttu-id="82130-110">以下是 [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) Global Memory 執行的方法。</span><span class="sxs-lookup"><span data-stu-id="82130-110">The following are the methods of the [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) Global Memory Implementation.</span></span>

<dl> <dt>

<span data-ttu-id="82130-111"><span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes：： ReadAt**</span><span class="sxs-lookup"><span data-stu-id="82130-111"><span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes::ReadAt**</span></span>
</dt> <dd>

<span data-ttu-id="82130-112">從位元組陣列開頭的指定位移讀取位元組區塊。</span><span class="sxs-lookup"><span data-stu-id="82130-112">Reads a block of bytes from a specified offset at the beginning of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="82130-113"><span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes：： WriteAt**</span><span class="sxs-lookup"><span data-stu-id="82130-113"><span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes::WriteAt**</span></span>
</dt> <dd>

<span data-ttu-id="82130-114">從位元組陣列開頭的指定位移寫入位元組區塊。</span><span class="sxs-lookup"><span data-stu-id="82130-114">Writes the block of bytes from a specified offset at the beginning of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="82130-115"><span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes：： Flush**</span><span class="sxs-lookup"><span data-stu-id="82130-115"><span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes::Flush**</span></span>
</dt> <dd>

<span data-ttu-id="82130-116">不同于以檔案為基礎的執行，在全域記憶體執行中呼叫這個方法沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="82130-116">Unlike file-based implementation, calling this method in global memory implementation has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="82130-117"><span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes：： SetSize**</span><span class="sxs-lookup"><span data-stu-id="82130-117"><span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes::SetSize**</span></span>
</dt> <dd>

<span data-ttu-id="82130-118">設定位元組陣列的大小。</span><span class="sxs-lookup"><span data-stu-id="82130-118">Sets the size of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="82130-119"><span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes：： LockRegion**</span><span class="sxs-lookup"><span data-stu-id="82130-119"><span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes::LockRegion**</span></span>
</dt> <dd>

<span data-ttu-id="82130-120">這項執行不支援鎖定，所以 *dwLocksType* 會設定為零。</span><span class="sxs-lookup"><span data-stu-id="82130-120">This implementation does not support locking, so *dwLocksType* is set to zero.</span></span> <span data-ttu-id="82130-121">呼叫端必須確定存取有效且互斥。</span><span class="sxs-lookup"><span data-stu-id="82130-121">The caller must ensure accesses are valid and mutually exclusive.</span></span>

</dd> <dt>

<span data-ttu-id="82130-122"><span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes：： UnlockRegion**</span><span class="sxs-lookup"><span data-stu-id="82130-122"><span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes::UnlockRegion**</span></span>
</dt> <dd>

<span data-ttu-id="82130-123">這種執行不支援鎖定。</span><span class="sxs-lookup"><span data-stu-id="82130-123">This implementation does not support locking.</span></span>

</dd> <dt>

<span data-ttu-id="82130-124"><span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes：： Stat**</span><span class="sxs-lookup"><span data-stu-id="82130-124"><span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes::Stat**</span></span>
</dt> <dd>

<span data-ttu-id="82130-125">COM 提供的 [**IStorage：： stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) 實，會呼叫 [**ILockBytes：： stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) 方法來取出位元組陣列物件的相關資料。</span><span class="sxs-lookup"><span data-stu-id="82130-125">The COM-provided [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) implementation calls the [**ILockBytes::Stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) method to retrieve data about the byte array object.</span></span> <span data-ttu-id="82130-126">如果位元組陣列沒有合理的名稱，則 COM 提供的 **ILockBytes：： Stat** 方法會在 [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg)結構的 **pwcsName** 成員中傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="82130-126">If there is no reasonable name for the byte array, the COM-provided **ILockBytes::Stat** method returns **NULL** in the **pwcsName** member of the [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) structure.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="82130-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="82130-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82130-128">**ILockBytes**</span><span class="sxs-lookup"><span data-stu-id="82130-128">**ILockBytes**</span></span>](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[<span data-ttu-id="82130-129">**IStorage**</span><span class="sxs-lookup"><span data-stu-id="82130-129">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[<span data-ttu-id="82130-130">**IStream**</span><span class="sxs-lookup"><span data-stu-id="82130-130">**IStream**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> </dl>

 

 




