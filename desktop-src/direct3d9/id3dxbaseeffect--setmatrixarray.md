---
description: 設定 nontransposed 矩陣的陣列。
ms.assetid: 008de62c-3a36-4499-8a0b-9075756395e9
title: 'ID3DXBaseEffect：： SetMatrixArray 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c48dcb3288930a9170c932f335a4b20c258acbb4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322619"
---
# <a name="id3dxbaseeffectsetmatrixarray-method"></a><span data-ttu-id="fa065-103">ID3DXBaseEffect：： SetMatrixArray 方法</span><span class="sxs-lookup"><span data-stu-id="fa065-103">ID3DXBaseEffect::SetMatrixArray method</span></span>

<span data-ttu-id="fa065-104">設定 nontransposed 矩陣的陣列。</span><span class="sxs-lookup"><span data-stu-id="fa065-104">Sets an array of nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa065-105">語法</span><span class="sxs-lookup"><span data-stu-id="fa065-105">Syntax</span></span>


```C++
HRESULT SetMatrixArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="fa065-106">參數</span><span class="sxs-lookup"><span data-stu-id="fa065-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa065-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fa065-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa065-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="fa065-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="fa065-109">唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="fa065-109">Unique identifier.</span></span> <span data-ttu-id="fa065-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="fa065-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa065-111">*pMatrix* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fa065-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa065-112">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="fa065-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fa065-113">Nontransposed 矩陣的陣列。</span><span class="sxs-lookup"><span data-stu-id="fa065-113">Array of nontransposed matrices.</span></span> <span data-ttu-id="fa065-114">請參閱 [**D3DXMATRIX**](d3dxmatrix.md)。</span><span class="sxs-lookup"><span data-stu-id="fa065-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa065-115">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fa065-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa065-116">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fa065-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fa065-117">陣列中的矩陣數目。</span><span class="sxs-lookup"><span data-stu-id="fa065-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa065-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="fa065-118">Return value</span></span>

<span data-ttu-id="fa065-119">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fa065-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fa065-120">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="fa065-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fa065-121">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="fa065-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa065-122">備註</span><span class="sxs-lookup"><span data-stu-id="fa065-122">Remarks</span></span>

<span data-ttu-id="fa065-123">Nontransposed 矩陣包含資料列主要資料;也就是說，每個向量都包含在資料列中。</span><span class="sxs-lookup"><span data-stu-id="fa065-123">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="fa065-124">如果目的地矩陣小於來源矩陣，則會忽略來源矩陣的其他元件。</span><span class="sxs-lookup"><span data-stu-id="fa065-124">If the destination matrices are smaller than the source matrices, the additional components of the source matrices will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa065-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa065-125">Requirements</span></span>



| <span data-ttu-id="fa065-126">需求</span><span class="sxs-lookup"><span data-stu-id="fa065-126">Requirement</span></span> | <span data-ttu-id="fa065-127">值</span><span class="sxs-lookup"><span data-stu-id="fa065-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa065-128">標頭</span><span class="sxs-lookup"><span data-stu-id="fa065-128">Header</span></span><br/>  | <dl> <span data-ttu-id="fa065-129"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="fa065-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="fa065-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="fa065-130">Library</span></span><br/> | <dl> <span data-ttu-id="fa065-131"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa065-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="fa065-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa065-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa065-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="fa065-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="fa065-134">**GetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="fa065-134">**GetMatrixArray**</span></span>](id3dxbaseeffect--getmatrixarray.md)
</dt> </dl>

 

 
