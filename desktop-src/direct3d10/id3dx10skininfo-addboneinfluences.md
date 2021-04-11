---
description: 啟用現有的骨骼來影響一組頂點，並定義骨骼對每個頂點的影響程度。
ms.assetid: 37ba97a8-ba40-4700-b8b8-fa7cc9118307
title: 'ID3DX10SkinInfo：： AddBoneInfluences 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.AddBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8531d70e301b0583309817ac23a36762cacf563f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196274"
---
# <a name="id3dx10skininfoaddboneinfluences-method"></a><span data-ttu-id="5e983-103">ID3DX10SkinInfo：： AddBoneInfluences 方法</span><span class="sxs-lookup"><span data-stu-id="5e983-103">ID3DX10SkinInfo::AddBoneInfluences method</span></span>

<span data-ttu-id="5e983-104">啟用現有的骨骼來影響一組頂點，並定義骨骼對每個頂點的影響程度。</span><span class="sxs-lookup"><span data-stu-id="5e983-104">Enable an existing bone to influence a group of vertices and define how much influence the bone has on each vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e983-105">語法</span><span class="sxs-lookup"><span data-stu-id="5e983-105">Syntax</span></span>


```C++
HRESULT AddBoneInfluences(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceCount,
  [in] UINT  *pIndices,
  [in] float *pWeights
);
```



## <a name="parameters"></a><span data-ttu-id="5e983-106">參數</span><span class="sxs-lookup"><span data-stu-id="5e983-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e983-107">*BoneIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5e983-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e983-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5e983-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5e983-109">指定現有骨骼的索引。</span><span class="sxs-lookup"><span data-stu-id="5e983-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="5e983-110">必須介於0和 [**ID3DX10SkinInfo：： GetNumBones**](id3dx10skininfo-getnumbones.md)所傳回的值之間。</span><span class="sxs-lookup"><span data-stu-id="5e983-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e983-111">*InfluenceCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5e983-111">*InfluenceCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e983-112">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5e983-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5e983-113">要加入至骨骼影響的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="5e983-113">Number of vertices to add to the bone's influence.</span></span>

</dd> <dt>

<span data-ttu-id="5e983-114">*pIndices* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5e983-114">*pIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e983-115">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5e983-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5e983-116">頂點索引陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="5e983-116">Pointer to an array of vertex indices.</span></span> <span data-ttu-id="5e983-117">這個陣列的每個成員在 pWeights 中都有對應的成員，因此 pIndices \[ 我 \] 對應到 pWeights \[ i \] 。</span><span class="sxs-lookup"><span data-stu-id="5e983-117">Each member of this array has a corresponding member in pWeights, such that pIndices\[i\] corresponds to pWeights\[i\].</span></span> <span data-ttu-id="5e983-118">PWeights i 中的對應值， \[ \] 會決定 BoneIndex 對 pIndices i 所編制索引之頂點的影響程度 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="5e983-118">The corresponding value in pWeights\[i\] determines how much influence BoneIndex will have on the vertex indexed by pIndices\[i\].</span></span> <span data-ttu-id="5e983-119">PIndices 陣列的大小必須等於或大於 InfluenceCount。</span><span class="sxs-lookup"><span data-stu-id="5e983-119">The size of the pIndices array must be equal to or greater than InfluenceCount.</span></span>

</dd> <dt>

<span data-ttu-id="5e983-120">*pWeights* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5e983-120">*pWeights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e983-121">類型： **float \***</span><span class="sxs-lookup"><span data-stu-id="5e983-121">Type: **float\***</span></span>

<span data-ttu-id="5e983-122">骨骼加權陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="5e983-122">Pointer to an array of bone weights.</span></span> <span data-ttu-id="5e983-123">這個陣列的每個成員在 pIndices 中都有對應的成員，因此 pWeights \[ 我 \] 對應到 pIndices \[ i \] 。</span><span class="sxs-lookup"><span data-stu-id="5e983-123">Each member of this array has a corresponding member in pIndices, such that pWeights\[i\] corresponds to pIndices\[i\].</span></span> <span data-ttu-id="5e983-124">PWeights 中的每個值都介於0和1之間，而且會定義骨骼對每個頂點的影響量。</span><span class="sxs-lookup"><span data-stu-id="5e983-124">Each value in pWeights is between 0 and 1 and defines the amount of influence the bone has over each vertex.</span></span> <span data-ttu-id="5e983-125">PWeights 的大小必須等於或大於 InfluenceCount。</span><span class="sxs-lookup"><span data-stu-id="5e983-125">The size of pWeights must be equal to or greater than InfluenceCount.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e983-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="5e983-126">Return value</span></span>

<span data-ttu-id="5e983-127">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5e983-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5e983-128">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="5e983-128">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5e983-129">如果方法失敗，則傳回值可以是： E \_ INVALIDARG 或 e \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="5e983-129">If the method fails, the return value can be: E\_INVALIDARG or E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e983-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e983-130">Requirements</span></span>



| <span data-ttu-id="5e983-131">需求</span><span class="sxs-lookup"><span data-stu-id="5e983-131">Requirement</span></span> | <span data-ttu-id="5e983-132">值</span><span class="sxs-lookup"><span data-stu-id="5e983-132">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5e983-133">標頭</span><span class="sxs-lookup"><span data-stu-id="5e983-133">Header</span></span><br/>  | <dl> <span data-ttu-id="5e983-134"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="5e983-134"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="5e983-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="5e983-135">Library</span></span><br/> | <dl> <span data-ttu-id="5e983-136"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e983-136"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e983-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5e983-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e983-138">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="5e983-138">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="5e983-139">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="5e983-139">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
