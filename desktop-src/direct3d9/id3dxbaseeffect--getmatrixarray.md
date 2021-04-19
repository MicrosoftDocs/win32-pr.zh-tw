---
description: 取得 nontransposed 矩陣的陣列。
ms.assetid: 37b08f55-22f1-4b60-8cd4-566a77e7dbd6
title: 'ID3DXBaseEffect：： GetMatrixArray 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 242b3c42976f9bfe4ad8ecad4d965c473839ffdd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999051"
---
# <a name="id3dxbaseeffectgetmatrixarray-method"></a><span data-ttu-id="24c21-103">ID3DXBaseEffect：： GetMatrixArray 方法</span><span class="sxs-lookup"><span data-stu-id="24c21-103">ID3DXBaseEffect::GetMatrixArray method</span></span>

<span data-ttu-id="24c21-104">取得 nontransposed 矩陣的陣列。</span><span class="sxs-lookup"><span data-stu-id="24c21-104">Gets an array of nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="24c21-105">語法</span><span class="sxs-lookup"><span data-stu-id="24c21-105">Syntax</span></span>


```C++
HRESULT GetMatrixArray(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="24c21-106">參數</span><span class="sxs-lookup"><span data-stu-id="24c21-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24c21-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="24c21-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24c21-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="24c21-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="24c21-109">唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="24c21-109">Unique identifier.</span></span> <span data-ttu-id="24c21-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="24c21-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="24c21-111">*pMatrix* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="24c21-111">*pMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24c21-112">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="24c21-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="24c21-113">傳回 nontransposed 矩陣的陣列。</span><span class="sxs-lookup"><span data-stu-id="24c21-113">Returns an array of nontransposed matrices.</span></span> <span data-ttu-id="24c21-114">請參閱 [**D3DXMATRIX**](d3dxmatrix.md)。</span><span class="sxs-lookup"><span data-stu-id="24c21-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="24c21-115">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="24c21-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24c21-116">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="24c21-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="24c21-117">陣列中的矩陣數目。</span><span class="sxs-lookup"><span data-stu-id="24c21-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24c21-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="24c21-118">Return value</span></span>

<span data-ttu-id="24c21-119">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="24c21-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="24c21-120">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="24c21-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="24c21-121">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="24c21-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="24c21-122">備註</span><span class="sxs-lookup"><span data-stu-id="24c21-122">Remarks</span></span>

<span data-ttu-id="24c21-123">Nontransposed 矩陣包含資料列主要資料;也就是說，每個向量都包含在資料列中。</span><span class="sxs-lookup"><span data-stu-id="24c21-123">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="24c21-124">如果目的地矩陣大於來源矩陣，則只會填入每個目的地矩陣的左上角元件，而其餘的目的地矩陣元件則會設定為零。</span><span class="sxs-lookup"><span data-stu-id="24c21-124">If the destination matrices are larger than the source matrices, only the upper-left components of each destination matrix will be filled, and the remaining destination matrix components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="24c21-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="24c21-125">Requirements</span></span>



| <span data-ttu-id="24c21-126">需求</span><span class="sxs-lookup"><span data-stu-id="24c21-126">Requirement</span></span> | <span data-ttu-id="24c21-127">值</span><span class="sxs-lookup"><span data-stu-id="24c21-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="24c21-128">標頭</span><span class="sxs-lookup"><span data-stu-id="24c21-128">Header</span></span><br/>  | <dl> <span data-ttu-id="24c21-129"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="24c21-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="24c21-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="24c21-130">Library</span></span><br/> | <dl> <span data-ttu-id="24c21-131"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="24c21-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="24c21-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="24c21-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24c21-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="24c21-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="24c21-134">**SetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="24c21-134">**SetMatrixArray**</span></span>](id3dxbaseeffect--setmatrixarray.md)
</dt> </dl>

 

 
