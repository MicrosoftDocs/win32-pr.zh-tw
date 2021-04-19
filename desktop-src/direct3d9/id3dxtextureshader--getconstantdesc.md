---
description: 取得常數資料表中常數陣列的指標。
ms.assetid: 2476344b-8433-46bb-9242-dff84e3168e7
title: 'ID3DXTextureShader：： GetConstantDesc 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 22898880e5cef5669defae89cda4f7d9818f9f1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106990023"
---
# <a name="id3dxtextureshadergetconstantdesc-method"></a><span data-ttu-id="9b3b0-103">ID3DXTextureShader：： GetConstantDesc 方法</span><span class="sxs-lookup"><span data-stu-id="9b3b0-103">ID3DXTextureShader::GetConstantDesc method</span></span>

<span data-ttu-id="9b3b0-104">取得常數資料表中常數陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="9b3b0-104">Gets a pointer to the array of constants in the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b3b0-105">語法</span><span class="sxs-lookup"><span data-stu-id="9b3b0-105">Syntax</span></span>


```C++
HRESULT GetConstantDesc(
  [in]      D3DXHANDLE        hConstant,
  [in, out] D3DXCONSTANT_DESC *pDesc,
  [in, out] UINT              *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="9b3b0-106">參數</span><span class="sxs-lookup"><span data-stu-id="9b3b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b3b0-107">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9b3b0-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b3b0-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="9b3b0-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="9b3b0-109">常數的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="9b3b0-109">Unique identifier to a constant.</span></span> <span data-ttu-id="9b3b0-110">請參閱 [D3DXHANDLE](d3dxfx.md)。</span><span class="sxs-lookup"><span data-stu-id="9b3b0-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b3b0-111">*pDesc* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="9b3b0-111">*pDesc* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b3b0-112">類型： **[ **D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="9b3b0-112">Type: **[**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md)\***</span></span>

<span data-ttu-id="9b3b0-113">傳回描述陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="9b3b0-113">Returns a pointer to an array of descriptions.</span></span> <span data-ttu-id="9b3b0-114">請參閱 [**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)。</span><span class="sxs-lookup"><span data-stu-id="9b3b0-114">See [**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b3b0-115">*pCount* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="9b3b0-115">*pCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b3b0-116">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9b3b0-116">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9b3b0-117">提供的輸入必須是陣列的大小上限。</span><span class="sxs-lookup"><span data-stu-id="9b3b0-117">The input supplied must be the maximum size of the array.</span></span> <span data-ttu-id="9b3b0-118">輸出是當函式傳回時，在陣列中填入的元素數目。</span><span class="sxs-lookup"><span data-stu-id="9b3b0-118">The output is the number of elements that are filled in the array when the function returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b3b0-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="9b3b0-119">Return value</span></span>

<span data-ttu-id="9b3b0-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9b3b0-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9b3b0-121">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="9b3b0-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9b3b0-122">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="9b3b0-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b3b0-123">備註</span><span class="sxs-lookup"><span data-stu-id="9b3b0-123">Remarks</span></span>

<span data-ttu-id="9b3b0-124">取樣器可以在常數資料表中出現一次以上，因此，這個方法可以傳回各有不同暫存器索引的描述陣列。</span><span class="sxs-lookup"><span data-stu-id="9b3b0-124">Samplers can appear more than once in a constant table, therefore, this method can return an array of descriptions each with a different register index.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b3b0-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b3b0-125">Requirements</span></span>



| <span data-ttu-id="9b3b0-126">需求</span><span class="sxs-lookup"><span data-stu-id="9b3b0-126">Requirement</span></span> | <span data-ttu-id="9b3b0-127">值</span><span class="sxs-lookup"><span data-stu-id="9b3b0-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b3b0-128">標頭</span><span class="sxs-lookup"><span data-stu-id="9b3b0-128">Header</span></span><br/>  | <dl> <span data-ttu-id="9b3b0-129"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="9b3b0-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="9b3b0-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="9b3b0-130">Library</span></span><br/> | <dl> <span data-ttu-id="9b3b0-131"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b3b0-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="9b3b0-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9b3b0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b3b0-133">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="9b3b0-133">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> <dt>

[<span data-ttu-id="9b3b0-134">**ID3DXTextureShader::GetDesc**</span><span class="sxs-lookup"><span data-stu-id="9b3b0-134">**ID3DXTextureShader::GetDesc**</span></span>](id3dxtextureshader--getdesc.md)
</dt> </dl>

 

 
