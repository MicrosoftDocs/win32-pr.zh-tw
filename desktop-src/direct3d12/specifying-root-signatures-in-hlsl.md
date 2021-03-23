---
title: 在 HLSL 中指定根簽章
description: 在 HLSL 著色器模型5.1 中指定根簽章是在 c + + 程式碼中指定它們的替代方法。
ms.assetid: 399F5E91-B017-4F5E-9037-DC055407D96F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 236876e22c3e1e0bb849ec1e1bc7d45692c900d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548353"
---
# <a name="specifying-root-signatures-in-hlsl"></a><span data-ttu-id="c68c6-103">在 HLSL 中指定根簽章</span><span class="sxs-lookup"><span data-stu-id="c68c6-103">Specifying Root Signatures in HLSL</span></span>

<span data-ttu-id="c68c6-104">在 HLSL 著色器模型5.1 中指定根簽章是在 c + + 程式碼中指定它們的替代方法。</span><span class="sxs-lookup"><span data-stu-id="c68c6-104">Specifying root signatures in HLSL Shader Model 5.1 is an alternative to specifying them in C++ code.</span></span>

-   [<span data-ttu-id="c68c6-105">HLSL 根簽章的範例</span><span class="sxs-lookup"><span data-stu-id="c68c6-105">An example HLSL Root Signature</span></span>](#an-example-hlsl-root-signature)
    -   [<span data-ttu-id="c68c6-106">根簽章版本1。0</span><span class="sxs-lookup"><span data-stu-id="c68c6-106">Root Signature Version 1.0</span></span>](#root-signature-version-10)
    -   [<span data-ttu-id="c68c6-107">根簽章版本1。1</span><span class="sxs-lookup"><span data-stu-id="c68c6-107">Root Signature Version 1.1</span></span>](#root-signature-version-11)
-   [<span data-ttu-id="c68c6-108">RootFlags</span><span class="sxs-lookup"><span data-stu-id="c68c6-108">RootFlags</span></span>](#rootflags)
-   [<span data-ttu-id="c68c6-109">根常數</span><span class="sxs-lookup"><span data-stu-id="c68c6-109">Root Constants</span></span>](#root-constants)
-   [<span data-ttu-id="c68c6-110">可見度</span><span class="sxs-lookup"><span data-stu-id="c68c6-110">Visibility</span></span>](#visibility)
-   [<span data-ttu-id="c68c6-111">根層級 CBV</span><span class="sxs-lookup"><span data-stu-id="c68c6-111">Root-level CBV</span></span>](#root-level-cbv)
-   [<span data-ttu-id="c68c6-112">根目錄層級 SRV</span><span class="sxs-lookup"><span data-stu-id="c68c6-112">Root-level SRV</span></span>](#root-level-srv)
-   [<span data-ttu-id="c68c6-113">根層級 UAV</span><span class="sxs-lookup"><span data-stu-id="c68c6-113">Root-level UAV</span></span>](#root-level-uav)
-   [<span data-ttu-id="c68c6-114">描述項資料表</span><span class="sxs-lookup"><span data-stu-id="c68c6-114">Descriptor Table</span></span>](#descriptor-table)
-   [<span data-ttu-id="c68c6-115">靜態取樣器</span><span class="sxs-lookup"><span data-stu-id="c68c6-115">Static Sampler</span></span>](#static-sampler)
-   [<span data-ttu-id="c68c6-116">編譯 HLSL 的根簽章</span><span class="sxs-lookup"><span data-stu-id="c68c6-116">Compiling an HLSL root signature</span></span>](#compiling-an-hlsl-root-signature)
-   [<span data-ttu-id="c68c6-117">使用 FXC.EXE 編譯器操作根簽章</span><span class="sxs-lookup"><span data-stu-id="c68c6-117">Manipulating root signatures with the FXC compiler</span></span>](#manipulating-root-signatures-with-the-fxc-compiler)
-   [<span data-ttu-id="c68c6-118">注意事項</span><span class="sxs-lookup"><span data-stu-id="c68c6-118">Notes</span></span>](#notes)
-   [<span data-ttu-id="c68c6-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="c68c6-119">Related topics</span></span>](#related-topics)

## <a name="an-example-hlsl-root-signature"></a><span data-ttu-id="c68c6-120">HLSL 根簽章的範例</span><span class="sxs-lookup"><span data-stu-id="c68c6-120">An example HLSL Root Signature</span></span>

<span data-ttu-id="c68c6-121">根簽章可以在 HLSL 中指定為字串。</span><span class="sxs-lookup"><span data-stu-id="c68c6-121">A root signature can be specified in HLSL as a string.</span></span> <span data-ttu-id="c68c6-122">字串包含以逗號分隔的子句集合，其描述根簽章構成元件。</span><span class="sxs-lookup"><span data-stu-id="c68c6-122">The string contains a collection of comma-separated clauses that describe root signature constituent components.</span></span> <span data-ttu-id="c68c6-123">在 (PSO) 的任何一個管線狀態物件的著色器中，根簽章應該相同。</span><span class="sxs-lookup"><span data-stu-id="c68c6-123">The root signature should be identical across shaders for any one pipeline state object (PSO).</span></span> <span data-ttu-id="c68c6-124">請看以下範例：</span><span class="sxs-lookup"><span data-stu-id="c68c6-124">Here is an example:</span></span>

### <a name="root-signature-version-10"></a><span data-ttu-id="c68c6-125">根簽章版本1。0</span><span class="sxs-lookup"><span data-stu-id="c68c6-125">Root Signature Version 1.0</span></span>

``` syntax
#define MyRS1 "RootFlags( ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | " \
                         "DENY_VERTEX_SHADER_ROOT_ACCESS), " \
              "CBV(b0, space = 1), " \
              "SRV(t0), " \
              "UAV(u0, visibility = SHADER_VISIBILITY_GEOMETRY), " \
              "DescriptorTable( CBV(b0), " \
                               "UAV(u1, numDescriptors = 2), " \
                               "SRV(t1, numDescriptors = unbounded)), " \
              "DescriptorTable(Sampler(s0, numDescriptors = 2)), " \
              "RootConstants(num32BitConstants=1, b9), " \
              "DescriptorTable( UAV(u3), " \
                               "UAV(u4), " \
                               "UAV(u5, offset=1)), " \

              "StaticSampler(s2)," \
              "StaticSampler(s3, " \
                             "addressU = TEXTURE_ADDRESS_CLAMP, " \
                             "filter = FILTER_MIN_MAG_MIP_LINEAR )"
```

### <a name="root-signature-version-11"></a><span data-ttu-id="c68c6-126">根簽章版本1。1</span><span class="sxs-lookup"><span data-stu-id="c68c6-126">Root Signature Version 1.1</span></span>

<span data-ttu-id="c68c6-127">[根簽章版本 1.1](root-signature-version-1-1.md) 可針對根簽章描述元和資料啟用驅動程式優化。</span><span class="sxs-lookup"><span data-stu-id="c68c6-127">[Root Signature Version 1.1](root-signature-version-1-1.md) enables driver optimizations on root signature descriptors and data.</span></span>

``` syntax
#define MyRS1 "RootFlags( ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | " \
                         "DENY_VERTEX_SHADER_ROOT_ACCESS), " \
              "CBV(b0, space = 1, flags = DATA_STATIC), " \
              "SRV(t0), " \
              "UAV(u0), " \
              "DescriptorTable( CBV(b1), " \
                               "SRV(t1, numDescriptors = 8, " \
                               "        flags = DESCRIPTORS_VOLATILE), " \
                               "UAV(u1, numDescriptors = unbounded, " \
                               "        flags = DESCRIPTORS_VOLATILE)), " \
              "DescriptorTable(Sampler(s0, space=1, numDescriptors = 4)), " \
              "RootConstants(num32BitConstants=3, b10), " \
              "StaticSampler(s1)," \
              "StaticSampler(s2, " \
                             "addressU = TEXTURE_ADDRESS_CLAMP, " \
                             "filter = FILTER_MIN_MAG_MIP_LINEAR )"
```

<span data-ttu-id="c68c6-128">這項定義會提供下列根簽章，請注意：</span><span class="sxs-lookup"><span data-stu-id="c68c6-128">This definition would give the following root signature, noting:</span></span>

-   <span data-ttu-id="c68c6-129">使用預設參數。</span><span class="sxs-lookup"><span data-stu-id="c68c6-129">The use of default parameters.</span></span>
-   <span data-ttu-id="c68c6-130">b0 和 (b0，space = 1) 不會衝突</span><span class="sxs-lookup"><span data-stu-id="c68c6-130">b0 and (b0, space=1) do not conflict</span></span>
-   <span data-ttu-id="c68c6-131">只有幾何著色器可以看到 u0</span><span class="sxs-lookup"><span data-stu-id="c68c6-131">u0 is only visible to the geometry shader</span></span>
-   <span data-ttu-id="c68c6-132">u4 和 u5 的別名為堆積中的相同描述元</span><span class="sxs-lookup"><span data-stu-id="c68c6-132">u4 and u5 are aliased to the same descriptor in a heap</span></span>

![使用高階著色器語言指定的根簽章](images/hlsl-root-signature.png)

<span data-ttu-id="c68c6-134">HLSL 根簽章語言會與 c + + 根簽章 Api 緊密對應，且具有相當的表達能力。</span><span class="sxs-lookup"><span data-stu-id="c68c6-134">The HLSL root signature language closely corresponds to the C++ root signature APIs and has equivalent expressive power.</span></span> <span data-ttu-id="c68c6-135">根簽章會指定為一系列的子句，並以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="c68c6-135">The root signature is specified as a sequence of clauses, separated by comma.</span></span> <span data-ttu-id="c68c6-136">子句順序很重要，因為剖析的順序會決定根簽章中的位置位置。</span><span class="sxs-lookup"><span data-stu-id="c68c6-136">The order of clauses is important, as the order of parsing determines the slot position in the root signature.</span></span> <span data-ttu-id="c68c6-137">每個子句都接受一個或多個具名引數。</span><span class="sxs-lookup"><span data-stu-id="c68c6-137">Each clause takes one or more named parameters.</span></span> <span data-ttu-id="c68c6-138">但參數的順序並不重要。</span><span class="sxs-lookup"><span data-stu-id="c68c6-138">The order of parameters is not important, however.</span></span>

## <a name="rootflags"></a><span data-ttu-id="c68c6-139">RootFlags</span><span class="sxs-lookup"><span data-stu-id="c68c6-139">RootFlags</span></span>

<span data-ttu-id="c68c6-140">選擇性 *RootFlags* 子句會採用 0 (預設值來指出沒有旗標) ，或透過或 ' ' 運算子連接的一或多個預先定義的根旗標值 \| 。</span><span class="sxs-lookup"><span data-stu-id="c68c6-140">The optional *RootFlags* clause takes either 0 (the default value to indicate no flags), or one or several of predefined root flags values, connected via the OR ‘\|’ operator.</span></span> <span data-ttu-id="c68c6-141">允許的根旗標值是透過 [**D3D12 \_ 根簽章 \_ \_ 旗標**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags)來定義。</span><span class="sxs-lookup"><span data-stu-id="c68c6-141">The allowed root flag values are defined by [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).</span></span>

<span data-ttu-id="c68c6-142">例如：</span><span class="sxs-lookup"><span data-stu-id="c68c6-142">For example:</span></span>

``` syntax
RootFlags(0) // default value – no flags
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT)
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | DENY_VERTEX_SHADER_ROOT_ACCESS)
```

## <a name="root-constants"></a><span data-ttu-id="c68c6-143">根常數</span><span class="sxs-lookup"><span data-stu-id="c68c6-143">Root Constants</span></span>

<span data-ttu-id="c68c6-144">*RootConstants* 子句會指定根簽章中的根常數。</span><span class="sxs-lookup"><span data-stu-id="c68c6-144">The *RootConstants* clause specifies root constants in the root signature.</span></span> <span data-ttu-id="c68c6-145">有兩個必要參數： *num32BitConstants* 和 *bReg* (註冊對應到 *Cbuffer* 的 c + + api) 中的 *BaseShaderRegister* 。</span><span class="sxs-lookup"><span data-stu-id="c68c6-145">Two mandatory parameters are: *num32BitConstants* and *bReg* (the register corresponding to *BaseShaderRegister* in C++ APIs) of the *cbuffer*.</span></span> <span data-ttu-id="c68c6-146">C + + Api 中 (*RegisterSpace* 的空間) 和 *(c* + +) 參數中的參數都是選擇性的，而預設值為：</span><span class="sxs-lookup"><span data-stu-id="c68c6-146">The space (*RegisterSpace* in C++ APIs) and visibility (*ShaderVisibility* in C++) parameters are optional, and the default values are:</span></span>

``` syntax
RootConstants(num32BitConstants=N, bReg [, space=0, 
              visibility=SHADER_VISIBILITY_ALL ])
```

<span data-ttu-id="c68c6-147">例如：</span><span class="sxs-lookup"><span data-stu-id="c68c6-147">For example:</span></span>

``` syntax
RootConstants(num32BitConstants=3, b3)
```

## <a name="visibility"></a><span data-ttu-id="c68c6-148">可見性</span><span class="sxs-lookup"><span data-stu-id="c68c6-148">Visibility</span></span>

<span data-ttu-id="c68c6-149">可見度是選擇性參數，可具有 [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c68c6-149">Visibility is an optional parameter that can have one of the values from [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).</span></span>

<span data-ttu-id="c68c6-150">著色器 \_ 可見度全都會將 \_ 根引數廣播到所有著色器。</span><span class="sxs-lookup"><span data-stu-id="c68c6-150">SHADER\_VISIBILITY\_ALL broadcasts the root arguments to all shaders.</span></span> <span data-ttu-id="c68c6-151">在某些硬體上，這不會產生任何費用，但在其他硬體上，將資料分支至所有著色器階段會有成本。</span><span class="sxs-lookup"><span data-stu-id="c68c6-151">On some hardware this has no cost, but on other hardware there is a cost to fork the data to all the shader stages.</span></span> <span data-ttu-id="c68c6-152">設定其中一個選項（例如著色器 \_ 可見度 \_ 頂點）會將根引數限制為單一著色器階段。</span><span class="sxs-lookup"><span data-stu-id="c68c6-152">Setting one of the options, such as SHADER\_VISIBILITY\_VERTEX, limits the root argument to a single shader stage.</span></span>

<span data-ttu-id="c68c6-153">將根引數設定為單一著色器階段，可讓您在不同階段使用相同的系結名稱。</span><span class="sxs-lookup"><span data-stu-id="c68c6-153">Setting root arguments to single shader stages allows the same bind name to be used at different stages.</span></span> <span data-ttu-id="c68c6-154">例如，和 SRV 系結的 SRV 系結將 `t0,SHADER_VISIBILITY_VERTEX` `t0,SHADER_VISIBILITY_PIXEL` 會是有效的。</span><span class="sxs-lookup"><span data-stu-id="c68c6-154">For example, an SRV binding of `t0,SHADER_VISIBILITY_VERTEX` and SRV binding of `t0,SHADER_VISIBILITY_PIXEL` would be valid.</span></span> <span data-ttu-id="c68c6-155">但是，如果其中一個系結的可見度設定為，根簽章將 `t0,SHADER_VISIBILITY_ALL` 會無效。</span><span class="sxs-lookup"><span data-stu-id="c68c6-155">But if the visibility setting was `t0,SHADER_VISIBILITY_ALL` for one of the bindings, the root signature would be invalid.</span></span>

## <a name="root-level-cbv"></a><span data-ttu-id="c68c6-156">根層級 CBV</span><span class="sxs-lookup"><span data-stu-id="c68c6-156">Root-level CBV</span></span>

<span data-ttu-id="c68c6-157">`CBV` (常數緩衝區 view) 子句會指定根層級的常數緩衝區 b 註冊 Reg 專案。</span><span class="sxs-lookup"><span data-stu-id="c68c6-157">The `CBV` (constant buffer view) clause specifies a root-level constant buffer b-register Reg entry.</span></span> <span data-ttu-id="c68c6-158">請注意，這是純量專案;您無法指定根層級的範圍。</span><span class="sxs-lookup"><span data-stu-id="c68c6-158">Note that this is a scalar entry; it is not possible to specify a range for the root level.</span></span>

``` syntax
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-srv"></a><span data-ttu-id="c68c6-159">根目錄層級 SRV</span><span class="sxs-lookup"><span data-stu-id="c68c6-159">Root-level SRV</span></span>

<span data-ttu-id="c68c6-160">`SRV` (著色器資源檢視) 子句會指定根層級的 SRV t a t a t a t a t a t a t a</span><span class="sxs-lookup"><span data-stu-id="c68c6-160">The `SRV` (shader resource view) clause specifies a root-level SRV t-register Reg entry.</span></span> <span data-ttu-id="c68c6-161">請注意，這是純量專案;您無法指定根層級的範圍。</span><span class="sxs-lookup"><span data-stu-id="c68c6-161">Note that this is a scalar entry; it is not possible to specify a range for the root level.</span></span>

``` syntax
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-uav"></a><span data-ttu-id="c68c6-162">根層級 UAV</span><span class="sxs-lookup"><span data-stu-id="c68c6-162">Root-level UAV</span></span>

<span data-ttu-id="c68c6-163">`UAV` (未排序的存取 view) 子句會指定根層級的 UAV u 註冊 Reg 專案。</span><span class="sxs-lookup"><span data-stu-id="c68c6-163">The `UAV` (unordered access view) clause specifies a root-level UAV u-register Reg entry.</span></span> <span data-ttu-id="c68c6-164">請注意，這是純量專案;您無法指定根層級的範圍。</span><span class="sxs-lookup"><span data-stu-id="c68c6-164">Note that this is a scalar entry; it is not possible to specify a range for the root level.</span></span>

``` syntax
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_VOLATILE ])
```

<span data-ttu-id="c68c6-165">例如：</span><span class="sxs-lookup"><span data-stu-id="c68c6-165">For example:</span></span>

``` syntax
UAV(u3)
```

## <a name="descriptor-table"></a><span data-ttu-id="c68c6-166">描述項資料表</span><span class="sxs-lookup"><span data-stu-id="c68c6-166">Descriptor Table</span></span>

<span data-ttu-id="c68c6-167">`DescriptorTable`子句本身是以逗號分隔的描述元表子句清單，以及選擇性的可見度參數。</span><span class="sxs-lookup"><span data-stu-id="c68c6-167">The `DescriptorTable` clause is itself a list of comma-separated descriptor table clauses, as well as an optional visibility parameter.</span></span> <span data-ttu-id="c68c6-168">*DescriptorTable* 子句包括 CBV、SRV、UAV 和取樣器。</span><span class="sxs-lookup"><span data-stu-id="c68c6-168">The *DescriptorTable* clauses include CBV, SRV, UAV, and Sampler.</span></span> <span data-ttu-id="c68c6-169">請注意，其參數與根層級子句的參數不同。</span><span class="sxs-lookup"><span data-stu-id="c68c6-169">Note that their parameters differ from those of the root-level clauses.</span></span>

``` syntax
DescriptorTable( DTClause1, [ DTClause2, … DTClauseN,
                 visibility=SHADER_VISIBILITY_ALL ] )
```

<span data-ttu-id="c68c6-170">描述中繼資料表 `CBV` 有下列語法：</span><span class="sxs-lookup"><span data-stu-id="c68c6-170">The Descriptor Table `CBV` has the following syntax:</span></span>

``` syntax
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])   // Version 1.0
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND      // Version 1.1
          , flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

<span data-ttu-id="c68c6-171">例如：</span><span class="sxs-lookup"><span data-stu-id="c68c6-171">For example:</span></span>

``` syntax
DescriptorTable(CBV(b0),SRV(t3, numDescriptors=unbounded))
```

<span data-ttu-id="c68c6-172">強制參數 *bReg* 指定 cbuffer 範圍的起始登錄。</span><span class="sxs-lookup"><span data-stu-id="c68c6-172">The mandatory parameter *bReg* specifies the start Reg of the cbuffer range.</span></span> <span data-ttu-id="c68c6-173">*NumDescriptors* 參數會指定連續 cbuffer 範圍中的描述元數目;預設值為1。</span><span class="sxs-lookup"><span data-stu-id="c68c6-173">The *numDescriptors* parameter specifies the number of descriptors in the contiguous cbuffer range; the default value being 1.</span></span> <span data-ttu-id="c68c6-174">` [Reg, Reg + numDescriptors - 1]`當 *numDescriptors* 為數字時，專案會宣告 cbuffer 範圍。</span><span class="sxs-lookup"><span data-stu-id="c68c6-174">The entry declares a cbuffer range` [Reg, Reg + numDescriptors - 1]`, when *numDescriptors* is a number.</span></span> <span data-ttu-id="c68c6-175">如果 *numDescriptors* 等於「未系結」，則範圍為 `[Reg, UINT_MAX]` ，這表示應用程式必須確定它未參考超出範圍的區域。</span><span class="sxs-lookup"><span data-stu-id="c68c6-175">If *numDescriptors* is equal to "unbounded", the range is `[Reg, UINT_MAX]`, which means the app must ensure it is not referencing an out-of-bounds area.</span></span> <span data-ttu-id="c68c6-176">*Offset* 欄位代表 c + + api 中的 *OffsetInDescriptorsFromTableStart* 參數，也就是從資料表開頭開始，) 描述項中 (的位移。</span><span class="sxs-lookup"><span data-stu-id="c68c6-176">The *offset* field represents the *OffsetInDescriptorsFromTableStart* parameter in the C++ APIs, that is, the offset (in descriptors) from the start of the table.</span></span> <span data-ttu-id="c68c6-177">如果位移設定為描述 \_ \_ 項範圍位移 \_ 附加 (預設) ，則表示範圍是緊接在先前的範圍之後。</span><span class="sxs-lookup"><span data-stu-id="c68c6-177">If the offset is set to DESCRIPTOR\_RANGE\_OFFSET\_APPEND (the default), it means the range is directly after the previous range.</span></span> <span data-ttu-id="c68c6-178">但是，輸入特定位移可讓範圍彼此重迭，允許註冊別名。</span><span class="sxs-lookup"><span data-stu-id="c68c6-178">However, entering specific offsets does allow for ranges to overlap each other, allowing register aliasing.</span></span>

<span data-ttu-id="c68c6-179">描述中繼資料表 `SRV` 有下列語法：</span><span class="sxs-lookup"><span data-stu-id="c68c6-179">The Descriptor Table `SRV` has the following syntax:</span></span>

``` syntax
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

<span data-ttu-id="c68c6-180">這與描述項資料表專案類似 `CBV` ，不同之處在于指定的範圍適用于著色器資源檢視。</span><span class="sxs-lookup"><span data-stu-id="c68c6-180">This is similar to the descriptor table `CBV` entry, except the specified range is for shader resource views.</span></span>

<span data-ttu-id="c68c6-181">描述中繼資料表 `UAV` 有下列語法：</span><span class="sxs-lookup"><span data-stu-id="c68c6-181">The Descriptor Table `UAV` has the following syntax:</span></span>

``` syntax
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_VOLATILE ])
```

<span data-ttu-id="c68c6-182">這與描述項資料表專案類似 `CBV` ，不同之處在于指定的範圍適用于未排序的存取視圖。</span><span class="sxs-lookup"><span data-stu-id="c68c6-182">This is similar to the descriptor table `CBV` entry, except the specified range is for unordered access views.</span></span>

<span data-ttu-id="c68c6-183">描述中繼資料表 `Sampler` 有下列語法：</span><span class="sxs-lookup"><span data-stu-id="c68c6-183">The Descriptor Table `Sampler` has the following syntax:</span></span>

``` syntax
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])  // Version 1.0
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,    // Version 1.1
                flags=0 ])
```

<span data-ttu-id="c68c6-184">這類似于描述中繼資料表 `CBV` 專案，但指定的範圍適用于著色器取樣器。</span><span class="sxs-lookup"><span data-stu-id="c68c6-184">This is similar to the descriptor table `CBV` entry, except the specified range is for shader samplers.</span></span> <span data-ttu-id="c68c6-185">請注意，取樣器無法與相同描述項資料表中的其他類型的描述項混合 (，因為它們位於不同的描述項堆積) 中。</span><span class="sxs-lookup"><span data-stu-id="c68c6-185">Note that Samplers can’t be mixed with other types of descriptors in the same descriptor table (since they are in a separate descriptor heap).</span></span>

## <a name="static-sampler"></a><span data-ttu-id="c68c6-186">靜態取樣器</span><span class="sxs-lookup"><span data-stu-id="c68c6-186">Static Sampler</span></span>

<span data-ttu-id="c68c6-187">靜態取樣器代表 [**D3D12 \_ 靜態取樣 \_ 器 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) 結構。</span><span class="sxs-lookup"><span data-stu-id="c68c6-187">The static sampler represents the [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) structure.</span></span> <span data-ttu-id="c68c6-188">*StaticSampler* 的必要參數是純量、取樣器 s-註冊 Reg。其他參數則是選擇性的，預設值如下所示。</span><span class="sxs-lookup"><span data-stu-id="c68c6-188">The mandatory parameter for *StaticSampler* is a scalar, sampler s-register Reg. Other parameters are optional with default values shown below.</span></span> <span data-ttu-id="c68c6-189">大部分的欄位都接受一組預先定義的列舉。</span><span class="sxs-lookup"><span data-stu-id="c68c6-189">Most fields accept a set of predefined enums.</span></span>

``` syntax
StaticSampler( sReg,
              [ filter = FILTER_ANISOTROPIC, 
                addressU = TEXTURE_ADDRESS_WRAP,
                addressV = TEXTURE_ADDRESS_WRAP,
                addressW = TEXTURE_ADDRESS_WRAP,
                mipLODBias = 0.f,
                maxAnisotropy = 16,
                comparisonFunc = COMPARISON_LESS_EQUAL,
                borderColor = STATIC_BORDER_COLOR_OPAQUE_WHITE,
                minLOD = 0.f,         
                maxLOD = 3.402823466e+38f,
                space = 0, 
                visibility = SHADER_VISIBILITY_ALL ])
```

<span data-ttu-id="c68c6-190">例如：</span><span class="sxs-lookup"><span data-stu-id="c68c6-190">For example:</span></span>

``` syntax
StaticSampler(s4, filter=FILTER_MIN_MAG_MIP_LINEAR)
```

<span data-ttu-id="c68c6-191">參數選項與 c + + API 呼叫非常類似，但 *邊框* 除外，只限于 HLSL 中的列舉。</span><span class="sxs-lookup"><span data-stu-id="c68c6-191">The parameter options are very similar to the C++ API calls, except for *borderColor*, which is restricted to an enum in HLSL.</span></span>

<span data-ttu-id="c68c6-192">篩選欄位可以是 [**D3D12 \_ 篩選準則**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter)的其中一個。</span><span class="sxs-lookup"><span data-stu-id="c68c6-192">The filter field can be one of [**D3D12\_FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter).</span></span>

<span data-ttu-id="c68c6-193">[位址] 欄位可以是 [**D3D12 \_ 材質 \_ 位址 \_ 模式**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode)的其中一種。</span><span class="sxs-lookup"><span data-stu-id="c68c6-193">The address fields can each be one of [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode).</span></span>

<span data-ttu-id="c68c6-194">比較函數可以是 [**D3D12 \_ 比較 \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func)的其中一個。</span><span class="sxs-lookup"><span data-stu-id="c68c6-194">The comparison function can be one of [**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func).</span></span>

<span data-ttu-id="c68c6-195">[框線色彩] 欄位可以是 [**D3D12 \_ 靜態 \_ 框線 \_ 色彩**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color)的其中一個。</span><span class="sxs-lookup"><span data-stu-id="c68c6-195">The border color field can be one of [**D3D12\_STATIC\_BORDER\_COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color).</span></span>

<span data-ttu-id="c68c6-196">可見度可以是 [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)的其中之一。</span><span class="sxs-lookup"><span data-stu-id="c68c6-196">Visibility can be one of [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).</span></span>

## <a name="compiling-an-hlsl-root-signature"></a><span data-ttu-id="c68c6-197">編譯 HLSL 的根簽章</span><span class="sxs-lookup"><span data-stu-id="c68c6-197">Compiling an HLSL root signature</span></span>

<span data-ttu-id="c68c6-198">有兩種機制可編譯 HLSL 的根簽章。</span><span class="sxs-lookup"><span data-stu-id="c68c6-198">There are two mechanisms to compile an HLSL root signature.</span></span> <span data-ttu-id="c68c6-199">首先，您可以使用下列範例中的 *RootSignature* 屬性，將根簽章字串附加至特定著色器 (在下列範例中，使用 **MyRS1** 進入點) ：</span><span class="sxs-lookup"><span data-stu-id="c68c6-199">First, it is possible to attach a root signature string to a particular shader via the *RootSignature* attribute (in the following example, using the **MyRS1** entry point):</span></span>

``` syntax
[RootSignature(MyRS1)]
float4 main(float4 coord : COORD) : SV_Target
{
…
}
```

<span data-ttu-id="c68c6-200">編譯器會建立並驗證著色器的根簽章 blob，並將其與著色器位元組程式碼一起內嵌到著色器 blob 中。</span><span class="sxs-lookup"><span data-stu-id="c68c6-200">The compiler will create and verify the root signature blob for the shader and embed it alongside the shader byte code into the shader blob.</span></span> <span data-ttu-id="c68c6-201">編譯器支援著色器模型5.0 和更新版本的根簽章語法。</span><span class="sxs-lookup"><span data-stu-id="c68c6-201">The compiler supports root signature syntax for shader model 5.0 and higher.</span></span> <span data-ttu-id="c68c6-202">如果根簽章內嵌于著色器模型5.0 著色器中，而且該著色器會傳送至 D3D11 執行時間（而不是 D3D12），則 D3D11 會以無訊息方式忽略根簽章部分。</span><span class="sxs-lookup"><span data-stu-id="c68c6-202">If a root signature is embedded in a shader model 5.0 shader and that shader is sent to the D3D11 runtime, as opposed to D3D12, the root signature portion will get silently ignored by D3D11.</span></span>

<span data-ttu-id="c68c6-203">另一種機制是建立獨立的根簽章 blob，可能會使用大量著色器來重複使用它，以節省空間。</span><span class="sxs-lookup"><span data-stu-id="c68c6-203">The other mechanism is to create a standalone root signature blob, perhaps to reuse it with a large set of shaders, saving space.</span></span> <span data-ttu-id="c68c6-204">[效果編譯器工具](/windows/desktop/direct3dtools/fxc) (fxc.exe) 支援 **rootsig \_ 1 \_ 0** 和 **rootsig \_ 1 \_ 1** 著色器模型。</span><span class="sxs-lookup"><span data-stu-id="c68c6-204">The [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) (FXC) supports both **rootsig\_1\_0** and **rootsig\_1\_1** shader models.</span></span> <span data-ttu-id="c68c6-205">定義字串的名稱是透過一般的/E 引數所指定。</span><span class="sxs-lookup"><span data-stu-id="c68c6-205">The name of the define string is specified via the usual /E argument.</span></span> <span data-ttu-id="c68c6-206">例如：</span><span class="sxs-lookup"><span data-stu-id="c68c6-206">For example:</span></span>

``` syntax
fxc.exe /T rootsig_1_1 MyRS1.hlsl /E MyRS1 /Fo MyRS1.fxo
```

<span data-ttu-id="c68c6-207">請注意，根簽章字串定義也可以在命令列上傳遞，例如/D MyRS1 = "..."。</span><span class="sxs-lookup"><span data-stu-id="c68c6-207">Note that the root signature string define can also be passed on the command line, e.g, /D MyRS1=”…”.</span></span>

## <a name="manipulating-root-signatures-with-the-fxc-compiler"></a><span data-ttu-id="c68c6-208">使用 FXC.EXE 編譯器操作根簽章</span><span class="sxs-lookup"><span data-stu-id="c68c6-208">Manipulating root signatures with the FXC compiler</span></span>

<span data-ttu-id="c68c6-209">FXC.EXE 編譯器會從 HLSL 來源檔案建立著色器位元組程式碼。</span><span class="sxs-lookup"><span data-stu-id="c68c6-209">The FXC compiler creates shader byte-code from HLSL source files.</span></span> <span data-ttu-id="c68c6-210">此編譯器有許多選擇性參數，請參閱 [效果編譯器工具](/windows/desktop/direct3dtools/fxc)。</span><span class="sxs-lookup"><span data-stu-id="c68c6-210">There are a lot of optional parameters for this compiler, refer to the [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc).</span></span>

<span data-ttu-id="c68c6-211">為了管理 HLSL 撰寫的根簽章，下表提供使用 FXC.EXE 的一些範例。</span><span class="sxs-lookup"><span data-stu-id="c68c6-211">For managing HLSL authored root signatures, the following table gives some examples of using FXC.</span></span>



| <span data-ttu-id="c68c6-212">線條</span><span class="sxs-lookup"><span data-stu-id="c68c6-212">Line</span></span> | <span data-ttu-id="c68c6-213">命令列</span><span class="sxs-lookup"><span data-stu-id="c68c6-213">Command line</span></span>                                                                 | <span data-ttu-id="c68c6-214">描述</span><span class="sxs-lookup"><span data-stu-id="c68c6-214">Description</span></span>                                                                                                                                                                                                                              |
|------|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c68c6-215">1</span><span class="sxs-lookup"><span data-stu-id="c68c6-215">1</span></span>    | `fxc /T ps_5_1 shaderWithRootSig.hlsl /Fo rs1.fxo`                           | <span data-ttu-id="c68c6-216">編譯圖元著色器5.1 目標的著色器，著色器來源位於 shaderWithRootSig. hlsl 檔案中，其中包含根簽章。</span><span class="sxs-lookup"><span data-stu-id="c68c6-216">Compiles a shader for the pixel shader 5.1 target, the shader source is in the shaderWithRootSig.hlsl file, which includes a root signature.</span></span> <span data-ttu-id="c68c6-217">著色器和根簽章會編譯為 rs1. fxo 二進位檔案中的個別 blob。</span><span class="sxs-lookup"><span data-stu-id="c68c6-217">The shader and root signature are compiled as separate blobs in the rs1.fxo binary file.</span></span>    |
| <span data-ttu-id="c68c6-218">2</span><span class="sxs-lookup"><span data-stu-id="c68c6-218">2</span></span>    | `fxc /dumpbin rs1.fxo /extractrootsignature /Fo rs1.rs.fxo`                  | <span data-ttu-id="c68c6-219">從行1建立的檔案中解壓縮根簽章，讓 rs1 檔案只包含根簽章。</span><span class="sxs-lookup"><span data-stu-id="c68c6-219">Extracts the root signature from the file created by line 1, so the rs1.rs.fxo file contains just a root signature.</span></span>                                                                                                                      |
| <span data-ttu-id="c68c6-220">3</span><span class="sxs-lookup"><span data-stu-id="c68c6-220">3</span></span>    | `fxc /dumpbin rs1.fxo /Qstrip_rootsignature /Fo rs1.stripped.fxo`            | <span data-ttu-id="c68c6-221">從行1建立的檔案中移除根簽章，因此 rs1 fxo 檔案包含沒有根簽章的著色器。</span><span class="sxs-lookup"><span data-stu-id="c68c6-221">Removes the root signature from the file created by line 1, so the rs1.stripped.fxo file contains a shader with no root signature.</span></span>                                                                                                       |
| <span data-ttu-id="c68c6-222">4</span><span class="sxs-lookup"><span data-stu-id="c68c6-222">4</span></span>    | `fxc /dumpbin rs1.stripped.fxo /setrootsignature rs1.rs.fxo /Fo rs1.new.fxo` | <span data-ttu-id="c68c6-223">將位於個別檔案中的著色器和根簽章合併為包含這兩個 blob 的二進位檔案。</span><span class="sxs-lookup"><span data-stu-id="c68c6-223">Combines a shader and root signature that are in separate files into a binary file containing both blobs.</span></span> <span data-ttu-id="c68c6-224">在此範例中，rs1 會與行1中的 rs1. fx0 相同。</span><span class="sxs-lookup"><span data-stu-id="c68c6-224">In this example rs1.new.fx0 would be identical to rs1.fx0 in line 1.</span></span>                                                           |
| <span data-ttu-id="c68c6-225">5</span><span class="sxs-lookup"><span data-stu-id="c68c6-225">5</span></span>    | `fxc /T rootsig_1_0 rootSigAndMaybeShaderInHereToo.hlsl /E RS1 /Fo rs2.fxo`  | <span data-ttu-id="c68c6-226">從可能包含不只是根簽章的來源，建立獨立的根簽章二進位檔案。</span><span class="sxs-lookup"><span data-stu-id="c68c6-226">Creates a stand-alone root signature binary file from a source that may contain more than just a root signature.</span></span> <span data-ttu-id="c68c6-227">請注意 rootsig \_ 1 \_ 0 目標，而該 RS1 是根簽章的名稱 (\# 在 HLSL 檔中定義) 宏字串。</span><span class="sxs-lookup"><span data-stu-id="c68c6-227">Note the rootsig\_1\_0 target, and that RS1 is the name of the root signature (\#define) macro string in the HLSL file.</span></span> |



 

<span data-ttu-id="c68c6-228">透過 FXC.EXE 提供的功能也可透過程式設計的方式使用 [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) 函式。</span><span class="sxs-lookup"><span data-stu-id="c68c6-228">The functionality available through FXC is also available programmatically using the [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) function.</span></span> <span data-ttu-id="c68c6-229">此呼叫會使用根簽章或獨立的根簽章來編譯著色器 (設定 rootsig \_ 1 \_ 0 目標) 。</span><span class="sxs-lookup"><span data-stu-id="c68c6-229">This call compiles a shader with a root signature, or stand-alone root signature (setting the rootsig\_1\_0 target).</span></span> <span data-ttu-id="c68c6-230">[**D3DGetBlobPart**](/windows/desktop/direct3dhlsl/d3dgetblobpart) 和 [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart) 可以解壓縮根簽章，並將其附加至現有的 blob。</span><span class="sxs-lookup"><span data-stu-id="c68c6-230">[**D3DGetBlobPart**](/windows/desktop/direct3dhlsl/d3dgetblobpart) and [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart) can extract and attach root signatures to an existing blob.</span></span><span data-ttu-id="c68c6-231">D3D \_ blob \_ 根簽章 \_ 用來指定根簽章 blob 元件類型。</span><span class="sxs-lookup"><span data-stu-id="c68c6-231">  D3D\_BLOB\_ROOT\_SIGNATURE is used to specify the root signature blob part type.</span></span> <span data-ttu-id="c68c6-232">[**D3DStripShader**](/windows/desktop/direct3dhlsl/d3dstripshader) 會使用 \_ \_ 從 blob) 的 D3DCOMPILER 帶根簽章旗標， (移除根簽章 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c68c6-232">[**D3DStripShader**](/windows/desktop/direct3dhlsl/d3dstripshader) removes the root signature (using the D3DCOMPILER\_STRIP\_ROOT\_SIGNATURE flag) from the blob.</span></span>

## <a name="notes"></a><span data-ttu-id="c68c6-233">備註</span><span class="sxs-lookup"><span data-stu-id="c68c6-233">Notes</span></span>

> [!Note]  
> <span data-ttu-id="c68c6-234">雖然強烈建議您以離線編譯著色器，但如果著色器必須在執行時間編譯，請參閱 [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2)的備註。</span><span class="sxs-lookup"><span data-stu-id="c68c6-234">Whereas the offline compilation of shaders is strongly recommended, if shaders have to be compiled at runtime, refer to the remarks for [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2).</span></span>

 

> [!Note]  
> <span data-ttu-id="c68c6-235">現有的 HLSL 資產不需要變更，即可處理要搭配它們使用的根簽章。</span><span class="sxs-lookup"><span data-stu-id="c68c6-235">Existing HLSL assets do not need to be changed to handle root signatures to be used with them.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c68c6-236">相關主題</span><span class="sxs-lookup"><span data-stu-id="c68c6-236">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c68c6-237">使用 HLSL 5.1 的動態索引</span><span class="sxs-lookup"><span data-stu-id="c68c6-237">Dynamic Indexing using HLSL 5.1</span></span>](dynamic-indexing-using-hlsl-5-1.md)
</dt> <dt>

[<span data-ttu-id="c68c6-238">適用于 Direct3D 12 的 HLSL 著色器模型5.1 功能</span><span class="sxs-lookup"><span data-stu-id="c68c6-238">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[<span data-ttu-id="c68c6-239">資源系結</span><span class="sxs-lookup"><span data-stu-id="c68c6-239">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="c68c6-240">HLSL 中的資源系結</span><span class="sxs-lookup"><span data-stu-id="c68c6-240">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="c68c6-241">根簽章</span><span class="sxs-lookup"><span data-stu-id="c68c6-241">Root Signatures</span></span>](root-signatures.md)
</dt> <dt>

[<span data-ttu-id="c68c6-242">著色器模型5。1</span><span class="sxs-lookup"><span data-stu-id="c68c6-242">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="c68c6-243">著色器指定的樣板參考值</span><span class="sxs-lookup"><span data-stu-id="c68c6-243">Shader Specified Stencil Reference Value</span></span>](shader-specified-stencil-reference-value.md)
</dt> <dt>

[<span data-ttu-id="c68c6-244">具類型的未排序存取視圖載入</span><span class="sxs-lookup"><span data-stu-id="c68c6-244">Typed Unordered Access View Loads</span></span>](typed-unordered-access-view-loads.md)
</dt> </dl>

 

 