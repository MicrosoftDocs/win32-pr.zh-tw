---
title: 建立根簽章
description: 根簽章是包含嵌套結構的複雜資料結構。
ms.assetid: 565B28C1-DBD1-42B6-87F9-70743E4A2E4A
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87209dfc324b950a74d2b31e5f1a1f6326792b9f
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826434"
---
# <a name="creating-a-root-signature"></a><span data-ttu-id="9f69e-103">建立根簽章</span><span class="sxs-lookup"><span data-stu-id="9f69e-103">Creating a Root Signature</span></span>

<span data-ttu-id="9f69e-104">根簽章是包含嵌套結構的複雜資料結構。</span><span class="sxs-lookup"><span data-stu-id="9f69e-104">Root signatures are a complex data structure containing nested structures.</span></span> <span data-ttu-id="9f69e-105">您可以使用下列資料結構定義，以程式設計的方式定義這些方法 (其中包含有助於初始化成員) 的方法。</span><span class="sxs-lookup"><span data-stu-id="9f69e-105">These can be defined programmatically using the data structure definition below (which includes methods to help initialize members).</span></span> <span data-ttu-id="9f69e-106">或者，您也可以使用高階的陰影語言來撰寫 (HLSL) –提供編譯器將會及早驗證配置與著色器相容的優點。</span><span class="sxs-lookup"><span data-stu-id="9f69e-106">Alternatively, they can be authored in High Level Shading Language (HLSL) – giving the advantage that the compiler will validate early that the layout is compatible with the shader.</span></span>

<span data-ttu-id="9f69e-107">用來建立根簽章的 API 會採用序列化的 (自我自主、指標 free) 版本的版面配置描述，如下所述。</span><span class="sxs-lookup"><span data-stu-id="9f69e-107">The API for creating a root signature takes in a serialized (self contained, pointer free) version of the layout description described below.</span></span> <span data-ttu-id="9f69e-108">提供的方法是用來從 c + + 資料結構產生這個序列化版本，但是取得序列化的根簽章定義的另一種方法，就是從已經使用根簽章編譯的著色器中取出。</span><span class="sxs-lookup"><span data-stu-id="9f69e-108">A method is provided for generating this serialized version from the C++ data structure, but another way to obtain a serialized root signature definition is to retrieve it from a shader that has been compiled with a root signature.</span></span>

<span data-ttu-id="9f69e-109">如果您想要利用根簽章描述元和資料的驅動程式優化，請參閱根簽章 [版本 1.1](root-signature-version-1-1.md)</span><span class="sxs-lookup"><span data-stu-id="9f69e-109">If you wish to take advantage of driver optimizations for root signature descriptors and data, refer to [Root Signature Version 1.1](root-signature-version-1-1.md)</span></span>

-   [<span data-ttu-id="9f69e-110">描述項資料表系結類型</span><span class="sxs-lookup"><span data-stu-id="9f69e-110">Descriptor Table Bind Types</span></span>](#descriptor-table-bind-types)
-   [<span data-ttu-id="9f69e-111">描述項範圍</span><span class="sxs-lookup"><span data-stu-id="9f69e-111">Descriptor Range</span></span>](#descriptor-range)
-   [<span data-ttu-id="9f69e-112">描述項資料表版面配置</span><span class="sxs-lookup"><span data-stu-id="9f69e-112">Descriptor Table Layout</span></span>](#descriptor-table-layout)
-   [<span data-ttu-id="9f69e-113">根常數</span><span class="sxs-lookup"><span data-stu-id="9f69e-113">Root Constants</span></span>](#root-constants)
-   [<span data-ttu-id="9f69e-114">根描述元</span><span class="sxs-lookup"><span data-stu-id="9f69e-114">Root Descriptor</span></span>](#root-descriptor)
-   [<span data-ttu-id="9f69e-115">著色器可見度</span><span class="sxs-lookup"><span data-stu-id="9f69e-115">Shader Visibility</span></span>](#shader-visibility)
-   [<span data-ttu-id="9f69e-116">根簽章定義</span><span class="sxs-lookup"><span data-stu-id="9f69e-116">Root Signature Definition</span></span>](#root-signature-definition)
-   [<span data-ttu-id="9f69e-117">根簽章資料結構序列化/還原序列化</span><span class="sxs-lookup"><span data-stu-id="9f69e-117">Root Signature Data Structure Serialization / Deserialization</span></span>](/windows)
-   [<span data-ttu-id="9f69e-118">建立根簽章 API</span><span class="sxs-lookup"><span data-stu-id="9f69e-118">Root Signature Creation API</span></span>](#root-signature-creation-api)
-   [<span data-ttu-id="9f69e-119">管線狀態物件中的根簽章</span><span class="sxs-lookup"><span data-stu-id="9f69e-119">Root Signature in Pipeline State Objects</span></span>](#root-signature-in-pipeline-state-objects)
-   [<span data-ttu-id="9f69e-120">定義版本1.1 根簽章的程式碼</span><span class="sxs-lookup"><span data-stu-id="9f69e-120">Code for Defining a Version 1.1 Root Signature</span></span>](#code-for-defining-a-version-11-root-signature)
-   [<span data-ttu-id="9f69e-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="9f69e-121">Related topics</span></span>](#related-topics)

## <a name="descriptor-table-bind-types"></a><span data-ttu-id="9f69e-122">描述項資料表系結類型</span><span class="sxs-lookup"><span data-stu-id="9f69e-122">Descriptor Table Bind Types</span></span>

<span data-ttu-id="9f69e-123">列舉 [**D3D12 \_ 描述項 \_ 範圍 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) 會定義描述項的類型，這些描述元可以參考為描述項資料表配置定義的一部分。</span><span class="sxs-lookup"><span data-stu-id="9f69e-123">The enum [**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) defines the types of descriptors that can be referenced as part of a descriptor table layout definition.</span></span>

<span data-ttu-id="9f69e-124">它是一個範圍，例如，如果部分描述中繼資料表有 100 SRVs，則可以在一個專案中宣告該範圍，而不是100。</span><span class="sxs-lookup"><span data-stu-id="9f69e-124">It is a range so that, for example if part of a descriptor table has 100 SRVs, that range can be declared in one entry rather than 100.</span></span> <span data-ttu-id="9f69e-125">因此描述項資料表定義是範圍的集合。</span><span class="sxs-lookup"><span data-stu-id="9f69e-125">So a descriptor table definition is a collection of ranges.</span></span>

``` syntax
typedef enum D3D12_DESCRIPTOR_RANGE_TYPE
{
  D3D12_DESCRIPTOR_RANGE_TYPE_SRV,
  D3D12_DESCRIPTOR_RANGE_TYPE_UAV,
  D3D12_DESCRIPTOR_RANGE_TYPE_CBV,
  D3D12_DESCRIPTOR_RANGE_TYPE_SAMPLER
} D3D12_DESCRIPTOR_RANGE_TYPE;
```

## <a name="descriptor-range"></a><span data-ttu-id="9f69e-126">描述項範圍</span><span class="sxs-lookup"><span data-stu-id="9f69e-126">Descriptor Range</span></span>

<span data-ttu-id="9f69e-127">[**D3D12 \_ 描述項 \_ 範圍**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)結構會定義指定類型的描述項範圍 (例如在描述中繼資料表內的 SRVs) 。</span><span class="sxs-lookup"><span data-stu-id="9f69e-127">The [**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) structure defines a range of descriptors of a given type (such as SRVs) within a descriptor table.</span></span>

<span data-ttu-id="9f69e-128">`D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND`宏通常可以用於 `OffsetInDescriptorsFromTableStart` [**D3D12 \_ 描述項 \_ 範圍**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)的參數。</span><span class="sxs-lookup"><span data-stu-id="9f69e-128">The `D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND` macro can typically be used for the `OffsetInDescriptorsFromTableStart` parameter of [**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range).</span></span> <span data-ttu-id="9f69e-129">這表示會將描述項範圍附加在描述中繼資料表中的上一個描述項之後，再加以定義。</span><span class="sxs-lookup"><span data-stu-id="9f69e-129">This means append the descriptor range being defined after the previous one in the descriptor table.</span></span> <span data-ttu-id="9f69e-130">如果應用程式想要別名描述項，或基於某些原因想要略過位置，它可以設定 `OffsetInDescriptorsFromTableStart` 為所需的任何位移。</span><span class="sxs-lookup"><span data-stu-id="9f69e-130">If the application wants to alias descriptors or for some reason wants to skip slots, it can set `OffsetInDescriptorsFromTableStart` to whatever offset is desired.</span></span> <span data-ttu-id="9f69e-131">定義不同類型的重迭範圍無效。</span><span class="sxs-lookup"><span data-stu-id="9f69e-131">Defining overlapping ranges of different types is invalid.</span></span>

<span data-ttu-id="9f69e-132">由、、和組合所指定的著色器集合 `RangeType` ，在 `NumDescriptors` `BaseShaderRegister` `RegisterSpace` 具有通用 [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) 的根簽章中的任何宣告之間，不能互相衝突或重迭 (請參閱下方的著色器可見度區段) 。</span><span class="sxs-lookup"><span data-stu-id="9f69e-132">The set of shader registers specified by the combination of `RangeType`, `NumDescriptors`, `BaseShaderRegister`, and `RegisterSpace` cannot conflict or overlap across any declarations in a root signature that have common [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) (refer to the shader visibility section below).</span></span>

## <a name="descriptor-table-layout"></a><span data-ttu-id="9f69e-133">描述項資料表版面配置</span><span class="sxs-lookup"><span data-stu-id="9f69e-133">Descriptor Table Layout</span></span>

<span data-ttu-id="9f69e-134">[**D3D12 \_ 根描述 \_ 元 \_ 資料表**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table)結構會將描述項資料表的配置宣告為描述項範圍的集合，而這些描述項範圍會在描述元堆積中的另一個後面出現。</span><span class="sxs-lookup"><span data-stu-id="9f69e-134">The [**D3D12\_ROOT\_DESCRIPTOR\_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) structure declares the layout of a descriptor table as a collection of descriptor ranges that appear one after the other in a descriptor heap.</span></span> <span data-ttu-id="9f69e-135">在 CBV/UAV/SRVs 的相同描述項資料表中，不允許取樣器。</span><span class="sxs-lookup"><span data-stu-id="9f69e-135">Samplers are not allowed in the same descriptor table as CBV/UAV/SRVs.</span></span>

<span data-ttu-id="9f69e-136">當根簽章位置類型設定為時，就會使用這個結構 `D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE` 。</span><span class="sxs-lookup"><span data-stu-id="9f69e-136">This struct is used when the root signature slot type is set to `D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE`.</span></span>

<span data-ttu-id="9f69e-137">若要設定圖形 (CBV、SRV、UAV、取樣器) 描述中繼資料表，請使用 [**ID3D12GraphicsCommandList：： SetGraphicsRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable)。</span><span class="sxs-lookup"><span data-stu-id="9f69e-137">To set a graphics (CBV, SRV, UAV, Sampler) descriptor table, use [**ID3D12GraphicsCommandList::SetGraphicsRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable).</span></span>

<span data-ttu-id="9f69e-138">若要設定計算描述中繼資料表，請使用 [**ID3D12GraphicsCommandList：： SetComputeRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable)。</span><span class="sxs-lookup"><span data-stu-id="9f69e-138">To set a compute descriptor table, use [**ID3D12GraphicsCommandList::SetComputeRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable).</span></span>

## <a name="root-constants"></a><span data-ttu-id="9f69e-139">根常數</span><span class="sxs-lookup"><span data-stu-id="9f69e-139">Root Constants</span></span>

<span data-ttu-id="9f69e-140">[**D3D12 \_ 根 \_ 常數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants)結構會在以著色器形式出現的根簽章中宣告內嵌常數，作為一個常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="9f69e-140">The [**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) structure declares constants inline in the root signature that appear in shaders as one constant buffer.</span></span>

<span data-ttu-id="9f69e-141">當根簽章位置類型設定為時，就會使用這個結構 `D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS` 。</span><span class="sxs-lookup"><span data-stu-id="9f69e-141">This struct is used when the root signature slot type is set to `D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS`.</span></span>

## <a name="root-descriptor"></a><span data-ttu-id="9f69e-142">根描述元</span><span class="sxs-lookup"><span data-stu-id="9f69e-142">Root Descriptor</span></span>

<span data-ttu-id="9f69e-143">[**D3D12 的 \_ 根 \_ 描述**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor)元結構會宣告出現在根簽章中，) 內嵌于著色器中的描述元 (。</span><span class="sxs-lookup"><span data-stu-id="9f69e-143">The [**D3D12\_ROOT\_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) structure declares descriptors (that appear in shaders) inline in the root signature.</span></span>

<span data-ttu-id="9f69e-144">當根簽章位置類型設定為或時，會使用此結構 `D3D12_ROOT_PARAMETER_TYPE_CBV` `D3D12_ROOT_PARAMETER_TYPE_SRV` `D3D12_ROOT_PARAMETER_TYPE_UAV` 。</span><span class="sxs-lookup"><span data-stu-id="9f69e-144">This struct is used when the root signature slot type is set to `D3D12_ROOT_PARAMETER_TYPE_CBV`, `D3D12_ROOT_PARAMETER_TYPE_SRV` or `D3D12_ROOT_PARAMETER_TYPE_UAV`.</span></span>

## <a name="shader-visibility"></a><span data-ttu-id="9f69e-145">著色器可見度</span><span class="sxs-lookup"><span data-stu-id="9f69e-145">Shader Visibility</span></span>

<span data-ttu-id="9f69e-146">[**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)列舉集合中的成員會設定為 [**D3D12 \_ 根 \_ 參數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)的著色器可見度參數，以決定哪一種著色器會查看指定之根簽章位置的內容。</span><span class="sxs-lookup"><span data-stu-id="9f69e-146">The member of [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) enum set into the shader visibility parameter of [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) determines which shaders see the contents of a given root signature slot.</span></span> <span data-ttu-id="9f69e-147">計算一律 \_ 會使用所有 (，因為只有一個使用中階段) 。</span><span class="sxs-lookup"><span data-stu-id="9f69e-147">Compute always uses \_ALL (since there is only one active stage).</span></span> <span data-ttu-id="9f69e-148">圖形可以選擇，但如果它使用 \_ all，所有著色器階段都會看到任何系結于根簽章位置。</span><span class="sxs-lookup"><span data-stu-id="9f69e-148">Graphics can choose, but if it uses \_ALL, all shader stages see whatever is bound at the root signature slot.</span></span>

<span data-ttu-id="9f69e-149">著色器可見度的其中一種用法是協助使用重迭的命名空間，針對每個著色器階段所撰寫的著色器提供不同的系結。</span><span class="sxs-lookup"><span data-stu-id="9f69e-149">One use of shader visibility is to help with shaders that are authored expecting different bindings per shader stage using an overlapping namespace.</span></span> <span data-ttu-id="9f69e-150">例如，頂點著色器可能會宣告：</span><span class="sxs-lookup"><span data-stu-id="9f69e-150">For example, a vertex shader may declare:</span></span>

```hlsl
Texture2D foo : register(t0);
```

<span data-ttu-id="9f69e-151">此外，圖元著色器也可以宣告：</span><span class="sxs-lookup"><span data-stu-id="9f69e-151">and the pixel shader may also declare:</span></span>

```hlsl
Texture2D bar : register(t0);
```

<span data-ttu-id="9f69e-152">如果應用程式將根簽章系結至 t0 可見度 \_ ，則這兩種著色器會看到相同的材質。</span><span class="sxs-lookup"><span data-stu-id="9f69e-152">If the application makes a root signature binding to t0 VISIBILITY\_ALL, both shaders see the same texture.</span></span> <span data-ttu-id="9f69e-153">如果著色器定義真的希望每個著色器都能看到不同的材質，則可以使用可見度 \_ 頂點和圖元來定義2個根簽章位置 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9f69e-153">If the shader defines actually wants each shader to see different textures, it can define 2 root signature slots with VISIBILITY\_VERTEX and \_PIXEL.</span></span> <span data-ttu-id="9f69e-154">無論根簽章位置上的可見度為何，它一律會具有相同的成本 (成本，而這取決於將 SlotType) 至一個固定的根簽章大小上限。</span><span class="sxs-lookup"><span data-stu-id="9f69e-154">No matter what the visibility is on a root signature slot, it always has the same cost (cost only depending on what the SlotType is) towards one fixed maximum root signature size.</span></span>

<span data-ttu-id="9f69e-155">在低終端 D3D11 硬體上，在 \_ 根配置中驗證描述項資料表的大小時，也會將著色器可見度納入考慮，因為某些 D3D11 硬體只支援每一階段的系結數量上限。</span><span class="sxs-lookup"><span data-stu-id="9f69e-155">On low end D3D11 hardware, SHADER\_VISIBILITY is also taken into account used when validating the sizes of descriptor tables in a root layout, since some D3D11 hardware can only support a maximum amount of bindings per-stage.</span></span> <span data-ttu-id="9f69e-156">只有在低層級硬體上執行時才會強制執行這些限制，而且完全不會限制更新式的硬體。</span><span class="sxs-lookup"><span data-stu-id="9f69e-156">These restrictions are only imposed when running on low tier hardware and do not limit more modern hardware at all.</span></span>

<span data-ttu-id="9f69e-157">如果根簽章有定義在命名空間中彼此重迭的多個描述中繼資料表 (將) 的暫存器系結，而且其中任何一個都指定 \_ 為可見度，則配置無效 (建立將會失敗) 。</span><span class="sxs-lookup"><span data-stu-id="9f69e-157">If a root signature has multiple descriptor tables defined that overlap each other in namespace (the register bindings to the shader) and any one of them specifies \_ALL for visibility, the layout is invalid (creation will fail).</span></span>

## <a name="root-signature-definition"></a><span data-ttu-id="9f69e-158">根簽章定義</span><span class="sxs-lookup"><span data-stu-id="9f69e-158">Root Signature Definition</span></span>

<span data-ttu-id="9f69e-159">[**D3D12 根簽章 \_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)結構可以包含描述項資料表和內嵌常數，以及 [**D3D12 \_ 根 \_ 參數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)結構和 enum [**D3D12 \_ 根 \_ 參數 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type)所定義的每個位置類型。</span><span class="sxs-lookup"><span data-stu-id="9f69e-159">The [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) structure can contain descriptor tables and inline constants, each slot type defined by the [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) structure and the enum [**D3D12\_ROOT\_PARAMETER\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type).</span></span>

<span data-ttu-id="9f69e-160">若要起始根簽章位置，請參閱 [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)的 **SetComputeRoot \* \* \*** 和 **SetGraphicsRoot \* \* \*** 方法。</span><span class="sxs-lookup"><span data-stu-id="9f69e-160">To initiate a root signature slot, refer to the **SetComputeRoot\*\*\*** and **SetGraphicsRoot\*\*\*** methods of [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span></span>

<span data-ttu-id="9f69e-161">靜態取樣器會使用 [**D3D12 \_ 靜態 \_ 取樣**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) 器結構，在根簽章中描述。</span><span class="sxs-lookup"><span data-stu-id="9f69e-161">Static samplers are described in the root signature using the [**D3D12\_STATIC\_SAMPLER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) structure.</span></span>

<span data-ttu-id="9f69e-162">許多旗標會限制某些著色器存取根簽章的許可權，請參閱 [**D3D12 \_ 根簽章 \_ \_ 旗標**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags)。</span><span class="sxs-lookup"><span data-stu-id="9f69e-162">A number of flags limit the access of certain shaders to the root signature, refer to [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).</span></span>

## <a name="root-signature-data-structure-serialization--deserialization"></a><span data-ttu-id="9f69e-163">根簽章資料結構序列化/還原序列化</span><span class="sxs-lookup"><span data-stu-id="9f69e-163">Root Signature Data Structure Serialization / Deserialization</span></span>

<span data-ttu-id="9f69e-164">本節中所述的方法是由 D3D12Core.dll 匯出，並且提供序列化和還原序列化根簽章資料結構的方法。</span><span class="sxs-lookup"><span data-stu-id="9f69e-164">The methods described in this section are exported by D3D12Core.dll and provide methods for serializing and deserializing a root signature data structure.</span></span>

<span data-ttu-id="9f69e-165">序列化形式是在建立根簽章時傳遞至 API 的表單。</span><span class="sxs-lookup"><span data-stu-id="9f69e-165">The serialized form is what is passed into the API when creating a root signature.</span></span> <span data-ttu-id="9f69e-166">如果著色器在其中以根簽章撰寫 (當) 新增該功能時，已編譯的著色器會在其中包含已序列化的根簽章。</span><span class="sxs-lookup"><span data-stu-id="9f69e-166">If a shader has been authored with a root signature in it (when that capability is added), then the compiled shader will contain a serialized root signature in it already.</span></span>

<span data-ttu-id="9f69e-167">如果應用程式 cti 產生 D3D12 的根簽章 [**\_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) 資料結構，它必須使用 [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature)來建立序列化的表單。</span><span class="sxs-lookup"><span data-stu-id="9f69e-167">If an application procedurally generates a [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) data structure, it must make the serialized form using [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature).</span></span> <span data-ttu-id="9f69e-168">可以傳遞至 [**ID3D12Device：： CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature)的輸出。</span><span class="sxs-lookup"><span data-stu-id="9f69e-168">The output of that can be passed into [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span></span>

<span data-ttu-id="9f69e-169">如果應用程式已經有序列化的根簽章，或具有已編譯的著色器，其中包含根簽章，而且想要以程式設計的方式探索配置定義 (稱為「反映」 ) ，則可以呼叫 [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) 。</span><span class="sxs-lookup"><span data-stu-id="9f69e-169">If an application has a serialized root signature already, or has a compiled shader that contains a root signature and wishes to programmatically discover the layout definition (known as "reflection"), [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) can be called.</span></span> <span data-ttu-id="9f69e-170">這會產生 [**ID3D12RootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) 介面，其中包含傳回已還原序列化之 [**D3D12 根簽章 \_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) 資料結構的方法。</span><span class="sxs-lookup"><span data-stu-id="9f69e-170">This generates an [**ID3D12RootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) interface, which contains a method to return the deserialized [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) data structure.</span></span> <span data-ttu-id="9f69e-171">介面擁有還原序列化之資料結構的存留期。</span><span class="sxs-lookup"><span data-stu-id="9f69e-171">The interface owns the lifetime of the deserialized data structure.</span></span>

## <a name="root-signature-creation-api"></a><span data-ttu-id="9f69e-172">建立根簽章 API</span><span class="sxs-lookup"><span data-stu-id="9f69e-172">Root Signature Creation API</span></span>

<span data-ttu-id="9f69e-173">[**ID3D12Device：： CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) API 會採用根簽章的序列化版本。</span><span class="sxs-lookup"><span data-stu-id="9f69e-173">The [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) API takes in a serialized version of a root signature.</span></span>

## <a name="root-signature-in-pipeline-state-objects"></a><span data-ttu-id="9f69e-174">管線狀態物件中的根簽章</span><span class="sxs-lookup"><span data-stu-id="9f69e-174">Root Signature in Pipeline State Objects</span></span>

<span data-ttu-id="9f69e-175">建立管線狀態 ([**ID3D12Device：： CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) 和 [**ID3D12Device：： ) CreateComputePipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) 的方法會採用選擇性的 [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) 介面做為輸入參數 (儲存在 [**D3D12 \_ 圖形 \_ 管線 \_ 狀態 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) 結構) 中。</span><span class="sxs-lookup"><span data-stu-id="9f69e-175">The methods to create pipeline state ([**ID3D12Device::CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) and [**ID3D12Device::CreateComputePipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) ) take an optional [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) interface as an input parameter (stored in a [**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) structure).</span></span> <span data-ttu-id="9f69e-176">這將會覆寫已在著色器中的任何根簽章。</span><span class="sxs-lookup"><span data-stu-id="9f69e-176">This will override any root signature already in the shaders.</span></span>

<span data-ttu-id="9f69e-177">如果將根簽章傳遞給其中一個「建立管線」狀態方法，此根簽章會針對 PSO 中的所有著色器進行驗證，以提供相容性，並提供給驅動程式以搭配所有著色器使用。</span><span class="sxs-lookup"><span data-stu-id="9f69e-177">If a root signature is passed into one of the create pipeline state methods, this root signature is validated against all the shaders in the PSO for compatibility and given to the driver to use with all the shaders.</span></span> <span data-ttu-id="9f69e-178">如果任何著色器中有不同的根簽章，它就會被傳入 API 的根簽章取代。</span><span class="sxs-lookup"><span data-stu-id="9f69e-178">If any of the shaders has a different root signature in it, it gets replaced by the root signature passed in at the API.</span></span> <span data-ttu-id="9f69e-179">如果未傳入根簽章，則所有傳入的著色器都必須有根簽章，而且必須相符–這會提供給驅動程式。</span><span class="sxs-lookup"><span data-stu-id="9f69e-179">If a root signature is not passed in, all shaders passed in must have a root signature and they must match – this will be given to the driver.</span></span> <span data-ttu-id="9f69e-180">設定命令清單或配套上的 PSO 並不會變更根簽章。</span><span class="sxs-lookup"><span data-stu-id="9f69e-180">Setting a PSO on a command list or bundle does not change the root signature.</span></span> <span data-ttu-id="9f69e-181">這是透過 [**SetGraphicsRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature) 和 [**SetComputeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)方法來完成。</span><span class="sxs-lookup"><span data-stu-id="9f69e-181">That is accomplished by the methods [**SetGraphicsRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature) and [**SetComputeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature).</span></span> <span data-ttu-id="9f69e-182">隨著時間繪製 (graphics) /dispatch (計算) 叫用，應用程式必須確定目前的 PSO 符合目前的根簽章;否則，行為會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="9f69e-182">By the time draw(graphics)/dispatch(compute) is invoked, the application must ensure that the current PSO matches the current root signature; otherwise, the behavior is undefined.</span></span>

## <a name="code-for-defining-a-version-11-root-signature"></a><span data-ttu-id="9f69e-183">定義版本1.1 根簽章的程式碼</span><span class="sxs-lookup"><span data-stu-id="9f69e-183">Code for Defining a Version 1.1 Root Signature</span></span>

<span data-ttu-id="9f69e-184">下列範例顯示如何建立具有下列格式的根簽章：</span><span class="sxs-lookup"><span data-stu-id="9f69e-184">The example below shows how to create a root signature with the following format:</span></span>



| <span data-ttu-id="9f69e-185">RootParameterIndex</span><span class="sxs-lookup"><span data-stu-id="9f69e-185">RootParameterIndex</span></span>                       | <span data-ttu-id="9f69e-186">目錄</span><span class="sxs-lookup"><span data-stu-id="9f69e-186">Contents</span></span>                                               | <span data-ttu-id="9f69e-187">值</span><span class="sxs-lookup"><span data-stu-id="9f69e-187">Values</span></span>                                             |
|------------------------|------------------------------------------------|----------------------------------------------|                                              
| <span data-ttu-id="9f69e-188">\[0\]</span><span class="sxs-lookup"><span data-stu-id="9f69e-188">\[0\]</span></span>                  | <span data-ttu-id="9f69e-189">根常數： {b2}</span><span class="sxs-lookup"><span data-stu-id="9f69e-189">Root constants: { b2 }</span></span>                         | <span data-ttu-id="9f69e-190"> (1 CBV) </span><span class="sxs-lookup"><span data-stu-id="9f69e-190">(1 CBV)</span></span>                                      |
| <span data-ttu-id="9f69e-191">\[1\]</span><span class="sxs-lookup"><span data-stu-id="9f69e-191">\[1\]</span></span>                  | <span data-ttu-id="9f69e-192">描述項資料表： {t2-t7，u0-u3}</span><span class="sxs-lookup"><span data-stu-id="9f69e-192">Descriptor table: { t2-t7, u0-u3 }</span></span>             | <span data-ttu-id="9f69e-193"> (6 SRVs + 4 UAVs) </span><span class="sxs-lookup"><span data-stu-id="9f69e-193">(6 SRVs + 4 UAVs)</span></span>                            |
| <span data-ttu-id="9f69e-194">\[2\]</span><span class="sxs-lookup"><span data-stu-id="9f69e-194">\[2\]</span></span>                  | <span data-ttu-id="9f69e-195">根 CBV： {b0}</span><span class="sxs-lookup"><span data-stu-id="9f69e-195">Root CBV: { b0 }</span></span>                               | <span data-ttu-id="9f69e-196"> (1 CBV、靜態資料) </span><span class="sxs-lookup"><span data-stu-id="9f69e-196">(1 CBV, static data)</span></span>                         |
| <span data-ttu-id="9f69e-197">\[3\]</span><span class="sxs-lookup"><span data-stu-id="9f69e-197">\[3\]</span></span>                  | <span data-ttu-id="9f69e-198">描述項資料表： {s0-s1}</span><span class="sxs-lookup"><span data-stu-id="9f69e-198">Descriptor table: { s0-s1 }</span></span>                    | <span data-ttu-id="9f69e-199"> (2 取樣器) </span><span class="sxs-lookup"><span data-stu-id="9f69e-199">(2 Samplers)</span></span>                                 |
| <span data-ttu-id="9f69e-200">\[4\]</span><span class="sxs-lookup"><span data-stu-id="9f69e-200">\[4\]</span></span>                  | <span data-ttu-id="9f69e-201">描述項資料表： {t8-未系結}</span><span class="sxs-lookup"><span data-stu-id="9f69e-201">Descriptor table: { t8 - unbounded }</span></span>           | <span data-ttu-id="9f69e-202"> (未系結 \# 的 SRVs、volatile 描述項) </span><span class="sxs-lookup"><span data-stu-id="9f69e-202">(unbounded \# of SRVs, volatile descriptors)</span></span> |
| <span data-ttu-id="9f69e-203">\[5\]</span><span class="sxs-lookup"><span data-stu-id="9f69e-203">\[5\]</span></span>                  | <span data-ttu-id="9f69e-204">描述項資料表： { (t0，space1) -未系結}</span><span class="sxs-lookup"><span data-stu-id="9f69e-204">Descriptor table: { (t0, space1) - unbounded }</span></span> | <span data-ttu-id="9f69e-205"> (未系結 \# 的 SRVs、volatile 描述項) </span><span class="sxs-lookup"><span data-stu-id="9f69e-205">(unbounded \# of SRVs, volatile descriptors)</span></span> |
| <span data-ttu-id="9f69e-206">\[6\]</span><span class="sxs-lookup"><span data-stu-id="9f69e-206">\[6\]</span></span>                  | <span data-ttu-id="9f69e-207">描述項資料表： {b1}</span><span class="sxs-lookup"><span data-stu-id="9f69e-207">Descriptor table: { b1 }</span></span>                       | <span data-ttu-id="9f69e-208"> (1 CBV、靜態資料) </span><span class="sxs-lookup"><span data-stu-id="9f69e-208">(1 CBV, static data)</span></span>                         |



 

<span data-ttu-id="9f69e-209">如果根本簽章大部分的部分都是在大部分的時間內使用，則可能比太頻繁地切換根簽章更好。</span><span class="sxs-lookup"><span data-stu-id="9f69e-209">If most parts of the root signature get used most of the time it can be better than having to switch the root signature too frequently.</span></span> <span data-ttu-id="9f69e-210">應用程式應該將根簽章中的專案排序為最常變更為最少。</span><span class="sxs-lookup"><span data-stu-id="9f69e-210">Applications should sort entries in the root signature from most frequently changing to least.</span></span> <span data-ttu-id="9f69e-211">當應用程式將系結變更為根簽章的任何部分時，驅動程式可能必須複製部分或全部的根簽章狀態，而這可能會在乘以許多狀態變更時成為重要成本。</span><span class="sxs-lookup"><span data-stu-id="9f69e-211">When an app changes the bindings to any part of the root signature, the driver may have to make a copy of some or all of root signature state, which can become a nontrivial cost when multiplied across many state changes.</span></span>

<span data-ttu-id="9f69e-212">此外，根簽章會定義在著色器註冊 s3 執行非等向材質篩選的靜態取樣器。</span><span class="sxs-lookup"><span data-stu-id="9f69e-212">In addition, the root signature will define a static sampler that does anisotropic texture filtering at shader register s3.</span></span>

<span data-ttu-id="9f69e-213">系結這個根簽章之後，可以將描述中繼資料表、根 CBV 和常數指派給 \[ 0.. 6 \] 參數空間。</span><span class="sxs-lookup"><span data-stu-id="9f69e-213">After this root signature is bound, descriptor tables, root CBV and constants can be assigned to the \[0..6\] parameter space.</span></span> <span data-ttu-id="9f69e-214">例如，描述元堆積中 (範圍的描述項資料表) 可以在每個根參數 \[ 1 \] 和 \[ 3. 6 上 \] 系結。</span><span class="sxs-lookup"><span data-stu-id="9f69e-214">e.g. descriptor tables (ranges in a descriptor heap) can be bound at each of root parameters \[1\] and \[3..6\].</span></span>

``` syntax
CD3DX12_DESCRIPTOR_RANGE1 DescRange[6];

DescRange[0].Init(D3D12_DESCRIPTOR_RANGE_SRV,6,2); // t2-t7
DescRange[1].Init(D3D12_DESCRIPTOR_RANGE_UAV,4,0); // u0-u3
DescRange[2].Init(D3D12_DESCRIPTOR_RANGE_SAMPLER,2,0); // s0-s1
DescRange[3].Init(D3D12_DESCRIPTOR_RANGE_SRV,-1,8, 0,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE); // t8-unbounded
DescRange[4].Init(D3D12_DESCRIPTOR_RANGE_SRV,-1,0,1,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE); 
                                                            // (t0,space1)-unbounded
DescRange[5].Init(D3D12_DESCRIPTOR_RANGE_CBV,1,1,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC); // b1

CD3DX12_ROOT_PARAMETER1 RP[7];

RP[0].InitAsConstants(3,2); // 3 constants at b2
RP[1].InitAsDescriptorTable(2,&DescRange[0]); // 2 ranges t2-t7 and u0-u3
RP[2].InitAsConstantBufferView(0, 0, 
                               D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC); // b0
RP[3].InitAsDescriptorTable(1,&DescRange[2]); // s0-s1
RP[4].InitAsDescriptorTable(1,&DescRange[3]); // t8-unbounded
RP[5].InitAsDescriptorTable(1,&DescRange[4]); // (t0,space1)-unbounded
RP[6].InitAsDescriptorTable(1,&DescRange[5]); // b1

CD3DX12_STATIC_SAMPLER StaticSamplers[1];
StaticSamplers[0].Init(3, D3D12_FILTER_ANISOTROPIC); // s3
CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC RootSig(7,RP,1,StaticSamplers);
ID3DBlob* pSerializedRootSig;
CheckHR(D3D12SerializeVersionedRootSignature(&RootSig,pSerializedRootSig)); 

ID3D12RootSignature* pRootSignature;
hr = CheckHR(pDevice->CreateRootSignature(
    pSerializedRootSig->GetBufferPointer(),pSerializedRootSig->GetBufferSize(),
    __uuidof(ID3D12RootSignature),
    &pRootSignature));
```

<span data-ttu-id="9f69e-215">下列程式碼說明如何在圖形命令清單上使用上述的根簽章。</span><span class="sxs-lookup"><span data-stu-id="9f69e-215">The following code illustrates how the above root signature might be used on a graphics command list.</span></span>

``` syntax
InitializeMyDescriptorHeapContentsAheadOfTime(); // for simplicity of the 
                                                 // example
CreatePipelineStatesAhreadOfTime(pRootSignature); // The root signature is passed into 
                                     // shader / pipeline state creation
...

ID3D12DescriptorHeap* pHeaps[2] = {pCommonHeap, pSamplerHeap};
pGraphicsCommandList->SetDescriptorHeaps(2,pHeaps);
pGraphicsCommandList->SetGraphicsRootSignature(pRootSignature);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                        6,heapOffsetForMoreData,DescRange[5].NumDescriptors);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(5,heapOffsetForMisc,5000); 
pGraphicsCommandList->SetGraphicsRootDescriptorTable(4,heapOffsetForTerrain,20000);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                        3,heapOffsetForSamplers,DescRange[2].NumDescriptors);
pGraphicsCommandList->SetComputeRootConstantBufferView(2,pDynamicCBHeap,&CBVDesc);

MY_PER_DRAW_STUFF stuff;
InitMyPerDrawStuff(&stuff);
pGraphicsCommandList->SetSetGraphicsRoot32BitConstants(
                        0,&stuff,0,RTSlot[0].Constants.Num32BitValues);

SetMyRTVAndOtherMiscBindings();

for(UINT i = 0; i < numObjects; i++)
{
    pGraphicsCommandList->SetPipelineState(PSO[i]);
    pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                    1,heapOffsetForFooAndBar[i],DescRange[1].NumDescriptors);
    pGraphicsCommandList->SetGraphicsRoot32BitConstant(0,&i,1,drawIDOffset);
    SetMyIndexBuffers(i);
    pGraphicsCommandList->DrawIndexedInstanced(...);
}
```

## <a name="related-topics"></a><span data-ttu-id="9f69e-216">相關主題</span><span class="sxs-lookup"><span data-stu-id="9f69e-216">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f69e-217">根簽章</span><span class="sxs-lookup"><span data-stu-id="9f69e-217">Root Signatures</span></span>](root-signatures.md)
</dt> <dt>

[<span data-ttu-id="9f69e-218">在 HLSL 中指定根簽章</span><span class="sxs-lookup"><span data-stu-id="9f69e-218">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="9f69e-219">使用根簽章</span><span class="sxs-lookup"><span data-stu-id="9f69e-219">Using a Root Signature</span></span>](using-a-root-signature.md)
</dt> </dl>

 

 
