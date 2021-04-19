---
description: 設定 nontransposed 矩陣。
ms.assetid: 30369e34-6e9d-4480-a142-e38f46fd38b0
title: 'ID3DXConstantTable：： SetMatrix 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ae227663a61087fae309d1954b8f0dc438f6df2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982017"
---
# <a name="id3dxconstanttablesetmatrix-method"></a><span data-ttu-id="1cc0e-103">ID3DXConstantTable：： SetMatrix 方法</span><span class="sxs-lookup"><span data-stu-id="1cc0e-103">ID3DXConstantTable::SetMatrix method</span></span>

<span data-ttu-id="1cc0e-104">設定 nontransposed 矩陣。</span><span class="sxs-lookup"><span data-stu-id="1cc0e-104">Sets a nontransposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cc0e-105">語法</span><span class="sxs-lookup"><span data-stu-id="1cc0e-105">Syntax</span></span>


```C++
HRESULT SetMatrix(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="1cc0e-106">參數</span><span class="sxs-lookup"><span data-stu-id="1cc0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cc0e-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1cc0e-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc0e-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="1cc0e-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="1cc0e-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，表示與常數資料表相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="1cc0e-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="1cc0e-110">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1cc0e-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc0e-111">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="1cc0e-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="1cc0e-112">常數矩陣的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="1cc0e-112">Unique identifier to the matrix of constants.</span></span> <span data-ttu-id="1cc0e-113">請參閱 [D3DXHANDLE](dx9-graphics-reference-effects-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="1cc0e-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="1cc0e-114">*pMatrix* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1cc0e-114">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc0e-115">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="1cc0e-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1cc0e-116">Nontransposed 矩陣的指標。</span><span class="sxs-lookup"><span data-stu-id="1cc0e-116">Pointer to a nontransposed matrix.</span></span> <span data-ttu-id="1cc0e-117">請參閱 [**D3DXMATRIX**](d3dxmatrix.md)。</span><span class="sxs-lookup"><span data-stu-id="1cc0e-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cc0e-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="1cc0e-118">Return value</span></span>

<span data-ttu-id="1cc0e-119">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1cc0e-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1cc0e-120">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="1cc0e-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1cc0e-121">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="1cc0e-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cc0e-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="1cc0e-122">Requirements</span></span>



| <span data-ttu-id="1cc0e-123">需求</span><span class="sxs-lookup"><span data-stu-id="1cc0e-123">Requirement</span></span> | <span data-ttu-id="1cc0e-124">值</span><span class="sxs-lookup"><span data-stu-id="1cc0e-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cc0e-125">標頭</span><span class="sxs-lookup"><span data-stu-id="1cc0e-125">Header</span></span><br/>  | <dl> <span data-ttu-id="1cc0e-126"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="1cc0e-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="1cc0e-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="1cc0e-127">Library</span></span><br/> | <dl> <span data-ttu-id="1cc0e-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1cc0e-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1cc0e-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1cc0e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cc0e-130">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="1cc0e-130">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
