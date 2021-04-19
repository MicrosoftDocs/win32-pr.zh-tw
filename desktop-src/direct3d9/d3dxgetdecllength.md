---
description: 傳回頂點宣告中的元素數目。
ms.assetid: 3ce24e59-0ec3-4d53-8bc8-8a5a7cdf53b2
title: 'D3DXGetDeclLength 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetDeclLength
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5576b4b86d5238d4942e09d605f695c66136799a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106975673"
---
# <a name="d3dxgetdecllength-function"></a><span data-ttu-id="dc791-103">D3DXGetDeclLength 函式</span><span class="sxs-lookup"><span data-stu-id="dc791-103">D3DXGetDeclLength function</span></span>

<span data-ttu-id="dc791-104">傳回頂點宣告中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="dc791-104">Returns the number of elements in the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc791-105">語法</span><span class="sxs-lookup"><span data-stu-id="dc791-105">Syntax</span></span>


```C++
UINT D3DXGetDeclLength(
  _In_ const D3DVERTEXELEMENT9 *pDecl
);
```



## <a name="parameters"></a><span data-ttu-id="dc791-106">參數</span><span class="sxs-lookup"><span data-stu-id="dc791-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc791-107">*pDecl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dc791-107">*pDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc791-108">Type： **Const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="dc791-108">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="dc791-109">頂點宣告的指標。</span><span class="sxs-lookup"><span data-stu-id="dc791-109">A pointer to the vertex declaration.</span></span> <span data-ttu-id="dc791-110">請參閱 [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)。</span><span class="sxs-lookup"><span data-stu-id="dc791-110">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc791-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="dc791-111">Return value</span></span>

<span data-ttu-id="dc791-112">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc791-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dc791-113">頂點宣告中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="dc791-113">The number of elements in the vertex declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc791-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc791-114">Requirements</span></span>



| <span data-ttu-id="dc791-115">需求</span><span class="sxs-lookup"><span data-stu-id="dc791-115">Requirement</span></span> | <span data-ttu-id="dc791-116">值</span><span class="sxs-lookup"><span data-stu-id="dc791-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc791-117">標頭</span><span class="sxs-lookup"><span data-stu-id="dc791-117">Header</span></span><br/>  | <dl> <span data-ttu-id="dc791-118"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="dc791-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="dc791-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="dc791-119">Library</span></span><br/> | <dl> <span data-ttu-id="dc791-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="dc791-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dc791-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc791-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc791-122">網格函數</span><span class="sxs-lookup"><span data-stu-id="dc791-122">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
