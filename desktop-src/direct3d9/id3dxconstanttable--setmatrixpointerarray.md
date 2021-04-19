---
description: 設定 nontransposed 矩陣的指標陣列。
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
ms.openlocfilehash: 4b29d4298d8ca52d2826cc780fb90d769c3337f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106975679"
---
# <a name="id3dxconstanttablesetmatrixpointerarray-method"></a><span data-ttu-id="d5875-103">ID3DXConstantTable：： SetMatrixPointerArray 方法</span><span class="sxs-lookup"><span data-stu-id="d5875-103">ID3DXConstantTable::SetMatrixPointerArray method</span></span>

<span data-ttu-id="d5875-104">設定 nontransposed 矩陣的指標陣列。</span><span class="sxs-lookup"><span data-stu-id="d5875-104">Sets an array of pointers to nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5875-105">語法</span><span class="sxs-lookup"><span data-stu-id="d5875-105">Syntax</span></span>


```C++
HRESULT SetMatrixPointerArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        **ppMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="d5875-106">參數</span><span class="sxs-lookup"><span data-stu-id="d5875-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5875-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d5875-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5875-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="d5875-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="d5875-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，表示與常數資料表相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="d5875-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="d5875-110">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d5875-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5875-111">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d5875-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d5875-112">常數矩陣陣列的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="d5875-112">Unique identifier to an array of constant matrices.</span></span> <span data-ttu-id="d5875-113">請參閱 [D3DXHANDLE](dx9-graphics-reference-effects-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="d5875-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5875-114">*ppMatrix* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d5875-114">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5875-115">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="d5875-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="d5875-116">Nontransposed 矩陣的指標陣列。</span><span class="sxs-lookup"><span data-stu-id="d5875-116">Array of pointers to nontransposed matrices.</span></span> <span data-ttu-id="d5875-117">請參閱 [**D3DXMATRIX**](d3dxmatrix.md)。</span><span class="sxs-lookup"><span data-stu-id="d5875-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5875-118">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d5875-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5875-119">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5875-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d5875-120">陣列中的矩陣數目。</span><span class="sxs-lookup"><span data-stu-id="d5875-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5875-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="d5875-121">Return value</span></span>

<span data-ttu-id="d5875-122">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d5875-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d5875-123">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="d5875-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d5875-124">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="d5875-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5875-125">備註</span><span class="sxs-lookup"><span data-stu-id="d5875-125">Remarks</span></span>

<span data-ttu-id="d5875-126">Nontransposed 矩陣包含資料列主要資料;也就是說，每個向量都包含在資料列中。</span><span class="sxs-lookup"><span data-stu-id="d5875-126">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5875-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5875-127">Requirements</span></span>



| <span data-ttu-id="d5875-128">需求</span><span class="sxs-lookup"><span data-stu-id="d5875-128">Requirement</span></span> | <span data-ttu-id="d5875-129">值</span><span class="sxs-lookup"><span data-stu-id="d5875-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5875-130">標頭</span><span class="sxs-lookup"><span data-stu-id="d5875-130">Header</span></span><br/>  | <dl> <span data-ttu-id="d5875-131"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="d5875-131"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d5875-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="d5875-132">Library</span></span><br/> | <dl> <span data-ttu-id="d5875-133"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5875-133"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d5875-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5875-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5875-135">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="d5875-135">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
