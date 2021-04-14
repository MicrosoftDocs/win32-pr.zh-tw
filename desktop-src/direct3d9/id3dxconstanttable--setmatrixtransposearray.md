---
description: 設定已轉置矩陣的陣列。
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
ms.openlocfilehash: 69755ed973a8c412373287f128642b78ea2ad346
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514621"
---
# <a name="id3dxconstanttablesetmatrixtransposearray-method"></a><span data-ttu-id="7181a-103">ID3DXConstantTable：： SetMatrixTransposeArray 方法</span><span class="sxs-lookup"><span data-stu-id="7181a-103">ID3DXConstantTable::SetMatrixTransposeArray method</span></span>

<span data-ttu-id="7181a-104">設定已轉置矩陣的陣列。</span><span class="sxs-lookup"><span data-stu-id="7181a-104">Sets an array of transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="7181a-105">語法</span><span class="sxs-lookup"><span data-stu-id="7181a-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposeArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="7181a-106">參數</span><span class="sxs-lookup"><span data-stu-id="7181a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7181a-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7181a-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7181a-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="7181a-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="7181a-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，表示與常數資料表相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="7181a-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="7181a-110">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7181a-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7181a-111">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="7181a-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="7181a-112">矩陣常數陣列的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="7181a-112">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="7181a-113">請參閱 [D3DXHANDLE](dx9-graphics-reference-effects-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="7181a-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="7181a-114">*pMatrix* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7181a-114">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7181a-115">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="7181a-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7181a-116">已轉置矩陣的陣列。</span><span class="sxs-lookup"><span data-stu-id="7181a-116">Array of transposed matrices.</span></span> <span data-ttu-id="7181a-117">請參閱 [**D3DXMATRIX**](d3dxmatrix.md)。</span><span class="sxs-lookup"><span data-stu-id="7181a-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="7181a-118">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7181a-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7181a-119">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7181a-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7181a-120">陣列中的矩陣數目。</span><span class="sxs-lookup"><span data-stu-id="7181a-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7181a-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="7181a-121">Return value</span></span>

<span data-ttu-id="7181a-122">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7181a-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7181a-123">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="7181a-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7181a-124">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="7181a-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="7181a-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="7181a-125">Requirements</span></span>



| <span data-ttu-id="7181a-126">需求</span><span class="sxs-lookup"><span data-stu-id="7181a-126">Requirement</span></span> | <span data-ttu-id="7181a-127">值</span><span class="sxs-lookup"><span data-stu-id="7181a-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7181a-128">標頭</span><span class="sxs-lookup"><span data-stu-id="7181a-128">Header</span></span><br/>  | <dl> <span data-ttu-id="7181a-129"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="7181a-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="7181a-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="7181a-130">Library</span></span><br/> | <dl> <span data-ttu-id="7181a-131"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7181a-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7181a-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7181a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7181a-133">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="7181a-133">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
