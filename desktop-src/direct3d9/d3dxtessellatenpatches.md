---
description: 使用 N 修補程式鑲嵌式配置 Tessellates 指定的網格。
ms.assetid: e804905d-ee0b-484f-a621-58b197bd370b
title: 'D3DXTessellateNPatches 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateNPatches
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9c8811816447deb858b5c8b42d651d219f06fef5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992307"
---
# <a name="d3dxtessellatenpatches-function"></a><span data-ttu-id="ed6bd-103">D3DXTessellateNPatches 函式</span><span class="sxs-lookup"><span data-stu-id="ed6bd-103">D3DXTessellateNPatches function</span></span>

<span data-ttu-id="ed6bd-104">使用 N 修補程式鑲嵌式配置 Tessellates 指定的網格。</span><span class="sxs-lookup"><span data-stu-id="ed6bd-104">Tessellates the given mesh using the N-patch tessellation scheme.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed6bd-105">語法</span><span class="sxs-lookup"><span data-stu-id="ed6bd-105">Syntax</span></span>


```C++
HRESULT D3DXTessellateNPatches(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const CONST DWORD  *pAdjacencyIn,
  _In_        FLOAT        NumSegs,
  _In_        BOOL         QuadraticInterpNormals,
  _Out_       LPD3DXMESH   *ppMeshOut,
  _Out_       LPD3DXBUFFER *ppAdjacencyOut
);
```



## <a name="parameters"></a><span data-ttu-id="ed6bd-106">參數</span><span class="sxs-lookup"><span data-stu-id="ed6bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed6bd-107">*pMeshIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ed6bd-107">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed6bd-108">類型： **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="ed6bd-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="ed6bd-109">[**ID3DXMesh**](id3dxmesh.md)介面的指標，代表要 tessellate 的網格。</span><span class="sxs-lookup"><span data-stu-id="ed6bd-109">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the mesh to tessellate.</span></span>

</dd> <dt>

<span data-ttu-id="ed6bd-110">*pAdjacencyIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ed6bd-110">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed6bd-111">類型： **CONST CONST DWORD \***</span><span class="sxs-lookup"><span data-stu-id="ed6bd-111">Type: **const CONST DWORD\***</span></span>

<span data-ttu-id="ed6bd-112">指標，指向每個臉部的三個 Dword 陣列，以針對來源網格中的每個臉部指定三個相鄰專案。</span><span class="sxs-lookup"><span data-stu-id="ed6bd-112">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the source mesh.</span></span> <span data-ttu-id="ed6bd-113">這個參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ed6bd-113">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ed6bd-114">*NumSegs* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ed6bd-114">*NumSegs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed6bd-115">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed6bd-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed6bd-116">要 tessellate 的每個邊緣區段數目。</span><span class="sxs-lookup"><span data-stu-id="ed6bd-116">Number of segments per edge to tessellate.</span></span>

</dd> <dt>

<span data-ttu-id="ed6bd-117">*QuadraticInterpNormals* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ed6bd-117">*QuadraticInterpNormals* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed6bd-118">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed6bd-118">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed6bd-119">設定為 **TRUE** 以針對法線使用二次插補;線性插補的設定為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="ed6bd-119">Set to **TRUE** to use quadratic interpolation for normals; set to **FALSE** for linear interpolation.</span></span>

</dd> <dt>

<span data-ttu-id="ed6bd-120">*ppMeshOut* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ed6bd-120">*ppMeshOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed6bd-121">類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="ed6bd-121">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="ed6bd-122">[**ID3DXMesh**](id3dxmesh.md)介面指標的位址，表示傳回的鑲嵌網格。</span><span class="sxs-lookup"><span data-stu-id="ed6bd-122">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the returned tessellated mesh.</span></span>

</dd> <dt>

<span data-ttu-id="ed6bd-123">*ppAdjacencyOut* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ed6bd-123">*ppAdjacencyOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed6bd-124">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="ed6bd-124">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="ed6bd-125">[**ID3DXBuffer**](id3dxbuffer.md)介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="ed6bd-125">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="ed6bd-126">如果這個參數的值不是設定為 **Null**，此緩衝區將會包含每個臉部的三個 dword 陣列，以針對輸出網格中的每個臉部指定三個相鄰專案。</span><span class="sxs-lookup"><span data-stu-id="ed6bd-126">If the value of this parameter is not set to **NULL**, this buffer will contain an array of three DWORDs per face that specify the three neighbors for each face in the output mesh.</span></span> <span data-ttu-id="ed6bd-127">這個參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ed6bd-127">This parameter may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed6bd-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="ed6bd-128">Return value</span></span>

<span data-ttu-id="ed6bd-129">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ed6bd-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ed6bd-130">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="ed6bd-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ed6bd-131">如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="ed6bd-131">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed6bd-132">備註</span><span class="sxs-lookup"><span data-stu-id="ed6bd-132">Remarks</span></span>

<span data-ttu-id="ed6bd-133">此函式會使用 N 修補演算法 tessellates。</span><span class="sxs-lookup"><span data-stu-id="ed6bd-133">This function tessellates by using the N-patch algorithm.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed6bd-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed6bd-134">Requirements</span></span>



| <span data-ttu-id="ed6bd-135">需求</span><span class="sxs-lookup"><span data-stu-id="ed6bd-135">Requirement</span></span> | <span data-ttu-id="ed6bd-136">值</span><span class="sxs-lookup"><span data-stu-id="ed6bd-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed6bd-137">標頭</span><span class="sxs-lookup"><span data-stu-id="ed6bd-137">Header</span></span><br/>  | <dl> <span data-ttu-id="ed6bd-138"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="ed6bd-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ed6bd-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="ed6bd-139">Library</span></span><br/> | <dl> <span data-ttu-id="ed6bd-140"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed6bd-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ed6bd-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed6bd-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed6bd-142">網格函數</span><span class="sxs-lookup"><span data-stu-id="ed6bd-142">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
