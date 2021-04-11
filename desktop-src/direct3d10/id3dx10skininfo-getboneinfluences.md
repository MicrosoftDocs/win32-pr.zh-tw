---
description: 取得指定之骨骼影響的頂點清單，以及骨骼對每個頂點的影響數量清單。
ms.assetid: d1dea694-874d-4f21-87a8-f6b013617544
title: 'ID3DX10SkinInfo：： GetBoneInfluences 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9aead6b1dd381011a922c5bfbc1874976a78417c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196452"
---
# <a name="id3dx10skininfogetboneinfluences-method"></a><span data-ttu-id="99aea-103">ID3DX10SkinInfo：： GetBoneInfluences 方法</span><span class="sxs-lookup"><span data-stu-id="99aea-103">ID3DX10SkinInfo::GetBoneInfluences method</span></span>

<span data-ttu-id="99aea-104">取得指定之骨骼影響的頂點清單，以及骨骼對每個頂點的影響數量清單。</span><span class="sxs-lookup"><span data-stu-id="99aea-104">Get a list of vertices that a given bone influences and a list of the amount of influence that bone has on each vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="99aea-105">語法</span><span class="sxs-lookup"><span data-stu-id="99aea-105">Syntax</span></span>


```C++
HRESULT GetBoneInfluences(
  [in]      UINT  BoneIndex,
  [in]      UINT  Offset,
  [in]      UINT  Count,
  [in, out] UINT  *pDestIndices,
  [in, out] float *pDestWeights
);
```



## <a name="parameters"></a><span data-ttu-id="99aea-106">參數</span><span class="sxs-lookup"><span data-stu-id="99aea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99aea-107">*BoneIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99aea-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99aea-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99aea-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99aea-109">指定現有骨骼的索引。</span><span class="sxs-lookup"><span data-stu-id="99aea-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="99aea-110">必須介於0和 [**ID3DX10SkinInfo：： GetNumBones**](id3dx10skininfo-getnumbones.md)所傳回的值之間。</span><span class="sxs-lookup"><span data-stu-id="99aea-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> <dt>

<span data-ttu-id="99aea-111">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99aea-111">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99aea-112">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99aea-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99aea-113">來自骨骼受影響頂點清單頂端的位移。</span><span class="sxs-lookup"><span data-stu-id="99aea-113">An offset from the top of the bone's list of influenced vertices.</span></span> <span data-ttu-id="99aea-114">這必須介於0和 [**ID3DX10SkinInfo：： GetBoneInfluenceCount**](id3dx10skininfo-getboneinfluencecount.md)所傳回的值之間。</span><span class="sxs-lookup"><span data-stu-id="99aea-114">This must be between 0 and the value returned by [**ID3DX10SkinInfo::GetBoneInfluenceCount**](id3dx10skininfo-getboneinfluencecount.md).</span></span>

</dd> <dt>

<span data-ttu-id="99aea-115">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99aea-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99aea-116">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99aea-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99aea-117">要取出的索引和加權數目。</span><span class="sxs-lookup"><span data-stu-id="99aea-117">The number of indices and weights to retrieve.</span></span> <span data-ttu-id="99aea-118">必須介於0和 ID3DX10SkinInfo：： GetBoneInfluenceCount 所傳回的值之間。</span><span class="sxs-lookup"><span data-stu-id="99aea-118">Must be between 0 and the value returned by ID3DX10SkinInfo::GetBoneInfluenceCount.</span></span>

</dd> <dt>

<span data-ttu-id="99aea-119">*pDestIndices* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="99aea-119">*pDestIndices* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="99aea-120">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="99aea-120">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="99aea-121">頂點緩衝區中的索引清單，每一個都代表一個由骨骼影響的頂點。</span><span class="sxs-lookup"><span data-stu-id="99aea-121">A list of indices into the vertex buffer, each one representing a vertex influenced by the bone.</span></span> <span data-ttu-id="99aea-122">這些值會對應至 pDestWeights 中的值，因此 pDestIndices \[ 我 \] 對應到 pDestWeights \[ i \] 。</span><span class="sxs-lookup"><span data-stu-id="99aea-122">These values correspond to the values in pDestWeights, such that pDestIndices\[i\] corresponds to pDestWeights\[i\].</span></span>

</dd> <dt>

<span data-ttu-id="99aea-123">*pDestWeights* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="99aea-123">*pDestWeights* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="99aea-124">類型： **float \***</span><span class="sxs-lookup"><span data-stu-id="99aea-124">Type: **float\***</span></span>

<span data-ttu-id="99aea-125">此骨骼對每個頂點的影響數量清單。</span><span class="sxs-lookup"><span data-stu-id="99aea-125">A list of the amount of influence the bone has on each vertex.</span></span> <span data-ttu-id="99aea-126">這些值會對應到 pDestIndices 中的值，因此，pDestWeights \[ i \] 對應到 pDestIndices 的 \[ \] f</span><span class="sxs-lookup"><span data-stu-id="99aea-126">These values correspond to the values in pDestIndices, such that pDestWeights\[i\] corresponds to pDestIndices\[i\].f</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99aea-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="99aea-127">Return value</span></span>

<span data-ttu-id="99aea-128">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="99aea-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="99aea-129">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="99aea-129">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="99aea-130">如果方法失敗，則傳回值可以是： E \_ INVALIDARG 或 e \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="99aea-130">If the method fails, the return value can be: E\_INVALIDARG or E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="99aea-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="99aea-131">Requirements</span></span>



| <span data-ttu-id="99aea-132">需求</span><span class="sxs-lookup"><span data-stu-id="99aea-132">Requirement</span></span> | <span data-ttu-id="99aea-133">值</span><span class="sxs-lookup"><span data-stu-id="99aea-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="99aea-134">標頭</span><span class="sxs-lookup"><span data-stu-id="99aea-134">Header</span></span><br/>  | <dl> <span data-ttu-id="99aea-135"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="99aea-135"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="99aea-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="99aea-136">Library</span></span><br/> | <dl> <span data-ttu-id="99aea-137"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="99aea-137"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99aea-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="99aea-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99aea-139">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="99aea-139">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="99aea-140">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="99aea-140">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
