---
description: 設定已轉置的矩陣。
ms.assetid: 5339a9de-528f-4404-880b-73964192b766
title: 'ID3DXTextureShader：： SetMatrixTranspose 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixTranspose
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cf5507d935d2fea1b6210624e70344a2c4a1da81
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946116"
---
# <a name="id3dxtextureshadersetmatrixtranspose-method"></a><span data-ttu-id="c1069-103">ID3DXTextureShader：： SetMatrixTranspose 方法</span><span class="sxs-lookup"><span data-stu-id="c1069-103">ID3DXTextureShader::SetMatrixTranspose method</span></span>

<span data-ttu-id="c1069-104">設定已轉置的矩陣。</span><span class="sxs-lookup"><span data-stu-id="c1069-104">Sets a transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1069-105">語法</span><span class="sxs-lookup"><span data-stu-id="c1069-105">Syntax</span></span>


```C++
HRESULT SetMatrixTranspose(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="c1069-106">參數</span><span class="sxs-lookup"><span data-stu-id="c1069-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1069-107">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c1069-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1069-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c1069-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c1069-109">常數矩陣的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="c1069-109">Unique identifier to the matrix of constants.</span></span> <span data-ttu-id="c1069-110">請參閱 [D3DXHANDLE](d3dxfx.md)。</span><span class="sxs-lookup"><span data-stu-id="c1069-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1069-111">*pMatrix* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c1069-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1069-112">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c1069-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c1069-113">已轉置矩陣的指標。</span><span class="sxs-lookup"><span data-stu-id="c1069-113">Pointer to a transposed matrix.</span></span> <span data-ttu-id="c1069-114">請參閱 [**D3DXMATRIX**](d3dxmatrix.md)。</span><span class="sxs-lookup"><span data-stu-id="c1069-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1069-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="c1069-115">Return value</span></span>

<span data-ttu-id="c1069-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c1069-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c1069-117">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="c1069-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c1069-118">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="c1069-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1069-119">備註</span><span class="sxs-lookup"><span data-stu-id="c1069-119">Remarks</span></span>

<span data-ttu-id="c1069-120">已轉換的矩陣包含資料行主要資料;也就是說，每個向量都包含在資料行中。</span><span class="sxs-lookup"><span data-stu-id="c1069-120">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1069-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1069-121">Requirements</span></span>



| <span data-ttu-id="c1069-122">需求</span><span class="sxs-lookup"><span data-stu-id="c1069-122">Requirement</span></span> | <span data-ttu-id="c1069-123">值</span><span class="sxs-lookup"><span data-stu-id="c1069-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1069-124">標頭</span><span class="sxs-lookup"><span data-stu-id="c1069-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c1069-125"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="c1069-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c1069-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="c1069-126">Library</span></span><br/> | <dl> <span data-ttu-id="c1069-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1069-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c1069-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1069-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1069-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="c1069-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




