---
description: 取得已轉置矩陣的指標陣列。
ms.assetid: b859ff2f-cf62-4619-b8be-b940fa0513b3
title: 'ID3DXBaseEffect：： GetMatrixTransposePointerArray 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixTransposePointerArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e69c01395582691e6fdd0a695991ff1f726a362b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196439"
---
# <a name="id3dxbaseeffectgetmatrixtransposepointerarray-method"></a><span data-ttu-id="62575-103">ID3DXBaseEffect：： GetMatrixTransposePointerArray 方法</span><span class="sxs-lookup"><span data-stu-id="62575-103">ID3DXBaseEffect::GetMatrixTransposePointerArray method</span></span>

<span data-ttu-id="62575-104">取得已轉置矩陣的指標陣列。</span><span class="sxs-lookup"><span data-stu-id="62575-104">Gets an array of pointers to transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="62575-105">語法</span><span class="sxs-lookup"><span data-stu-id="62575-105">Syntax</span></span>


```C++
HRESULT GetMatrixTransposePointerArray(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX **ppMatrix,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="62575-106">參數</span><span class="sxs-lookup"><span data-stu-id="62575-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62575-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="62575-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62575-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="62575-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="62575-109">唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="62575-109">Unique identifier.</span></span> <span data-ttu-id="62575-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="62575-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="62575-111">*ppMatrix* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="62575-111">*ppMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62575-112">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="62575-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="62575-113">已轉置矩陣的指標陣列。</span><span class="sxs-lookup"><span data-stu-id="62575-113">Array of pointers to transposed matrices.</span></span> <span data-ttu-id="62575-114">請參閱 [**D3DXMATRIX**](d3dxmatrix.md)。</span><span class="sxs-lookup"><span data-stu-id="62575-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="62575-115">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="62575-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62575-116">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="62575-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="62575-117">陣列中的矩陣數目。</span><span class="sxs-lookup"><span data-stu-id="62575-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62575-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="62575-118">Return value</span></span>

<span data-ttu-id="62575-119">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="62575-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="62575-120">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="62575-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="62575-121">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="62575-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="62575-122">備註</span><span class="sxs-lookup"><span data-stu-id="62575-122">Remarks</span></span>

<span data-ttu-id="62575-123">已轉換的矩陣包含資料行主要資料;也就是說，每個向量都包含在資料行中。</span><span class="sxs-lookup"><span data-stu-id="62575-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="62575-124">如果目的地矩陣大於來源矩陣，則只會填入每個目的地矩陣的左上角元件，而其餘的目的地矩陣元件則會設定為零。</span><span class="sxs-lookup"><span data-stu-id="62575-124">If the destination matrices are larger than the source matrices, only the upper-left components of each destination matrix will be filled, and the remaining destination matrix components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="62575-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="62575-125">Requirements</span></span>



| <span data-ttu-id="62575-126">需求</span><span class="sxs-lookup"><span data-stu-id="62575-126">Requirement</span></span> | <span data-ttu-id="62575-127">值</span><span class="sxs-lookup"><span data-stu-id="62575-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="62575-128">標頭</span><span class="sxs-lookup"><span data-stu-id="62575-128">Header</span></span><br/>  | <dl> <span data-ttu-id="62575-129"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="62575-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="62575-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="62575-130">Library</span></span><br/> | <dl> <span data-ttu-id="62575-131"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="62575-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="62575-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62575-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62575-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="62575-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="62575-134">**GetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="62575-134">**GetMatrixTransposeArray**</span></span>](id3dxbaseeffect--getmatrixtransposearray.md)
</dt> </dl>

 

 
