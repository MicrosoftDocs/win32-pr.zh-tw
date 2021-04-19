---
description: 清除網格以進行簡化。
ms.assetid: 2b586ecc-db87-4b20-a4fc-c8b547bebf65
title: 'D3DXCleanMesh 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCleanMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5565978dc1ad0e80c33718275ea65080930ce7cf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999021"
---
# <a name="d3dxcleanmesh-function"></a><span data-ttu-id="85d46-103">D3DXCleanMesh 函式</span><span class="sxs-lookup"><span data-stu-id="85d46-103">D3DXCleanMesh function</span></span>

<span data-ttu-id="85d46-104">清除網格以進行簡化。</span><span class="sxs-lookup"><span data-stu-id="85d46-104">Cleans a mesh, preparing it for simplification.</span></span>

## <a name="syntax"></a><span data-ttu-id="85d46-105">語法</span><span class="sxs-lookup"><span data-stu-id="85d46-105">Syntax</span></span>


```C++
HRESULT D3DXCleanMesh(
  _In_        D3DXCLEANTYPE CleanType,
  _In_        LPD3DXMESH    pMeshIn,
  _In_  const DWORD         *pAdjacencyIn,
  _Out_       LPD3DXMESH    *ppMeshOut,
  _Out_       DWORD         *pAdjacencyOut,
  _Out_       LPD3DXBUFFER  *ppErrorsAndWarnings
);
```



## <a name="parameters"></a><span data-ttu-id="85d46-106">參數</span><span class="sxs-lookup"><span data-stu-id="85d46-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85d46-107">*CleanType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="85d46-107">*CleanType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85d46-108">類型： **[ **D3DXCLEANTYPE**](./d3dxcleantype.md)**</span><span class="sxs-lookup"><span data-stu-id="85d46-108">Type: **[**D3DXCLEANTYPE**](./d3dxcleantype.md)**</span></span>

<span data-ttu-id="85d46-109">要在準備進行網格清除時執行的頂點作業。</span><span class="sxs-lookup"><span data-stu-id="85d46-109">Vertex operations to perform in preparation for mesh cleaning.</span></span> <span data-ttu-id="85d46-110">請參閱 [**D3DXCLEANTYPE**](./d3dxcleantype.md)。</span><span class="sxs-lookup"><span data-stu-id="85d46-110">See [**D3DXCLEANTYPE**](./d3dxcleantype.md).</span></span>

</dd> <dt>

<span data-ttu-id="85d46-111">*pMeshIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="85d46-111">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85d46-112">類型： **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="85d46-112">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="85d46-113">[**ID3DXMesh**](id3dxmesh.md)介面的指標，代表要清除的網格。</span><span class="sxs-lookup"><span data-stu-id="85d46-113">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the mesh to be cleaned.</span></span>

</dd> <dt>

<span data-ttu-id="85d46-114">*pAdjacencyIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="85d46-114">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85d46-115">類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="85d46-115">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="85d46-116">指標，指向每個臉部的三個 Dword 陣列，以指定要清除網格中每個臉部的三個相鄰專案。</span><span class="sxs-lookup"><span data-stu-id="85d46-116">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh to be cleaned.</span></span>

</dd> <dt>

<span data-ttu-id="85d46-117">*ppMeshOut* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="85d46-117">*ppMeshOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85d46-118">類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="85d46-118">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="85d46-119">[**ID3DXMesh**](id3dxmesh.md)介面指標的位址，表示傳回的已清除網格。</span><span class="sxs-lookup"><span data-stu-id="85d46-119">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the returned cleaned mesh.</span></span> <span data-ttu-id="85d46-120">如果不需要進行清理，則會傳回相同的網格。</span><span class="sxs-lookup"><span data-stu-id="85d46-120">The same mesh is returned that was passed in if no cleaning was necessary.</span></span>

</dd> <dt>

<span data-ttu-id="85d46-121">*pAdjacencyOut* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="85d46-121">*pAdjacencyOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85d46-122">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="85d46-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="85d46-123">指標，指向每個臉部的三個 Dword 陣列，以針對輸出網格中的每個臉部指定三個相鄰專案。</span><span class="sxs-lookup"><span data-stu-id="85d46-123">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the output mesh.</span></span>

</dd> <dt>

<span data-ttu-id="85d46-124">*ppErrorsAndWarnings* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="85d46-124">*ppErrorsAndWarnings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85d46-125">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="85d46-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="85d46-126">傳回包含錯誤和警告字串的緩衝區，以說明在網格中找到的問題。</span><span class="sxs-lookup"><span data-stu-id="85d46-126">Returns a buffer containing a string of errors and warnings, which explain the problems found in the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85d46-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="85d46-127">Return value</span></span>

<span data-ttu-id="85d46-128">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="85d46-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="85d46-129">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="85d46-129">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="85d46-130">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="85d46-130">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="85d46-131">備註</span><span class="sxs-lookup"><span data-stu-id="85d46-131">Remarks</span></span>

<span data-ttu-id="85d46-132">此函式會使用 CleanType 參數中指定的清除方法和選項來清除網格。</span><span class="sxs-lookup"><span data-stu-id="85d46-132">This function cleans a mesh using the cleaning method and options specified in the CleanType parameter.</span></span> <span data-ttu-id="85d46-133">如需可用選項的描述，請參閱 [**D3DXCLEANTYPE**](./d3dxcleantype.md) 列舉。</span><span class="sxs-lookup"><span data-stu-id="85d46-133">See the [**D3DXCLEANTYPE**](./d3dxcleantype.md) enumeration for a description of the available options.</span></span>

## <a name="requirements"></a><span data-ttu-id="85d46-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="85d46-134">Requirements</span></span>



| <span data-ttu-id="85d46-135">需求</span><span class="sxs-lookup"><span data-stu-id="85d46-135">Requirement</span></span> | <span data-ttu-id="85d46-136">值</span><span class="sxs-lookup"><span data-stu-id="85d46-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="85d46-137">標頭</span><span class="sxs-lookup"><span data-stu-id="85d46-137">Header</span></span><br/>  | <dl> <span data-ttu-id="85d46-138"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="85d46-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="85d46-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="85d46-139">Library</span></span><br/> | <dl> <span data-ttu-id="85d46-140"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="85d46-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="85d46-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="85d46-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85d46-142">網格函數</span><span class="sxs-lookup"><span data-stu-id="85d46-142">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
