---
description: 設定向量。
ms.assetid: 7dae88fc-d5d3-4751-859a-fa1bde4d0ce8
title: 'ID3DXBaseEffect：： SetVector 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetVector
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5d6fccc24410e06dd9bb4e6b0b1f1c36b03dd355
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988622"
---
# <a name="id3dxbaseeffectsetvector-method"></a><span data-ttu-id="21ead-103">ID3DXBaseEffect：： SetVector 方法</span><span class="sxs-lookup"><span data-stu-id="21ead-103">ID3DXBaseEffect::SetVector method</span></span>

<span data-ttu-id="21ead-104">設定向量。</span><span class="sxs-lookup"><span data-stu-id="21ead-104">Sets a vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="21ead-105">語法</span><span class="sxs-lookup"><span data-stu-id="21ead-105">Syntax</span></span>


```C++
HRESULT SetVector(
  [in]       D3DXHANDLE  hParameter,
  [in] const D3DXVECTOR4 *pVector
);
```



## <a name="parameters"></a><span data-ttu-id="21ead-106">參數</span><span class="sxs-lookup"><span data-stu-id="21ead-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21ead-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="21ead-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21ead-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="21ead-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="21ead-109">唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="21ead-109">Unique identifier.</span></span> <span data-ttu-id="21ead-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="21ead-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="21ead-111">*pVector* \[在\]</span><span class="sxs-lookup"><span data-stu-id="21ead-111">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21ead-112">Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="21ead-112">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="21ead-113">4D 向量的指標。</span><span class="sxs-lookup"><span data-stu-id="21ead-113">Pointer to a 4D vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21ead-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="21ead-114">Return value</span></span>

<span data-ttu-id="21ead-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="21ead-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="21ead-116">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="21ead-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="21ead-117">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="21ead-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="21ead-118">備註</span><span class="sxs-lookup"><span data-stu-id="21ead-118">Remarks</span></span>

<span data-ttu-id="21ead-119">如果目的地向量小於來源向量，則會忽略來源向量的其他元件。</span><span class="sxs-lookup"><span data-stu-id="21ead-119">If the destination vector is smaller than the source vector, the additional components of the source vector will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="21ead-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="21ead-120">Requirements</span></span>



| <span data-ttu-id="21ead-121">需求</span><span class="sxs-lookup"><span data-stu-id="21ead-121">Requirement</span></span> | <span data-ttu-id="21ead-122">值</span><span class="sxs-lookup"><span data-stu-id="21ead-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="21ead-123">標頭</span><span class="sxs-lookup"><span data-stu-id="21ead-123">Header</span></span><br/>  | <dl> <span data-ttu-id="21ead-124"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="21ead-124"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="21ead-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="21ead-125">Library</span></span><br/> | <dl> <span data-ttu-id="21ead-126"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="21ead-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="21ead-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21ead-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21ead-128">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="21ead-128">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="21ead-129">**GetVector**</span><span class="sxs-lookup"><span data-stu-id="21ead-129">**GetVector**</span></span>](id3dxbaseeffect--getvector.md)
</dt> </dl>

 

 




