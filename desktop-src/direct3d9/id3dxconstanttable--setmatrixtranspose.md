---
description: 設定已轉置的矩陣。
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
ms.openlocfilehash: aa84f9e483be0c6c2ddae37c52ef6df2c43fda90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988189"
---
# <a name="id3dxconstanttablesetmatrixtranspose-method"></a><span data-ttu-id="13120-103">ID3DXConstantTable：： SetMatrixTranspose 方法</span><span class="sxs-lookup"><span data-stu-id="13120-103">ID3DXConstantTable::SetMatrixTranspose method</span></span>

<span data-ttu-id="13120-104">設定已轉置的矩陣。</span><span class="sxs-lookup"><span data-stu-id="13120-104">Sets a transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="13120-105">語法</span><span class="sxs-lookup"><span data-stu-id="13120-105">Syntax</span></span>


```C++
HRESULT SetMatrixTranspose(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="13120-106">參數</span><span class="sxs-lookup"><span data-stu-id="13120-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13120-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="13120-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13120-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="13120-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="13120-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，表示與常數資料表相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="13120-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="13120-110">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="13120-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13120-111">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="13120-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="13120-112">常數矩陣的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="13120-112">Unique identifier to the matrix of constants.</span></span> <span data-ttu-id="13120-113">請參閱 [D3DXHANDLE](dx9-graphics-reference-effects-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="13120-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="13120-114">*pMatrix* \[在\]</span><span class="sxs-lookup"><span data-stu-id="13120-114">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13120-115">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="13120-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="13120-116">已轉置矩陣的指標。</span><span class="sxs-lookup"><span data-stu-id="13120-116">Pointer to a transposed matrix.</span></span> <span data-ttu-id="13120-117">請參閱 [**D3DXMATRIX**](d3dxmatrix.md)。</span><span class="sxs-lookup"><span data-stu-id="13120-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13120-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="13120-118">Return value</span></span>

<span data-ttu-id="13120-119">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="13120-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="13120-120">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="13120-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="13120-121">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="13120-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="13120-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="13120-122">Requirements</span></span>



| <span data-ttu-id="13120-123">需求</span><span class="sxs-lookup"><span data-stu-id="13120-123">Requirement</span></span> | <span data-ttu-id="13120-124">值</span><span class="sxs-lookup"><span data-stu-id="13120-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="13120-125">標頭</span><span class="sxs-lookup"><span data-stu-id="13120-125">Header</span></span><br/>  | <dl> <span data-ttu-id="13120-126"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="13120-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="13120-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="13120-127">Library</span></span><br/> | <dl> <span data-ttu-id="13120-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="13120-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="13120-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13120-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13120-130">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="13120-130">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
