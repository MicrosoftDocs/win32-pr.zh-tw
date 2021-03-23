---
title: 著色器可見的描述元堆積
description: 著色器可見的描述元堆積是可透過描述中繼資料表來參考著色器的描述元堆積。
ms.assetid: 37691fd1-212d-4786-ac9c-861c1a6a4918
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e650d324f0826e00d8ffff08348597112f6d5cc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104609"
---
# <a name="shader-visible-descriptor-heaps"></a><span data-ttu-id="69cef-103">著色器可見的描述元堆積</span><span class="sxs-lookup"><span data-stu-id="69cef-103">Shader Visible Descriptor Heaps</span></span>

<span data-ttu-id="69cef-104">著色器可見的描述元堆積是可透過描述中繼資料表來參考著色器的描述元堆積。</span><span class="sxs-lookup"><span data-stu-id="69cef-104">Shader visible descriptor heaps, are descriptor heaps that can be referenced by shaders through descriptor tables.</span></span>

-   [<span data-ttu-id="69cef-105">概觀</span><span class="sxs-lookup"><span data-stu-id="69cef-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="69cef-106">範例</span><span class="sxs-lookup"><span data-stu-id="69cef-106">An example</span></span>](#an-example)
-   [<span data-ttu-id="69cef-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="69cef-107">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="69cef-108">概觀</span><span class="sxs-lookup"><span data-stu-id="69cef-108">Overview</span></span>

<span data-ttu-id="69cef-109">著色器可透過描述項資料表參考的描述元堆積有幾個類別：一個堆積類型、D3D12 \_ SRV \_ UAV \_ CBV 描述元 \_ \_ 堆積、可以保留著色器資源檢視、未排序的存取權，以及常數緩衝區的觀點。</span><span class="sxs-lookup"><span data-stu-id="69cef-109">Descriptor heaps that can be referenced by shaders through descriptor tables come in a couple of flavors: One heap type, D3D12\_SRV\_UAV\_CBV\_DESCRIPTOR\_HEAP, can hold Shader Resource Views, Unordered Access Views, and Constant Buffer Views, all intermixed.</span></span> <span data-ttu-id="69cef-110">堆積中的任何指定位置都可以是任何一種列出的描述項類型。</span><span class="sxs-lookup"><span data-stu-id="69cef-110">Any given location in the heap can be any one of the listed types of descriptors.</span></span> <span data-ttu-id="69cef-111">另一種堆積型別 D3D12 \_ 描述元 \_ 堆積 \_ 型別取樣器 \_ ，只會儲存取樣器，反映大部分硬體的情況，取樣器會與 SRVs、UAVs、CBVs 分開管理。</span><span class="sxs-lookup"><span data-stu-id="69cef-111">Another heap type, D3D12\_DESCRIPTOR\_HEAP\_TYPE\_SAMPLER, only stores samplers, reflecting the fact that for the majority of hardware, samplers are managed separately from SRVs, UAVs, CBVs.</span></span>

<span data-ttu-id="69cef-112">當堆積建立 (後者（非著色器可見）時，這些類型的描述元堆積可能會被要求為著色器，對於 CPU) 上的預備描述項而言很有用。</span><span class="sxs-lookup"><span data-stu-id="69cef-112">Descriptor heaps of these types may be requested to be shader visible or not when the heap is created (the latter – non shader visible - can be useful for staging descriptors on the CPU).</span></span> <span data-ttu-id="69cef-113">當要求顯示著色器時，上述每個堆積類型可能會有任何個別描述元堆積配置的硬體大小限制。</span><span class="sxs-lookup"><span data-stu-id="69cef-113">When requested to be shader visible, each of the above heap types may have a hardware size limit for any individual descriptor heap allocation.</span></span>

<span data-ttu-id="69cef-114">應用程式可以建立任意數目的描述元堆積，而非著色器可見的描述元堆積不會受到大小限制。</span><span class="sxs-lookup"><span data-stu-id="69cef-114">Applications can create any number of descriptor heaps , and non shader visible descriptor heaps are not constrained in size.</span></span> <span data-ttu-id="69cef-115">如果應用程式所建立的著色器可見描述元堆積小於硬體大小限制，驅動程式可能會選擇從較大的基礎描述項堆積中將描述項堆積子配置出來，讓多個 API 描述元堆積符合一個硬體描述元堆積。</span><span class="sxs-lookup"><span data-stu-id="69cef-115">If a shader visible descriptor heap that is created by the application is smaller than the hardware size limit, the driver may choose to sub-allocate the descriptor heap out of a larger underlying descriptor heap so that multiple API descriptor heaps fit within one hardware descriptor heap.</span></span> <span data-ttu-id="69cef-116">發生這種情況的原因是在某些硬體上，在執行期間于硬體描述項堆積之間切換需要 GPU 等候閒置 (，以確保) 之前的描述項堆積的 GPU 參考已完成。</span><span class="sxs-lookup"><span data-stu-id="69cef-116">The reason this may happen is that for some hardware, switching between hardware descriptor heaps during execution requires a GPU wait for idle (to ensure that GPU references to the previously descriptor heap are finished).</span></span> <span data-ttu-id="69cef-117">如果應用程式所建立的所有描述元堆積都符合適用硬體堆積的最大容量，則在轉譯期間切換 API 描述元堆積時，將不會發生這類等候。</span><span class="sxs-lookup"><span data-stu-id="69cef-117">If all of the descriptor heaps that an application creates fit into the applicable hardware heap's maximum capacities, then no such waits will occur when switching API descriptor heaps during rendering.</span></span> <span data-ttu-id="69cef-118">但是，應用程式必須能夠允許，但切換目前的描述項堆積可能會導致等待閒置。</span><span class="sxs-lookup"><span data-stu-id="69cef-118">Applications must allow for the possibility, however, that switching the current descriptor heap may incur a wait for idle.</span></span>

<span data-ttu-id="69cef-119">為了避免受到這項可能等候在描述項堆積參數上閒置的影響，應用程式可能會利用在轉譯時可能造成 GPU 閒置的中斷，因為其他原因仍是等候閒置的情況。</span><span class="sxs-lookup"><span data-stu-id="69cef-119">To avoid being impacted by this possible wait for idle on the descriptor heap switch, applications can take advantage of breaks in rendering that would cause the GPU to idle for other reasons as the time to do descriptor heap switches, since a wait for idle is happening anyway.</span></span>

<span data-ttu-id="69cef-120">在「命令清單/套件組合」中，用來識別描述元堆積至著色器的機制和語義會在 API 參考中描述。</span><span class="sxs-lookup"><span data-stu-id="69cef-120">The mechanism and semantics for identifying descriptor heaps to shaders during command list / bundle recording are described in the API reference.</span></span>

## <a name="an-example"></a><span data-ttu-id="69cef-121">範例</span><span class="sxs-lookup"><span data-stu-id="69cef-121">An example</span></span>

<span data-ttu-id="69cef-122">下圖顯示兩個描述元參考兩個不同2D 紋理的描述元，並儲存在大型預設堆積的兩個插槽中。</span><span class="sxs-lookup"><span data-stu-id="69cef-122">The image below shows two descriptor heaps referencing two separate 2D textures being stored in two slots of a large default heap.</span></span> <span data-ttu-id="69cef-123">著色器可見的描述元堆積可以由圖形管線 (，包括著色器) ，因此2D 材質可供管線使用。</span><span class="sxs-lookup"><span data-stu-id="69cef-123">The descriptor heap that is shader visible can be accessed by the graphics pipeline (including the shaders), and hence the 2D texture is available to the pipeline.</span></span>

![可見和不可見的描述元堆積](images/descriptor-heaps.png)

> [!Note]  
> <span data-ttu-id="69cef-125">CPU (可寫入的 GPU 本機記憶體數量的 GPU 硬體通常會有限制，稱為描述項堆積的寫入合併記憶體) 。</span><span class="sxs-lookup"><span data-stu-id="69cef-125">There is often a limit on GPU hardware of the amount of GPU local memory writeable by the CPU (referred to as write-combined memory) for descriptor heaps.</span></span> <span data-ttu-id="69cef-126">這項限制通常會在所有進程的96MB 周圍。</span><span class="sxs-lookup"><span data-stu-id="69cef-126">Typically this limit is around 96MB for all processes.</span></span> <span data-ttu-id="69cef-127">例如，具有32byte 描述項的1000000成員描述元堆積會使用多個32MB。</span><span class="sxs-lookup"><span data-stu-id="69cef-127">A one million member descriptor heap, with 32byte descriptors, would use up 32MB, for example.</span></span> <span data-ttu-id="69cef-128">如果有需要，驅動程式將會在系統記憶體上回複，但最好不要建立大量的大型描述元堆積。</span><span class="sxs-lookup"><span data-stu-id="69cef-128">The driver will fall back on system memory if needed, though it is good practice not to create large numbers of large descriptor heaps.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="69cef-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="69cef-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69cef-130">描述元堆積</span><span class="sxs-lookup"><span data-stu-id="69cef-130">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




