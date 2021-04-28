---
description: ID3DXBaseEffect：： SetMatrix 方法：設定未轉換的矩陣。
ms.assetid: 90329460-756e-4b3e-9ff3-be9dc556eb9f
title: 'ID3DXBaseEffect：： SetMatrix 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrix
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 7af7dc0daa3dcd29e7b15c4fe435b9626ea41746
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097496"
---
# <a name="id3dxbaseeffectsetmatrix-method"></a><span data-ttu-id="8fff5-103">ID3DXBaseEffect：： SetMatrix 方法</span><span class="sxs-lookup"><span data-stu-id="8fff5-103">ID3DXBaseEffect::SetMatrix method</span></span>

<span data-ttu-id="8fff5-104">設定非轉換的矩陣。</span><span class="sxs-lookup"><span data-stu-id="8fff5-104">Sets a non-transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fff5-105">語法</span><span class="sxs-lookup"><span data-stu-id="8fff5-105">Syntax</span></span>


```C++
HRESULT SetMatrix(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="8fff5-106">參數</span><span class="sxs-lookup"><span data-stu-id="8fff5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fff5-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8fff5-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fff5-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="8fff5-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="8fff5-109">唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="8fff5-109">Unique identifier.</span></span> <span data-ttu-id="8fff5-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="8fff5-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="8fff5-111">*pMatrix* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8fff5-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fff5-112">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="8fff5-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8fff5-113">Nontransposed 矩陣的指標。</span><span class="sxs-lookup"><span data-stu-id="8fff5-113">Pointer to a nontransposed matrix.</span></span> <span data-ttu-id="8fff5-114">請參閱 [**D3DXMATRIX**](d3dxmatrix.md)。</span><span class="sxs-lookup"><span data-stu-id="8fff5-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fff5-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="8fff5-115">Return value</span></span>

<span data-ttu-id="8fff5-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8fff5-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8fff5-117">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="8fff5-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8fff5-118">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="8fff5-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fff5-119">備註</span><span class="sxs-lookup"><span data-stu-id="8fff5-119">Remarks</span></span>

<span data-ttu-id="8fff5-120">未轉換的矩陣包含資料列主要資料。</span><span class="sxs-lookup"><span data-stu-id="8fff5-120">A non-transposed matrix contains row-major data.</span></span> <span data-ttu-id="8fff5-121">換句話說，每個向量都會包含在資料列中。</span><span class="sxs-lookup"><span data-stu-id="8fff5-121">In other words, each vector is contained in a row.</span></span>

<span data-ttu-id="8fff5-122">如果目的地矩陣小於來源矩陣，則會忽略來源矩陣的其他元件。</span><span class="sxs-lookup"><span data-stu-id="8fff5-122">If the destination matrix is smaller than the source matrix, the additional components of the source matrix will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fff5-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="8fff5-123">Requirements</span></span>



| <span data-ttu-id="8fff5-124">需求</span><span class="sxs-lookup"><span data-stu-id="8fff5-124">Requirement</span></span> | <span data-ttu-id="8fff5-125">值</span><span class="sxs-lookup"><span data-stu-id="8fff5-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fff5-126">標頭</span><span class="sxs-lookup"><span data-stu-id="8fff5-126">Header</span></span><br/>  | <dl> <span data-ttu-id="8fff5-127"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="8fff5-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="8fff5-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="8fff5-128">Library</span></span><br/> | <dl> <span data-ttu-id="8fff5-129"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8fff5-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8fff5-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8fff5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fff5-131">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="8fff5-131">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="8fff5-132">**GetMatrix**</span><span class="sxs-lookup"><span data-stu-id="8fff5-132">**GetMatrix**</span></span>](id3dxbaseeffect--getmatrix.md)
</dt> </dl>

 

 




