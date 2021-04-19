---
description: 為三角形清單產生優化的臉部重新對應。
ms.assetid: 428c2af8-43e7-4cf7-8b9b-04ba5cff82c8
title: 'D3DXOptimizeFaces 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXOptimizeFaces
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6c56dec04e01b542d2c760852a58826a8186c213
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982858"
---
# <a name="d3dxoptimizefaces-function"></a><span data-ttu-id="8c6e9-103">D3DXOptimizeFaces 函式</span><span class="sxs-lookup"><span data-stu-id="8c6e9-103">D3DXOptimizeFaces function</span></span>

<span data-ttu-id="8c6e9-104">為三角形清單產生優化的臉部重新對應。</span><span class="sxs-lookup"><span data-stu-id="8c6e9-104">Generates an optimized face remapping for a triangle list.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c6e9-105">語法</span><span class="sxs-lookup"><span data-stu-id="8c6e9-105">Syntax</span></span>


```C++
HRESULT D3DXOptimizeFaces(
  _In_    LPCVOID pIndices,
  _In_    UINT    NumFaces,
  _In_    UINT    NumVertices,
  _In_    BOOL    Indices32Bit,
  _Inout_ DWORD   *pFaceRemap
);
```



## <a name="parameters"></a><span data-ttu-id="8c6e9-106">參數</span><span class="sxs-lookup"><span data-stu-id="8c6e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c6e9-107">*pIndices* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8c6e9-107">*pIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c6e9-108">類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c6e9-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c6e9-109">用來排序頂點的三角形清單索引指標。</span><span class="sxs-lookup"><span data-stu-id="8c6e9-109">Pointer to triangle list indices to use for ordering vertices.</span></span>

</dd> <dt>

<span data-ttu-id="8c6e9-110">*NumFaces* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8c6e9-110">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c6e9-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c6e9-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c6e9-112">三角形清單中的臉部數目。</span><span class="sxs-lookup"><span data-stu-id="8c6e9-112">Number of faces in the triangle list.</span></span> <span data-ttu-id="8c6e9-113">若為16位網格，這僅限於 2 ^ 16-1 (65535) 或較少的臉部。</span><span class="sxs-lookup"><span data-stu-id="8c6e9-113">For 16-bit meshes, this is limited to 2^16 - 1 (65535) or fewer faces.</span></span>

</dd> <dt>

<span data-ttu-id="8c6e9-114">*NumVertices* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8c6e9-114">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c6e9-115">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c6e9-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c6e9-116">三角形清單所參考的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="8c6e9-116">Number of vertices referenced by the triangle list.</span></span>

</dd> <dt>

<span data-ttu-id="8c6e9-117">*Indices32Bit* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8c6e9-117">*Indices32Bit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c6e9-118">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c6e9-118">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c6e9-119">表示索引類型的旗標：如果索引是32位 (65535 個以上的索引) ，則為 **TRUE** ，如果索引為16位 (65535 或較少的索引) ，則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="8c6e9-119">Flag indicating index type: **TRUE** if indices are 32-bit (more than 65535 indices), **FALSE** if indices are 16-bit (65535 or fewer indices).</span></span>

</dd> <dt>

<span data-ttu-id="8c6e9-120">*pFaceRemap* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="8c6e9-120">*pFaceRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c6e9-121">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8c6e9-121">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8c6e9-122">已分割以產生目前臉部的原始網狀臉部指標。</span><span class="sxs-lookup"><span data-stu-id="8c6e9-122">Pointer to the original mesh face that was split to generate the current face.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c6e9-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="8c6e9-123">Return value</span></span>

<span data-ttu-id="8c6e9-124">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8c6e9-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8c6e9-125">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="8c6e9-125">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8c6e9-126">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="8c6e9-126">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c6e9-127">備註</span><span class="sxs-lookup"><span data-stu-id="8c6e9-127">Remarks</span></span>

<span data-ttu-id="8c6e9-128">這個函式的優化程式在功能上相當於呼叫 [**ID3DXMesh：： Optimize**](id3dxmesh--optimize.md) WITH with D3DXMESHOPT \_ DEVICEINDEPENDENT 旗標，但此函式可讓您更有效率地使用頂點快取。</span><span class="sxs-lookup"><span data-stu-id="8c6e9-128">This function's optimization procedure is functionally equivalent to calling [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) with the D3DXMESHOPT\_DEVICEINDEPENDENT flag, but this function makes more efficient use of vertex caches.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c6e9-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c6e9-129">Requirements</span></span>



| <span data-ttu-id="8c6e9-130">需求</span><span class="sxs-lookup"><span data-stu-id="8c6e9-130">Requirement</span></span> | <span data-ttu-id="8c6e9-131">值</span><span class="sxs-lookup"><span data-stu-id="8c6e9-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c6e9-132">標頭</span><span class="sxs-lookup"><span data-stu-id="8c6e9-132">Header</span></span><br/>  | <dl> <span data-ttu-id="8c6e9-133"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="8c6e9-133"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8c6e9-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="8c6e9-134">Library</span></span><br/> | <dl> <span data-ttu-id="8c6e9-135"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c6e9-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8c6e9-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c6e9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c6e9-137">網格函數</span><span class="sxs-lookup"><span data-stu-id="8c6e9-137">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
