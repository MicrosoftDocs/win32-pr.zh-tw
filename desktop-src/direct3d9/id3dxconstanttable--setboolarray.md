---
description: 設定布林值的陣列。
ms.assetid: 323ad654-81e3-4986-a667-8333dd44a2d1
title: 'ID3DXConstantTable：： SetBoolArray 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetBoolArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d573a2c44b54809ec259a0ceb5abab02ef37df34
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106998365"
---
# <a name="id3dxconstanttablesetboolarray-method"></a><span data-ttu-id="b5db1-103">ID3DXConstantTable：： SetBoolArray 方法</span><span class="sxs-lookup"><span data-stu-id="b5db1-103">ID3DXConstantTable::SetBoolArray method</span></span>

<span data-ttu-id="b5db1-104">設定布林值的陣列。</span><span class="sxs-lookup"><span data-stu-id="b5db1-104">Sets an array of Boolean values.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5db1-105">語法</span><span class="sxs-lookup"><span data-stu-id="b5db1-105">Syntax</span></span>


```C++
HRESULT SetBoolArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const BOOL              *pB,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="b5db1-106">參數</span><span class="sxs-lookup"><span data-stu-id="b5db1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5db1-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b5db1-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5db1-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="b5db1-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="b5db1-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，表示與常數資料表相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="b5db1-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="b5db1-110">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b5db1-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5db1-111">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="b5db1-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="b5db1-112">常數陣列的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="b5db1-112">Unique identifier to the array of constants.</span></span> <span data-ttu-id="b5db1-113">請參閱 [D3DXHANDLE](dx9-graphics-reference-effects-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="b5db1-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5db1-114">*pB* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b5db1-114">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5db1-115">類型： **Const [**BOOL**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b5db1-115">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b5db1-116">布林值的陣列。</span><span class="sxs-lookup"><span data-stu-id="b5db1-116">Array of Boolean values.</span></span>

</dd> <dt>

<span data-ttu-id="b5db1-117">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b5db1-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5db1-118">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b5db1-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b5db1-119">陣列中的布林值數目。</span><span class="sxs-lookup"><span data-stu-id="b5db1-119">Number of Boolean values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5db1-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="b5db1-120">Return value</span></span>

<span data-ttu-id="b5db1-121">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b5db1-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b5db1-122">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="b5db1-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b5db1-123">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="b5db1-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5db1-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="b5db1-124">Requirements</span></span>



| <span data-ttu-id="b5db1-125">需求</span><span class="sxs-lookup"><span data-stu-id="b5db1-125">Requirement</span></span> | <span data-ttu-id="b5db1-126">值</span><span class="sxs-lookup"><span data-stu-id="b5db1-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5db1-127">標頭</span><span class="sxs-lookup"><span data-stu-id="b5db1-127">Header</span></span><br/>  | <dl> <span data-ttu-id="b5db1-128"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="b5db1-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="b5db1-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="b5db1-129">Library</span></span><br/> | <dl> <span data-ttu-id="b5db1-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5db1-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b5db1-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b5db1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5db1-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="b5db1-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
