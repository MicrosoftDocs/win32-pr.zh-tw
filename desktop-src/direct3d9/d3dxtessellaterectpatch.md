---
description: 將矩形的高序位介面 patch Tessellates 為三角形網格。
ms.assetid: d941d994-8a13-49ff-a0b1-b21a3f84ed78
title: 'D3DXTessellateRectPatch 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateRectPatch
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 887f0035b50efd860149410e50dd6abff301968d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196237"
---
# <a name="d3dxtessellaterectpatch-function"></a><span data-ttu-id="f08b3-103">D3DXTessellateRectPatch 函式</span><span class="sxs-lookup"><span data-stu-id="f08b3-103">D3DXTessellateRectPatch function</span></span>

<span data-ttu-id="f08b3-104">將矩形的高序位介面 patch Tessellates 為三角形網格。</span><span class="sxs-lookup"><span data-stu-id="f08b3-104">Tessellates a rectangular higher-order surface patch into a triangle mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="f08b3-105">語法</span><span class="sxs-lookup"><span data-stu-id="f08b3-105">Syntax</span></span>


```C++
HRESULT D3DXTessellateRectPatch(
  _In_          LPDIRECT3DVERTEXBUFFER9 pVB,
  _In_    const FLOAT                   *pNumSegs,
  _In_    const D3DVERTEXELEMENT9       *pInDecl,
  _In_    const D3DRECTPATCH_INFO       *pRectPatchInfo,
  _Inout_       LPD3DXMESH              pMesh
);
```



## <a name="parameters"></a><span data-ttu-id="f08b3-106">參數</span><span class="sxs-lookup"><span data-stu-id="f08b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f08b3-107">*pVB* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f08b3-107">*pVB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f08b3-108">類型： **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**</span><span class="sxs-lookup"><span data-stu-id="f08b3-108">Type: **[**LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**</span></span>

<span data-ttu-id="f08b3-109">包含修補資料的頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f08b3-109">Vertex buffer containing the patch data.</span></span>

</dd> <dt>

<span data-ttu-id="f08b3-110">*pNumSegs* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f08b3-110">*pNumSegs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f08b3-111">Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="f08b3-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f08b3-112">指向四個浮點值陣列的指標，這些值會識別矩形 patch 的每個邊緣在鑲嵌時應除以的區段數目。</span><span class="sxs-lookup"><span data-stu-id="f08b3-112">Pointer to an array of four floating-point values that identify the number of segments into which each edge of the rectangle patch should be divided when tessellated.</span></span> <span data-ttu-id="f08b3-113">請參閱 [**D3DRECTPATCH \_ 資訊**](d3drectpatch-info.md)。</span><span class="sxs-lookup"><span data-stu-id="f08b3-113">See [**D3DRECTPATCH\_INFO**](d3drectpatch-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="f08b3-114">*pInDecl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f08b3-114">*pInDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f08b3-115">Type： **Const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="f08b3-115">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="f08b3-116">定義頂點資料的頂點宣告結構。</span><span class="sxs-lookup"><span data-stu-id="f08b3-116">Vertex declaration structure that defines the vertex data.</span></span> <span data-ttu-id="f08b3-117">請參閱 [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)。</span><span class="sxs-lookup"><span data-stu-id="f08b3-117">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> <dt>

<span data-ttu-id="f08b3-118">*pRectPatchInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f08b3-118">*pRectPatchInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f08b3-119">類型： **Const [**D3DRECTPATCH \_ INFO**](d3drectpatch-info.md) \***</span><span class="sxs-lookup"><span data-stu-id="f08b3-119">Type: **const [**D3DRECTPATCH\_INFO**](d3drectpatch-info.md)\***</span></span>

<span data-ttu-id="f08b3-120">描述矩形修補程式。</span><span class="sxs-lookup"><span data-stu-id="f08b3-120">Describes a rectangular patch.</span></span> <span data-ttu-id="f08b3-121">請參閱 [**D3DRECTPATCH \_ 資訊**](d3drectpatch-info.md)。</span><span class="sxs-lookup"><span data-stu-id="f08b3-121">See [**D3DRECTPATCH\_INFO**](d3drectpatch-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="f08b3-122">*pMesh* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="f08b3-122">*pMesh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f08b3-123">類型： **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="f08b3-123">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="f08b3-124">所建立之網格的指標。</span><span class="sxs-lookup"><span data-stu-id="f08b3-124">Pointer to the created mesh.</span></span> <span data-ttu-id="f08b3-125">請參閱 [**ID3DXMesh**](id3dxmesh.md)。</span><span class="sxs-lookup"><span data-stu-id="f08b3-125">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f08b3-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="f08b3-126">Return value</span></span>

<span data-ttu-id="f08b3-127">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f08b3-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f08b3-128">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="f08b3-128">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f08b3-129">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="f08b3-129">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="f08b3-130">備註</span><span class="sxs-lookup"><span data-stu-id="f08b3-130">Remarks</span></span>

<span data-ttu-id="f08b3-131">使用 [**D3DXRectPatchSize**](d3dxrectpatchsize.md) 來取得鑲嵌式函數所需的輸出頂點和索引數目。</span><span class="sxs-lookup"><span data-stu-id="f08b3-131">Use [**D3DXRectPatchSize**](d3dxrectpatchsize.md) to get the number of output vertices and indices that the tessellation function needs.</span></span>

## <a name="requirements"></a><span data-ttu-id="f08b3-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="f08b3-132">Requirements</span></span>



| <span data-ttu-id="f08b3-133">需求</span><span class="sxs-lookup"><span data-stu-id="f08b3-133">Requirement</span></span> | <span data-ttu-id="f08b3-134">值</span><span class="sxs-lookup"><span data-stu-id="f08b3-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f08b3-135">標頭</span><span class="sxs-lookup"><span data-stu-id="f08b3-135">Header</span></span><br/>  | <dl> <span data-ttu-id="f08b3-136"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="f08b3-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f08b3-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="f08b3-137">Library</span></span><br/> | <dl> <span data-ttu-id="f08b3-138"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f08b3-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f08b3-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f08b3-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f08b3-140">網格函數</span><span class="sxs-lookup"><span data-stu-id="f08b3-140">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="f08b3-141">**D3DXTessellateTriPatch**</span><span class="sxs-lookup"><span data-stu-id="f08b3-141">**D3DXTessellateTriPatch**</span></span>](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
