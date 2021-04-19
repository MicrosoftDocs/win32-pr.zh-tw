---
description: 傳回4D 向量長度的平方。
ms.assetid: 73091179-4acb-408b-8c91-766052999f26
title: 'D3DXVec4LengthSq 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4LengthSq
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6348d4c42039c5aff47998721119c16317e22791
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997659"
---
# <a name="d3dxvec4lengthsq-function"></a><span data-ttu-id="2564c-103">D3DXVec4LengthSq 函式</span><span class="sxs-lookup"><span data-stu-id="2564c-103">D3DXVec4LengthSq function</span></span>

<span data-ttu-id="2564c-104">傳回4D 向量長度的平方。</span><span class="sxs-lookup"><span data-stu-id="2564c-104">Returns the square of the length of a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="2564c-105">語法</span><span class="sxs-lookup"><span data-stu-id="2564c-105">Syntax</span></span>


```C++
FLOAT D3DXVec4LengthSq(
  _In_ const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="2564c-106">參數</span><span class="sxs-lookup"><span data-stu-id="2564c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2564c-107">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2564c-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2564c-108">Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="2564c-108">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="2564c-109">來源 [**D3DXVECTOR4**](d3dxvector4.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="2564c-109">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2564c-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="2564c-110">Return value</span></span>

<span data-ttu-id="2564c-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2564c-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2564c-112">向量的平方長度。</span><span class="sxs-lookup"><span data-stu-id="2564c-112">The vector's squared length.</span></span>

## <a name="requirements"></a><span data-ttu-id="2564c-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="2564c-113">Requirements</span></span>



| <span data-ttu-id="2564c-114">需求</span><span class="sxs-lookup"><span data-stu-id="2564c-114">Requirement</span></span> | <span data-ttu-id="2564c-115">值</span><span class="sxs-lookup"><span data-stu-id="2564c-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2564c-116">標頭</span><span class="sxs-lookup"><span data-stu-id="2564c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="2564c-117"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="2564c-117"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2564c-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="2564c-118">Library</span></span><br/> | <dl> <span data-ttu-id="2564c-119"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2564c-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2564c-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2564c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2564c-121">數學函數</span><span class="sxs-lookup"><span data-stu-id="2564c-121">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="2564c-122">**D3DXVec4Length**</span><span class="sxs-lookup"><span data-stu-id="2564c-122">**D3DXVec4Length**</span></span>](d3dxvec4length.md)
</dt> </dl>

 

 
