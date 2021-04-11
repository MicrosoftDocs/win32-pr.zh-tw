---
description: 找出表示指定頂點在受影響頂點的指定清單中之位置的索引。
ms.assetid: vs|directx_sdk|~\id3dx10skininfo_findboneinfluenceindex.htm
title: 'ID3DX10SkinInfo：： FindBoneInfluenceIndex 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.FindBoneInfluenceIndex
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1468fed3c0cf999e7635ba0f5ae53cee72fe70c6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196351"
---
# <a name="id3dx10skininfofindboneinfluenceindex-method"></a><span data-ttu-id="e7fff-103">ID3DX10SkinInfo：： FindBoneInfluenceIndex 方法</span><span class="sxs-lookup"><span data-stu-id="e7fff-103">ID3DX10SkinInfo::FindBoneInfluenceIndex method</span></span>

<span data-ttu-id="e7fff-104">找出表示指定頂點在受影響頂點的指定清單中之位置的索引。</span><span class="sxs-lookup"><span data-stu-id="e7fff-104">Find the index that indicates where a given vertex is in a given bone's list of influenced vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7fff-105">語法</span><span class="sxs-lookup"><span data-stu-id="e7fff-105">Syntax</span></span>


```C++
HRESULT FindBoneInfluenceIndex(
  [in] UINT BoneIndex,
  [in] UINT VertexIndex,
  [in] UINT *pInfluenceIndex
);
```



## <a name="parameters"></a><span data-ttu-id="e7fff-106">參數</span><span class="sxs-lookup"><span data-stu-id="e7fff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7fff-107">*BoneIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e7fff-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7fff-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e7fff-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e7fff-109">指定現有骨骼的索引。</span><span class="sxs-lookup"><span data-stu-id="e7fff-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="e7fff-110">必須介於0和 [**ID3DX10SkinInfo：： GetNumBones**](id3dx10skininfo-getnumbones.md)所傳回的值之間。</span><span class="sxs-lookup"><span data-stu-id="e7fff-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7fff-111">*VertexIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e7fff-111">*VertexIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7fff-112">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e7fff-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e7fff-113">頂點緩衝區中頂點的索引。</span><span class="sxs-lookup"><span data-stu-id="e7fff-113">The index of the vertex in the vertex buffer.</span></span>

</dd> <dt>

<span data-ttu-id="e7fff-114">*pInfluenceIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e7fff-114">*pInfluenceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7fff-115">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e7fff-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e7fff-116">骨骼之受影響頂點清單中頂點的索引。</span><span class="sxs-lookup"><span data-stu-id="e7fff-116">The index of the vertex in the bone's list of influenced vertices.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7fff-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="e7fff-117">Return value</span></span>

<span data-ttu-id="e7fff-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e7fff-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e7fff-119">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="e7fff-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e7fff-120">如果方法失敗，則傳回值可以是： E \_ INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="e7fff-120">If the method fails, the return value can be: E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7fff-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7fff-121">Requirements</span></span>



| <span data-ttu-id="e7fff-122">需求</span><span class="sxs-lookup"><span data-stu-id="e7fff-122">Requirement</span></span> | <span data-ttu-id="e7fff-123">值</span><span class="sxs-lookup"><span data-stu-id="e7fff-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7fff-124">標頭</span><span class="sxs-lookup"><span data-stu-id="e7fff-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e7fff-125"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="e7fff-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="e7fff-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="e7fff-126">Library</span></span><br/> | <dl> <span data-ttu-id="e7fff-127"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7fff-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7fff-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7fff-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7fff-129">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="e7fff-129">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="e7fff-130">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="e7fff-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
