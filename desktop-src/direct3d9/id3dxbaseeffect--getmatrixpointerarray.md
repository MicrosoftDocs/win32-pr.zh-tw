---
description: 取得 nontransposed 矩陣的指標陣列。
ms.assetid: ee9f752d-a06a-43a3-b4ce-d1d585ba8c08
title: 'ID3DXBaseEffect：： GetMatrixPointerArray 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixPointerArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a841c321e641b74841a76432eab8b016f396f61a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946251"
---
# <a name="id3dxbaseeffectgetmatrixpointerarray-method"></a><span data-ttu-id="9e8cf-103">ID3DXBaseEffect：： GetMatrixPointerArray 方法</span><span class="sxs-lookup"><span data-stu-id="9e8cf-103">ID3DXBaseEffect::GetMatrixPointerArray method</span></span>

<span data-ttu-id="9e8cf-104">取得 nontransposed 矩陣的指標陣列。</span><span class="sxs-lookup"><span data-stu-id="9e8cf-104">Gets an array of pointers to nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e8cf-105">語法</span><span class="sxs-lookup"><span data-stu-id="9e8cf-105">Syntax</span></span>


```C++
HRESULT GetMatrixPointerArray(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX **ppMatrix,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="9e8cf-106">參數</span><span class="sxs-lookup"><span data-stu-id="9e8cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e8cf-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9e8cf-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e8cf-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="9e8cf-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="9e8cf-109">唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="9e8cf-109">Unique identifier.</span></span> <span data-ttu-id="9e8cf-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="9e8cf-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e8cf-111">*ppMatrix* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9e8cf-111">*ppMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e8cf-112">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="9e8cf-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="9e8cf-113">Nontransposed 矩陣的指標陣列。</span><span class="sxs-lookup"><span data-stu-id="9e8cf-113">Array of pointers to nontransposed matrices.</span></span> <span data-ttu-id="9e8cf-114">請參閱 [**D3DXMATRIX**](d3dxmatrix.md)。</span><span class="sxs-lookup"><span data-stu-id="9e8cf-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e8cf-115">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9e8cf-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e8cf-116">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9e8cf-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9e8cf-117">陣列中的矩陣數目。</span><span class="sxs-lookup"><span data-stu-id="9e8cf-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e8cf-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="9e8cf-118">Return value</span></span>

<span data-ttu-id="9e8cf-119">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9e8cf-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9e8cf-120">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="9e8cf-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9e8cf-121">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="9e8cf-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e8cf-122">備註</span><span class="sxs-lookup"><span data-stu-id="9e8cf-122">Remarks</span></span>

<span data-ttu-id="9e8cf-123">Nontransposed 矩陣包含資料列主要資料;也就是說，每個向量都包含在資料列中。</span><span class="sxs-lookup"><span data-stu-id="9e8cf-123">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="9e8cf-124">如果目的地矩陣大於來源矩陣，則只會填入每個目的地矩陣的左上角元件，而其餘的目的地矩陣元件則會設定為零。</span><span class="sxs-lookup"><span data-stu-id="9e8cf-124">If the destination matrices are larger than the source matrices, only the upper-left components of each destination matrix will be filled, and the remaining destination matrix components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e8cf-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="9e8cf-125">Requirements</span></span>



| <span data-ttu-id="9e8cf-126">需求</span><span class="sxs-lookup"><span data-stu-id="9e8cf-126">Requirement</span></span> | <span data-ttu-id="9e8cf-127">值</span><span class="sxs-lookup"><span data-stu-id="9e8cf-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e8cf-128">標頭</span><span class="sxs-lookup"><span data-stu-id="9e8cf-128">Header</span></span><br/>  | <dl> <span data-ttu-id="9e8cf-129"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="9e8cf-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="9e8cf-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="9e8cf-130">Library</span></span><br/> | <dl> <span data-ttu-id="9e8cf-131"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e8cf-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="9e8cf-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9e8cf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e8cf-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="9e8cf-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="9e8cf-134">**GetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="9e8cf-134">**GetMatrixArray**</span></span>](id3dxbaseeffect--getmatrixarray.md)
</dt> </dl>

 

 
