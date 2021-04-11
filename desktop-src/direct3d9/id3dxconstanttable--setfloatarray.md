---
description: 設定浮點數字的陣列。
ms.assetid: 7a622dd5-47ed-4166-a6df-f484b03e0b5a
title: 'ID3DXConstantTable：： SetFloatArray 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetFloatArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d75d4171ab51859e4095acbe5d3e86d704b1f437
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196293"
---
# <a name="id3dxconstanttablesetfloatarray-method"></a><span data-ttu-id="e13d3-103">ID3DXConstantTable：： SetFloatArray 方法</span><span class="sxs-lookup"><span data-stu-id="e13d3-103">ID3DXConstantTable::SetFloatArray method</span></span>

<span data-ttu-id="e13d3-104">設定浮點數字的陣列。</span><span class="sxs-lookup"><span data-stu-id="e13d3-104">Sets an array of floating-point numbers.</span></span>

## <a name="syntax"></a><span data-ttu-id="e13d3-105">語法</span><span class="sxs-lookup"><span data-stu-id="e13d3-105">Syntax</span></span>


```C++
HRESULT SetFloatArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const FLOAT             *pf,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="e13d3-106">參數</span><span class="sxs-lookup"><span data-stu-id="e13d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e13d3-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e13d3-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e13d3-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="e13d3-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="e13d3-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，表示與常數資料表相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="e13d3-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="e13d3-110">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e13d3-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e13d3-111">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e13d3-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e13d3-112">常數陣列的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="e13d3-112">Unique identifier to the array of constants.</span></span> <span data-ttu-id="e13d3-113">請參閱 [D3DXHANDLE](dx9-graphics-reference-effects-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="e13d3-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="e13d3-114">*pf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e13d3-114">*pf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e13d3-115">Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="e13d3-115">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e13d3-116">浮點數的陣列。</span><span class="sxs-lookup"><span data-stu-id="e13d3-116">Array of floating-point numbers.</span></span>

</dd> <dt>

<span data-ttu-id="e13d3-117">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e13d3-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e13d3-118">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e13d3-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e13d3-119">陣列中的浮點值數目。</span><span class="sxs-lookup"><span data-stu-id="e13d3-119">Number of floating-point values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e13d3-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="e13d3-120">Return value</span></span>

<span data-ttu-id="e13d3-121">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e13d3-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e13d3-122">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="e13d3-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e13d3-123">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="e13d3-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e13d3-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="e13d3-124">Requirements</span></span>



| <span data-ttu-id="e13d3-125">需求</span><span class="sxs-lookup"><span data-stu-id="e13d3-125">Requirement</span></span> | <span data-ttu-id="e13d3-126">值</span><span class="sxs-lookup"><span data-stu-id="e13d3-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e13d3-127">標頭</span><span class="sxs-lookup"><span data-stu-id="e13d3-127">Header</span></span><br/>  | <dl> <span data-ttu-id="e13d3-128"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="e13d3-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e13d3-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="e13d3-129">Library</span></span><br/> | <dl> <span data-ttu-id="e13d3-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e13d3-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e13d3-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e13d3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e13d3-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="e13d3-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
