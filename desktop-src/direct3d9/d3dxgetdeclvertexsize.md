---
description: 從頂點宣告傳回頂點的大小。
ms.assetid: a2524f96-103e-43ab-bdcb-b99e7402fd89
title: 'D3DXGetDeclVertexSize 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetDeclVertexSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c962064faa61dc7045b0111c5efbf1d1bea9fd40
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000592"
---
# <a name="d3dxgetdeclvertexsize-function"></a><span data-ttu-id="e40a7-103">D3DXGetDeclVertexSize 函式</span><span class="sxs-lookup"><span data-stu-id="e40a7-103">D3DXGetDeclVertexSize function</span></span>

<span data-ttu-id="e40a7-104">從頂點宣告傳回頂點的大小。</span><span class="sxs-lookup"><span data-stu-id="e40a7-104">Returns the size of a vertex from the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="e40a7-105">語法</span><span class="sxs-lookup"><span data-stu-id="e40a7-105">Syntax</span></span>


```C++
UINT D3DXGetDeclVertexSize(
  _In_ const D3DVERTEXELEMENT9 *pDecl,
  _In_       DWORD             Stream
);
```



## <a name="parameters"></a><span data-ttu-id="e40a7-106">參數</span><span class="sxs-lookup"><span data-stu-id="e40a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e40a7-107">*pDecl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e40a7-107">*pDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e40a7-108">Type： **Const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="e40a7-108">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="e40a7-109">頂點宣告的指標。</span><span class="sxs-lookup"><span data-stu-id="e40a7-109">A pointer to the vertex declaration.</span></span> <span data-ttu-id="e40a7-110">請參閱 [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)。</span><span class="sxs-lookup"><span data-stu-id="e40a7-110">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> <dt>

<span data-ttu-id="e40a7-111">*資料流程* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e40a7-111">*Stream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e40a7-112">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e40a7-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e40a7-113">以零為基底的資料流程索引。</span><span class="sxs-lookup"><span data-stu-id="e40a7-113">The zero-based stream index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e40a7-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="e40a7-114">Return value</span></span>

<span data-ttu-id="e40a7-115">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e40a7-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e40a7-116">頂點宣告大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e40a7-116">The vertex declaration size, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="e40a7-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="e40a7-117">Requirements</span></span>



| <span data-ttu-id="e40a7-118">需求</span><span class="sxs-lookup"><span data-stu-id="e40a7-118">Requirement</span></span> | <span data-ttu-id="e40a7-119">值</span><span class="sxs-lookup"><span data-stu-id="e40a7-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e40a7-120">標頭</span><span class="sxs-lookup"><span data-stu-id="e40a7-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e40a7-121"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="e40a7-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e40a7-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="e40a7-122">Library</span></span><br/> | <dl> <span data-ttu-id="e40a7-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e40a7-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e40a7-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e40a7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e40a7-125">網格函數</span><span class="sxs-lookup"><span data-stu-id="e40a7-125">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
