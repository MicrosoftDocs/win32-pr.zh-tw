---
description: 變更哪些骨骼會影響哪些頂點。
ms.assetid: 0955e0ba-ffc5-408b-ab38-2abd39e1c429
title: 'ID3DX10SkinInfo：： RemapBones 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemapBones
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 238e4628740fa74e055312c82de2635316f5bde5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988186"
---
# <a name="id3dx10skininforemapbones-method"></a><span data-ttu-id="8ce8c-103">ID3DX10SkinInfo：： RemapBones 方法</span><span class="sxs-lookup"><span data-stu-id="8ce8c-103">ID3DX10SkinInfo::RemapBones method</span></span>

<span data-ttu-id="8ce8c-104">變更哪些骨骼會影響哪些頂點。</span><span class="sxs-lookup"><span data-stu-id="8ce8c-104">Change which bones influence which vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ce8c-105">語法</span><span class="sxs-lookup"><span data-stu-id="8ce8c-105">Syntax</span></span>


```C++
HRESULT RemapBones(
  [in] UINT NewBoneCount,
  [in] UINT *pBoneRemap
);
```



## <a name="parameters"></a><span data-ttu-id="8ce8c-106">參數</span><span class="sxs-lookup"><span data-stu-id="8ce8c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ce8c-107">*NewBoneCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8ce8c-107">*NewBoneCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ce8c-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ce8c-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8ce8c-109">新的骨骼數目。</span><span class="sxs-lookup"><span data-stu-id="8ce8c-109">The new number of bones.</span></span>

</dd> <dt>

<span data-ttu-id="8ce8c-110">*pBoneRemap* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8ce8c-110">*pBoneRemap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ce8c-111">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ce8c-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8ce8c-112">描述重新對應之骨骼索引陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="8ce8c-112">A pointer to an array of bone indices, which describe the remapping.</span></span> <span data-ttu-id="8ce8c-113">例如，假設 SkinInfo 包含一些骨骼，例如 bone0 對應至 v0、bone1 至 v1，以及 bone2 為 v2，而且指定了2，1，0的陣列為 pBoneRemap。</span><span class="sxs-lookup"><span data-stu-id="8ce8c-113">For example, say SkinInfo contains some bones such that bone0 is mapped to v0, bone1 to v1, and bone2 to v2, and array with 2,1,0 is specified for pBoneRemap.</span></span> <span data-ttu-id="8ce8c-114">這會導致 bone0 對應至 v2、bone1 至 v1，並 bone2 至 v0。</span><span class="sxs-lookup"><span data-stu-id="8ce8c-114">This will cause bone0 to be mapped to v2, bone1 to v1, and bone2 to v0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ce8c-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="8ce8c-115">Return value</span></span>

<span data-ttu-id="8ce8c-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8ce8c-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8ce8c-117">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="8ce8c-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="8ce8c-118">如果方法失敗，則傳回值可以是： E \_ OUTOFMEMORY 或 e \_ INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="8ce8c-118">If the method fails, the return value can be: E\_OUTOFMEMORY or E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ce8c-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ce8c-119">Requirements</span></span>



| <span data-ttu-id="8ce8c-120">需求</span><span class="sxs-lookup"><span data-stu-id="8ce8c-120">Requirement</span></span> | <span data-ttu-id="8ce8c-121">值</span><span class="sxs-lookup"><span data-stu-id="8ce8c-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8ce8c-122">標頭</span><span class="sxs-lookup"><span data-stu-id="8ce8c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="8ce8c-123"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="8ce8c-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="8ce8c-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="8ce8c-124">Library</span></span><br/> | <dl> <span data-ttu-id="8ce8c-125"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ce8c-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ce8c-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ce8c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ce8c-127">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="8ce8c-127">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="8ce8c-128">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="8ce8c-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
