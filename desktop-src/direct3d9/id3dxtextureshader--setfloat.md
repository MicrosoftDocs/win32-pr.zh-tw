---
description: 設定浮點數。
ms.assetid: 69bb9b15-5d66-4b1a-9559-29bcb38a965f
title: 'ID3DXTextureShader：： SetFloat 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetFloat
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 85923fe20731b4482f70c439cb9df75712ab09f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997418"
---
# <a name="id3dxtextureshadersetfloat-method"></a><span data-ttu-id="d2f8a-103">ID3DXTextureShader：： SetFloat 方法</span><span class="sxs-lookup"><span data-stu-id="d2f8a-103">ID3DXTextureShader::SetFloat method</span></span>

<span data-ttu-id="d2f8a-104">設定浮點數。</span><span class="sxs-lookup"><span data-stu-id="d2f8a-104">Sets a floating-point number.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2f8a-105">語法</span><span class="sxs-lookup"><span data-stu-id="d2f8a-105">Syntax</span></span>


```C++
HRESULT SetFloat(
  [in] D3DXHANDLE hConstant,
  [in] FLOAT      f
);
```



## <a name="parameters"></a><span data-ttu-id="d2f8a-106">參數</span><span class="sxs-lookup"><span data-stu-id="d2f8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2f8a-107">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d2f8a-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2f8a-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d2f8a-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d2f8a-109">常數的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="d2f8a-109">Unique identifier to the constant.</span></span> <span data-ttu-id="d2f8a-110">請參閱 [D3DXHANDLE](d3dxfx.md)。</span><span class="sxs-lookup"><span data-stu-id="d2f8a-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2f8a-111">*f* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2f8a-111">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2f8a-112">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d2f8a-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d2f8a-113">浮點數。</span><span class="sxs-lookup"><span data-stu-id="d2f8a-113">Floating-point number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2f8a-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="d2f8a-114">Return value</span></span>

<span data-ttu-id="d2f8a-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d2f8a-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d2f8a-116">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="d2f8a-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d2f8a-117">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="d2f8a-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2f8a-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="d2f8a-118">Requirements</span></span>



| <span data-ttu-id="d2f8a-119">需求</span><span class="sxs-lookup"><span data-stu-id="d2f8a-119">Requirement</span></span> | <span data-ttu-id="d2f8a-120">值</span><span class="sxs-lookup"><span data-stu-id="d2f8a-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2f8a-121">標頭</span><span class="sxs-lookup"><span data-stu-id="d2f8a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d2f8a-122"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="d2f8a-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d2f8a-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="d2f8a-123">Library</span></span><br/> | <dl> <span data-ttu-id="d2f8a-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2f8a-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d2f8a-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d2f8a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2f8a-126">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="d2f8a-126">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
