---
description: ID3DXConstantTable：： SetMatrixTranspose 方法：設定已轉置的矩陣。
ms.assetid: 1c4d64ce-64bd-47d4-9912-879f4834c0e8
title: 'ID3DXConstantTable：： SetMatrixTranspose 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixTranspose
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 06cc989a14da6f2fe84d30f7f5d7d9fc35acd3bc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115056"
---
# <a name="id3dxconstanttablesetmatrixtranspose-method"></a><span data-ttu-id="21720-103">ID3DXConstantTable：： SetMatrixTranspose 方法</span><span class="sxs-lookup"><span data-stu-id="21720-103">ID3DXConstantTable::SetMatrixTranspose method</span></span>

<span data-ttu-id="21720-104">設定已轉置的矩陣。</span><span class="sxs-lookup"><span data-stu-id="21720-104">Sets a transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="21720-105">語法</span><span class="sxs-lookup"><span data-stu-id="21720-105">Syntax</span></span>


```C++
HRESULT SetMatrixTranspose(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="21720-106">參數</span><span class="sxs-lookup"><span data-stu-id="21720-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21720-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="21720-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21720-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="21720-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="21720-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，表示與常數資料表相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="21720-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="21720-110">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="21720-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21720-111">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="21720-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="21720-112">常數矩陣的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="21720-112">Unique identifier to the matrix of constants.</span></span> <span data-ttu-id="21720-113">請參閱 [D3DXHANDLE](dx9-graphics-reference-effects-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="21720-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="21720-114">*pMatrix* \[在\]</span><span class="sxs-lookup"><span data-stu-id="21720-114">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21720-115">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="21720-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="21720-116">已轉置矩陣的指標。</span><span class="sxs-lookup"><span data-stu-id="21720-116">Pointer to a transposed matrix.</span></span> <span data-ttu-id="21720-117">請參閱 [**D3DXMATRIX**](d3dxmatrix.md)。</span><span class="sxs-lookup"><span data-stu-id="21720-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21720-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="21720-118">Return value</span></span>

<span data-ttu-id="21720-119">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="21720-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="21720-120">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="21720-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="21720-121">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="21720-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="21720-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="21720-122">Requirements</span></span>



| <span data-ttu-id="21720-123">需求</span><span class="sxs-lookup"><span data-stu-id="21720-123">Requirement</span></span> | <span data-ttu-id="21720-124">值</span><span class="sxs-lookup"><span data-stu-id="21720-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="21720-125">標頭</span><span class="sxs-lookup"><span data-stu-id="21720-125">Header</span></span><br/>  | <dl> <span data-ttu-id="21720-126"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="21720-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="21720-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="21720-127">Library</span></span><br/> | <dl> <span data-ttu-id="21720-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="21720-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="21720-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21720-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21720-130">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="21720-130">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
