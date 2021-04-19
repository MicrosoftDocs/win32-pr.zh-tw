---
description: 設定指定之骨骼對指定頂點的影響量。
ms.assetid: adbdc784-c6b4-4e10-85c8-5e0b794d946f
title: 'ID3DX10SkinInfo：： SetBoneInfluence 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.SetBoneInfluence
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d136ddf4491a2a00c029422512c671a5439ba47c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000609"
---
# <a name="id3dx10skininfosetboneinfluence-method"></a><span data-ttu-id="0cf21-103">ID3DX10SkinInfo：： SetBoneInfluence 方法</span><span class="sxs-lookup"><span data-stu-id="0cf21-103">ID3DX10SkinInfo::SetBoneInfluence method</span></span>

<span data-ttu-id="0cf21-104">設定指定之骨骼對指定頂點的影響量。</span><span class="sxs-lookup"><span data-stu-id="0cf21-104">Set the amount of influence a given bone has over a given vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cf21-105">語法</span><span class="sxs-lookup"><span data-stu-id="0cf21-105">Syntax</span></span>


```C++
HRESULT SetBoneInfluence(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceIndex,
  [in] float Weight
);
```



## <a name="parameters"></a><span data-ttu-id="0cf21-106">參數</span><span class="sxs-lookup"><span data-stu-id="0cf21-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cf21-107">*BoneIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0cf21-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cf21-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0cf21-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0cf21-109">指定現有骨骼的索引。</span><span class="sxs-lookup"><span data-stu-id="0cf21-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="0cf21-110">必須介於0和 [**ID3DX10SkinInfo：： GetNumBones**](id3dx10skininfo-getnumbones.md)所傳回的值之間。</span><span class="sxs-lookup"><span data-stu-id="0cf21-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> <dt>

<span data-ttu-id="0cf21-111">*InfluenceIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0cf21-111">*InfluenceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cf21-112">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0cf21-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0cf21-113">在骨骼的頂點清單中，其會影響的索引。</span><span class="sxs-lookup"><span data-stu-id="0cf21-113">An index into the bone's list of vertices that it influences.</span></span>

</dd> <dt>

<span data-ttu-id="0cf21-114">*權數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0cf21-114">*Weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cf21-115">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="0cf21-115">Type: **float**</span></span>

<span data-ttu-id="0cf21-116">骨骼在頂點上的影響數量，介於0和1之間。</span><span class="sxs-lookup"><span data-stu-id="0cf21-116">The amount of influence, between 0 and 1, that the bone has over the vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cf21-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="0cf21-117">Return value</span></span>

<span data-ttu-id="0cf21-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0cf21-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0cf21-119">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="0cf21-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0cf21-120">如果方法失敗，則傳回值可以是 E \_ INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="0cf21-120">If the method fails, the return value can be E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cf21-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="0cf21-121">Requirements</span></span>



| <span data-ttu-id="0cf21-122">需求</span><span class="sxs-lookup"><span data-stu-id="0cf21-122">Requirement</span></span> | <span data-ttu-id="0cf21-123">值</span><span class="sxs-lookup"><span data-stu-id="0cf21-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0cf21-124">標頭</span><span class="sxs-lookup"><span data-stu-id="0cf21-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0cf21-125"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="0cf21-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="0cf21-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="0cf21-126">Library</span></span><br/> | <dl> <span data-ttu-id="0cf21-127"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0cf21-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cf21-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0cf21-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cf21-129">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="0cf21-129">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="0cf21-130">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="0cf21-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
