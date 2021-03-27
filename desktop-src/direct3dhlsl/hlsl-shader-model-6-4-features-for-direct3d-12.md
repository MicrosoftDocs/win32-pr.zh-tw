---
title: HLSL 著色器模型6。4
description: 描述新增至 HLSL 著色器模型6.4 的機器學習內建函式。
ms.topic: article
ms.date: 02/21/2019
ms.openlocfilehash: 10e74b268243ab059c2d0945887a6d429d40bb53
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "103853528"
---
# <a name="hlsl-shader-model-64"></a><span data-ttu-id="c22a0-103">HLSL 著色器模型6。4</span><span class="sxs-lookup"><span data-stu-id="c22a0-103">HLSL Shader Model 6.4</span></span>

<span data-ttu-id="c22a0-104">描述新增至 HLSL 著色器模型6.4 的機器學習內建函式。</span><span class="sxs-lookup"><span data-stu-id="c22a0-104">Describes the machine learning intrinsics added to HLSL Shader Model 6.4.</span></span>

## <a name="shader-model-64"></a><span data-ttu-id="c22a0-105">著色器模型6。4</span><span class="sxs-lookup"><span data-stu-id="c22a0-105">Shader Model 6.4</span></span>
<span data-ttu-id="c22a0-106">這些內建函式是著色器模型6.4 的必要/支援功能。</span><span class="sxs-lookup"><span data-stu-id="c22a0-106">These intrinsics are a required/supported feature of Shader model 6.4.</span></span> <span data-ttu-id="c22a0-107">因此，除了確保使用著色器模型6.4 之外，不需要個別的功能位檢查。</span><span class="sxs-lookup"><span data-stu-id="c22a0-107">Consequently, no separate capability bit check is required, beyond assuring the use of Shader Model 6.4.</span></span> <span data-ttu-id="c22a0-108">這些常式的最小支援用戶端是 Windows 10 1903 版。</span><span class="sxs-lookup"><span data-stu-id="c22a0-108">The minimum supported client for these routines is Windows 10, version 1903.</span></span>

## <a name="shading-language-intrinsics"></a><span data-ttu-id="c22a0-109">網底語言內建函式</span><span class="sxs-lookup"><span data-stu-id="c22a0-109">Shading language intrinsics</span></span>

### <a name="unsigned-integer-dot-product-of-4-elements-and-accumulate"></a><span data-ttu-id="c22a0-110">4個元素的不帶正負號整數 Dot-Product 並累積</span><span class="sxs-lookup"><span data-stu-id="c22a0-110">Unsigned Integer Dot-Product of 4 Elements and Accumulate</span></span>
```syntax
uint32 dot4add_u8packed(uint32 a, uint32 b, uint32 acc); // ubyte4 a, b;
```
 
<span data-ttu-id="c22a0-111">具有 add 的4維不帶正負號的整數點乘積。</span><span class="sxs-lookup"><span data-stu-id="c22a0-111">A 4-dimensional unsigned integer dot-product with add.</span></span> <span data-ttu-id="c22a0-112">將兩個輸入 Dword 中每個對應的不帶正負號的8位 int 位元組配對在一起，並將結果加總為32位不帶正負號整數的整數。</span><span class="sxs-lookup"><span data-stu-id="c22a0-112">Multiplies together each corresponding pair of unsigned 8-bit int bytes in the two input DWORDs, and sums the results into the 32-bit unsigned integer accumulator.</span></span> <span data-ttu-id="c22a0-113">此指令會在單一32位寬 SIM資料通道內運作。</span><span class="sxs-lookup"><span data-stu-id="c22a0-113">This instruction operates within a single 32-bit wide SIMD lane.</span></span> <span data-ttu-id="c22a0-114">輸入也會假設為32位數量。</span><span class="sxs-lookup"><span data-stu-id="c22a0-114">The inputs are also assumed to be 32-bit quantities.</span></span>
 
### <a name="signed-integer-dot-product-of-4-elements-and-accumulate"></a><span data-ttu-id="c22a0-115">4個元素的帶正負號整數 Dot-Product 並累積</span><span class="sxs-lookup"><span data-stu-id="c22a0-115">Signed Integer Dot-Product of 4 Elements and Accumulate</span></span>
```syntax
int32 dot4add_i8packed(uint32 a, uint32 b, int32 acc); // signed byte4 a, b;
```

<span data-ttu-id="c22a0-116">具有 add 的4維帶正負號的整數點乘積。</span><span class="sxs-lookup"><span data-stu-id="c22a0-116">A 4-dimensional signed integer dot-product with add.</span></span> <span data-ttu-id="c22a0-117">將兩個輸入 Dword 中每個對應的帶正負號8位 int 位元組配對在一起，並將結果加總為32位帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="c22a0-117">Multiplies together each corresponding pair of signed 8-bit int bytes in the two input DWORDs, and sums the results into the 32-bit signed integer accumulator.</span></span> <span data-ttu-id="c22a0-118">此指令會在單一32位寬 SIM資料通道內運作。</span><span class="sxs-lookup"><span data-stu-id="c22a0-118">This instruction operates within a single 32-bit wide SIMD lane.</span></span> <span data-ttu-id="c22a0-119">輸入也會假設為32位數量。</span><span class="sxs-lookup"><span data-stu-id="c22a0-119">The inputs are also assumed to be 32-bit quantities.</span></span>
 
### <a name="single-precision-floating-point-2-element-dot-product-and-accumulate"></a><span data-ttu-id="c22a0-120">單精確度浮點數 2-元素 Dot-Product 和累積</span><span class="sxs-lookup"><span data-stu-id="c22a0-120">Single Precision Floating Point 2-Element Dot-Product and Accumulate</span></span>
```syntax
float dot2add( half2 a, half2 b, float acc );
```

<span data-ttu-id="c22a0-121">具有 add 的 half2 向量之二維浮點數點乘積。</span><span class="sxs-lookup"><span data-stu-id="c22a0-121">A 2-dimensional floating point dot-product of half2 vectors with add.</span></span> <span data-ttu-id="c22a0-122">將兩個半精確度浮點數輸入向量的元素相乘，並將結果加總為32位浮點數。</span><span class="sxs-lookup"><span data-stu-id="c22a0-122">Multiplies the elements of the two half-precision float input vectors together and sums the results into the 32-bit float accumulator.</span></span> <span data-ttu-id="c22a0-123">此指示會在單一32位寬 SIM資料通道內運作。</span><span class="sxs-lookup"><span data-stu-id="c22a0-123">This instructions operates within a single 32-bit wide SIMD lane.</span></span> <span data-ttu-id="c22a0-124">輸入是封裝至相同通道的16位數量。</span><span class="sxs-lookup"><span data-stu-id="c22a0-124">The inputs are 16-bit quantities packed into the same lane.</span></span>

<span data-ttu-id="c22a0-125">這涵蓋在低精確度功能位之下 (表示) 提供原生半和簡短支援。</span><span class="sxs-lookup"><span data-stu-id="c22a0-125">This is covered under the low-precision feature bit (indicating that native half and short support are present).</span></span>

### <a name="sv_shadingrate"></a><span data-ttu-id="c22a0-126">SV_ShadingRate</span><span class="sxs-lookup"><span data-stu-id="c22a0-126">SV_ShadingRate</span></span>
```syntax
uint shadingRate : SV_ShadingRate
```

<span data-ttu-id="c22a0-127">不帶正負號的整數，代表圖元著色器的每個調用所寫入的目標圖元數目。</span><span class="sxs-lookup"><span data-stu-id="c22a0-127">An unsigned integer representing how many target pixels are written by each invocation of the pixel shader.</span></span> <span data-ttu-id="c22a0-128">有效的值屬於 [D3D12_SHADING_RATE](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate)的列舉值集。</span><span class="sxs-lookup"><span data-stu-id="c22a0-128">Valid values belong to set of enumeration values [D3D12_SHADING_RATE](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate).</span></span>

<span data-ttu-id="c22a0-129">此系統值適用于 [D3D12_VARIABLE_SHADING_RATE_TIER_2](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) 或更高版本的平臺。</span><span class="sxs-lookup"><span data-stu-id="c22a0-129">This system value is available on platforms that are [D3D12_VARIABLE_SHADING_RATE_TIER_2](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) or higher.</span></span> <span data-ttu-id="c22a0-130">您可以從最多一個頂點或幾何著色器階段寫入它。</span><span class="sxs-lookup"><span data-stu-id="c22a0-130">It can be written from at most one of vertex or geometry shader stages.</span></span> <span data-ttu-id="c22a0-131">您可以從圖元著色器階段讀取它。</span><span class="sxs-lookup"><span data-stu-id="c22a0-131">It can be read from the pixel shader stage.</span></span> <span data-ttu-id="c22a0-132">如需詳細資訊，請參閱 [可變速率陰影](../direct3d12/vrs.md)。</span><span class="sxs-lookup"><span data-stu-id="c22a0-132">For more information, see the [Variable-rate Shading](../direct3d12/vrs.md).</span></span>