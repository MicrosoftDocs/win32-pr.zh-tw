---
title: 'D3DCOMPILE 常數 (D3DCompiler) '
description: D3DCOMPILE 常數會指定編譯器如何編譯 HLSL 程式碼。
ms.assetid: 039627DD-D6A4-4EA3-8E91-D2A20770E6FF
topic_type:
- apiref
api_name:
- D3DCOMPILE_DEBUG
- D3DCOMPILE_SKIP_VALIDATION
- D3DCOMPILE_SKIP_OPTIMIZATION
- D3DCOMPILE_PACK_MATRIX_ROW_MAJOR
- D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR
- D3DCOMPILE_PARTIAL_PRECISION
- D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT
- D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT
- D3DCOMPILE_NO_PRESHADER
- D3DCOMPILE_AVOID_FLOW_CONTROL
- D3DCOMPILE_PREFER_FLOW_CONTROL
- D3DCOMPILE_ENABLE_STRICTNESS
- D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY
- D3DCOMPILE_IEEE_STRICTNESS
- D3DCOMPILE_OPTIMIZATION_LEVEL0
- D3DCOMPILE_OPTIMIZATION_LEVEL1
- D3DCOMPILE_OPTIMIZATION_LEVEL2
- D3DCOMPILE_OPTIMIZATION_LEVEL3
- D3DCOMPILE_WARNINGS_ARE_ERRORS
- D3DCOMPILE_RESOURCES_MAY_ALIAS
- D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES
- D3DCOMPILE_ALL_RESOURCES_BOUND
api_location:
- D3DCompiler.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfd396eef06260ae879a3bb816d0bd89a078ea53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196197"
---
# <a name="d3dcompile-constants"></a><span data-ttu-id="e5b37-103">D3DCOMPILE 常數</span><span class="sxs-lookup"><span data-stu-id="e5b37-103">D3DCOMPILE Constants</span></span>

<span data-ttu-id="e5b37-104">D3DCOMPILE 常數會指定編譯器如何編譯 HLSL 程式碼。</span><span class="sxs-lookup"><span data-stu-id="e5b37-104">The D3DCOMPILE constants specify how the compiler compiles the HLSL code.</span></span>

<dl> <dt>

<span data-ttu-id="e5b37-105"><span id="D3DCOMPILE_DEBUG"></span><span id="d3dcompile_debug"></span>**D3DCOMPILE \_ DEBUG**</span><span class="sxs-lookup"><span data-stu-id="e5b37-105"><span id="D3DCOMPILE_DEBUG"></span><span id="d3dcompile_debug"></span>**D3DCOMPILE\_DEBUG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b37-106"> (1 << 0) </span><span class="sxs-lookup"><span data-stu-id="e5b37-106">(1 << 0)</span></span>
</dt> <dt>



<span data-ttu-id="e5b37-107">指示編譯器將 debug 檔案/行/型別/符號資訊插入輸出程式碼中。</span><span class="sxs-lookup"><span data-stu-id="e5b37-107">Directs the compiler to insert debug file/line/type/symbol information into the output code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e5b37-108"><span id="D3DCOMPILE_SKIP_VALIDATION"></span><span id="d3dcompile_skip_validation"></span>**D3DCOMPILE \_ 略過 \_ 驗證**</span><span class="sxs-lookup"><span data-stu-id="e5b37-108"><span id="D3DCOMPILE_SKIP_VALIDATION"></span><span id="d3dcompile_skip_validation"></span>**D3DCOMPILE\_SKIP\_VALIDATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b37-109"> (1 << 1) </span><span class="sxs-lookup"><span data-stu-id="e5b37-109">(1 << 1)</span></span>
</dt> <dt>



<span data-ttu-id="e5b37-110">指示編譯器不要針對已知的功能和條件約束來驗證產生的程式碼。</span><span class="sxs-lookup"><span data-stu-id="e5b37-110">Directs the compiler not to validate the generated code against known capabilities and constraints.</span></span> <span data-ttu-id="e5b37-111">我們建議您只將此常數用於過去已成功編譯的著色器。</span><span class="sxs-lookup"><span data-stu-id="e5b37-111">We recommend that you use this constant only with shaders that have been successfully compiled in the past.</span></span> <span data-ttu-id="e5b37-112">DirectX 一律會在著色器設定為裝置之前先進行驗證。</span><span class="sxs-lookup"><span data-stu-id="e5b37-112">DirectX always validates shaders before it sets them to a device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e5b37-113"><span id="D3DCOMPILE_SKIP_OPTIMIZATION"></span><span id="d3dcompile_skip_optimization"></span>**D3DCOMPILE \_ 略過 \_ 優化**</span><span class="sxs-lookup"><span data-stu-id="e5b37-113"><span id="D3DCOMPILE_SKIP_OPTIMIZATION"></span><span id="d3dcompile_skip_optimization"></span>**D3DCOMPILE\_SKIP\_OPTIMIZATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b37-114"> (1 << 2) </span><span class="sxs-lookup"><span data-stu-id="e5b37-114">(1 << 2)</span></span>
</dt> <dt>



<span data-ttu-id="e5b37-115">指示編譯器在程式碼產生期間略過優化步驟。</span><span class="sxs-lookup"><span data-stu-id="e5b37-115">Directs the compiler to skip optimization steps during code generation.</span></span> <span data-ttu-id="e5b37-116">我們建議您只針對 debug 用途設定這個常數。</span><span class="sxs-lookup"><span data-stu-id="e5b37-116">We recommend that you set this constant for debug purposes only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e5b37-117"><span id="D3DCOMPILE_PACK_MATRIX_ROW_MAJOR"></span><span id="d3dcompile_pack_matrix_row_major"></span>**D3DCOMPILE \_ PACK \_ 矩陣資料 \_ 列 \_ 主要**</span><span class="sxs-lookup"><span data-stu-id="e5b37-117"><span id="D3DCOMPILE_PACK_MATRIX_ROW_MAJOR"></span><span id="d3dcompile_pack_matrix_row_major"></span>**D3DCOMPILE\_PACK\_MATRIX\_ROW\_MAJOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b37-118"> (1 << 3) </span><span class="sxs-lookup"><span data-stu-id="e5b37-118">(1 << 3)</span></span>
</dt> <dt>



<span data-ttu-id="e5b37-119">指示編譯器針對著色器的輸入和輸出，以資料列主要順序封裝矩陣。</span><span class="sxs-lookup"><span data-stu-id="e5b37-119">Directs the compiler to pack matrices in row-major order on input and output from the shader.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e5b37-120"><span id="D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR"></span><span id="d3dcompile_pack_matrix_column_major"></span>**D3DCOMPILE \_ PACK \_ 矩陣資料 \_ 行 \_ 主要**</span><span class="sxs-lookup"><span data-stu-id="e5b37-120"><span id="D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR"></span><span id="d3dcompile_pack_matrix_column_major"></span>**D3DCOMPILE\_PACK\_MATRIX\_COLUMN\_MAJOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b37-121"> (1 << 4) </span><span class="sxs-lookup"><span data-stu-id="e5b37-121">(1 << 4)</span></span>
</dt> <dt>



<span data-ttu-id="e5b37-122">指示編譯器將資料行主要順序的矩陣封裝在著色器的輸入和輸出上。</span><span class="sxs-lookup"><span data-stu-id="e5b37-122">Directs the compiler to pack matrices in column-major order on input and output from the shader.</span></span> <span data-ttu-id="e5b37-123">這種類型的封裝通常更有效率，因為一系列的點積可以接著執行向量矩陣乘法。</span><span class="sxs-lookup"><span data-stu-id="e5b37-123">This type of packing is generally more efficient because a series of dot-products can then perform vector-matrix multiplication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e5b37-124"><span id="D3DCOMPILE_PARTIAL_PRECISION"></span><span id="d3dcompile_partial_precision"></span>**D3DCOMPILE \_ 部分有效 \_ 位數**</span><span class="sxs-lookup"><span data-stu-id="e5b37-124"><span id="D3DCOMPILE_PARTIAL_PRECISION"></span><span id="d3dcompile_partial_precision"></span>**D3DCOMPILE\_PARTIAL\_PRECISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b37-125"> (1 << 5) </span><span class="sxs-lookup"><span data-stu-id="e5b37-125">(1 << 5)</span></span>
</dt> <dt>



<span data-ttu-id="e5b37-126">指示編譯器以部分有效位數執行所有計算。</span><span class="sxs-lookup"><span data-stu-id="e5b37-126">Directs the compiler to perform all computations with partial precision.</span></span> <span data-ttu-id="e5b37-127">如果您設定這個常數，編譯的程式碼可能會在某些硬體上執行得更快。</span><span class="sxs-lookup"><span data-stu-id="e5b37-127">If you set this constant, the compiled code might run faster on some hardware.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e5b37-128"><span id="D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_vs_software_no_opt"></span>**D3DCOMPILE \_ 強制 \_ VS \_ SOFTWARE \_ 無 \_ 選擇**</span><span class="sxs-lookup"><span data-stu-id="e5b37-128"><span id="D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_vs_software_no_opt"></span>**D3DCOMPILE\_FORCE\_VS\_SOFTWARE\_NO\_OPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b37-129"> (1 << 6) </span><span class="sxs-lookup"><span data-stu-id="e5b37-129">(1 << 6)</span></span>
</dt> <dt>



<span data-ttu-id="e5b37-130">指示編譯器針對下一個最高的著色器設定檔編譯頂點著色器。</span><span class="sxs-lookup"><span data-stu-id="e5b37-130">Directs the compiler to compile a vertex shader for the next highest shader profile.</span></span> <span data-ttu-id="e5b37-131">這個常數會開啟和優化的調試。</span><span class="sxs-lookup"><span data-stu-id="e5b37-131">This constant turns debugging on and optimizations off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e5b37-132"><span id="D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_ps_software_no_opt"></span>**D3DCOMPILE \_ 強制 \_ PS \_ 軟體 \_ 無 \_ OPT**</span><span class="sxs-lookup"><span data-stu-id="e5b37-132"><span id="D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_ps_software_no_opt"></span>**D3DCOMPILE\_FORCE\_PS\_SOFTWARE\_NO\_OPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b37-133"> (1 << 7) </span><span class="sxs-lookup"><span data-stu-id="e5b37-133">(1 << 7)</span></span>
</dt> <dt>



<span data-ttu-id="e5b37-134">指示編譯器針對下一個最高的著色器設定檔編譯圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="e5b37-134">Directs the compiler to compile a pixel shader for the next highest shader profile.</span></span> <span data-ttu-id="e5b37-135">這個常數也會開啟和優化的調試。</span><span class="sxs-lookup"><span data-stu-id="e5b37-135">This constant also turns debugging on and optimizations off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e5b37-136"><span id="D3DCOMPILE_NO_PRESHADER"></span><span id="d3dcompile_no_preshader"></span>**D3DCOMPILE \_ NO \_ PRESHADER**</span><span class="sxs-lookup"><span data-stu-id="e5b37-136"><span id="D3DCOMPILE_NO_PRESHADER"></span><span id="d3dcompile_no_preshader"></span>**D3DCOMPILE\_NO\_PRESHADER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b37-137"> (1 << 8) </span><span class="sxs-lookup"><span data-stu-id="e5b37-137">(1 << 8)</span></span>
</dt> <dt>



<span data-ttu-id="e5b37-138">指示編譯器停用 Preshaders。</span><span class="sxs-lookup"><span data-stu-id="e5b37-138">Directs the compiler to disable Preshaders.</span></span> <span data-ttu-id="e5b37-139">如果您設定這個常數，編譯器不會提取用於評估的靜態運算式。</span><span class="sxs-lookup"><span data-stu-id="e5b37-139">If you set this constant, the compiler does not pull out static expression for evaluation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e5b37-140"><span id="D3DCOMPILE_AVOID_FLOW_CONTROL"></span><span id="d3dcompile_avoid_flow_control"></span>**D3DCOMPILE \_ 避免 \_ 流量 \_ 控制**</span><span class="sxs-lookup"><span data-stu-id="e5b37-140"><span id="D3DCOMPILE_AVOID_FLOW_CONTROL"></span><span id="d3dcompile_avoid_flow_control"></span>**D3DCOMPILE\_AVOID\_FLOW\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b37-141"> (1 << 9) </span><span class="sxs-lookup"><span data-stu-id="e5b37-141">(1 << 9)</span></span>
</dt> <dt>



<span data-ttu-id="e5b37-142">指示編譯器在可能的情況下不使用流程式控制制結構。</span><span class="sxs-lookup"><span data-stu-id="e5b37-142">Directs the compiler to not use flow-control constructs where possible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e5b37-143"><span id="D3DCOMPILE_PREFER_FLOW_CONTROL"></span><span id="d3dcompile_prefer_flow_control"></span>**D3DCOMPILE \_ 偏好 \_ 流程 \_ 控制**</span><span class="sxs-lookup"><span data-stu-id="e5b37-143"><span id="D3DCOMPILE_PREFER_FLOW_CONTROL"></span><span id="d3dcompile_prefer_flow_control"></span>**D3DCOMPILE\_PREFER\_FLOW\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b37-144"> (1 << 10) </span><span class="sxs-lookup"><span data-stu-id="e5b37-144">(1 << 10)</span></span>
</dt> <dt>



<span data-ttu-id="e5b37-145">指示編譯器盡可能使用流程式控制制結構。</span><span class="sxs-lookup"><span data-stu-id="e5b37-145">Directs the compiler to use flow-control constructs where possible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e5b37-146"><span id="D3DCOMPILE_ENABLE_STRICTNESS"></span><span id="d3dcompile_enable_strictness"></span>**D3DCOMPILE \_ 啟用 \_ 嚴謹度**</span><span class="sxs-lookup"><span data-stu-id="e5b37-146"><span id="D3DCOMPILE_ENABLE_STRICTNESS"></span><span id="d3dcompile_enable_strictness"></span>**D3DCOMPILE\_ENABLE\_STRICTNESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b37-147"> (1 << 11) </span><span class="sxs-lookup"><span data-stu-id="e5b37-147">(1 << 11)</span></span>
</dt> <dt>



<span data-ttu-id="e5b37-148">強制執行嚴格的編譯，這可能不允許舊版語法。</span><span class="sxs-lookup"><span data-stu-id="e5b37-148">Forces strict compile, which might not allow for legacy syntax.</span></span>

<span data-ttu-id="e5b37-149">根據預設，編譯器會在已被取代的語法上停用嚴謹度。</span><span class="sxs-lookup"><span data-stu-id="e5b37-149">By default, the compiler disables strictness on deprecated syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e5b37-150"><span id="D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY"></span><span id="d3dcompile_enable_backwards_compatibility"></span>**D3DCOMPILE \_ 啟用 \_ 回溯 \_ 相容性**</span><span class="sxs-lookup"><span data-stu-id="e5b37-150"><span id="D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY"></span><span id="d3dcompile_enable_backwards_compatibility"></span>**D3DCOMPILE\_ENABLE\_BACKWARDS\_COMPATIBILITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b37-151"> (1 << 12) </span><span class="sxs-lookup"><span data-stu-id="e5b37-151">(1 << 12)</span></span>
</dt> <dt>



<span data-ttu-id="e5b37-152">指示編譯器啟用較舊的著色器，以編譯為 5 \_ 0 目標。</span><span class="sxs-lookup"><span data-stu-id="e5b37-152">Directs the compiler to enable older shaders to compile to 5\_0 targets.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e5b37-153"><span id="D3DCOMPILE_IEEE_STRICTNESS"></span><span id="d3dcompile_ieee_strictness"></span>**D3DCOMPILE \_ IEEE \_ 嚴謹度**</span><span class="sxs-lookup"><span data-stu-id="e5b37-153"><span id="D3DCOMPILE_IEEE_STRICTNESS"></span><span id="d3dcompile_ieee_strictness"></span>**D3DCOMPILE\_IEEE\_STRICTNESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b37-154"> (1 << 13) </span><span class="sxs-lookup"><span data-stu-id="e5b37-154">(1 << 13)</span></span>
</dt> <dt>



<span data-ttu-id="e5b37-155">強制 IEEE strict 編譯。</span><span class="sxs-lookup"><span data-stu-id="e5b37-155">Forces the IEEE strict compile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e5b37-156"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL0"></span><span id="d3dcompile_optimization_level0"></span>**D3DCOMPILE \_ 優化 \_ LEVEL0**</span><span class="sxs-lookup"><span data-stu-id="e5b37-156"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL0"></span><span id="d3dcompile_optimization_level0"></span>**D3DCOMPILE\_OPTIMIZATION\_LEVEL0**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b37-157"> (1 << 14) </span><span class="sxs-lookup"><span data-stu-id="e5b37-157">(1 << 14)</span></span>
</dt> <dt>



<span data-ttu-id="e5b37-158">指示編譯器使用最低的優化層級。</span><span class="sxs-lookup"><span data-stu-id="e5b37-158">Directs the compiler to use the lowest optimization level.</span></span> <span data-ttu-id="e5b37-159">如果您設定這個常數，編譯器可能會產生較慢的程式碼，但會更快速地產生程式碼。</span><span class="sxs-lookup"><span data-stu-id="e5b37-159">If you set this constant, the compiler might produce slower code but produces the code more quickly.</span></span> <span data-ttu-id="e5b37-160">當您反復開發著色器時，請設定這個常數。</span><span class="sxs-lookup"><span data-stu-id="e5b37-160">Set this constant when you develop the shader iteratively.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e5b37-161"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL1"></span><span id="d3dcompile_optimization_level1"></span>**D3DCOMPILE \_ 優化 \_ 級別1**</span><span class="sxs-lookup"><span data-stu-id="e5b37-161"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL1"></span><span id="d3dcompile_optimization_level1"></span>**D3DCOMPILE\_OPTIMIZATION\_LEVEL1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b37-162">0</span><span class="sxs-lookup"><span data-stu-id="e5b37-162">0</span></span>
</dt> <dt>



<span data-ttu-id="e5b37-163">指示編譯器使用第二個最低的優化層級。</span><span class="sxs-lookup"><span data-stu-id="e5b37-163">Directs the compiler to use the second lowest optimization level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e5b37-164"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL2"></span><span id="d3dcompile_optimization_level2"></span>**D3DCOMPILE \_ 優化的 \_ 級別2**</span><span class="sxs-lookup"><span data-stu-id="e5b37-164"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL2"></span><span id="d3dcompile_optimization_level2"></span>**D3DCOMPILE\_OPTIMIZATION\_LEVEL2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b37-165"> ( (1 << 14) \| (1 << 15) ) </span><span class="sxs-lookup"><span data-stu-id="e5b37-165">((1 << 14) \| (1 << 15))</span></span>
</dt> <dt>



<span data-ttu-id="e5b37-166">指示編譯器使用第二個最高的優化層級。</span><span class="sxs-lookup"><span data-stu-id="e5b37-166">Directs the compiler to use the second highest optimization level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e5b37-167"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL3"></span><span id="d3dcompile_optimization_level3"></span>**D3DCOMPILE \_ 優化- \_ 3**</span><span class="sxs-lookup"><span data-stu-id="e5b37-167"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL3"></span><span id="d3dcompile_optimization_level3"></span>**D3DCOMPILE\_OPTIMIZATION\_LEVEL3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b37-168"> (1 << 15) </span><span class="sxs-lookup"><span data-stu-id="e5b37-168">(1 << 15)</span></span>
</dt> <dt>



<span data-ttu-id="e5b37-169">指示編譯器使用最高的優化層級。</span><span class="sxs-lookup"><span data-stu-id="e5b37-169">Directs the compiler to use the highest optimization level.</span></span> <span data-ttu-id="e5b37-170">如果您設定這個常數，編譯器會產生最佳的程式碼，但可能需要花費很長的時間才能完成。</span><span class="sxs-lookup"><span data-stu-id="e5b37-170">If you set this constant, the compiler produces the best possible code but might take significantly longer to do so.</span></span> <span data-ttu-id="e5b37-171">當效能是最重要的因素時，請將此常數設定為最終的應用程式組建。</span><span class="sxs-lookup"><span data-stu-id="e5b37-171">Set this constant for final builds of an application when performance is the most important factor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e5b37-172"><span id="D3DCOMPILE_WARNINGS_ARE_ERRORS"></span><span id="d3dcompile_warnings_are_errors"></span>**D3DCOMPILE \_ 警告 \_ 為 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="e5b37-172"><span id="D3DCOMPILE_WARNINGS_ARE_ERRORS"></span><span id="d3dcompile_warnings_are_errors"></span>**D3DCOMPILE\_WARNINGS\_ARE\_ERRORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b37-173"> (1 << 18) </span><span class="sxs-lookup"><span data-stu-id="e5b37-173">(1 << 18)</span></span>
</dt> <dt>



<span data-ttu-id="e5b37-174">指示編譯器在編譯著色器程式碼時，將所有警告視為錯誤。</span><span class="sxs-lookup"><span data-stu-id="e5b37-174">Directs the compiler to treat all warnings as errors when it compiles the shader code.</span></span> <span data-ttu-id="e5b37-175">我們建議您針對新的著色器程式碼使用這個常數，如此您就可以解決所有警告，並減少難以找到的程式碼缺失數目。</span><span class="sxs-lookup"><span data-stu-id="e5b37-175">We recommend that you use this constant for new shader code, so that you can resolve all warnings and lower the number of hard-to-find code defects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e5b37-176"><span id="D3DCOMPILE_RESOURCES_MAY_ALIAS"></span><span id="d3dcompile_resources_may_alias"></span>**D3DCOMPILE \_ 資源 \_ 可能是 \_ 別名**</span><span class="sxs-lookup"><span data-stu-id="e5b37-176"><span id="D3DCOMPILE_RESOURCES_MAY_ALIAS"></span><span id="d3dcompile_resources_may_alias"></span>**D3DCOMPILE\_RESOURCES\_MAY\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b37-177"> (1 << 19) </span><span class="sxs-lookup"><span data-stu-id="e5b37-177">(1 << 19)</span></span>
</dt> <dt>



<span data-ttu-id="e5b37-178">指示編譯器假設未排序的存取視圖 (UAVs) 和著色器資源檢視 (SRVs) 可能是 cs \_ 5 0 的別名 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e5b37-178">Directs the compiler to assume that unordered access views (UAVs) and shader resource views (SRVs) may alias for cs\_5\_0.</span></span>

> [!Note]  
> <span data-ttu-id="e5b37-179">從 D3dcompiler47.dll 開始，這個編譯器常數是新的 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e5b37-179">This compiler constant is new starting with the D3dcompiler\_47.dll.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="e5b37-180"><span id="D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES"></span><span id="d3dcompile_enable_unbounded_descriptor_tables"></span>**D3DCOMPILE 啟用未系結的 \_ \_ 描述元 \_ \_ 資料表**</span><span class="sxs-lookup"><span data-stu-id="e5b37-180"><span id="D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES"></span><span id="d3dcompile_enable_unbounded_descriptor_tables"></span>**D3DCOMPILE\_ENABLE\_UNBOUNDED\_DESCRIPTOR\_TABLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b37-181"> (1 << 20) </span><span class="sxs-lookup"><span data-stu-id="e5b37-181">(1 << 20)</span></span>
</dt> <dt>



<span data-ttu-id="e5b37-182">指示編譯器啟用未系結的描述中繼資料表。</span><span class="sxs-lookup"><span data-stu-id="e5b37-182">Directs the compiler to enable unbounded descriptor tables.</span></span>

> [!Note]  
> <span data-ttu-id="e5b37-183">從 D3dcompiler47.dll 開始，這個編譯器常數是新的 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e5b37-183">This compiler constant is new starting with the D3dcompiler\_47.dll.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="e5b37-184"><span id="D3DCOMPILE_ALL_RESOURCES_BOUND"></span><span id="d3dcompile_all_resources_bound"></span>**D3DCOMPILE 所有系結的 \_ \_ 資源 \_**</span><span class="sxs-lookup"><span data-stu-id="e5b37-184"><span id="D3DCOMPILE_ALL_RESOURCES_BOUND"></span><span id="d3dcompile_all_resources_bound"></span>**D3DCOMPILE\_ALL\_RESOURCES\_BOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b37-185"> (1 << 21) </span><span class="sxs-lookup"><span data-stu-id="e5b37-185">(1 << 21)</span></span>
</dt> <dt>



<span data-ttu-id="e5b37-186">指示編譯器以確保所有資源都已系結。</span><span class="sxs-lookup"><span data-stu-id="e5b37-186">Directs the compiler to ensure all resources are bound.</span></span>

> [!Note]  
> <span data-ttu-id="e5b37-187">從 D3dcompiler47.dll 開始，這個編譯器常數是新的 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e5b37-187">This compiler constant is new starting with the D3dcompiler\_47.dll.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e5b37-188">規格需求</span><span class="sxs-lookup"><span data-stu-id="e5b37-188">Requirements</span></span>



| <span data-ttu-id="e5b37-189">需求</span><span class="sxs-lookup"><span data-stu-id="e5b37-189">Requirement</span></span> | <span data-ttu-id="e5b37-190">值</span><span class="sxs-lookup"><span data-stu-id="e5b37-190">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5b37-191">標頭</span><span class="sxs-lookup"><span data-stu-id="e5b37-191">Header</span></span><br/> | <dl> <span data-ttu-id="e5b37-192"><dt>D3DCompiler。h</dt></span><span class="sxs-lookup"><span data-stu-id="e5b37-192"><dt>D3DCompiler.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5b37-193">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e5b37-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5b37-194">D3DCompiler 常數</span><span class="sxs-lookup"><span data-stu-id="e5b37-194">D3DCompiler Constants</span></span>](dx-graphics-d3dcompiler-reference-constants.md)
</dt> </dl>

 

 





