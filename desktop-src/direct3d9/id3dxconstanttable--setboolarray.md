---
description: ID3DXConstantTable：： SetBoolArray 方法：設定布林值的陣列。
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
ms.openlocfilehash: c967ffd1a6601144787621628ed1b019e775eddd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115206"
---
# <a name="id3dxconstanttablesetboolarray-method"></a><span data-ttu-id="61ae9-103">ID3DXConstantTable：： SetBoolArray 方法</span><span class="sxs-lookup"><span data-stu-id="61ae9-103">ID3DXConstantTable::SetBoolArray method</span></span>

<span data-ttu-id="61ae9-104">設定布林值的陣列。</span><span class="sxs-lookup"><span data-stu-id="61ae9-104">Sets an array of Boolean values.</span></span>

## <a name="syntax"></a><span data-ttu-id="61ae9-105">語法</span><span class="sxs-lookup"><span data-stu-id="61ae9-105">Syntax</span></span>


```C++
HRESULT SetBoolArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const BOOL              *pB,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="61ae9-106">參數</span><span class="sxs-lookup"><span data-stu-id="61ae9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61ae9-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="61ae9-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61ae9-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="61ae9-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="61ae9-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，表示與常數資料表相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="61ae9-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="61ae9-110">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="61ae9-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61ae9-111">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="61ae9-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="61ae9-112">常數陣列的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="61ae9-112">Unique identifier to the array of constants.</span></span> <span data-ttu-id="61ae9-113">請參閱 [D3DXHANDLE](dx9-graphics-reference-effects-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="61ae9-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="61ae9-114">*pB* \[在\]</span><span class="sxs-lookup"><span data-stu-id="61ae9-114">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61ae9-115">類型： **Const [**BOOL**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="61ae9-115">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="61ae9-116">布林值的陣列。</span><span class="sxs-lookup"><span data-stu-id="61ae9-116">Array of Boolean values.</span></span>

</dd> <dt>

<span data-ttu-id="61ae9-117">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="61ae9-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61ae9-118">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="61ae9-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="61ae9-119">陣列中的布林值數目。</span><span class="sxs-lookup"><span data-stu-id="61ae9-119">Number of Boolean values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61ae9-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="61ae9-120">Return value</span></span>

<span data-ttu-id="61ae9-121">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="61ae9-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="61ae9-122">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="61ae9-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="61ae9-123">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="61ae9-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="61ae9-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="61ae9-124">Requirements</span></span>



| <span data-ttu-id="61ae9-125">需求</span><span class="sxs-lookup"><span data-stu-id="61ae9-125">Requirement</span></span> | <span data-ttu-id="61ae9-126">值</span><span class="sxs-lookup"><span data-stu-id="61ae9-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="61ae9-127">標頭</span><span class="sxs-lookup"><span data-stu-id="61ae9-127">Header</span></span><br/>  | <dl> <span data-ttu-id="61ae9-128"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="61ae9-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="61ae9-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="61ae9-129">Library</span></span><br/> | <dl> <span data-ttu-id="61ae9-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="61ae9-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="61ae9-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61ae9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61ae9-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="61ae9-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
