---
description: 設定整數值。
ms.assetid: e7dcf3f4-1d0c-432a-85fc-0473c49956ff
title: 'ID3DXTextureShader：： SetInt 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetInt
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3b440811123935f279b0c4c1661c2a39aa86669f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992132"
---
# <a name="id3dxtextureshadersetint-method"></a><span data-ttu-id="b2059-103">ID3DXTextureShader：： SetInt 方法</span><span class="sxs-lookup"><span data-stu-id="b2059-103">ID3DXTextureShader::SetInt method</span></span>

<span data-ttu-id="b2059-104">設定整數值。</span><span class="sxs-lookup"><span data-stu-id="b2059-104">Sets an integer value.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2059-105">語法</span><span class="sxs-lookup"><span data-stu-id="b2059-105">Syntax</span></span>


```C++
HRESULT SetInt(
  [in] D3DXHANDLE hConstant,
  [in] INT        n
);
```



## <a name="parameters"></a><span data-ttu-id="b2059-106">參數</span><span class="sxs-lookup"><span data-stu-id="b2059-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2059-107">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b2059-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2059-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="b2059-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="b2059-109">常數的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="b2059-109">Unique identifier to the constant.</span></span> <span data-ttu-id="b2059-110">請參閱 [D3DXHANDLE](d3dxfx.md)。</span><span class="sxs-lookup"><span data-stu-id="b2059-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2059-111">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2059-111">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2059-112">類型： **[ **INT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b2059-112">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b2059-113">整數值。</span><span class="sxs-lookup"><span data-stu-id="b2059-113">Integer value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2059-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="b2059-114">Return value</span></span>

<span data-ttu-id="b2059-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b2059-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b2059-116">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="b2059-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b2059-117">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="b2059-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2059-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2059-118">Requirements</span></span>



| <span data-ttu-id="b2059-119">需求</span><span class="sxs-lookup"><span data-stu-id="b2059-119">Requirement</span></span> | <span data-ttu-id="b2059-120">值</span><span class="sxs-lookup"><span data-stu-id="b2059-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2059-121">標頭</span><span class="sxs-lookup"><span data-stu-id="b2059-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b2059-122"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="b2059-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="b2059-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="b2059-123">Library</span></span><br/> | <dl> <span data-ttu-id="b2059-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2059-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b2059-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2059-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2059-126">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="b2059-126">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
