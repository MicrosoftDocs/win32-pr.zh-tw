---
description: 取得指定之骨骼對指定頂點的影響量。
ms.assetid: 0586fdfd-e5b1-4699-b489-c54a0f305ee4
title: 'ID3DX10SkinInfo：： GetBoneInfluence 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluence
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b2f7e6b75e9c0f9f08463b6dacf9d7c9d72f4f28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976721"
---
# <a name="id3dx10skininfogetboneinfluence-method"></a><span data-ttu-id="e877a-103">ID3DX10SkinInfo：： GetBoneInfluence 方法</span><span class="sxs-lookup"><span data-stu-id="e877a-103">ID3DX10SkinInfo::GetBoneInfluence method</span></span>

<span data-ttu-id="e877a-104">取得指定之骨骼對指定頂點的影響量。</span><span class="sxs-lookup"><span data-stu-id="e877a-104">Get the amount of influence a given bone has over a given vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="e877a-105">語法</span><span class="sxs-lookup"><span data-stu-id="e877a-105">Syntax</span></span>


```C++
HRESULT GetBoneInfluence(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceIndex,
  [in] float *pWeight
);
```



## <a name="parameters"></a><span data-ttu-id="e877a-106">參數</span><span class="sxs-lookup"><span data-stu-id="e877a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e877a-107">*BoneIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e877a-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e877a-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e877a-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e877a-109">指定現有骨骼的索引。</span><span class="sxs-lookup"><span data-stu-id="e877a-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="e877a-110">必須介於0和 [**ID3DX10SkinInfo：： GetNumBones**](id3dx10skininfo-getnumbones.md)所傳回的值之間。</span><span class="sxs-lookup"><span data-stu-id="e877a-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> <dt>

<span data-ttu-id="e877a-111">*InfluenceIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e877a-111">*InfluenceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e877a-112">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e877a-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e877a-113">在骨骼的頂點清單中，其會影響的索引。</span><span class="sxs-lookup"><span data-stu-id="e877a-113">An index into the bone's list of vertices that it influences.</span></span>

</dd> <dt>

<span data-ttu-id="e877a-114">*pWeight* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e877a-114">*pWeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e877a-115">類型： **float \***</span><span class="sxs-lookup"><span data-stu-id="e877a-115">Type: **float\***</span></span>

<span data-ttu-id="e877a-116">骨骼在頂點上的影響數量，介於0和1之間。</span><span class="sxs-lookup"><span data-stu-id="e877a-116">The amount of influence, between 0 and 1, that the bone has over the vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e877a-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="e877a-117">Return value</span></span>

<span data-ttu-id="e877a-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e877a-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e877a-119">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="e877a-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e877a-120">如果方法失敗，則傳回值可以是 E \_ INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="e877a-120">If the method fails, the return value can be E\_INVALIDARG.</span></span>

## <a name="remarks"></a><span data-ttu-id="e877a-121">備註</span><span class="sxs-lookup"><span data-stu-id="e877a-121">Remarks</span></span>

<span data-ttu-id="e877a-122">使用 ID3DX10SkinInfo：： GetBoneInfluenceCount 來找出骨骼影響的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="e877a-122">Use ID3DX10SkinInfo::GetBoneInfluenceCount to find out how many vertices the bone influences.</span></span>

## <a name="requirements"></a><span data-ttu-id="e877a-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="e877a-123">Requirements</span></span>



| <span data-ttu-id="e877a-124">需求</span><span class="sxs-lookup"><span data-stu-id="e877a-124">Requirement</span></span> | <span data-ttu-id="e877a-125">值</span><span class="sxs-lookup"><span data-stu-id="e877a-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e877a-126">標頭</span><span class="sxs-lookup"><span data-stu-id="e877a-126">Header</span></span><br/>  | <dl> <span data-ttu-id="e877a-127"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="e877a-127"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="e877a-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="e877a-128">Library</span></span><br/> | <dl> <span data-ttu-id="e877a-129"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e877a-129"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e877a-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e877a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e877a-131">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="e877a-131">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="e877a-132">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="e877a-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
