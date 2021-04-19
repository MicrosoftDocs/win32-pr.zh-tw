---
description: 變更哪些頂點受哪些骨骼影響。
ms.assetid: b0d71f3e-9a2d-469d-808b-2fa768cf14b0
title: 'ID3DX10SkinInfo：： RemapVertices 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemapVertices
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cc51c912794135b456542bb9a8a779601681f393
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991463"
---
# <a name="id3dx10skininforemapvertices-method"></a><span data-ttu-id="04fcc-103">ID3DX10SkinInfo：： RemapVertices 方法</span><span class="sxs-lookup"><span data-stu-id="04fcc-103">ID3DX10SkinInfo::RemapVertices method</span></span>

<span data-ttu-id="04fcc-104">變更哪些頂點受哪些骨骼影響。</span><span class="sxs-lookup"><span data-stu-id="04fcc-104">Change which vertices are influenced by which bones.</span></span>

## <a name="syntax"></a><span data-ttu-id="04fcc-105">語法</span><span class="sxs-lookup"><span data-stu-id="04fcc-105">Syntax</span></span>


```C++
HRESULT RemapVertices(
  [in] UINT NewVertexCount,
  [in] UINT *pVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="04fcc-106">參數</span><span class="sxs-lookup"><span data-stu-id="04fcc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04fcc-107">*NewVertexCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="04fcc-107">*NewVertexCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04fcc-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="04fcc-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="04fcc-109">新的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="04fcc-109">The new number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="04fcc-110">*pVertexRemap* \[在\]</span><span class="sxs-lookup"><span data-stu-id="04fcc-110">*pVertexRemap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04fcc-111">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="04fcc-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="04fcc-112">指向頂點索引陣列的指標，其描述重新對應。</span><span class="sxs-lookup"><span data-stu-id="04fcc-112">A pointer to an array of vertex indices, which describe the remapping.</span></span> <span data-ttu-id="04fcc-113">例如，假設 SkinInfo 包含一些頂點，例如 bone0 對應至 v0、bone1 至 v1，以及 bone2 為 v2，而且指定了2，1，0的陣列為 pBoneRemap。</span><span class="sxs-lookup"><span data-stu-id="04fcc-113">For example, say SkinInfo contains some vertices such that bone0 is mapped to v0, bone1 to v1, and bone2 to v2, and array with 2,1,0 is specified for pBoneRemap.</span></span> <span data-ttu-id="04fcc-114">這會導致 bone0 對應至 v2、bone1 至 v1，並 bone2 至 v0。</span><span class="sxs-lookup"><span data-stu-id="04fcc-114">This will cause bone0 to be mapped to v2, bone1 to v1, and bone2 to v0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04fcc-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="04fcc-115">Return value</span></span>

<span data-ttu-id="04fcc-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="04fcc-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="04fcc-117">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="04fcc-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="04fcc-118">如果方法失敗，則傳回值可以是： E \_ OUTOFMEMORY 或 e \_ INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="04fcc-118">If the method fails, the return value can be: E\_OUTOFMEMORY or E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="04fcc-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="04fcc-119">Requirements</span></span>



| <span data-ttu-id="04fcc-120">需求</span><span class="sxs-lookup"><span data-stu-id="04fcc-120">Requirement</span></span> | <span data-ttu-id="04fcc-121">值</span><span class="sxs-lookup"><span data-stu-id="04fcc-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="04fcc-122">標頭</span><span class="sxs-lookup"><span data-stu-id="04fcc-122">Header</span></span><br/>  | <dl> <span data-ttu-id="04fcc-123"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="04fcc-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="04fcc-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="04fcc-124">Library</span></span><br/> | <dl> <span data-ttu-id="04fcc-125"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="04fcc-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04fcc-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04fcc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04fcc-127">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="04fcc-127">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="04fcc-128">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="04fcc-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
