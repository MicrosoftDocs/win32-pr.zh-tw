---
description: ID3DXTextureShader：： SetMatrix 方法：設定未轉換的矩陣。
ms.assetid: 891441ea-09d5-43b6-a080-578d7f8e4586
title: 'ID3DXTextureShader：： SetMatrix 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 15ba6b289ad106a8fad4a932b9c5d01e0a52dc18
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090216"
---
# <a name="id3dxtextureshadersetmatrix-method"></a><span data-ttu-id="c71af-103">ID3DXTextureShader：： SetMatrix 方法</span><span class="sxs-lookup"><span data-stu-id="c71af-103">ID3DXTextureShader::SetMatrix method</span></span>

<span data-ttu-id="c71af-104">設定非轉換的矩陣。</span><span class="sxs-lookup"><span data-stu-id="c71af-104">Sets a non-transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c71af-105">語法</span><span class="sxs-lookup"><span data-stu-id="c71af-105">Syntax</span></span>


```C++
HRESULT SetMatrix(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="c71af-106">參數</span><span class="sxs-lookup"><span data-stu-id="c71af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c71af-107">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c71af-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c71af-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c71af-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c71af-109">常數矩陣的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="c71af-109">Unique identifier to the matrix of constants.</span></span> <span data-ttu-id="c71af-110">請參閱 [D3DXHANDLE](d3dxfx.md)。</span><span class="sxs-lookup"><span data-stu-id="c71af-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="c71af-111">*pMatrix* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c71af-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c71af-112">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c71af-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c71af-113">非轉換矩陣的指標。</span><span class="sxs-lookup"><span data-stu-id="c71af-113">Pointer to a non-transposed matrix.</span></span> <span data-ttu-id="c71af-114">請參閱 [**D3DXMATRIX**](d3dxmatrix.md)。</span><span class="sxs-lookup"><span data-stu-id="c71af-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c71af-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="c71af-115">Return value</span></span>

<span data-ttu-id="c71af-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c71af-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c71af-117">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="c71af-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c71af-118">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="c71af-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c71af-119">備註</span><span class="sxs-lookup"><span data-stu-id="c71af-119">Remarks</span></span>

<span data-ttu-id="c71af-120">未轉換的矩陣包含資料列主要資料;也就是說，每個向量都包含在資料列中。</span><span class="sxs-lookup"><span data-stu-id="c71af-120">A non-transposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

## <a name="requirements"></a><span data-ttu-id="c71af-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="c71af-121">Requirements</span></span>



| <span data-ttu-id="c71af-122">需求</span><span class="sxs-lookup"><span data-stu-id="c71af-122">Requirement</span></span> | <span data-ttu-id="c71af-123">值</span><span class="sxs-lookup"><span data-stu-id="c71af-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c71af-124">標頭</span><span class="sxs-lookup"><span data-stu-id="c71af-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c71af-125"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="c71af-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c71af-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="c71af-126">Library</span></span><br/> | <dl> <span data-ttu-id="c71af-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c71af-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c71af-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c71af-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c71af-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="c71af-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




