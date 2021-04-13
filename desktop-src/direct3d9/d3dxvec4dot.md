---
description: 決定兩個4D 向量的點乘積。
ms.assetid: 565dede8-6cc8-4313-9480-2f252cac94f2
title: 'D3DXVec4Dot 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Dot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a0ef075a768fe9b70a38a4bc3d88b094359bd546
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386469"
---
# <a name="d3dxvec4dot-function"></a><span data-ttu-id="a8f2a-103">D3DXVec4Dot 函式</span><span class="sxs-lookup"><span data-stu-id="a8f2a-103">D3DXVec4Dot function</span></span>

<span data-ttu-id="a8f2a-104">決定兩個4D 向量的點乘積。</span><span class="sxs-lookup"><span data-stu-id="a8f2a-104">Determines the dot product of two 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8f2a-105">語法</span><span class="sxs-lookup"><span data-stu-id="a8f2a-105">Syntax</span></span>


```C++
FLOAT D3DXVec4Dot(
  _In_ const D3DXVECTOR4 *pV1,
  _In_ const D3DXVECTOR4 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="a8f2a-106">參數</span><span class="sxs-lookup"><span data-stu-id="a8f2a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8f2a-107">*pV1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a8f2a-107">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8f2a-108">Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="a8f2a-108">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="a8f2a-109">來源 [**D3DXVECTOR4**](d3dxvector4.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="a8f2a-109">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a8f2a-110">*pV2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a8f2a-110">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8f2a-111">Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="a8f2a-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="a8f2a-112">來源 [**D3DXVECTOR4**](d3dxvector4.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="a8f2a-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8f2a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a8f2a-113">Return value</span></span>

<span data-ttu-id="a8f2a-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a8f2a-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a8f2a-115">內積。</span><span class="sxs-lookup"><span data-stu-id="a8f2a-115">The dot product.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8f2a-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8f2a-116">Requirements</span></span>



| <span data-ttu-id="a8f2a-117">需求</span><span class="sxs-lookup"><span data-stu-id="a8f2a-117">Requirement</span></span> | <span data-ttu-id="a8f2a-118">值</span><span class="sxs-lookup"><span data-stu-id="a8f2a-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8f2a-119">標頭</span><span class="sxs-lookup"><span data-stu-id="a8f2a-119">Header</span></span><br/>  | <dl> <span data-ttu-id="a8f2a-120"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="a8f2a-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a8f2a-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="a8f2a-121">Library</span></span><br/> | <dl> <span data-ttu-id="a8f2a-122"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8f2a-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a8f2a-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8f2a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8f2a-124">數學函數</span><span class="sxs-lookup"><span data-stu-id="a8f2a-124">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="a8f2a-125">**D3DXVec4Cross**</span><span class="sxs-lookup"><span data-stu-id="a8f2a-125">**D3DXVec4Cross**</span></span>](d3dxvec4cross.md)
</dt> </dl>

 

 
