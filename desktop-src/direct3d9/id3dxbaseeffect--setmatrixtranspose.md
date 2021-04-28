---
description: ID3DXBaseEffect：： SetMatrixTranspose 方法：設定已轉置的矩陣。
ms.assetid: d340b058-6ba5-43ec-b398-111064965730
title: 'ID3DXBaseEffect：： SetMatrixTranspose 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixTranspose
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 384d4a7ed5e1b769218b9290ed6cc0f7f060bd66
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107396"
---
# <a name="id3dxbaseeffectsetmatrixtranspose-method"></a><span data-ttu-id="2255e-103">ID3DXBaseEffect：： SetMatrixTranspose 方法</span><span class="sxs-lookup"><span data-stu-id="2255e-103">ID3DXBaseEffect::SetMatrixTranspose method</span></span>

<span data-ttu-id="2255e-104">設定已轉置的矩陣。</span><span class="sxs-lookup"><span data-stu-id="2255e-104">Sets a transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="2255e-105">語法</span><span class="sxs-lookup"><span data-stu-id="2255e-105">Syntax</span></span>


```C++
HRESULT SetMatrixTranspose(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="2255e-106">參數</span><span class="sxs-lookup"><span data-stu-id="2255e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2255e-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2255e-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2255e-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2255e-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2255e-109">唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="2255e-109">Unique identifier.</span></span> <span data-ttu-id="2255e-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="2255e-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="2255e-111">*pMatrix* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2255e-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2255e-112">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="2255e-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2255e-113">已轉置矩陣的指標。</span><span class="sxs-lookup"><span data-stu-id="2255e-113">Pointer to a transposed matrix.</span></span> <span data-ttu-id="2255e-114">請參閱 [**D3DXMATRIX**](d3dxmatrix.md)。</span><span class="sxs-lookup"><span data-stu-id="2255e-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2255e-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="2255e-115">Return value</span></span>

<span data-ttu-id="2255e-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2255e-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2255e-117">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="2255e-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2255e-118">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="2255e-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="2255e-119">備註</span><span class="sxs-lookup"><span data-stu-id="2255e-119">Remarks</span></span>

<span data-ttu-id="2255e-120">已轉換的矩陣包含資料行主要資料;也就是說，每個向量都包含在資料行中。</span><span class="sxs-lookup"><span data-stu-id="2255e-120">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="2255e-121">如果目的地矩陣小於來源矩陣，則會忽略來源矩陣的其他元件。</span><span class="sxs-lookup"><span data-stu-id="2255e-121">If the destination matrix is smaller than the source matrix, the additional components of the source matrix will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="2255e-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="2255e-122">Requirements</span></span>



| <span data-ttu-id="2255e-123">需求</span><span class="sxs-lookup"><span data-stu-id="2255e-123">Requirement</span></span> | <span data-ttu-id="2255e-124">值</span><span class="sxs-lookup"><span data-stu-id="2255e-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2255e-125">標頭</span><span class="sxs-lookup"><span data-stu-id="2255e-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2255e-126"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="2255e-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2255e-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="2255e-127">Library</span></span><br/> | <dl> <span data-ttu-id="2255e-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2255e-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2255e-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2255e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2255e-130">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="2255e-130">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="2255e-131">**GetMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="2255e-131">**GetMatrixTranspose**</span></span>](id3dxbaseeffect--getmatrixtranspose.md)
</dt> </dl>

 

 




