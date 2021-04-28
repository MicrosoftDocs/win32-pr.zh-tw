---
description: ID3DXTextureShader：： SetIntArray 方法：設定整數的陣列。
ms.assetid: 1ceb8bb0-d168-49cf-8964-8ae582b5ec2e
title: 'ID3DXTextureShader：： SetIntArray 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetIntArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ddc00637bddf2810e73be7755a9dcfb8696053e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097486"
---
# <a name="id3dxtextureshadersetintarray-method"></a><span data-ttu-id="abef6-103">ID3DXTextureShader：： SetIntArray 方法</span><span class="sxs-lookup"><span data-stu-id="abef6-103">ID3DXTextureShader::SetIntArray method</span></span>

<span data-ttu-id="abef6-104">設定整數的陣列。</span><span class="sxs-lookup"><span data-stu-id="abef6-104">Sets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="abef6-105">語法</span><span class="sxs-lookup"><span data-stu-id="abef6-105">Syntax</span></span>


```C++
HRESULT SetIntArray(
  [in]       D3DXHANDLE hConstant,
  [in] const INT        *pn,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="abef6-106">參數</span><span class="sxs-lookup"><span data-stu-id="abef6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abef6-107">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="abef6-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abef6-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="abef6-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="abef6-109">常數陣列的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="abef6-109">Unique identifier to the array of constants.</span></span> <span data-ttu-id="abef6-110">請參閱 [D3DXHANDLE](d3dxfx.md)。</span><span class="sxs-lookup"><span data-stu-id="abef6-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="abef6-111">*pn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="abef6-111">*pn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abef6-112">類型： **Const [**INT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="abef6-112">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="abef6-113">整數的陣列。</span><span class="sxs-lookup"><span data-stu-id="abef6-113">Array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="abef6-114">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="abef6-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abef6-115">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="abef6-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="abef6-116">陣列中的整數數目。</span><span class="sxs-lookup"><span data-stu-id="abef6-116">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abef6-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="abef6-117">Return value</span></span>

<span data-ttu-id="abef6-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="abef6-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="abef6-119">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="abef6-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="abef6-120">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="abef6-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="abef6-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="abef6-121">Requirements</span></span>



| <span data-ttu-id="abef6-122">需求</span><span class="sxs-lookup"><span data-stu-id="abef6-122">Requirement</span></span> | <span data-ttu-id="abef6-123">值</span><span class="sxs-lookup"><span data-stu-id="abef6-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="abef6-124">標頭</span><span class="sxs-lookup"><span data-stu-id="abef6-124">Header</span></span><br/>  | <dl> <span data-ttu-id="abef6-125"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="abef6-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="abef6-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="abef6-126">Library</span></span><br/> | <dl> <span data-ttu-id="abef6-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="abef6-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="abef6-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="abef6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abef6-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="abef6-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
