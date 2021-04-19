---
description: 決定兩個3D 向量的點乘積。
ms.assetid: 61aa7751-cc06-4673-929b-d7c1e691e395
title: 'D3DXVec3Dot 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Dot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 22d6930a44f129154482f9b1aab24337e8bcdc83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986510"
---
# <a name="d3dxvec3dot-function"></a><span data-ttu-id="d75e5-103">D3DXVec3Dot 函式</span><span class="sxs-lookup"><span data-stu-id="d75e5-103">D3DXVec3Dot function</span></span>

<span data-ttu-id="d75e5-104">決定兩個3D 向量的點乘積。</span><span class="sxs-lookup"><span data-stu-id="d75e5-104">Determines the dot product of two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="d75e5-105">語法</span><span class="sxs-lookup"><span data-stu-id="d75e5-105">Syntax</span></span>


```C++
FLOAT D3DXVec3Dot(
  _In_ const D3DXVECTOR3 *pV1,
  _In_ const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="d75e5-106">參數</span><span class="sxs-lookup"><span data-stu-id="d75e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d75e5-107">*pV1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d75e5-107">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d75e5-108">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d75e5-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="d75e5-109">來源 [**D3DXVECTOR3**](d3dxvector3.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="d75e5-109">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d75e5-110">*pV2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d75e5-110">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d75e5-111">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d75e5-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="d75e5-112">來源 [**D3DXVECTOR3**](d3dxvector3.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="d75e5-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d75e5-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d75e5-113">Return value</span></span>

<span data-ttu-id="d75e5-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d75e5-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d75e5-115">點乘積。</span><span class="sxs-lookup"><span data-stu-id="d75e5-115">The dot-product.</span></span>

## <a name="requirements"></a><span data-ttu-id="d75e5-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="d75e5-116">Requirements</span></span>



| <span data-ttu-id="d75e5-117">需求</span><span class="sxs-lookup"><span data-stu-id="d75e5-117">Requirement</span></span> | <span data-ttu-id="d75e5-118">值</span><span class="sxs-lookup"><span data-stu-id="d75e5-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d75e5-119">標頭</span><span class="sxs-lookup"><span data-stu-id="d75e5-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d75e5-120"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="d75e5-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d75e5-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="d75e5-121">Library</span></span><br/> | <dl> <span data-ttu-id="d75e5-122"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d75e5-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d75e5-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d75e5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d75e5-124">數學函數</span><span class="sxs-lookup"><span data-stu-id="d75e5-124">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="d75e5-125">**D3DXVec3Cross**</span><span class="sxs-lookup"><span data-stu-id="d75e5-125">**D3DXVec3Cross**</span></span>](d3dxvec3cross.md)
</dt> </dl>

 

 
