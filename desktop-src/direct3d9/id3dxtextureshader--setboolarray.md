---
description: 設定 BOOL 值的陣列。
ms.assetid: d168d362-86b3-4db4-bc52-748a640ebc18
title: 'ID3DXTextureShader：： SetBoolArray 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetBoolArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0799e4ef9d35a886e59fae44c37a841bcda3aed6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986764"
---
# <a name="id3dxtextureshadersetboolarray-method"></a><span data-ttu-id="499a7-103">ID3DXTextureShader：： SetBoolArray 方法</span><span class="sxs-lookup"><span data-stu-id="499a7-103">ID3DXTextureShader::SetBoolArray method</span></span>

<span data-ttu-id="499a7-104">設定 BOOL 值的陣列。</span><span class="sxs-lookup"><span data-stu-id="499a7-104">Sets an array of BOOL values.</span></span>

## <a name="syntax"></a><span data-ttu-id="499a7-105">語法</span><span class="sxs-lookup"><span data-stu-id="499a7-105">Syntax</span></span>


```C++
HRESULT SetBoolArray(
  [in]       D3DXHANDLE hConstant,
  [in] const BOOL       *pB,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="499a7-106">參數</span><span class="sxs-lookup"><span data-stu-id="499a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="499a7-107">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="499a7-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="499a7-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="499a7-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="499a7-109">常數陣列的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="499a7-109">Unique identifier to the array of constants.</span></span> <span data-ttu-id="499a7-110">請參閱 [D3DXHANDLE](d3dxfx.md)。</span><span class="sxs-lookup"><span data-stu-id="499a7-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="499a7-111">*pB* \[在\]</span><span class="sxs-lookup"><span data-stu-id="499a7-111">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="499a7-112">類型： **Const [**BOOL**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="499a7-112">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="499a7-113">BOOL 值的陣列。</span><span class="sxs-lookup"><span data-stu-id="499a7-113">Array of BOOL values.</span></span>

</dd> <dt>

<span data-ttu-id="499a7-114">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="499a7-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="499a7-115">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="499a7-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="499a7-116">陣列中的 BOOL 值數目。</span><span class="sxs-lookup"><span data-stu-id="499a7-116">Number of BOOL values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="499a7-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="499a7-117">Return value</span></span>

<span data-ttu-id="499a7-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="499a7-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="499a7-119">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="499a7-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="499a7-120">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="499a7-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="499a7-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="499a7-121">Requirements</span></span>



| <span data-ttu-id="499a7-122">需求</span><span class="sxs-lookup"><span data-stu-id="499a7-122">Requirement</span></span> | <span data-ttu-id="499a7-123">值</span><span class="sxs-lookup"><span data-stu-id="499a7-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="499a7-124">標頭</span><span class="sxs-lookup"><span data-stu-id="499a7-124">Header</span></span><br/>  | <dl> <span data-ttu-id="499a7-125"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="499a7-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="499a7-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="499a7-126">Library</span></span><br/> | <dl> <span data-ttu-id="499a7-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="499a7-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="499a7-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="499a7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="499a7-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="499a7-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
