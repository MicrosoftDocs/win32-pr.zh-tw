---
description: 所有資源都會共用下列屬性。
ms.assetid: 6ef6ce68-44fa-4964-8b61-2a37382eda1c
title: " (Direct3D 9) 的資源屬性"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e7b53a23e489b5f53495c5d2626da1e2633c9cf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688260"
---
# <a name="resource-properties-direct3d-9"></a><span data-ttu-id="60ba1-103"> (Direct3D 9) 的資源屬性</span><span class="sxs-lookup"><span data-stu-id="60ba1-103">Resource Properties (Direct3D 9)</span></span>

<span data-ttu-id="60ba1-104">所有資源都會共用下列屬性。</span><span class="sxs-lookup"><span data-stu-id="60ba1-104">All resources share the following properties.</span></span>

-   <span data-ttu-id="60ba1-105">使用狀況。</span><span class="sxs-lookup"><span data-stu-id="60ba1-105">Usage.</span></span> <span data-ttu-id="60ba1-106">使用資源的方式，例如，作為材質或轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="60ba1-106">The way a resource is used, for example, as a texture or a render target.</span></span>
-   <span data-ttu-id="60ba1-107">格式化。</span><span class="sxs-lookup"><span data-stu-id="60ba1-107">Format.</span></span> <span data-ttu-id="60ba1-108">資料的格式，例如2D 介面的像素格式。</span><span class="sxs-lookup"><span data-stu-id="60ba1-108">The format of the data, for example, the pixel format of a 2D surface.</span></span>
-   <span data-ttu-id="60ba1-109">池。</span><span class="sxs-lookup"><span data-stu-id="60ba1-109">Pool.</span></span> <span data-ttu-id="60ba1-110">配置資源的記憶體類型。</span><span class="sxs-lookup"><span data-stu-id="60ba1-110">The type of memory where the resource is allocated.</span></span>
-   <span data-ttu-id="60ba1-111">輸入 。</span><span class="sxs-lookup"><span data-stu-id="60ba1-111">Type.</span></span> <span data-ttu-id="60ba1-112">資源的類型，例如頂點緩衝區或轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="60ba1-112">The type of resource, for example, a vertex buffer or render target.</span></span>

<span data-ttu-id="60ba1-113">系統會強制執行資源使用。</span><span class="sxs-lookup"><span data-stu-id="60ba1-113">Resource uses are enforced.</span></span> <span data-ttu-id="60ba1-114">將在特定作業中使用資源的應用程式，必須在資源建立時間指定該操作。</span><span class="sxs-lookup"><span data-stu-id="60ba1-114">An application that will use a resource in a certain operation must specify that operation at resource-creation time.</span></span> <span data-ttu-id="60ba1-115">如需為資源定義的使用常數清單，請參閱 [**D3DUSAGE**](d3dusage.md)。</span><span class="sxs-lookup"><span data-stu-id="60ba1-115">For a list of the usage constants defined for resources, see [**D3DUSAGE**](d3dusage.md).</span></span>

<span data-ttu-id="60ba1-116">D3DUSAGE \_ RTPATCHES、D3DUSAGE \_ NPATCHES 和 D3DUSAGE point \_ 常數向驅動程式指出，這些緩衝區中的資料可能會分別用於三角形或方格修補程式、N 修補程式或分階段。</span><span class="sxs-lookup"><span data-stu-id="60ba1-116">The D3DUSAGE\_RTPATCHES, D3DUSAGE\_NPATCHES, and D3DUSAGE\_POINTS constants indicate to the driver that the data in these buffers is likely to be used for triangular or grid patches, N-patches, or point sprites, respectively.</span></span> <span data-ttu-id="60ba1-117">系統會提供這些旗標，以防硬體無法在未進行主機處理的情況下執行這些作業。</span><span class="sxs-lookup"><span data-stu-id="60ba1-117">These flags are provided in case the hardware cannot perform these operations without host processing.</span></span> <span data-ttu-id="60ba1-118">因此，驅動程式會想要在系統記憶體中配置這些表面，讓 CPU 可以存取它們。</span><span class="sxs-lookup"><span data-stu-id="60ba1-118">Therefore, the driver will want to allocate these surfaces in system memory so that the CPU can access them.</span></span> <span data-ttu-id="60ba1-119">如果驅動程式可以完全在硬體中執行這些作業，它就可以在影片或 AGP 記憶體中配置這些表面，以避免主機複本，並提高效能至少兩次。</span><span class="sxs-lookup"><span data-stu-id="60ba1-119">If the driver can perform these operations entirely in hardware, it can allocate these surfaces in video or AGP memory to avoid a host copy and improve performance at least twofold.</span></span> <span data-ttu-id="60ba1-120">請注意，這些旗標所提供的資訊並不是絕對必要的。</span><span class="sxs-lookup"><span data-stu-id="60ba1-120">Note that the information provided by these flags is not absolutely required.</span></span> <span data-ttu-id="60ba1-121">驅動程式可以偵測到這類作業正在資料上執行，而且會將緩衝區移回系統記憶體以供後續的框架使用。</span><span class="sxs-lookup"><span data-stu-id="60ba1-121">A driver can detect that such operations are being performed on the data, and it will move the buffer back to system memory for subsequent frames.</span></span>

<span data-ttu-id="60ba1-122">如需使用方式旗標的詳細資訊，以及它們與特定資源之間的關聯性，請參閱個別資源建立方法上的參考頁面。</span><span class="sxs-lookup"><span data-stu-id="60ba1-122">For details about the usage flags and how they relate to specific resources, see the reference pages on the individual resource creation methods.</span></span>

<span data-ttu-id="60ba1-123">如需有關資源表面格式的詳細資訊，請參閱 [D3DFORMAT](d3dformat.md) 列舉型別。</span><span class="sxs-lookup"><span data-stu-id="60ba1-123">For information about the surface format of resources, see the [D3DFORMAT](d3dformat.md) enumerated type.</span></span>

<span data-ttu-id="60ba1-124">保存資源緩衝區的記憶體類別稱為「集區」。</span><span class="sxs-lookup"><span data-stu-id="60ba1-124">The class of memory that holds a resource's buffers is called a pool.</span></span> <span data-ttu-id="60ba1-125">集區值是由 [**D3DPOOL**](./d3dpool.md) 列舉類型所定義。</span><span class="sxs-lookup"><span data-stu-id="60ba1-125">Pool values are defined by the [**D3DPOOL**](./d3dpool.md) enumerated type.</span></span> <span data-ttu-id="60ba1-126">針對單一資源中包含的不同物件（也就是 mipmap 中的 mip 層級），不能混用集區，而且當為資源選擇集區時，無法變更集區。</span><span class="sxs-lookup"><span data-stu-id="60ba1-126">A pool cannot be mixed for different objects contained in a single resource - that is, mip levels in a mipmap - and, when a pool is chosen for a resource, the pool cannot be changed.</span></span>

<span data-ttu-id="60ba1-127">當應用程式呼叫資源建立方法（例如 [**IDirect3DDevice9：： CreateCubeTexture**](/windows/desktop/api)）時，這些資源類型會在執行時間隱含設定。</span><span class="sxs-lookup"><span data-stu-id="60ba1-127">The resources types are set implicitly at run time when the application calls a resource creation method such as [**IDirect3DDevice9::CreateCubeTexture**](/windows/desktop/api).</span></span> <span data-ttu-id="60ba1-128">資源類型是由 [**D3DRESOURCETYPE**](./d3dresourcetype.md) 列舉類型所定義。</span><span class="sxs-lookup"><span data-stu-id="60ba1-128">Resource types are defined by the [**D3DRESOURCETYPE**](./d3dresourcetype.md) enumerated type.</span></span> <span data-ttu-id="60ba1-129">應用程式可以在執行時間查詢這些類型;不過，大部分案例都不需要執行時間類型檢查。</span><span class="sxs-lookup"><span data-stu-id="60ba1-129">Applications can query these types at run time; however, it is expected that most scenarios will not require run-time type checking.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60ba1-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="60ba1-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60ba1-131">Direct3D 資源</span><span class="sxs-lookup"><span data-stu-id="60ba1-131">Direct3D Resources</span></span>](direct3d-resources.md)
</dt> </dl>

 

 
