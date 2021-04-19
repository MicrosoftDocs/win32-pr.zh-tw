---
description: 設定4D 向量的陣列。
ms.assetid: 45bc5cb1-b44a-468b-8c80-a639da8a033f
title: 'ID3DXTextureShader：： SetVectorArray 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetVectorArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c91a012cda9d1aa992682b5cb5aa769bf41de180
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986087"
---
# <a name="id3dxtextureshadersetvectorarray-method"></a><span data-ttu-id="fbb6e-103">ID3DXTextureShader：： SetVectorArray 方法</span><span class="sxs-lookup"><span data-stu-id="fbb6e-103">ID3DXTextureShader::SetVectorArray method</span></span>

<span data-ttu-id="fbb6e-104">設定4D 向量的陣列。</span><span class="sxs-lookup"><span data-stu-id="fbb6e-104">Sets an array of 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbb6e-105">語法</span><span class="sxs-lookup"><span data-stu-id="fbb6e-105">Syntax</span></span>


```C++
HRESULT SetVectorArray(
  [in]       D3DXHANDLE  hConstant,
  [in] const D3DXVECTOR4 *pVector,
  [in]       UINT        Count
);
```



## <a name="parameters"></a><span data-ttu-id="fbb6e-106">參數</span><span class="sxs-lookup"><span data-stu-id="fbb6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbb6e-107">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fbb6e-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbb6e-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="fbb6e-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="fbb6e-109">向量常數陣列的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="fbb6e-109">Unique identifier to the array of vector constants.</span></span> <span data-ttu-id="fbb6e-110">請參閱 [D3DXHANDLE](d3dxfx.md)。</span><span class="sxs-lookup"><span data-stu-id="fbb6e-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="fbb6e-111">*pVector* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fbb6e-111">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbb6e-112">Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="fbb6e-112">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="fbb6e-113">4D 向量的陣列。</span><span class="sxs-lookup"><span data-stu-id="fbb6e-113">Array of 4D vectors.</span></span> <span data-ttu-id="fbb6e-114">請參閱 [**D3DXVECTOR4**](d3dxvector4.md)。</span><span class="sxs-lookup"><span data-stu-id="fbb6e-114">See [**D3DXVECTOR4**](d3dxvector4.md).</span></span>

</dd> <dt>

<span data-ttu-id="fbb6e-115">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fbb6e-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbb6e-116">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fbb6e-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fbb6e-117">陣列中的向量數目。</span><span class="sxs-lookup"><span data-stu-id="fbb6e-117">Number of vectors in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbb6e-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="fbb6e-118">Return value</span></span>

<span data-ttu-id="fbb6e-119">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fbb6e-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fbb6e-120">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="fbb6e-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fbb6e-121">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="fbb6e-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbb6e-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="fbb6e-122">Requirements</span></span>



| <span data-ttu-id="fbb6e-123">需求</span><span class="sxs-lookup"><span data-stu-id="fbb6e-123">Requirement</span></span> | <span data-ttu-id="fbb6e-124">值</span><span class="sxs-lookup"><span data-stu-id="fbb6e-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbb6e-125">標頭</span><span class="sxs-lookup"><span data-stu-id="fbb6e-125">Header</span></span><br/>  | <dl> <span data-ttu-id="fbb6e-126"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="fbb6e-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="fbb6e-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="fbb6e-127">Library</span></span><br/> | <dl> <span data-ttu-id="fbb6e-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fbb6e-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="fbb6e-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fbb6e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbb6e-130">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="fbb6e-130">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
