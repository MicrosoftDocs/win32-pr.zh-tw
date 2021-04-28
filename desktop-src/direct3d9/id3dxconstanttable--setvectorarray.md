---
description: ID3DXConstantTable：： SetVectorArray 方法-設定4D 向量的陣列。
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
ms.openlocfilehash: fe93ef7a75cda743399133445a5f6efd34dd5ad7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115006"
---
# <a name="id3dxconstanttablesetvectorarray-method"></a><span data-ttu-id="e9a40-103">ID3DXConstantTable：： SetVectorArray 方法</span><span class="sxs-lookup"><span data-stu-id="e9a40-103">ID3DXConstantTable::SetVectorArray method</span></span>

<span data-ttu-id="e9a40-104">設定4D 向量的陣列。</span><span class="sxs-lookup"><span data-stu-id="e9a40-104">Sets an array of 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9a40-105">語法</span><span class="sxs-lookup"><span data-stu-id="e9a40-105">Syntax</span></span>


```C++
HRESULT SetVectorArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXVECTOR4       *pVector,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="e9a40-106">參數</span><span class="sxs-lookup"><span data-stu-id="e9a40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9a40-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e9a40-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9a40-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="e9a40-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="e9a40-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，表示與常數資料表相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="e9a40-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="e9a40-110">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e9a40-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9a40-111">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e9a40-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e9a40-112">向量常數陣列的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="e9a40-112">Unique identifier to the array of vector constants.</span></span> <span data-ttu-id="e9a40-113">請參閱 [D3DXHANDLE](dx9-graphics-reference-effects-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="e9a40-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9a40-114">*pVector* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e9a40-114">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9a40-115">Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="e9a40-115">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="e9a40-116">4D 向量的陣列。</span><span class="sxs-lookup"><span data-stu-id="e9a40-116">Array of 4D vectors.</span></span>

</dd> <dt>

<span data-ttu-id="e9a40-117">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e9a40-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9a40-118">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e9a40-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e9a40-119">陣列中的向量數目。</span><span class="sxs-lookup"><span data-stu-id="e9a40-119">Number of vectors in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9a40-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="e9a40-120">Return value</span></span>

<span data-ttu-id="e9a40-121">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e9a40-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e9a40-122">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="e9a40-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e9a40-123">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="e9a40-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9a40-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9a40-124">Requirements</span></span>



| <span data-ttu-id="e9a40-125">需求</span><span class="sxs-lookup"><span data-stu-id="e9a40-125">Requirement</span></span> | <span data-ttu-id="e9a40-126">值</span><span class="sxs-lookup"><span data-stu-id="e9a40-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9a40-127">標頭</span><span class="sxs-lookup"><span data-stu-id="e9a40-127">Header</span></span><br/>  | <dl> <span data-ttu-id="e9a40-128"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="e9a40-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e9a40-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="e9a40-129">Library</span></span><br/> | <dl> <span data-ttu-id="e9a40-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9a40-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e9a40-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9a40-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9a40-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="e9a40-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
