---
description: ID3DXTextureShader：： SetFloatArray 方法：設定浮點數的陣列。
ms.assetid: 8e64b569-a6bf-4925-9d21-4df0b6661ee2
title: 'ID3DXTextureShader：： SetFloatArray 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetFloatArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bd42455e16cbfc203f76de868a82935e0e25401f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090246"
---
# <a name="id3dxtextureshadersetfloatarray-method"></a><span data-ttu-id="f2d0f-103">ID3DXTextureShader：： SetFloatArray 方法</span><span class="sxs-lookup"><span data-stu-id="f2d0f-103">ID3DXTextureShader::SetFloatArray method</span></span>

<span data-ttu-id="f2d0f-104">設定浮點數字的陣列。</span><span class="sxs-lookup"><span data-stu-id="f2d0f-104">Sets an array of floating-point numbers.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2d0f-105">語法</span><span class="sxs-lookup"><span data-stu-id="f2d0f-105">Syntax</span></span>


```C++
HRESULT SetFloatArray(
  [in]       D3DXHANDLE hConstant,
  [in] const FLOAT      *pf,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="f2d0f-106">參數</span><span class="sxs-lookup"><span data-stu-id="f2d0f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2d0f-107">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f2d0f-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2d0f-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f2d0f-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f2d0f-109">常數陣列的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="f2d0f-109">Unique identifier to the array of constants.</span></span> <span data-ttu-id="f2d0f-110">請參閱 [D3DXHANDLE](d3dxfx.md)。</span><span class="sxs-lookup"><span data-stu-id="f2d0f-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2d0f-111">*pf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f2d0f-111">*pf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2d0f-112">Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="f2d0f-112">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f2d0f-113">浮點數的陣列。</span><span class="sxs-lookup"><span data-stu-id="f2d0f-113">Array of floating-point numbers.</span></span>

</dd> <dt>

<span data-ttu-id="f2d0f-114">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f2d0f-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2d0f-115">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f2d0f-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f2d0f-116">陣列中的浮點值數目。</span><span class="sxs-lookup"><span data-stu-id="f2d0f-116">Number of floating-point values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2d0f-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="f2d0f-117">Return value</span></span>

<span data-ttu-id="f2d0f-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f2d0f-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f2d0f-119">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="f2d0f-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f2d0f-120">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="f2d0f-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2d0f-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="f2d0f-121">Requirements</span></span>



| <span data-ttu-id="f2d0f-122">需求</span><span class="sxs-lookup"><span data-stu-id="f2d0f-122">Requirement</span></span> | <span data-ttu-id="f2d0f-123">值</span><span class="sxs-lookup"><span data-stu-id="f2d0f-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2d0f-124">標頭</span><span class="sxs-lookup"><span data-stu-id="f2d0f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f2d0f-125"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="f2d0f-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="f2d0f-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="f2d0f-126">Library</span></span><br/> | <dl> <span data-ttu-id="f2d0f-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2d0f-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f2d0f-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2d0f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2d0f-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="f2d0f-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
