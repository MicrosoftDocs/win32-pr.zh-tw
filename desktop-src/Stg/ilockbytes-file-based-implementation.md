---
title: ILockBytes-File-Based 執行
description: 在 COM 複合檔案儲存物件基礎的位元組陣列物件上執行，並設計成直接讀取和寫入磁片檔案。
ms.assetid: 700b6a3c-1046-4c21-8887-16f344c23510
keywords:
- ILockBytes Strctd Stg.，以檔案為基礎
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93dfe09ab0157d2d24d81b7bb2798e984d3848f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371937"
---
# <a name="ilockbytes---file-based-implementation"></a><span data-ttu-id="b849d-104">ILockBytes-File-Based 執行</span><span class="sxs-lookup"><span data-stu-id="b849d-104">ILockBytes - File-Based Implementation</span></span>

<span data-ttu-id="b849d-105">在 COM 複合檔案儲存物件基礎的位元組陣列物件上執行，並設計成直接讀取和寫入磁片檔案。</span><span class="sxs-lookup"><span data-stu-id="b849d-105">Implemented on a byte array object underlying a COM compound file storage object, and designed to read and write directly to a disk file.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="b849d-106">使用時機</span><span class="sxs-lookup"><span data-stu-id="b849d-106">When to Use</span></span>

<span data-ttu-id="b849d-107">[**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)的方法是從透過呼叫 [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)所建立的複合檔案儲存物件上 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)和 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)的複合檔案執行所呼叫，因此您不需要直接呼叫它們。</span><span class="sxs-lookup"><span data-stu-id="b849d-107">Methods of [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) are called from the compound file implementations of [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) and [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) on the compound file storage object created through a call to [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), so you do not need to call them directly.</span></span>

## <a name="remarks"></a><span data-ttu-id="b849d-108">備註</span><span class="sxs-lookup"><span data-stu-id="b849d-108">Remarks</span></span>

<span data-ttu-id="b849d-109">以下是 [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) File-Based 執行的方法。</span><span class="sxs-lookup"><span data-stu-id="b849d-109">The following are the methods of the [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) File-Based Implementation.</span></span>

<dl> <dt>

<span data-ttu-id="b849d-110"><span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes：： ReadAt**</span><span class="sxs-lookup"><span data-stu-id="b849d-110"><span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes::ReadAt**</span></span>
</dt> <dd>

<span data-ttu-id="b849d-111">從位元組陣列開頭的指定位移讀取位元組區塊。</span><span class="sxs-lookup"><span data-stu-id="b849d-111">Reads a block of bytes from a specified offset at the beginning of the byte-array.</span></span>

</dd> <dt>

<span data-ttu-id="b849d-112"><span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes：： WriteAt**</span><span class="sxs-lookup"><span data-stu-id="b849d-112"><span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes::WriteAt**</span></span>
</dt> <dd>

<span data-ttu-id="b849d-113">從位元組陣列開頭的指定位移寫入位元組區塊。</span><span class="sxs-lookup"><span data-stu-id="b849d-113">Writes a block of bytes from a specified offset at the beginning of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="b849d-114"><span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes：： Flush**</span><span class="sxs-lookup"><span data-stu-id="b849d-114"><span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes::Flush**</span></span>
</dt> <dd>

<span data-ttu-id="b849d-115">確保 [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) 執行所維護的任何內部緩衝區都會寫出到基礎實體儲存體。</span><span class="sxs-lookup"><span data-stu-id="b849d-115">Ensures that any internal buffers maintained by the [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) implementation are written out to the underlying physical storage.</span></span>

</dd> <dt>

<span data-ttu-id="b849d-116"><span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes：： SetSize**</span><span class="sxs-lookup"><span data-stu-id="b849d-116"><span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes::SetSize**</span></span>
</dt> <dd>

<span data-ttu-id="b849d-117">設定位元組陣列的大小。</span><span class="sxs-lookup"><span data-stu-id="b849d-117">Sets the size of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="b849d-118"><span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes：： LockRegion**</span><span class="sxs-lookup"><span data-stu-id="b849d-118"><span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes::LockRegion**</span></span>
</dt> <dd>

<span data-ttu-id="b849d-119">*DwLockTypes* 參數設定為 lock \_ ONLYONCE 或 \_ 獨佔鎖定，可允許或限制對鎖定區域的存取。</span><span class="sxs-lookup"><span data-stu-id="b849d-119">The *dwLockTypes* parameter is set to LOCK\_ONLYONCE or LOCK\_EXCLUSIVE, which will allow or restrict access to locked regions.</span></span>

</dd> <dt>

<span data-ttu-id="b849d-120"><span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes：： UnlockRegion**</span><span class="sxs-lookup"><span data-stu-id="b849d-120"><span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes::UnlockRegion**</span></span>
</dt> <dd>

<span data-ttu-id="b849d-121">這個方法會將 [**ILockBytes：： LockRegion**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-lockregion)鎖定的區域解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="b849d-121">This method unlocks the region locked by [**ILockBytes::LockRegion**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-lockregion).</span></span>

</dd> <dt>

<span data-ttu-id="b849d-122"><span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes：： Stat**</span><span class="sxs-lookup"><span data-stu-id="b849d-122"><span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes::Stat**</span></span>
</dt> <dd>

<span data-ttu-id="b849d-123">COM 提供的 [**IStorage：： stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) 實，會呼叫 [**ILockBytes：： stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) 方法，以取得位元組陣列物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b849d-123">The COM-provided [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) implementation calls the [**ILockBytes::Stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) method to retrieve information about the byte array object.</span></span> <span data-ttu-id="b849d-124">如果位元組陣列沒有合理的名稱，則 COM 提供的 **ILockBytes：： Stat** 方法會在 [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg)結構的 **pwcsName** 成員中傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="b849d-124">If there is no reasonable name for the byte array, the COM-provided **ILockBytes::Stat** method returns **NULL** in the **pwcsName** member of the [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) structure.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="b849d-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="b849d-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b849d-126">**ILockBytes**</span><span class="sxs-lookup"><span data-stu-id="b849d-126">**ILockBytes**</span></span>](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[<span data-ttu-id="b849d-127">**IStorage**</span><span class="sxs-lookup"><span data-stu-id="b849d-127">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[<span data-ttu-id="b849d-128">**IStream**</span><span class="sxs-lookup"><span data-stu-id="b849d-128">**IStream**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> </dl>

 

 




