---
description: 設定4D 向量。
ms.assetid: befed2a8-7695-4f06-a6ee-aff466d1940a
title: 'ID3DXTextureShader：： SetVector 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetVector
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b7bc7e3b7f4920c21c52111410c626090e452fa7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000583"
---
# <a name="id3dxtextureshadersetvector-method"></a><span data-ttu-id="bae6e-103">ID3DXTextureShader：： SetVector 方法</span><span class="sxs-lookup"><span data-stu-id="bae6e-103">ID3DXTextureShader::SetVector method</span></span>

<span data-ttu-id="bae6e-104">設定4D 向量。</span><span class="sxs-lookup"><span data-stu-id="bae6e-104">Sets a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="bae6e-105">語法</span><span class="sxs-lookup"><span data-stu-id="bae6e-105">Syntax</span></span>


```C++
HRESULT SetVector(
  [in]       D3DXHANDLE  hConstant,
  [in] const D3DXVECTOR4 *pVector
);
```



## <a name="parameters"></a><span data-ttu-id="bae6e-106">參數</span><span class="sxs-lookup"><span data-stu-id="bae6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bae6e-107">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bae6e-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bae6e-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="bae6e-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="bae6e-109">向量常數的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="bae6e-109">Unique identifier to the vector constant.</span></span> <span data-ttu-id="bae6e-110">請參閱 [D3DXHANDLE](d3dxfx.md)。</span><span class="sxs-lookup"><span data-stu-id="bae6e-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="bae6e-111">*pVector* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bae6e-111">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bae6e-112">Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="bae6e-112">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="bae6e-113">4D 向量的指標。</span><span class="sxs-lookup"><span data-stu-id="bae6e-113">Pointer to a 4D vector.</span></span> <span data-ttu-id="bae6e-114">請參閱 [**D3DXVECTOR4**](d3dxvector4.md)。</span><span class="sxs-lookup"><span data-stu-id="bae6e-114">See [**D3DXVECTOR4**](d3dxvector4.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bae6e-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="bae6e-115">Return value</span></span>

<span data-ttu-id="bae6e-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bae6e-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bae6e-117">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="bae6e-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bae6e-118">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="bae6e-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="bae6e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="bae6e-119">Requirements</span></span>



| <span data-ttu-id="bae6e-120">需求</span><span class="sxs-lookup"><span data-stu-id="bae6e-120">Requirement</span></span> | <span data-ttu-id="bae6e-121">值</span><span class="sxs-lookup"><span data-stu-id="bae6e-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bae6e-122">標頭</span><span class="sxs-lookup"><span data-stu-id="bae6e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="bae6e-123"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="bae6e-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="bae6e-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="bae6e-124">Library</span></span><br/> | <dl> <span data-ttu-id="bae6e-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bae6e-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="bae6e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bae6e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bae6e-127">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="bae6e-127">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




