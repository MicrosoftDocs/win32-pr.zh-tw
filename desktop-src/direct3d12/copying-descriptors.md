---
title: 複製描述項
description: 裝置介面上的 ID3D12Device CopyDescriptors 和 ID3D12Device CopyDescriptorsSimple 方法會使用 CPU 來立即複製描述項。
ms.assetid: 65AE4D96-6221-46B5-BF55-F86479FCF97C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14fdec6c76f29800f2a0e42bde76b32ebc794275
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104125"
---
# <a name="copying-descriptors"></a><span data-ttu-id="23fdf-103">複製描述項</span><span class="sxs-lookup"><span data-stu-id="23fdf-103">Copying Descriptors</span></span>

<span data-ttu-id="23fdf-104">裝置介面上的 [**ID3D12Device：： CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) 和 [**ID3D12Device：： CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) 方法會使用 CPU 來立即複製描述項。</span><span class="sxs-lookup"><span data-stu-id="23fdf-104">The [**ID3D12Device::CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) and [**ID3D12Device::CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) methods on the device interface use the CPU to immediately copy descriptors.</span></span> <span data-ttu-id="23fdf-105">只要 CPU 或 GPU 上的多個執行緒不會執行任何可能衝突的寫入，就可以將它們稱為「自由執行緒」。</span><span class="sxs-lookup"><span data-stu-id="23fdf-105">They can be called free threaded as long as multiple threads on the CPU or GPU do not perform any potentially conflicting writes.</span></span>

## <a name="copying-descriptors-immediately-cpu-timeline"></a><span data-ttu-id="23fdf-106">立即複製描述項 (CPU 時間軸) </span><span class="sxs-lookup"><span data-stu-id="23fdf-106">Copying Descriptors Immediately (CPU Timeline)</span></span>

<span data-ttu-id="23fdf-107"> (從) 複製的來源描述項數目（指定為一組描述項範圍）必須等於要複製到) 的目的地 (描述項數目（指定為一組個別的描述項範圍）。</span><span class="sxs-lookup"><span data-stu-id="23fdf-107">The number of source descriptors (to copy from), specified as a set of descriptor ranges, must equal the number of destination descriptors (to copy to), specified as a separate set of descriptor ranges.</span></span> <span data-ttu-id="23fdf-108">來源和目的範圍也不需要行出。</span><span class="sxs-lookup"><span data-stu-id="23fdf-108">The source and destination ranges do not otherwise have to line up.</span></span> <span data-ttu-id="23fdf-109">例如，您可以將一組稀疏的描述項複製到連續的目的地，反之亦然，或是某種組合。</span><span class="sxs-lookup"><span data-stu-id="23fdf-109">For example, a sparse set of descriptors could be copied to a contiguous destination, vice versa, or in some combination.</span></span>

<span data-ttu-id="23fdf-110">複製作業可包含多個描述元堆積，兩者皆為來源和目的地。</span><span class="sxs-lookup"><span data-stu-id="23fdf-110">Multiple descriptor heaps can be involved in the copy operation, both as source and destination.</span></span> <span data-ttu-id="23fdf-111">使用描述項控制碼作為參數，表示複製方法不在意任何指定之描述項所在的堆積–它們都只是記憶體。</span><span class="sxs-lookup"><span data-stu-id="23fdf-111">The use of descriptor handles as parameters means the copy methods don’t care about which heaps any given descriptor lies in – they are all just memory.</span></span>

<span data-ttu-id="23fdf-112">要從中複製或的描述元堆積類型必須相符，因此方法會採用單一描述元堆積類型做為輸入。</span><span class="sxs-lookup"><span data-stu-id="23fdf-112">The descriptor heap types being copied from and to must match, so the methods take a single descriptor heap type as input.</span></span> <span data-ttu-id="23fdf-113">驅動程式必須知道指定複製作業中所有描述項的堆積類型，因此它知道複製作業中牽涉到的資料大小。</span><span class="sxs-lookup"><span data-stu-id="23fdf-113">The driver needs to know the heap type of all the descriptors in the given copy operation, so it knows what size of data is involved in the copy operation.</span></span> <span data-ttu-id="23fdf-114">如果指定的描述項堆積類型需要，驅動程式也可能需要執行自訂複製工作，這是一個實作為的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="23fdf-114">The driver might also need to do custom copying work if a given descriptor heap type warrants it – an implementation detail.</span></span> <span data-ttu-id="23fdf-115">請注意，描述項本身不會識別它們所指向的類型;因此，複製作業需要額外的參數。</span><span class="sxs-lookup"><span data-stu-id="23fdf-115">Note that descriptor handles themselves do not otherwise identify what type they are pointing to; therefore, an additional parameter is required for the copy operation.</span></span>

<span data-ttu-id="23fdf-116">針對將單一範圍的描述項從一個位置複製到另一個位置（ [**CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple)）的簡單案例，提供 [**COPYDESCRIPTORS**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors)的替代 API。</span><span class="sxs-lookup"><span data-stu-id="23fdf-116">An alternative API to [**CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) is provided for the simple case of copying a single range of descriptors from one location to another – [**CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple).</span></span>

<span data-ttu-id="23fdf-117">針對這些以裝置為基礎的 (CPU 時間軸) 描述項複製方法，來源描述項必須來自非著色器可見的描述元堆積。</span><span class="sxs-lookup"><span data-stu-id="23fdf-117">For these device based (CPU timeline) descriptor copy methods, source descriptors must come from a non-shader visible descriptor heap.</span></span> <span data-ttu-id="23fdf-118">目的地描述項可以位於任何可顯示 CPU (著色器可見或未) 的描述元堆積中。</span><span class="sxs-lookup"><span data-stu-id="23fdf-118">The destination descriptors can be in any descriptor heap that is CPU visible (shader visible or not).</span></span>

## <a name="related-topics"></a><span data-ttu-id="23fdf-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="23fdf-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23fdf-120">描述項</span><span class="sxs-lookup"><span data-stu-id="23fdf-120">Descriptors</span></span>](descriptors.md)
</dt> </dl>

 

 




