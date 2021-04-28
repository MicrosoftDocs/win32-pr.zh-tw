---
description: ID3DXConstantTable：： SetVector 方法：設定4D 向量。
ms.assetid: d5849a8b-b372-4ad0-8773-8c9c4bac3799
title: 'ID3DXConstantTable：： SetVector 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetVector
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2d7c464cebb050b9fd54c27656505e6f2221fe4d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115016"
---
# <a name="id3dxconstanttablesetvector-method"></a><span data-ttu-id="5e396-103">ID3DXConstantTable：： SetVector 方法</span><span class="sxs-lookup"><span data-stu-id="5e396-103">ID3DXConstantTable::SetVector method</span></span>

<span data-ttu-id="5e396-104">設定4D 向量。</span><span class="sxs-lookup"><span data-stu-id="5e396-104">Sets a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e396-105">語法</span><span class="sxs-lookup"><span data-stu-id="5e396-105">Syntax</span></span>


```C++
HRESULT SetVector(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXVECTOR4       *pVector
);
```



## <a name="parameters"></a><span data-ttu-id="5e396-106">參數</span><span class="sxs-lookup"><span data-stu-id="5e396-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e396-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5e396-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e396-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="5e396-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="5e396-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，表示與常數資料表相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="5e396-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="5e396-110">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5e396-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e396-111">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5e396-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5e396-112">向量常數的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="5e396-112">Unique identifier to the vector constant.</span></span> <span data-ttu-id="5e396-113">請參閱 [D3DXHANDLE](dx9-graphics-reference-effects-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="5e396-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e396-114">*pVector* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5e396-114">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e396-115">Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="5e396-115">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="5e396-116">4D 向量的指標。</span><span class="sxs-lookup"><span data-stu-id="5e396-116">Pointer to a 4D vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e396-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="5e396-117">Return value</span></span>

<span data-ttu-id="5e396-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5e396-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5e396-119">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="5e396-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5e396-120">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="5e396-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e396-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e396-121">Requirements</span></span>



| <span data-ttu-id="5e396-122">需求</span><span class="sxs-lookup"><span data-stu-id="5e396-122">Requirement</span></span> | <span data-ttu-id="5e396-123">值</span><span class="sxs-lookup"><span data-stu-id="5e396-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e396-124">標頭</span><span class="sxs-lookup"><span data-stu-id="5e396-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5e396-125"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="5e396-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="5e396-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="5e396-126">Library</span></span><br/> | <dl> <span data-ttu-id="5e396-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e396-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5e396-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5e396-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e396-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="5e396-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
