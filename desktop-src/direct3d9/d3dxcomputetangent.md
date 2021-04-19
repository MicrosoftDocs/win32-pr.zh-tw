---
description: 計算紋理階段中指定之材質座標的正切向量。 提供支援繼承應用程式。 使用 D3DXComputeTangentFrameEx 以獲得更好的結果。
ms.assetid: 39748459-3f9b-4b48-ae13-7143eb29c292
title: 'D3DXComputeTangent 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangent
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5cdb6a9dae3bdbad0f239fa61ba066d7b1bffb14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982008"
---
# <a name="d3dxcomputetangent-function"></a><span data-ttu-id="85055-105">D3DXComputeTangent 函式</span><span class="sxs-lookup"><span data-stu-id="85055-105">D3DXComputeTangent function</span></span>

<span data-ttu-id="85055-106">計算紋理階段中指定之材質座標的正切向量。</span><span class="sxs-lookup"><span data-stu-id="85055-106">Computes the tangent vectors for the texture coordinates given in the texture stage.</span></span> <span data-ttu-id="85055-107">提供支援繼承應用程式。</span><span class="sxs-lookup"><span data-stu-id="85055-107">Provided to support legacy applications.</span></span> <span data-ttu-id="85055-108">使用 [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) 以獲得更好的結果。</span><span class="sxs-lookup"><span data-stu-id="85055-108">Use [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) for better results.</span></span>

## <a name="syntax"></a><span data-ttu-id="85055-109">語法</span><span class="sxs-lookup"><span data-stu-id="85055-109">Syntax</span></span>


```C++
HRESULT D3DXComputeTangent(
  _In_       LPD3DXMESH Mesh,
  _In_       DWORD      TexStageIndex,
  _In_       DWORD      TangentIndex,
  _In_       DWORD      BinormIndex,
  _In_       DWORD      Wrap,
  _In_ const DWORD      *pAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="85055-110">參數</span><span class="sxs-lookup"><span data-stu-id="85055-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85055-111">*網格* \[在\]</span><span class="sxs-lookup"><span data-stu-id="85055-111">*Mesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85055-112">類型： **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="85055-112">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="85055-113">代表輸入網格之 [**ID3DXMesh**](id3dxmesh.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="85055-113">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface that represent the input mesh.</span></span>

</dd> <dt>

<span data-ttu-id="85055-114">*TexStageIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="85055-114">*TexStageIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85055-115">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="85055-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="85055-116">表示紋理階段的索引。</span><span class="sxs-lookup"><span data-stu-id="85055-116">Index that represents the texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="85055-117">*TangentIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="85055-117">*TangentIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85055-118">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="85055-118">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="85055-119">為正切資料提供使用方式索引的索引。</span><span class="sxs-lookup"><span data-stu-id="85055-119">Index that provides the usage index for the tangent data.</span></span> <span data-ttu-id="85055-120">頂點宣告表示使用方式;此索引會使用使用方式索引來修改使用方式。</span><span class="sxs-lookup"><span data-stu-id="85055-120">The vertex declaration implies the usage; this index modifies the usage with the usage index.</span></span> <span data-ttu-id="85055-121">如需頂點宣告的詳細資訊，請參閱 [ (Direct3D 9) 的頂點 ](vertex-declaration.md)宣告。</span><span class="sxs-lookup"><span data-stu-id="85055-121">For more information about a vertex declaration, see [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

</dd> <dt>

<span data-ttu-id="85055-122">*BinormIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="85055-122">*BinormIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85055-123">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="85055-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="85055-124">提供 binormal 資料之使用方式索引的索引。</span><span class="sxs-lookup"><span data-stu-id="85055-124">Index that provides the usage index for the binormal data.</span></span> <span data-ttu-id="85055-125">頂點宣告表示使用方式;此索引會使用使用方式索引來修改使用方式。</span><span class="sxs-lookup"><span data-stu-id="85055-125">The vertex declaration implies the usage; this index modifies the usage with the usage index.</span></span> <span data-ttu-id="85055-126">如需頂點宣告的詳細資訊，請參閱 [ (Direct3D 9) 的頂點 ](vertex-declaration.md)宣告。</span><span class="sxs-lookup"><span data-stu-id="85055-126">For more information about a vertex declaration, see [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

</dd> <dt>

<span data-ttu-id="85055-127">*換行* \[在\]</span><span class="sxs-lookup"><span data-stu-id="85055-127">*Wrap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85055-128">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="85055-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="85055-129">將此值設定為0表示不換行，或設定為1以換行您的和 V 指示。</span><span class="sxs-lookup"><span data-stu-id="85055-129">Set this value to 0 for no wrapping, or to 1 for wrapping in the U and V directions.</span></span>

</dd> <dt>

<span data-ttu-id="85055-130">*pAdjacency* \[在\]</span><span class="sxs-lookup"><span data-stu-id="85055-130">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85055-131">類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="85055-131">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="85055-132">要填入相鄰臉部索引的每個臉部陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="85055-132">Pointer to an array of three DWORDs per face to be filled with adjacent face indices.</span></span> <span data-ttu-id="85055-133">此陣列中的位元組數目必須至少為 ( (3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof (DWORD) ) 。</span><span class="sxs-lookup"><span data-stu-id="85055-133">The number of bytes in this array must be at least ((3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof(DWORD)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85055-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="85055-134">Return value</span></span>

<span data-ttu-id="85055-135">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="85055-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="85055-136">如果函式成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="85055-136">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="85055-137">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="85055-137">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="85055-138">備註</span><span class="sxs-lookup"><span data-stu-id="85055-138">Remarks</span></span>

<span data-ttu-id="85055-139">如果網格頂點宣告指定了正切函數或 binormal 欄位， **D3DXComputeTangent** 將會更新任何使用者提供的正切函數或 binormal 資料。</span><span class="sxs-lookup"><span data-stu-id="85055-139">If the mesh vertex declaration specifies tangent or binormal fields, **D3DXComputeTangent** will update any user-supplied tangent or binormal data.</span></span> <span data-ttu-id="85055-140">或者，將 TangentIndex 設定為 [D3DX \_ 預設](other-d3dx-constants.md) 為不更新使用者提供的正切資料，或將 BINORMINDEX 設定為 D3DX \_ 預設為不更新使用者提供的 binormal 資料。</span><span class="sxs-lookup"><span data-stu-id="85055-140">Alternatively, set TangentIndex to [D3DX\_DEFAULT](other-d3dx-constants.md) to not update the user-supplied tangent data, or set BinormIndex to D3DX\_DEFAULT to not update the user-supplied binormal data.</span></span> <span data-ttu-id="85055-141">TexStageIndex 不能設定為 D3DX \_ 預設值。</span><span class="sxs-lookup"><span data-stu-id="85055-141">TexStageIndex cannot be set to D3DX\_DEFAULT.</span></span>

<span data-ttu-id="85055-142">**D3DXComputeTangent** 取決於包含 binormal 欄位 (BinormIndex) 、正切欄位 (TangentIndex) 或兩者的網格頂點宣告。</span><span class="sxs-lookup"><span data-stu-id="85055-142">**D3DXComputeTangent** depends on the mesh vertex declaration containing either the binormal field (BinormIndex), the tangent field (TangentIndex), or both.</span></span> <span data-ttu-id="85055-143">如果兩者都不存在，此函式將會失敗。</span><span class="sxs-lookup"><span data-stu-id="85055-143">If both are missing, this function will fail.</span></span>

<span data-ttu-id="85055-144">此函式只會使用下列輸入參數來呼叫 [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) ：</span><span class="sxs-lookup"><span data-stu-id="85055-144">This function simply calls [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) with the following input parameters:</span></span>


```
D3DXComputeTangentFrameEx( Mesh,
                           D3DDECLUSAGE_TEXCOORD,
                           TexStageIndex,
                           ( BinormIndex == D3DX_DEFAULT ) ?
                               D3DX_DEFAULT : D3DDECLUSAGE_BINORMAL,
                               // provides backward function compatibility
                           BinormIndex,
                           ( TangentIndex == D3DX_DEFAULT ) ?
                               D3DX_DEFAULT : D3DDECLUSAGE_TANGENT,
                           TangentIndex,
                           D3DX_DEFAULT, // do not store normals
                           0,
                           ( Wrap ? D3DXTANGENT_WRAP_UV : 0 )
                               | D3DXTANGENT_GENERATE_IN_PLACE
                               | D3DXTANGENT_ORTHOGONALIZE_FROM_U,
                           pAdjacency,
                           -1.01f,
                           -0.01f,
                           -1.01f,
                           NULL,
                           NULL);
```



## <a name="requirements"></a><span data-ttu-id="85055-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="85055-145">Requirements</span></span>



| <span data-ttu-id="85055-146">需求</span><span class="sxs-lookup"><span data-stu-id="85055-146">Requirement</span></span> | <span data-ttu-id="85055-147">值</span><span class="sxs-lookup"><span data-stu-id="85055-147">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="85055-148">標頭</span><span class="sxs-lookup"><span data-stu-id="85055-148">Header</span></span><br/>  | <dl> <span data-ttu-id="85055-149"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="85055-149"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="85055-150">程式庫</span><span class="sxs-lookup"><span data-stu-id="85055-150">Library</span></span><br/> | <dl> <span data-ttu-id="85055-151"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="85055-151"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="85055-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="85055-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85055-153">網格函數</span><span class="sxs-lookup"><span data-stu-id="85055-153">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
