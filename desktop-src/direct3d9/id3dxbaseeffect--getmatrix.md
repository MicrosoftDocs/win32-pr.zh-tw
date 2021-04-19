---
description: 取得 nontransposed 矩陣。
ms.assetid: d507c82c-b1a5-4e83-8921-5d45f52faba0
title: 'ID3DXBaseEffect：： GetMatrix 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrix
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 17d59700d8752526f3f4c48efeaf7f3e6bd985bb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993913"
---
# <a name="id3dxbaseeffectgetmatrix-method"></a><span data-ttu-id="ec936-103">ID3DXBaseEffect：： GetMatrix 方法</span><span class="sxs-lookup"><span data-stu-id="ec936-103">ID3DXBaseEffect::GetMatrix method</span></span>

<span data-ttu-id="ec936-104">取得 nontransposed 矩陣。</span><span class="sxs-lookup"><span data-stu-id="ec936-104">Gets a nontransposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec936-105">語法</span><span class="sxs-lookup"><span data-stu-id="ec936-105">Syntax</span></span>


```C++
HRESULT GetMatrix(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="ec936-106">參數</span><span class="sxs-lookup"><span data-stu-id="ec936-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec936-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ec936-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec936-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="ec936-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="ec936-109">唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="ec936-109">Unique identifier.</span></span> <span data-ttu-id="ec936-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="ec936-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec936-111">*pMatrix* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ec936-111">*pMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec936-112">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ec936-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ec936-113">傳回 nontransposed 矩陣。</span><span class="sxs-lookup"><span data-stu-id="ec936-113">Returns a nontransposed matrix.</span></span> <span data-ttu-id="ec936-114">請參閱 [**D3DXMATRIX**](d3dxmatrix.md)。</span><span class="sxs-lookup"><span data-stu-id="ec936-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec936-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="ec936-115">Return value</span></span>

<span data-ttu-id="ec936-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ec936-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ec936-117">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="ec936-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ec936-118">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="ec936-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec936-119">備註</span><span class="sxs-lookup"><span data-stu-id="ec936-119">Remarks</span></span>

<span data-ttu-id="ec936-120">Nontransposed 矩陣包含資料列主要資料;也就是說，每個向量都包含在資料列中。</span><span class="sxs-lookup"><span data-stu-id="ec936-120">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="ec936-121">如果目的地矩陣大於來源矩陣，則只會填入目的地矩陣的左上角元件，其餘元件則會設定為零。</span><span class="sxs-lookup"><span data-stu-id="ec936-121">If the destination matrix is larger than the source matrix, only the upper-left components of the destination matrix will be filled, and the remaining components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec936-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec936-122">Requirements</span></span>



| <span data-ttu-id="ec936-123">需求</span><span class="sxs-lookup"><span data-stu-id="ec936-123">Requirement</span></span> | <span data-ttu-id="ec936-124">值</span><span class="sxs-lookup"><span data-stu-id="ec936-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec936-125">標頭</span><span class="sxs-lookup"><span data-stu-id="ec936-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ec936-126"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="ec936-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ec936-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="ec936-127">Library</span></span><br/> | <dl> <span data-ttu-id="ec936-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ec936-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ec936-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec936-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec936-130">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="ec936-130">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="ec936-131">**SetMatrix**</span><span class="sxs-lookup"><span data-stu-id="ec936-131">**SetMatrix**</span></span>](id3dxbaseeffect--setmatrix.md)
</dt> </dl>

 

 




