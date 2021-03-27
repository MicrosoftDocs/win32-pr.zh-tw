---
title: 'CalculateLevelOfDetail (DirectX HLSL 材質物件) '
description: 計算詳細資料的層級。
ms.assetid: 7c7c3754-45a9-49c6-8420-aac22f776b15
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c59b8da97ff1cbe0bd88d6a49120a0a040cf3c30
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "104971804"
---
# <a name="calculatelevelofdetail-directx-hlsl-texture-object"></a><span data-ttu-id="46e94-103">CalculateLevelOfDetail (DirectX HLSL 材質物件) </span><span class="sxs-lookup"><span data-stu-id="46e94-103">CalculateLevelOfDetail (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="46e94-104">計算詳細資料的層級。</span><span class="sxs-lookup"><span data-stu-id="46e94-104">Calculates the level of detail.</span></span>



|                                                                 |
|-----------------------------------------------------------------|
| <span data-ttu-id="46e94-105">ret 物件. CalculateLevelOfDetail ( 取樣器 \_ 狀態 S，float x ) ;</span><span class="sxs-lookup"><span data-stu-id="46e94-105">ret Object.CalculateLevelOfDetail( sampler\_state S, float x );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="46e94-106">參數</span><span class="sxs-lookup"><span data-stu-id="46e94-106">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="46e94-107">項目</span><span class="sxs-lookup"><span data-stu-id="46e94-107">Item</span></span></th>
<th><span data-ttu-id="46e94-108">描述</span><span class="sxs-lookup"><span data-stu-id="46e94-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="46e94-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>物件</em></span><span class="sxs-lookup"><span data-stu-id="46e94-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="46e94-110">任何 <a href="dx-graphics-hlsl-to-type.md">材質物件</a> 類型 (除了 Texture2DMS 和 Texture2DMSArray) 之外。</span><span class="sxs-lookup"><span data-stu-id="46e94-110">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="46e94-111"><span id="S"></span><span id="s"></span><em>！</em></span><span class="sxs-lookup"><span data-stu-id="46e94-111"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="46e94-112">在 <a href="/windows/desktop/direct3d10/d3d10-effect-sampler-syntax">取樣器狀態</a>。</span><span class="sxs-lookup"><span data-stu-id="46e94-112">[in] A <a href="/windows/desktop/direct3d10/d3d10-effect-sampler-syntax">Sampler state</a>.</span></span> <span data-ttu-id="46e94-113">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="46e94-113">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="46e94-114"><span id="x"></span><span id="X"></span><em>X</em></span><span class="sxs-lookup"><span data-stu-id="46e94-114"><span id="x"></span><span id="X"></span><em>x</em></span></span><br/></td>
<td><span data-ttu-id="46e94-115">在線性插補值或值，這是介於0.0 和1.0 （含）之間的浮點數。</span><span class="sxs-lookup"><span data-stu-id="46e94-115">[in] The linear interpolation value or values, which is a floating-point number between 0.0 and 1.0 inclusive.</span></span> <span data-ttu-id="46e94-116">元件的數目取決於材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="46e94-116">The number of components is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="46e94-117">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="46e94-117">Texture-Object Type</span></span></th>
<th><span data-ttu-id="46e94-118">參數類型</span><span class="sxs-lookup"><span data-stu-id="46e94-118">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="46e94-119">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="46e94-119">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="46e94-120">float1</span><span class="sxs-lookup"><span data-stu-id="46e94-120">float1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="46e94-121">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="46e94-121">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="46e94-122">float2</span><span class="sxs-lookup"><span data-stu-id="46e94-122">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="46e94-123">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="46e94-123">Texture3D, TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="46e94-124">float3</span><span class="sxs-lookup"><span data-stu-id="46e94-124">float3</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="46e94-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="46e94-125">Return Value</span></span>

<span data-ttu-id="46e94-126">傳回匯出的」 LOD，也就是單一浮點值。</span><span class="sxs-lookup"><span data-stu-id="46e94-126">Returns the calculated LOD, a single floating-point value.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="46e94-127">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="46e94-127">Minimum Shader Model</span></span>

<span data-ttu-id="46e94-128">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="46e94-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="46e94-129">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="46e94-129">vs\_4\_0</span></span> | <span data-ttu-id="46e94-130">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="46e94-130">vs\_4\_1</span></span>  | <span data-ttu-id="46e94-131">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="46e94-131">ps\_4\_0</span></span> | <span data-ttu-id="46e94-132">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="46e94-132">ps\_4\_1</span></span>  | <span data-ttu-id="46e94-133">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="46e94-133">gs\_4\_0</span></span> | <span data-ttu-id="46e94-134">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="46e94-134">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           |          | <span data-ttu-id="46e94-135">x</span><span class="sxs-lookup"><span data-stu-id="46e94-135">x</span></span>         |          |           |



 

1.  <span data-ttu-id="46e94-136">TextureCubeArray 適用于著色器模型4.1 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="46e94-136">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="46e94-137">在 Direct3D 10.1 或更高版本中可以使用著色器模型4.1。</span><span class="sxs-lookup"><span data-stu-id="46e94-137">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="46e94-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="46e94-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46e94-139">材質物件</span><span class="sxs-lookup"><span data-stu-id="46e94-139">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

