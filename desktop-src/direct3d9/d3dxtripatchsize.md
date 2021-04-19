---
description: 取得三角形 patch 的大小。
ms.assetid: 3bfbed4c-59af-43eb-a462-478e89cfe9ae
title: 'D3DXTriPatchSize 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTriPatchSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5ee254b12485153f4d5c5ba0843189399d1aed0f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985882"
---
# <a name="d3dxtripatchsize-function"></a><span data-ttu-id="1bfe7-103">D3DXTriPatchSize 函式</span><span class="sxs-lookup"><span data-stu-id="1bfe7-103">D3DXTriPatchSize function</span></span>

<span data-ttu-id="1bfe7-104">取得三角形 patch 的大小。</span><span class="sxs-lookup"><span data-stu-id="1bfe7-104">Gets the size of the triangle patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bfe7-105">語法</span><span class="sxs-lookup"><span data-stu-id="1bfe7-105">Syntax</span></span>


```C++
HRESULT D3DXTriPatchSize(
  _In_  const FLOAT *pfNumSegs,
  _Out_       DWORD *pdwTriangles,
  _Out_       DWORD *pdwVertices
);
```



## <a name="parameters"></a><span data-ttu-id="1bfe7-106">參數</span><span class="sxs-lookup"><span data-stu-id="1bfe7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bfe7-107">*pfNumSegs* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1bfe7-107">*pfNumSegs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bfe7-108">Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="1bfe7-108">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1bfe7-109">要 tessellate 的每個邊緣區段數目。</span><span class="sxs-lookup"><span data-stu-id="1bfe7-109">Number of segments per edge to tessellate.</span></span>

</dd> <dt>

<span data-ttu-id="1bfe7-110">*pdwTriangles* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1bfe7-110">*pdwTriangles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1bfe7-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1bfe7-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1bfe7-112">DWORD 的指標，其中包含修補程式中的三角形數目。</span><span class="sxs-lookup"><span data-stu-id="1bfe7-112">Pointer to a DWORD that contains the number of triangles in the patch.</span></span>

</dd> <dt>

<span data-ttu-id="1bfe7-113">*pdwVertices* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1bfe7-113">*pdwVertices* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1bfe7-114">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1bfe7-114">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1bfe7-115">DWORD 的指標，其中包含三角形 patch 中的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="1bfe7-115">Pointer to a DWORD that contains the number of vertices in the triangle patch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bfe7-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="1bfe7-116">Return value</span></span>

<span data-ttu-id="1bfe7-117">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1bfe7-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1bfe7-118">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="1bfe7-118">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1bfe7-119">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="1bfe7-119">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bfe7-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="1bfe7-120">Requirements</span></span>



| <span data-ttu-id="1bfe7-121">需求</span><span class="sxs-lookup"><span data-stu-id="1bfe7-121">Requirement</span></span> | <span data-ttu-id="1bfe7-122">值</span><span class="sxs-lookup"><span data-stu-id="1bfe7-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1bfe7-123">標頭</span><span class="sxs-lookup"><span data-stu-id="1bfe7-123">Header</span></span><br/>  | <dl> <span data-ttu-id="1bfe7-124"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="1bfe7-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1bfe7-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="1bfe7-125">Library</span></span><br/> | <dl> <span data-ttu-id="1bfe7-126"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1bfe7-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1bfe7-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1bfe7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bfe7-128">網格函數</span><span class="sxs-lookup"><span data-stu-id="1bfe7-128">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="1bfe7-129">**D3DXTessellateTriPatch**</span><span class="sxs-lookup"><span data-stu-id="1bfe7-129">**D3DXTessellateTriPatch**</span></span>](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
