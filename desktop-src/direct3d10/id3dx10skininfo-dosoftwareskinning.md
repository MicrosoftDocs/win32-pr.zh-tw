---
description: 在頂點的陣列上進行軟體外觀。
ms.assetid: 6c1a713f-4ae7-4ee2-afa6-079dd8354fe7
title: 'ID3DX10SkinInfo：:D oSoftwareSkinning 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.DoSoftwareSkinning
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 54dfe909e36be0273e0679a824ff0674b0e3b38c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997398"
---
# <a name="id3dx10skininfodosoftwareskinning-method"></a><span data-ttu-id="91bb8-103">ID3DX10SkinInfo：:D oSoftwareSkinning 方法</span><span class="sxs-lookup"><span data-stu-id="91bb8-103">ID3DX10SkinInfo::DoSoftwareSkinning method</span></span>

<span data-ttu-id="91bb8-104">在頂點的陣列上進行軟體外觀。</span><span class="sxs-lookup"><span data-stu-id="91bb8-104">Do software skinning on an array of vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="91bb8-105">語法</span><span class="sxs-lookup"><span data-stu-id="91bb8-105">Syntax</span></span>


```C++
HRESULT DoSoftwareSkinning(
  [in]      UINT                    StartVertex,
  [in]      UINT                    VertexCount,
  [in]      void                    *pSrcVertices,
  [in]      UINT                    SrcStride,
  [in, out] void                    *pDestVertices,
  [in]      UINT                    DestStride,
  [in]      D3DXMATRIX              *pBoneMatrices,
  [in]      D3DXMATRIX              *pInverseTransposeBoneMatrices,
  [in]      D3DX10_SKINNING_CHANNEL *pChannelDescs,
  [in]      UINT                    NumChannels
);
```



## <a name="parameters"></a><span data-ttu-id="91bb8-106">參數</span><span class="sxs-lookup"><span data-stu-id="91bb8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91bb8-107">*StartVertex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="91bb8-107">*StartVertex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91bb8-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91bb8-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="91bb8-109">PSrcVertices 的以零為基的索引。</span><span class="sxs-lookup"><span data-stu-id="91bb8-109">A 0-based index into pSrcVertices.</span></span>

</dd> <dt>

<span data-ttu-id="91bb8-110">*VertexCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="91bb8-110">*VertexCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91bb8-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91bb8-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="91bb8-112">要轉換的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="91bb8-112">Number of vertices to transform.</span></span>

</dd> <dt>

<span data-ttu-id="91bb8-113">*pSrcVertices* \[在\]</span><span class="sxs-lookup"><span data-stu-id="91bb8-113">*pSrcVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91bb8-114">類型： **void \***</span><span class="sxs-lookup"><span data-stu-id="91bb8-114">Type: **void\***</span></span>

<span data-ttu-id="91bb8-115">要轉換之頂點陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="91bb8-115">Pointer to an array of vertices to transform.</span></span>

</dd> <dt>

<span data-ttu-id="91bb8-116">*SrcStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="91bb8-116">*SrcStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91bb8-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91bb8-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="91bb8-118">PSrcVertices 中頂點的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="91bb8-118">The size, in bytes, of a vertex in pSrcVertices.</span></span>

</dd> <dt>

<span data-ttu-id="91bb8-119">*pDestVertices* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="91bb8-119">*pDestVertices* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="91bb8-120">類型： **void \***</span><span class="sxs-lookup"><span data-stu-id="91bb8-120">Type: **void\***</span></span>

<span data-ttu-id="91bb8-121">指向頂點陣列的指標，將會填入已轉換的頂點。</span><span class="sxs-lookup"><span data-stu-id="91bb8-121">Pointer to an array of vertices, which will be filled with the transformed vertices.</span></span>

</dd> <dt>

<span data-ttu-id="91bb8-122">*DestStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="91bb8-122">*DestStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91bb8-123">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91bb8-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="91bb8-124">PDestVertices 中頂點的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="91bb8-124">The size, in bytes, of a vertex in pDestVertices.</span></span>

</dd> <dt>

<span data-ttu-id="91bb8-125">*pBoneMatrices* \[在\]</span><span class="sxs-lookup"><span data-stu-id="91bb8-125">*pBoneMatrices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91bb8-126">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="91bb8-126">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="91bb8-127">矩陣的陣列，將用來轉換對應至每個骨骼的點，以便 \[ \] pBoneMatrices i 轉換對應至骨骼的頂點 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="91bb8-127">An array of matrices that will be used to transform the points mapped to each bone, such that the vertices mapped to bone\[i\] will be transformed by pBoneMatrices\[i\].</span></span> <span data-ttu-id="91bb8-128">只有在 pChannelDescs 中的 IsNormal 值設定為 **FALSE** 時，才會使用這個陣列來轉換矩陣，否則會使用 pInverseTransposeBoneMatrices。</span><span class="sxs-lookup"><span data-stu-id="91bb8-128">This array will be used to transform the matrices only if the IsNormal value in pChannelDescs is set to **FALSE**, otherwise pInverseTransposeBoneMatrices will be used.</span></span>

</dd> <dt>

<span data-ttu-id="91bb8-129">*pInverseTransposeBoneMatrices* \[在\]</span><span class="sxs-lookup"><span data-stu-id="91bb8-129">*pInverseTransposeBoneMatrices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91bb8-130">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="91bb8-130">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="91bb8-131">如果這個值為 **Null**，則會設定為等於 pBoneMatrices。</span><span class="sxs-lookup"><span data-stu-id="91bb8-131">If this value is **NULL**, it will be set equal to pBoneMatrices.</span></span> <span data-ttu-id="91bb8-132">只有在 pChannelDescs 中的 IsNormal 值設定為 **TRUE** 時，才會使用此矩陣陣列來轉換頂點，否則會使用 pBoneMatrices。</span><span class="sxs-lookup"><span data-stu-id="91bb8-132">This array of matrices will be used to transform the vertices only if the IsNormal value in pChannelDescs is set to **TRUE**, otherwise pBoneMatrices will be used.</span></span>

</dd> <dt>

<span data-ttu-id="91bb8-133">*pChannelDescs* \[在\]</span><span class="sxs-lookup"><span data-stu-id="91bb8-133">*pChannelDescs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91bb8-134">類型： **[ **D3DX10 \_ 外觀 \_ 通道**](d3dx10-skinning-channel.md)\***</span><span class="sxs-lookup"><span data-stu-id="91bb8-134">Type: **[**D3DX10\_SKINNING\_CHANNEL**](d3dx10-skinning-channel.md)\***</span></span>

<span data-ttu-id="91bb8-135">D3DX10 \_ 外觀 \_ 通道結構的指標，它會決定要對其執行軟體外觀的頂點 decl 成員。</span><span class="sxs-lookup"><span data-stu-id="91bb8-135">Pointer to a D3DX10\_SKINNING\_CHANNEL structure, which determines the member of the vertex decl the software skinning will be done on.</span></span>

</dd> <dt>

<span data-ttu-id="91bb8-136">*NumChannels* \[在\]</span><span class="sxs-lookup"><span data-stu-id="91bb8-136">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91bb8-137">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91bb8-137">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="91bb8-138">PChannelDescs 中 D3DX10 的 \_ 外觀 \_ 通道結構數目。</span><span class="sxs-lookup"><span data-stu-id="91bb8-138">The number of D3DX10\_SKINNING\_CHANNEL structures in pChannelDescs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91bb8-139">傳回值</span><span class="sxs-lookup"><span data-stu-id="91bb8-139">Return value</span></span>

<span data-ttu-id="91bb8-140">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="91bb8-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="91bb8-141">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="91bb8-141">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="91bb8-142">如果方法失敗，則傳回值可以是： E \_ INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="91bb8-142">If the method fails, the return value can be: E\_INVALIDARG.</span></span>

## <a name="remarks"></a><span data-ttu-id="91bb8-143">備註</span><span class="sxs-lookup"><span data-stu-id="91bb8-143">Remarks</span></span>

<span data-ttu-id="91bb8-144">以下是如何使用軟體外觀的範例：</span><span class="sxs-lookup"><span data-stu-id="91bb8-144">Here is an example of how to use software skinning:</span></span>


```
//vertex definition
struct MyVertex
{
    D3DXVECTOR3 Position;
    D3DXVECTOR2 Weight;
    D3DXVECTOR2 TexCoord;
};

//create vertex data
const UINT numVertices = 16;
MyVertex vertices[numVertices] = {...};
MyVertex destVertices[numVertices];

//create bone matrices
D3DXMATRIX boneMatrices[2];
D3DXMatrixIdentity(&boneMatrices[0]);
D3DXMatrixRotationX(&boneMatrices[1], 3.14159f / 180.0f);

//create bone indices and weights
UINT boneIndices[numVertices] = {...};
float boneWeights[2][numVertices] = {...};

//create skin info, populate it with bones and vertices, and then map them to each other
ID3DX10SkinInfo *pSkinInfo = NULL;
D3DX10CreateSkinInfo(&pSkinInfo);
pSkinInfo->AddBones(2);
pSkinInfo->AddVertices(numVertices);
pSkinInfo->AddBoneInfluences(0, numVertices, boneIndices, boneWeights[0]);
pSkinInfo->AddBoneInfluences(1, numVertices, boneIndices, boneWeights[1]);

//create channel desc
D3DX10_SKINNING_CHANNEL channelDesc;
channelDesc.SrcOffset = 0;
channelDesc.DestOffset = 0;
channelDesc.IsNormal = FALSE;

//do the skinning
pSkinInfo->DoSoftwareSkinning(0, numVertices,
                              vertices, sizeof(MyVertex), 
                              destVertices, sizeof(MyVertex), 
                              boneMatrices, NULL, 
                              &channelDesc, 1);
```



## <a name="requirements"></a><span data-ttu-id="91bb8-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="91bb8-145">Requirements</span></span>



| <span data-ttu-id="91bb8-146">需求</span><span class="sxs-lookup"><span data-stu-id="91bb8-146">Requirement</span></span> | <span data-ttu-id="91bb8-147">值</span><span class="sxs-lookup"><span data-stu-id="91bb8-147">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91bb8-148">標頭</span><span class="sxs-lookup"><span data-stu-id="91bb8-148">Header</span></span><br/>  | <dl> <span data-ttu-id="91bb8-149"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="91bb8-149"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="91bb8-150">程式庫</span><span class="sxs-lookup"><span data-stu-id="91bb8-150">Library</span></span><br/> | <dl> <span data-ttu-id="91bb8-151"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="91bb8-151"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91bb8-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91bb8-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91bb8-153">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="91bb8-153">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="91bb8-154">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="91bb8-154">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
