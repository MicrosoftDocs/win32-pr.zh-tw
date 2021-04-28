---
description: ID3DXConstantTable：： SetMatrixTransposeArray 方法-設定已轉置矩陣的陣列。
ms.assetid: a67afc21-f43d-4dc5-b145-f3d66dd86dbb
title: 'ID3DXConstantTable：： SetMatrixTransposeArray 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixTransposeArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0118c888adc52671a943b7b159bae80deca26a1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115046"
---
# <a name="id3dxconstanttablesetmatrixtransposearray-method"></a><span data-ttu-id="60ca6-103">ID3DXConstantTable：： SetMatrixTransposeArray 方法</span><span class="sxs-lookup"><span data-stu-id="60ca6-103">ID3DXConstantTable::SetMatrixTransposeArray method</span></span>

<span data-ttu-id="60ca6-104">設定已轉置矩陣的陣列。</span><span class="sxs-lookup"><span data-stu-id="60ca6-104">Sets an array of transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="60ca6-105">語法</span><span class="sxs-lookup"><span data-stu-id="60ca6-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposeArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="60ca6-106">參數</span><span class="sxs-lookup"><span data-stu-id="60ca6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60ca6-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="60ca6-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60ca6-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="60ca6-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="60ca6-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，表示與常數資料表相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="60ca6-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="60ca6-110">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="60ca6-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60ca6-111">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="60ca6-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="60ca6-112">矩陣常數陣列的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="60ca6-112">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="60ca6-113">請參閱 [D3DXHANDLE](dx9-graphics-reference-effects-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="60ca6-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="60ca6-114">*pMatrix* \[在\]</span><span class="sxs-lookup"><span data-stu-id="60ca6-114">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60ca6-115">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="60ca6-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="60ca6-116">已轉置矩陣的陣列。</span><span class="sxs-lookup"><span data-stu-id="60ca6-116">Array of transposed matrices.</span></span> <span data-ttu-id="60ca6-117">請參閱 [**D3DXMATRIX**](d3dxmatrix.md)。</span><span class="sxs-lookup"><span data-stu-id="60ca6-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="60ca6-118">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="60ca6-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60ca6-119">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="60ca6-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="60ca6-120">陣列中的矩陣數目。</span><span class="sxs-lookup"><span data-stu-id="60ca6-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60ca6-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="60ca6-121">Return value</span></span>

<span data-ttu-id="60ca6-122">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="60ca6-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="60ca6-123">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="60ca6-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="60ca6-124">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="60ca6-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="60ca6-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="60ca6-125">Requirements</span></span>



| <span data-ttu-id="60ca6-126">需求</span><span class="sxs-lookup"><span data-stu-id="60ca6-126">Requirement</span></span> | <span data-ttu-id="60ca6-127">值</span><span class="sxs-lookup"><span data-stu-id="60ca6-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="60ca6-128">標頭</span><span class="sxs-lookup"><span data-stu-id="60ca6-128">Header</span></span><br/>  | <dl> <span data-ttu-id="60ca6-129"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="60ca6-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="60ca6-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="60ca6-130">Library</span></span><br/> | <dl> <span data-ttu-id="60ca6-131"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="60ca6-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="60ca6-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="60ca6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60ca6-133">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="60ca6-133">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
