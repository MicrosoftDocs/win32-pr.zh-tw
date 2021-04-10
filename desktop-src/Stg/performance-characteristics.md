---
title: 效能特色
description: 呼叫 IPropertySetStorage 介面的 COM 複合檔案執行以建立屬性集，會導致透過呼叫 IStorage CreateStream 或 IStorage CreateStorage 來建立資料流程或儲存體。
ms.assetid: 7773e649-19a4-4df2-84ed-027d73283140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8597862602a367ed93a3d6e5e0bcac76035c337a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933389"
---
# <a name="performance-characteristics"></a><span data-ttu-id="0380f-103">效能特色</span><span class="sxs-lookup"><span data-stu-id="0380f-103">Performance Characteristics</span></span>

<span data-ttu-id="0380f-104">呼叫 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 介面的 COM 複合檔案執行以建立屬性集，會導致透過呼叫 [**IStorage：： CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) 或 [**IStorage：： CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage)來建立資料流程或儲存體。</span><span class="sxs-lookup"><span data-stu-id="0380f-104">A call to the COM compound file implementation of the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interface to create a property set causes either a stream or storage to be created through a call to [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) or [**IStorage::CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage).</span></span> <span data-ttu-id="0380f-105">預設屬性集是在記憶體中建立的，但不會排清到磁片。</span><span class="sxs-lookup"><span data-stu-id="0380f-105">A default property set is created in memory, but not flushed to disk.</span></span> <span data-ttu-id="0380f-106">當呼叫 [**IPropertyStorage：： WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)時，它會在緩衝區內運作。</span><span class="sxs-lookup"><span data-stu-id="0380f-106">When there is a call to [**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple), it operates within the buffer.</span></span>

<span data-ttu-id="0380f-107">當屬性集開啟時，就會使用 [IStorage：： OpenStream](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) 或 [IStorage：： OpenStorage](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) 。</span><span class="sxs-lookup"><span data-stu-id="0380f-107">When a property set is opened, [IStorage::OpenStream](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) or [IStorage::OpenStorage](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) is used.</span></span> <span data-ttu-id="0380f-108">整個屬性集資料流程會讀入連續的記憶體中。</span><span class="sxs-lookup"><span data-stu-id="0380f-108">The entire property set stream is read into contiguous memory.</span></span> <span data-ttu-id="0380f-109">[**IPropertyStorage：： ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) 作業接著會讀取記憶體緩衝區來操作。</span><span class="sxs-lookup"><span data-stu-id="0380f-109">[**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) operations then operate by reading the memory buffer.</span></span> <span data-ttu-id="0380f-110">因此，第一次存取的時間很昂貴 (因為磁片讀取) 但後續的存取非常有效率。</span><span class="sxs-lookup"><span data-stu-id="0380f-110">Therefore, the first access is expensive in terms of time (because of disk reads) but subsequent accesses are very efficient.</span></span> <span data-ttu-id="0380f-111">寫入可能會稍微昂貴，因為在新增資料時，可能需要基礎資料流程上的 SetSize 作業，以保證磁碟空間可供使用。</span><span class="sxs-lookup"><span data-stu-id="0380f-111">Writes may be slightly more expensive because SetSize operations on the underlying stream may be required to guarantee that disk space is available if data is added.</span></span>

<span data-ttu-id="0380f-112">無論 [**IPropertyStorage：： WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) 是否會排清更新，都不會做出任何保證。</span><span class="sxs-lookup"><span data-stu-id="0380f-112">No guarantees are made as to whether [**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) will flush updates.</span></span> <span data-ttu-id="0380f-113">一般而言，用戶端應該假設 **IPropertyStorage：： WriteMultiple** 只會更新記憶體緩衝區中的。</span><span class="sxs-lookup"><span data-stu-id="0380f-113">In general, the client should assume that **IPropertyStorage::WriteMultiple** only updates the in memory buffer.</span></span> <span data-ttu-id="0380f-114">若要排清資料，應該呼叫 [**IPropertyStorage：： Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) 或 [**IUnknown：： Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) (上一個發行) 。</span><span class="sxs-lookup"><span data-stu-id="0380f-114">To flush data, [**IPropertyStorage::Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) or [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) (last release) should be called.</span></span>

<span data-ttu-id="0380f-115">此設計表示 [**WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) 可能會成功，但不會實際持續寫入資料。</span><span class="sxs-lookup"><span data-stu-id="0380f-115">This design means that [**WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) may succeed but the data is not actually persistently written.</span></span>

> [!Note]  
> <span data-ttu-id="0380f-116">這個屬性集資料流程的大小不能超過256K 個位元組。</span><span class="sxs-lookup"><span data-stu-id="0380f-116">This size of the property set stream cannot exceed 256K bytes.</span></span>

 

 

 