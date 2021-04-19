---
description: 設定整數的陣列。
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
ms.openlocfilehash: d2e43ac1451ec776339d7aba1a4b0288e948f43d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106989200"
---
# <a name="id3dxtextureshadersetintarray-method"></a><span data-ttu-id="37ec5-103">ID3DXTextureShader：： SetIntArray 方法</span><span class="sxs-lookup"><span data-stu-id="37ec5-103">ID3DXTextureShader::SetIntArray method</span></span>

<span data-ttu-id="37ec5-104">設定整數的陣列。</span><span class="sxs-lookup"><span data-stu-id="37ec5-104">Sets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="37ec5-105">語法</span><span class="sxs-lookup"><span data-stu-id="37ec5-105">Syntax</span></span>


```C++
HRESULT SetIntArray(
  [in]       D3DXHANDLE hConstant,
  [in] const INT        *pn,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="37ec5-106">參數</span><span class="sxs-lookup"><span data-stu-id="37ec5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37ec5-107">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="37ec5-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37ec5-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="37ec5-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="37ec5-109">常數陣列的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="37ec5-109">Unique identifier to the array of constants.</span></span> <span data-ttu-id="37ec5-110">請參閱 [D3DXHANDLE](d3dxfx.md)。</span><span class="sxs-lookup"><span data-stu-id="37ec5-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="37ec5-111">*pn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="37ec5-111">*pn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37ec5-112">類型： **Const [**INT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="37ec5-112">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="37ec5-113">整數的陣列。</span><span class="sxs-lookup"><span data-stu-id="37ec5-113">Array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="37ec5-114">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="37ec5-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37ec5-115">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="37ec5-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="37ec5-116">陣列中的整數數目。</span><span class="sxs-lookup"><span data-stu-id="37ec5-116">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37ec5-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="37ec5-117">Return value</span></span>

<span data-ttu-id="37ec5-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="37ec5-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="37ec5-119">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="37ec5-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="37ec5-120">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="37ec5-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="37ec5-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="37ec5-121">Requirements</span></span>



| <span data-ttu-id="37ec5-122">需求</span><span class="sxs-lookup"><span data-stu-id="37ec5-122">Requirement</span></span> | <span data-ttu-id="37ec5-123">值</span><span class="sxs-lookup"><span data-stu-id="37ec5-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="37ec5-124">標頭</span><span class="sxs-lookup"><span data-stu-id="37ec5-124">Header</span></span><br/>  | <dl> <span data-ttu-id="37ec5-125"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="37ec5-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="37ec5-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="37ec5-126">Library</span></span><br/> | <dl> <span data-ttu-id="37ec5-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="37ec5-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="37ec5-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="37ec5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37ec5-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="37ec5-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
