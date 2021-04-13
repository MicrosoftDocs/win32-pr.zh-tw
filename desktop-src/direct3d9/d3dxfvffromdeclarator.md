---
description: 傳回彈性頂點格式 (從宣告子 FVF) 程式碼。
ms.assetid: 4f30087e-0042-44bc-a7a5-5386b18fcad7
title: 'D3DXFVFFromDeclarator 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFVFFromDeclarator
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fdaf6f80340a08562ed644ee44ac92c42874d149
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322912"
---
# <a name="d3dxfvffromdeclarator-function"></a><span data-ttu-id="e335e-103">D3DXFVFFromDeclarator 函式</span><span class="sxs-lookup"><span data-stu-id="e335e-103">D3DXFVFFromDeclarator function</span></span>

<span data-ttu-id="e335e-104">傳回彈性頂點格式 (從宣告子 FVF) 程式碼。</span><span class="sxs-lookup"><span data-stu-id="e335e-104">Returns a flexible vertex format (FVF) code from a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="e335e-105">語法</span><span class="sxs-lookup"><span data-stu-id="e335e-105">Syntax</span></span>


```C++
HRESULT D3DXFVFFromDeclarator(
  _In_  const LPD3DVERTEXELEMENT9 *pDeclaration,
  _Out_       DWORD               *pFVF
);
```



## <a name="parameters"></a><span data-ttu-id="e335e-106">參數</span><span class="sxs-lookup"><span data-stu-id="e335e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e335e-107">*pDeclaration* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e335e-107">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e335e-108">Type： **Const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="e335e-108">Type: **const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="e335e-109">[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)元素的陣列，描述 FVF 程式碼。</span><span class="sxs-lookup"><span data-stu-id="e335e-109">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the FVF code.</span></span>

</dd> <dt>

<span data-ttu-id="e335e-110">*pFVF* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e335e-110">*pFVF* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e335e-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e335e-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e335e-112">DWORD 值的指標，代表傳回的 [D3DFVF](d3dfvf.md) 組合，其描述從宣告子傳回的頂點格式。</span><span class="sxs-lookup"><span data-stu-id="e335e-112">Pointer to a DWORD value, representing the returned combination of [D3DFVF](d3dfvf.md) that describes the vertex format returned from the declarator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e335e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e335e-113">Return value</span></span>

<span data-ttu-id="e335e-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e335e-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e335e-115">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="e335e-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e335e-116">如果函式失敗，則傳回值可以是： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="e335e-116">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e335e-117">備註</span><span class="sxs-lookup"><span data-stu-id="e335e-117">Remarks</span></span>

<span data-ttu-id="e335e-118">未直接對應至 FVF 的任何宣告子，此函式將會失敗。</span><span class="sxs-lookup"><span data-stu-id="e335e-118">This function will fail for any declarator that does not map directly to an FVF.</span></span>

## <a name="requirements"></a><span data-ttu-id="e335e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="e335e-119">Requirements</span></span>



| <span data-ttu-id="e335e-120">需求</span><span class="sxs-lookup"><span data-stu-id="e335e-120">Requirement</span></span> | <span data-ttu-id="e335e-121">值</span><span class="sxs-lookup"><span data-stu-id="e335e-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e335e-122">標頭</span><span class="sxs-lookup"><span data-stu-id="e335e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e335e-123"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="e335e-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e335e-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="e335e-124">Library</span></span><br/> | <dl> <span data-ttu-id="e335e-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e335e-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e335e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e335e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e335e-127">網格函數</span><span class="sxs-lookup"><span data-stu-id="e335e-127">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="e335e-128">**D3DXDeclaratorFromFVF**</span><span class="sxs-lookup"><span data-stu-id="e335e-128">**D3DXDeclaratorFromFVF**</span></span>](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
