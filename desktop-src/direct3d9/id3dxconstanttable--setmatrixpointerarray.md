---
description: ID3DXConstantTable：： SetMatrixPointerArray 方法-將指標陣列設定為 nontransposed 矩陣。
ms.assetid: 1b985e03-b5cb-48e5-969f-115ca165acdc
title: 'ID3DXConstantTable：： SetMatrixPointerArray 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixPointerArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bd9505f82674efc822d4921d7116c8eab17198c1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115066"
---
# <a name="id3dxconstanttablesetmatrixpointerarray-method"></a><span data-ttu-id="a2ef5-103">ID3DXConstantTable：： SetMatrixPointerArray 方法</span><span class="sxs-lookup"><span data-stu-id="a2ef5-103">ID3DXConstantTable::SetMatrixPointerArray method</span></span>

<span data-ttu-id="a2ef5-104">設定 nontransposed 矩陣的指標陣列。</span><span class="sxs-lookup"><span data-stu-id="a2ef5-104">Sets an array of pointers to nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2ef5-105">語法</span><span class="sxs-lookup"><span data-stu-id="a2ef5-105">Syntax</span></span>


```C++
HRESULT SetMatrixPointerArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        **ppMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="a2ef5-106">參數</span><span class="sxs-lookup"><span data-stu-id="a2ef5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2ef5-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a2ef5-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2ef5-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="a2ef5-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="a2ef5-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，表示與常數資料表相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="a2ef5-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="a2ef5-110">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a2ef5-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2ef5-111">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a2ef5-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a2ef5-112">常數矩陣陣列的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="a2ef5-112">Unique identifier to an array of constant matrices.</span></span> <span data-ttu-id="a2ef5-113">請參閱 [D3DXHANDLE](dx9-graphics-reference-effects-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="a2ef5-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2ef5-114">*ppMatrix* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a2ef5-114">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2ef5-115">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="a2ef5-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="a2ef5-116">Nontransposed 矩陣的指標陣列。</span><span class="sxs-lookup"><span data-stu-id="a2ef5-116">Array of pointers to nontransposed matrices.</span></span> <span data-ttu-id="a2ef5-117">請參閱 [**D3DXMATRIX**](d3dxmatrix.md)。</span><span class="sxs-lookup"><span data-stu-id="a2ef5-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2ef5-118">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a2ef5-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2ef5-119">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a2ef5-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a2ef5-120">陣列中的矩陣數目。</span><span class="sxs-lookup"><span data-stu-id="a2ef5-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2ef5-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="a2ef5-121">Return value</span></span>

<span data-ttu-id="a2ef5-122">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a2ef5-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a2ef5-123">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="a2ef5-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a2ef5-124">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="a2ef5-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2ef5-125">備註</span><span class="sxs-lookup"><span data-stu-id="a2ef5-125">Remarks</span></span>

<span data-ttu-id="a2ef5-126">Nontransposed 矩陣包含資料列主要資料;也就是說，每個向量都包含在資料列中。</span><span class="sxs-lookup"><span data-stu-id="a2ef5-126">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2ef5-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2ef5-127">Requirements</span></span>



| <span data-ttu-id="a2ef5-128">需求</span><span class="sxs-lookup"><span data-stu-id="a2ef5-128">Requirement</span></span> | <span data-ttu-id="a2ef5-129">值</span><span class="sxs-lookup"><span data-stu-id="a2ef5-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2ef5-130">標頭</span><span class="sxs-lookup"><span data-stu-id="a2ef5-130">Header</span></span><br/>  | <dl> <span data-ttu-id="a2ef5-131"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="a2ef5-131"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a2ef5-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="a2ef5-132">Library</span></span><br/> | <dl> <span data-ttu-id="a2ef5-133"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2ef5-133"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a2ef5-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2ef5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2ef5-135">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="a2ef5-135">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
