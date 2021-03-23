---
title: 描述項資料表的 Advanced 使用
description: 下列各節提供有關描述項資料表的 advanced 使用資訊。
ms.assetid: BB0CA29C-65CB-48B1-8351-EE13CC470B54
ms.date: 05/31/2018
ms.localizationpriority: high
ms.topic: article
ms.openlocfilehash: 79dad6914cff07726c2d40ed2ee27cccb6a0cf1e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104700"
---
# <a name="advanced-use-of-descriptor-tables"></a><span data-ttu-id="9e6eb-103">描述項資料表的 Advanced 使用</span><span class="sxs-lookup"><span data-stu-id="9e6eb-103">Advanced use of Descriptor Tables</span></span>

<span data-ttu-id="9e6eb-104">下列各節提供有關描述項資料表的 advanced 使用資訊。</span><span class="sxs-lookup"><span data-stu-id="9e6eb-104">The following sections provide information about the advanced use of descriptor tables.</span></span>

-   [<span data-ttu-id="9e6eb-105">變更轉譯呼叫之間的描述項資料表專案</span><span class="sxs-lookup"><span data-stu-id="9e6eb-105">Changing Descriptor Table Entries between Rendering Calls</span></span>](#changing-descriptor-table-entries-between-rendering-calls)
-   [<span data-ttu-id="9e6eb-106">超出範圍索引編制</span><span class="sxs-lookup"><span data-stu-id="9e6eb-106">Out of Bounds Indexing</span></span>](#out-of-bounds-indexing)
-   [<span data-ttu-id="9e6eb-107">著色器衍生和分歧索引</span><span class="sxs-lookup"><span data-stu-id="9e6eb-107">Shader Derivatives and Divergent Indexing</span></span>](#shader-derivatives-and-divergent-indexing)
-   [<span data-ttu-id="9e6eb-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="9e6eb-108">Related topics</span></span>](#related-topics)

## <a name="changing-descriptor-table-entries-between-rendering-calls"></a><span data-ttu-id="9e6eb-109">變更轉譯呼叫之間的描述項資料表專案</span><span class="sxs-lookup"><span data-stu-id="9e6eb-109">Changing Descriptor Table Entries between Rendering Calls</span></span>

<span data-ttu-id="9e6eb-110">在命令清單中，如果已將設定描述中繼資料表提交至佇列進行執行，應用程式就必須在應用程式知道 GPU 已使用參考完成之前，從 CPU 中編輯 GPU 可能會參考的部分描述項。</span><span class="sxs-lookup"><span data-stu-id="9e6eb-110">After command lists that set descriptor tables have been submitted to a queue for execution, the application must not edit from the CPU the portions of descriptor heaps that the GPU might reference until the application knows that the GPU has finished using the references.</span></span>

<span data-ttu-id="9e6eb-111">您可以使用 API 界限（用於追蹤 GPU 進度）進行緊密系結來判斷工作完成，或更粗略的機制，例如等待查看轉譯已傳送至顯示-任何適合應用程式的情況。</span><span class="sxs-lookup"><span data-stu-id="9e6eb-111">Work completion can be determined at a tight bound using API fences for tracking GPU progress, or more coarse mechanisms like waiting to see that rendering has been sent to display - whatever suits the application.</span></span> <span data-ttu-id="9e6eb-112">如果應用程式知道只會存取描述項資料表所指向的區域子集 (例如，由於著色器) 中的流量控制，其他未參考的描述項仍可自由變更。</span><span class="sxs-lookup"><span data-stu-id="9e6eb-112">If an application knows that only a subset of the region a descriptor table points to will be accessed (say due to flow control in the shader), the other unreferenced descriptors are still free to be changed.</span></span> <span data-ttu-id="9e6eb-113">如果應用程式需要在轉譯呼叫之間切換不同的描述中繼資料表，應用程式有幾種方法可以選擇：</span><span class="sxs-lookup"><span data-stu-id="9e6eb-113">If an application needs to switch between different descriptor tables between rendering calls, there are a few approaches the application can choose from:</span></span>

-   <span data-ttu-id="9e6eb-114">描述項資料表版本控制：建立 (或重複使用) 個別描述中繼資料表，以供命令清單所參考的每個唯一描述項集合使用。</span><span class="sxs-lookup"><span data-stu-id="9e6eb-114">Descriptor Table Versioning: Create (or reuse) a separate descriptor table for every unique collection of descriptors that is to be referenced by a command list.</span></span> <span data-ttu-id="9e6eb-115">在描述項堆積上編輯和重複使用先前填入的區域時，應用程式必須先確定 GPU 已使用將回收之描述項堆積的任何部分，來完成。</span><span class="sxs-lookup"><span data-stu-id="9e6eb-115">When editing and reusing previously populated areas on descriptor heaps, applications must first ensure that the GPU has finished using any portion of a descriptor heap that will be recycled.</span></span>
-   <span data-ttu-id="9e6eb-116">動態索引：應用程式可以排列不同繪製/分派 (的物件，或甚至在某個描述項堆積範圍內的繪圖) 內有所變化、定義橫跨所有專案的描述中繼資料表，以及從著色器中，在著色器執行期間使用資料表的動態索引編制，以選取要使用的物件。</span><span class="sxs-lookup"><span data-stu-id="9e6eb-116">Dynamic Indexing: Applications can arrange objects that vary across draw/dispatch (or even vary within a draw) in a range of a descriptor heap, define a descriptor table that spans all of them, and from the shader, use dynamic indexing of the table during shader execution to select which object to use.</span></span>
-   <span data-ttu-id="9e6eb-117">直接將描述項放在根簽章中。</span><span class="sxs-lookup"><span data-stu-id="9e6eb-117">Putting descriptors in the root signature directly.</span></span> <span data-ttu-id="9e6eb-118">因為根簽章空間有限，所以只能以此方式管理極少數的描述項。</span><span class="sxs-lookup"><span data-stu-id="9e6eb-118">Only a very small number of descriptors can be managed this way because root signature space is limited.</span></span>

<span data-ttu-id="9e6eb-119">使用描述項資料表版本設定的含意是，必須針對每個可執行、已排入佇列以執行的命令清單，或在任何指定時間記錄的每個命令清單，針對圖形管線所參考的每一組唯一描述項，來燒錄描述元堆積外的描述元記憶體。</span><span class="sxs-lookup"><span data-stu-id="9e6eb-119">The implication of using descriptor table versioning is that descriptor memory out of a descriptor heap must be burned through for every unique set of descriptors referenced by the graphics pipeline for every command list that could be either executing, queued for execution, or being recorded at any given time.</span></span>

<span data-ttu-id="9e6eb-120">D3D12 會負責管理透過描述元堆積和描述中繼資料表管理之物件類型的應用程式版本控制。</span><span class="sxs-lookup"><span data-stu-id="9e6eb-120">D3D12 leaves the responsibility of managing versioning to the application for the object types managed via descriptor heaps and descriptor tables.</span></span> <span data-ttu-id="9e6eb-121">其中一個優點是，應用程式可以選擇重複使用描述項資料表內容，而不是一律為每個命令清單提交定義新的描述項資料表版本。</span><span class="sxs-lookup"><span data-stu-id="9e6eb-121">One benefit of this is that applications can choose to reuse descriptor table contents as much as possible rather than always defining a new descriptor table version for every command list submission.</span></span> <span data-ttu-id="9e6eb-122">根簽章是 D3D12 驅動程式自動版本的空間。</span><span class="sxs-lookup"><span data-stu-id="9e6eb-122">The root signature is a space that the D3D12 driver automatically versions.</span></span>

<span data-ttu-id="9e6eb-123">可以將多個描述中繼資料表系結至根簽章 (，然後再將其系結至管線) 可讓應用程式在需要時，以不同的頻率來分組和切換描述項參考集。</span><span class="sxs-lookup"><span data-stu-id="9e6eb-123">The ability to bind multiple descriptor tables to the root signature (and thus to the pipeline) at a time allows applications to group and switch sets of descriptor references at different frequencies if desired.</span></span> <span data-ttu-id="9e6eb-124">例如，應用程式可以使用較小的數位 (可能只是一個很少變更的大型靜態描述項資料表) ，或是基礎描述項堆積記憶體中的哪些區域會視需要填入，並使用著色器的動態索引子來選取材質。</span><span class="sxs-lookup"><span data-stu-id="9e6eb-124">For example, an application could use a small number (perhaps just one) of large static descriptor tables that rarely change, or in which regions in the underlying descriptor heap memory are being populated as needed, with the use of dynamic indexing from the shader to select textures.</span></span> <span data-ttu-id="9e6eb-125">同時，應用程式可以維護另一個類別的資源，其中每個繪製呼叫所參考的集合都會使用描述項資料表版本控制技術從 CPU 切換。</span><span class="sxs-lookup"><span data-stu-id="9e6eb-125">At the same time, the application could maintain another class of resources where the set referenced by each draw call is switched from the CPU using the descriptor table versioning technique.</span></span>

## <a name="out-of-bounds-indexing"></a><span data-ttu-id="9e6eb-126">超出範圍索引編制</span><span class="sxs-lookup"><span data-stu-id="9e6eb-126">Out of Bounds Indexing</span></span>

<span data-ttu-id="9e6eb-127">從著色器中的任何描述中繼資料表的範圍外索引編制都會導致大量未定義的記憶體存取權，包括讀取任意同進程記憶體的可能性，如同硬體狀態原因項一樣</span><span class="sxs-lookup"><span data-stu-id="9e6eb-127">Out of bounds indexing of any descriptor table from the shader results in a largely undefined memory access, including the possibility of reading arbitrary in-process memory as if it is a hardware state descriptor and living with the consequence of what the hardware does with that.</span></span> <span data-ttu-id="9e6eb-128">這可能會產生裝置重設，但不會損毀 Windows。</span><span class="sxs-lookup"><span data-stu-id="9e6eb-128">This could produce a device reset, but will not crash Windows.</span></span>

## <a name="shader-derivatives-and-divergent-indexing"></a><span data-ttu-id="9e6eb-129">著色器衍生和分歧索引</span><span class="sxs-lookup"><span data-stu-id="9e6eb-129">Shader Derivatives and Divergent Indexing</span></span>

<span data-ttu-id="9e6eb-130">如果以2x2 戳記執行的圖元著色器調用 (為支援衍生計算) 選擇不同的材質索引從描述中繼資料表中取樣，而且，如果所選圖元的選取取樣器設定和材質需要從紋理座標衍生的」 LOD 計算，則」 LOD 計算和紋理取樣程式是由硬體針對2x2 戳記中的每個材質查閱而獨立執行，這會影響效能。</span><span class="sxs-lookup"><span data-stu-id="9e6eb-130">If pixel shader invocations that are executing in a 2x2 stamp (to support derivative calculations) choose different texture indices to sample from out of a descriptor table, and if the selected sampler configuration and texture for any given pixel requires an LOD calculation from texture coordinate derivatives, then the LOD calculation and texture sampling process is done by the hardware independently for each texture lookup in the 2x2 stamp, which will impact performance.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e6eb-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="9e6eb-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e6eb-132">描述中繼資料表</span><span class="sxs-lookup"><span data-stu-id="9e6eb-132">Descriptor Tables</span></span>](descriptor-tables.md)
</dt> </dl>

 

 




