---
description: 將指標的陣列設定為已轉置的矩陣。
ms.assetid: f2db10cb-a146-412d-8de8-f093253470fd
title: 'ID3DXConstantTable：： SetMatrixTransposePointerArray 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixTransposePointerArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6c78c051ff2d2ab52c9a741fa117a89f66ff450d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976489"
---
# <a name="id3dxconstanttablesetmatrixtransposepointerarray-method"></a><span data-ttu-id="f2192-103">ID3DXConstantTable：： SetMatrixTransposePointerArray 方法</span><span class="sxs-lookup"><span data-stu-id="f2192-103">ID3DXConstantTable::SetMatrixTransposePointerArray method</span></span>

<span data-ttu-id="f2192-104">將指標的陣列設定為已轉置的矩陣。</span><span class="sxs-lookup"><span data-stu-id="f2192-104">Sets an array of pointers to transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2192-105">語法</span><span class="sxs-lookup"><span data-stu-id="f2192-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposePointerArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        **ppMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="f2192-106">參數</span><span class="sxs-lookup"><span data-stu-id="f2192-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2192-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f2192-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2192-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="f2192-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="f2192-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，表示與常數資料表相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="f2192-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="f2192-110">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f2192-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2192-111">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f2192-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f2192-112">矩陣常數陣列的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="f2192-112">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="f2192-113">請參閱 [D3DXHANDLE](dx9-graphics-reference-effects-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="f2192-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2192-114">*ppMatrix* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f2192-114">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2192-115">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="f2192-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="f2192-116">已轉置矩陣的指標陣列。</span><span class="sxs-lookup"><span data-stu-id="f2192-116">Array of pointers to transposed matrices.</span></span> <span data-ttu-id="f2192-117">請參閱 [**D3DXMATRIX**](d3dxmatrix.md)。</span><span class="sxs-lookup"><span data-stu-id="f2192-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2192-118">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f2192-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2192-119">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f2192-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f2192-120">陣列中的矩陣數目。</span><span class="sxs-lookup"><span data-stu-id="f2192-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2192-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="f2192-121">Return value</span></span>

<span data-ttu-id="f2192-122">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f2192-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f2192-123">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="f2192-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f2192-124">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="f2192-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2192-125">備註</span><span class="sxs-lookup"><span data-stu-id="f2192-125">Remarks</span></span>

<span data-ttu-id="f2192-126">已轉換的矩陣包含資料行主要資料;也就是說，每個向量都包含在資料行中。</span><span class="sxs-lookup"><span data-stu-id="f2192-126">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2192-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="f2192-127">Requirements</span></span>



| <span data-ttu-id="f2192-128">需求</span><span class="sxs-lookup"><span data-stu-id="f2192-128">Requirement</span></span> | <span data-ttu-id="f2192-129">值</span><span class="sxs-lookup"><span data-stu-id="f2192-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2192-130">標頭</span><span class="sxs-lookup"><span data-stu-id="f2192-130">Header</span></span><br/>  | <dl> <span data-ttu-id="f2192-131"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="f2192-131"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="f2192-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="f2192-132">Library</span></span><br/> | <dl> <span data-ttu-id="f2192-133"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2192-133"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f2192-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2192-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2192-135">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="f2192-135">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
