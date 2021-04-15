---
description: 資源是 Direct3D 管線可以存取的記憶體中的區域。
ms.assetid: 24859fbc-b5e1-4963-baf8-4f083f41f39a
title: " (Direct3D 10) 的資源"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e8bb064bc771e36335527d68891bc76a1ce4df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468381"
---
# <a name="resources-direct3d-10"></a><span data-ttu-id="47f9a-103"> (Direct3D 10) 的資源</span><span class="sxs-lookup"><span data-stu-id="47f9a-103">Resources (Direct3D 10)</span></span>

<span data-ttu-id="47f9a-104">資源是 Direct3D 管線可以存取的記憶體中的區域。</span><span class="sxs-lookup"><span data-stu-id="47f9a-104">A resource is an area in memory that can be accessed by the Direct3D pipeline.</span></span> <span data-ttu-id="47f9a-105">為了讓管線能夠有效率地存取記憶體，提供給管線 (例如輸入幾何、著色器資源、紋理等) 的資料必須儲存在資源中。</span><span class="sxs-lookup"><span data-stu-id="47f9a-105">In order for the pipeline to access memory efficiently, data that is provided to the pipeline (such as input geometry, shader resources, textures etc) must be stored in a resource.</span></span> <span data-ttu-id="47f9a-106">所有 Direct3D 資源衍生兩種類型的資源︰緩衝區或紋理。</span><span class="sxs-lookup"><span data-stu-id="47f9a-106">There are two types of resources from which all Direct3D resources derive: a buffer or a texture.</span></span> <span data-ttu-id="47f9a-107">每個管線階段可使用多達 128 種資源。</span><span class="sxs-lookup"><span data-stu-id="47f9a-107">Up to 128 resources can be active for each pipeline stage.</span></span>

<span data-ttu-id="47f9a-108">每個應用程式通常會建立許多資源。</span><span class="sxs-lookup"><span data-stu-id="47f9a-108">Each application will typically create many resources.</span></span> <span data-ttu-id="47f9a-109">資源的範例包括︰頂點緩衝區、索引緩衝區、常數緩衝區、紋理和著色器資源。</span><span class="sxs-lookup"><span data-stu-id="47f9a-109">Examples of resource include: vertex buffers, index buffer, constant buffer, textures, and shader resources.</span></span> <span data-ttu-id="47f9a-110">有幾個決定資源如何使用的選項。</span><span class="sxs-lookup"><span data-stu-id="47f9a-110">There are several options that determine how resources can be used.</span></span> <span data-ttu-id="47f9a-111">您可以建立強類型或無類型的資源；您可以控制資源是否擁有讀取和寫入兩項存取權；您可以讓資源只供 CPU、GPU 或二者存取。</span><span class="sxs-lookup"><span data-stu-id="47f9a-111">You can create resources that are strongly typed or type less; you can control whether resources have both read and write access; you can make resources accessible to only the CPU, GPU, or both.</span></span> <span data-ttu-id="47f9a-112">當然，會有速度和功能上的取捨，您若允許資源擁有更多的功能，您可預期的效能會更低。</span><span class="sxs-lookup"><span data-stu-id="47f9a-112">Naturally, there will be speed vs. functionality tradeoff - the more functionality you allow a resource to have, the less performance you should expect.</span></span>

<span data-ttu-id="47f9a-113">因為應用程式通常會使用許多紋理，所以 Direct3D 也引進了材質陣列的概念，以簡化材質管理。</span><span class="sxs-lookup"><span data-stu-id="47f9a-113">Since an application often uses many textures, Direct3D also introduces the concept of a texture array to simplify texture management.</span></span> <span data-ttu-id="47f9a-114">紋理陣列包含一個或多個紋理 (所有類型與大小均相同)，可以從應用程式中或由著色器編制索引。</span><span class="sxs-lookup"><span data-stu-id="47f9a-114">A texture array contains one or more textures (all of the same type and dimensions) that can be indexed from within an application or by shaders.</span></span> <span data-ttu-id="47f9a-115">紋理陣列可讓您使用具有多個索引的單一介面來存取許多紋裡。</span><span class="sxs-lookup"><span data-stu-id="47f9a-115">Texture arrays allow you to use a single interface with multiple indexes to access many textures.</span></span> <span data-ttu-id="47f9a-116">您可以依需求建立任意數量的紋理陣列來管理不同紋理類型。</span><span class="sxs-lookup"><span data-stu-id="47f9a-116">You can create as many texture arrays to manage different texture types as you need.</span></span>

<span data-ttu-id="47f9a-117">當您建立好應用程式將使用的資源之後，您會連接或繫結每個資源到將使用它們的管線階段。</span><span class="sxs-lookup"><span data-stu-id="47f9a-117">Once you have created the resources that your application will use, you connect or bind each resource to the pipeline stages that will use them.</span></span> <span data-ttu-id="47f9a-118">您可以呼叫繫結 API 來完成這項作業，也就是指向資源。</span><span class="sxs-lookup"><span data-stu-id="47f9a-118">This is accomplished by calling a bind API, which takes a pointer to the resource.</span></span> <span data-ttu-id="47f9a-119">由於有一個以上的管線階段可能需要存取相同的資源，因此 Direct3D 10 引進了資源檢視的概念。</span><span class="sxs-lookup"><span data-stu-id="47f9a-119">Since more than one pipeline stage may need access to the same resource, Direct3D 10 introduces the concept of a resource view.</span></span> <span data-ttu-id="47f9a-120">檢視會辨識可存取的部分資源。</span><span class="sxs-lookup"><span data-stu-id="47f9a-120">A view identifies the portion of a resource that can be accessed.</span></span> <span data-ttu-id="47f9a-121">您可以建立 m 檢視或資源並將它們繫結到 n 管線階段，假設是您遵循共用資源的繫結規則 (若不這麼做，執行階段會在編譯時產生錯誤)。</span><span class="sxs-lookup"><span data-stu-id="47f9a-121">You can create m views or a resource and bind them to n pipeline stages, assuming you follow binding rules for shared resource (the runtime will generate errors at compile time if you don't).</span></span>

<span data-ttu-id="47f9a-122">資源檢視會提供存取資源的一般模型 (紋理、緩衝區等 ) 。</span><span class="sxs-lookup"><span data-stu-id="47f9a-122">A resource view provides a general model for access to a resource (textures, buffers, etc.).</span></span> <span data-ttu-id="47f9a-123">因為您可以使用檢視來告訴執行階段進行存取以及如何存取，所以資源檢視可讓您建立無類型的資源。</span><span class="sxs-lookup"><span data-stu-id="47f9a-123">Because you can use a view to tell the runtime what data to access and how to access it, resource views allow you create type less resources.</span></span> <span data-ttu-id="47f9a-124">也就是您可以在編譯時建立指定大小的資源，然後在資源繫結到管線時宣告資源內的資料類型。</span><span class="sxs-lookup"><span data-stu-id="47f9a-124">That is, you can create resources for a given size at compile time, and then declare the data type within the resource when the resource gets bound to the pipeline.</span></span> <span data-ttu-id="47f9a-125">Views 會公開許多使用資源的新功能，例如，在著色器中讀取深度/樣板表面、在單一行程中產生動態 cubemaps，以及同時轉譯為磁片區的多個配量。</span><span class="sxs-lookup"><span data-stu-id="47f9a-125">Views expose many new capabilities for using resources, such as the ability to read back depth/stencil surfaces in the shader, generating dynamic cubemaps in a single pass, and rendering simultaneously to multiple slices of a volume.</span></span>

<span data-ttu-id="47f9a-126">若要深入瞭解基本資源類型、材質陣列，以及如何建立和使用資源，請參閱下列其他主題：</span><span class="sxs-lookup"><span data-stu-id="47f9a-126">To find out more about the basic resource types, texture arrays, and how to create and use resources, see these other topics:</span></span>

-   [<span data-ttu-id="47f9a-127">資源類型</span><span class="sxs-lookup"><span data-stu-id="47f9a-127">Resource Types</span></span>](d3d10-graphics-programming-guide-resources-types.md)
-   [<span data-ttu-id="47f9a-128">選擇資源</span><span class="sxs-lookup"><span data-stu-id="47f9a-128">Choosing a Resource</span></span>](d3d10-graphics-programming-guide-resources-choosing-basic.md)
-   [<span data-ttu-id="47f9a-129">建立緩衝區資源</span><span class="sxs-lookup"><span data-stu-id="47f9a-129">Creating Buffer Resources</span></span>](d3d10-graphics-programming-guide-resources-creating.md)
-   [<span data-ttu-id="47f9a-130">建立材質資源</span><span class="sxs-lookup"><span data-stu-id="47f9a-130">Creating Texture Resources</span></span>](d3d10-graphics-programming-guide-resources-creating-textures.md)
-   [<span data-ttu-id="47f9a-131">複製和存取資源資料</span><span class="sxs-lookup"><span data-stu-id="47f9a-131">Copying and Accessing Resource Data</span></span>](d3d10-graphics-programming-guide-resources-mapping.md)
-   [<span data-ttu-id="47f9a-132">記憶體結構和 Views</span><span class="sxs-lookup"><span data-stu-id="47f9a-132">Memory Structure and Views</span></span>](d3d10-graphics-programming-guide-resources-access-views.md)
-   [<span data-ttu-id="47f9a-133">區塊壓縮</span><span class="sxs-lookup"><span data-stu-id="47f9a-133">Block Compression</span></span>](d3d10-graphics-programming-guide-resources-block-compression.md)
-   [<span data-ttu-id="47f9a-134">資源限制表</span><span class="sxs-lookup"><span data-stu-id="47f9a-134">Table of Resource Limits</span></span>](d3d10-graphics-programming-guide-resources-limits.md)
-   [<span data-ttu-id="47f9a-135">座標系統</span><span class="sxs-lookup"><span data-stu-id="47f9a-135">Coordinate Systems</span></span>](d3d10-graphics-programming-guide-resources-coordinates.md)
-   [<span data-ttu-id="47f9a-136">浮點數規則</span><span class="sxs-lookup"><span data-stu-id="47f9a-136">Floating-Point Rules</span></span>](d3d10-graphics-programming-guide-resources-float-rules.md)
-   [<span data-ttu-id="47f9a-137">資料類型轉換規則</span><span class="sxs-lookup"><span data-stu-id="47f9a-137">Data Type Conversion Rules</span></span>](d3d10-graphics-programming-guide-resources-data-conversion.md)
-   [<span data-ttu-id="47f9a-138">對應舊版格式</span><span class="sxs-lookup"><span data-stu-id="47f9a-138">Mapping Legacy Formats</span></span>](d3d10-graphics-programming-guide-resources-legacy-formats.md)

## <a name="related-topics"></a><span data-ttu-id="47f9a-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="47f9a-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47f9a-140">Direct3D 10 程式設計手冊</span><span class="sxs-lookup"><span data-stu-id="47f9a-140">Programming Guide for Direct3D 10</span></span>](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 



