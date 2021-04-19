---
description: 從輸入宣告產生輸出頂點宣告。 輸出宣告適用于網格鑲嵌函數。
ms.assetid: 528b0da3-fc31-4872-98f2-31e03c1cae5e
title: 'D3DXGenerateOutputDecl 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGenerateOutputDecl
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ce3fed752e74df3afa812c228a174503e20c6adf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106989195"
---
# <a name="d3dxgenerateoutputdecl-function"></a><span data-ttu-id="151dc-104">D3DXGenerateOutputDecl 函式</span><span class="sxs-lookup"><span data-stu-id="151dc-104">D3DXGenerateOutputDecl function</span></span>

<span data-ttu-id="151dc-105">從輸入宣告產生輸出頂點宣告。</span><span class="sxs-lookup"><span data-stu-id="151dc-105">Generates an output vertex declaration from the input declaration.</span></span> <span data-ttu-id="151dc-106">輸出宣告適用于網格鑲嵌函數。</span><span class="sxs-lookup"><span data-stu-id="151dc-106">The output declaration is intended for use by the mesh tessellation functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="151dc-107">語法</span><span class="sxs-lookup"><span data-stu-id="151dc-107">Syntax</span></span>


```C++
HRESULT D3DXGenerateOutputDecl(
  _Out_       D3DVERTEXELEMENT9 *pOutput,
  _In_  const D3DVERTEXELEMENT9 *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="151dc-108">參數</span><span class="sxs-lookup"><span data-stu-id="151dc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="151dc-109">*pOutput* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="151dc-109">*pOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="151dc-110">類型： **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span><span class="sxs-lookup"><span data-stu-id="151dc-110">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="151dc-111">輸出頂點宣告的指標。</span><span class="sxs-lookup"><span data-stu-id="151dc-111">Pointer to the output vertex declaration.</span></span> <span data-ttu-id="151dc-112">請參閱 [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)。</span><span class="sxs-lookup"><span data-stu-id="151dc-112">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> <dt>

<span data-ttu-id="151dc-113">*pInput* \[在\]</span><span class="sxs-lookup"><span data-stu-id="151dc-113">*pInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="151dc-114">Type： **Const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="151dc-114">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="151dc-115">輸入頂點宣告的指標。</span><span class="sxs-lookup"><span data-stu-id="151dc-115">Pointer to the input vertex declaration.</span></span> <span data-ttu-id="151dc-116">請參閱 [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)。</span><span class="sxs-lookup"><span data-stu-id="151dc-116">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="151dc-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="151dc-117">Return value</span></span>

<span data-ttu-id="151dc-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="151dc-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="151dc-119">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="151dc-119">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="151dc-120">如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="151dc-120">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="151dc-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="151dc-121">Requirements</span></span>



| <span data-ttu-id="151dc-122">需求</span><span class="sxs-lookup"><span data-stu-id="151dc-122">Requirement</span></span> | <span data-ttu-id="151dc-123">值</span><span class="sxs-lookup"><span data-stu-id="151dc-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="151dc-124">標頭</span><span class="sxs-lookup"><span data-stu-id="151dc-124">Header</span></span><br/>  | <dl> <span data-ttu-id="151dc-125"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="151dc-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="151dc-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="151dc-126">Library</span></span><br/> | <dl> <span data-ttu-id="151dc-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="151dc-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="151dc-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="151dc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="151dc-129">網格函數</span><span class="sxs-lookup"><span data-stu-id="151dc-129">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




