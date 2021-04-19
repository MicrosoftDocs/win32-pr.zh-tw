---
description: 傳回3D 向量的長度。
ms.assetid: 78da506c-3169-48e9-934c-cc09271a10d4
title: 'D3DXVec3Length 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Length
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 653e53fb22961c858c7649f95e4453fec08087fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997378"
---
# <a name="d3dxvec3length-function"></a><span data-ttu-id="4eb19-103">D3DXVec3Length 函式</span><span class="sxs-lookup"><span data-stu-id="4eb19-103">D3DXVec3Length function</span></span>

<span data-ttu-id="4eb19-104">傳回3D 向量的長度。</span><span class="sxs-lookup"><span data-stu-id="4eb19-104">Returns the length of a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="4eb19-105">語法</span><span class="sxs-lookup"><span data-stu-id="4eb19-105">Syntax</span></span>


```C++
FLOAT D3DXVec3Length(
  _In_ const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="4eb19-106">參數</span><span class="sxs-lookup"><span data-stu-id="4eb19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4eb19-107">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4eb19-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4eb19-108">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="4eb19-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="4eb19-109">來源 [**D3DXVECTOR3**](d3dxvector3.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="4eb19-109">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4eb19-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="4eb19-110">Return value</span></span>

<span data-ttu-id="4eb19-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4eb19-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4eb19-112">向量的長度。</span><span class="sxs-lookup"><span data-stu-id="4eb19-112">The vector's length.</span></span>

## <a name="requirements"></a><span data-ttu-id="4eb19-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="4eb19-113">Requirements</span></span>



| <span data-ttu-id="4eb19-114">需求</span><span class="sxs-lookup"><span data-stu-id="4eb19-114">Requirement</span></span> | <span data-ttu-id="4eb19-115">值</span><span class="sxs-lookup"><span data-stu-id="4eb19-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4eb19-116">標頭</span><span class="sxs-lookup"><span data-stu-id="4eb19-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4eb19-117"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="4eb19-117"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="4eb19-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="4eb19-118">Library</span></span><br/> | <dl> <span data-ttu-id="4eb19-119"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4eb19-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4eb19-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4eb19-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eb19-121">數學函數</span><span class="sxs-lookup"><span data-stu-id="4eb19-121">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="4eb19-122">**D3DXVec3LengthSq**</span><span class="sxs-lookup"><span data-stu-id="4eb19-122">**D3DXVec3LengthSq**</span></span>](d3dxvec3lengthsq.md)
</dt> </dl>

 

 
