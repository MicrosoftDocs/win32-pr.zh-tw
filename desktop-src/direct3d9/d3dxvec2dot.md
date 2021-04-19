---
description: 決定兩個2D 向量的點乘積。
ms.assetid: ae77ff29-44be-4b67-9c63-aaffa4fe8d59
title: 'D3DXVec2Dot 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Dot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 79b65127c415695b3df9f927b6edff8fcdd5c58d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976475"
---
# <a name="d3dxvec2dot-function"></a><span data-ttu-id="fdb4b-103">D3DXVec2Dot 函式</span><span class="sxs-lookup"><span data-stu-id="fdb4b-103">D3DXVec2Dot function</span></span>

<span data-ttu-id="fdb4b-104">決定兩個2D 向量的點乘積。</span><span class="sxs-lookup"><span data-stu-id="fdb4b-104">Determines the dot product of two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdb4b-105">語法</span><span class="sxs-lookup"><span data-stu-id="fdb4b-105">Syntax</span></span>


```C++
FLOAT D3DXVec2Dot(
  _In_ const D3DXVECTOR2 *pV1,
  _In_ const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="fdb4b-106">參數</span><span class="sxs-lookup"><span data-stu-id="fdb4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdb4b-107">*pV1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fdb4b-107">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb4b-108">Type： **Const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="fdb4b-108">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="fdb4b-109">來源 [**D3DXVECTOR2**](d3dxvector2.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="fdb4b-109">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="fdb4b-110">*pV2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fdb4b-110">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdb4b-111">Type： **Const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="fdb4b-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="fdb4b-112">來源 [**D3DXVECTOR2**](d3dxvector2.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="fdb4b-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdb4b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="fdb4b-113">Return value</span></span>

<span data-ttu-id="fdb4b-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fdb4b-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fdb4b-115">內積。</span><span class="sxs-lookup"><span data-stu-id="fdb4b-115">The dot product.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdb4b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="fdb4b-116">Requirements</span></span>



| <span data-ttu-id="fdb4b-117">需求</span><span class="sxs-lookup"><span data-stu-id="fdb4b-117">Requirement</span></span> | <span data-ttu-id="fdb4b-118">值</span><span class="sxs-lookup"><span data-stu-id="fdb4b-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fdb4b-119">標頭</span><span class="sxs-lookup"><span data-stu-id="fdb4b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="fdb4b-120"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="fdb4b-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="fdb4b-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="fdb4b-121">Library</span></span><br/> | <dl> <span data-ttu-id="fdb4b-122"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fdb4b-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fdb4b-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fdb4b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdb4b-124">數學函數</span><span class="sxs-lookup"><span data-stu-id="fdb4b-124">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="fdb4b-125">**D3DXVec2CCW**</span><span class="sxs-lookup"><span data-stu-id="fdb4b-125">**D3DXVec2CCW**</span></span>](d3dxvec2ccw.md)
</dt> </dl>

 

 
