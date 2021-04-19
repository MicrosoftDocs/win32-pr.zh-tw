---
description: 設定4D 向量的陣列。
ms.assetid: bd453384-4f38-4017-a9a5-cac605919940
title: 'ID3DXConstantTable：： SetVectorArray 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetVectorArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6c68621a3f97251cdd88836792bf55980f28311
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981833"
---
# <a name="id3dxconstanttablesetvectorarray-method"></a><span data-ttu-id="decc8-103">ID3DXConstantTable：： SetVectorArray 方法</span><span class="sxs-lookup"><span data-stu-id="decc8-103">ID3DXConstantTable::SetVectorArray method</span></span>

<span data-ttu-id="decc8-104">設定4D 向量的陣列。</span><span class="sxs-lookup"><span data-stu-id="decc8-104">Sets an array of 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="decc8-105">語法</span><span class="sxs-lookup"><span data-stu-id="decc8-105">Syntax</span></span>


```C++
HRESULT SetVectorArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXVECTOR4       *pVector,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="decc8-106">參數</span><span class="sxs-lookup"><span data-stu-id="decc8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="decc8-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="decc8-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="decc8-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="decc8-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="decc8-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，表示與常數資料表相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="decc8-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="decc8-110">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="decc8-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="decc8-111">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="decc8-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="decc8-112">向量常數陣列的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="decc8-112">Unique identifier to the array of vector constants.</span></span> <span data-ttu-id="decc8-113">請參閱 [D3DXHANDLE](dx9-graphics-reference-effects-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="decc8-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="decc8-114">*pVector* \[在\]</span><span class="sxs-lookup"><span data-stu-id="decc8-114">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="decc8-115">Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="decc8-115">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="decc8-116">4D 向量的陣列。</span><span class="sxs-lookup"><span data-stu-id="decc8-116">Array of 4D vectors.</span></span>

</dd> <dt>

<span data-ttu-id="decc8-117">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="decc8-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="decc8-118">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="decc8-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="decc8-119">陣列中的向量數目。</span><span class="sxs-lookup"><span data-stu-id="decc8-119">Number of vectors in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="decc8-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="decc8-120">Return value</span></span>

<span data-ttu-id="decc8-121">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="decc8-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="decc8-122">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="decc8-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="decc8-123">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="decc8-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="decc8-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="decc8-124">Requirements</span></span>



| <span data-ttu-id="decc8-125">需求</span><span class="sxs-lookup"><span data-stu-id="decc8-125">Requirement</span></span> | <span data-ttu-id="decc8-126">值</span><span class="sxs-lookup"><span data-stu-id="decc8-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="decc8-127">標頭</span><span class="sxs-lookup"><span data-stu-id="decc8-127">Header</span></span><br/>  | <dl> <span data-ttu-id="decc8-128"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="decc8-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="decc8-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="decc8-129">Library</span></span><br/> | <dl> <span data-ttu-id="decc8-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="decc8-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="decc8-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="decc8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="decc8-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="decc8-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
