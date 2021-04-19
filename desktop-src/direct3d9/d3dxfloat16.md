---
description: 描述16位浮點向量。
ms.assetid: f823a327-f07a-44e9-b58a-7865e11e80eb
title: 'D3DXFLOAT16 結構 (D3dx9math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFLOAT16
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 4b469c770b811ed11ec21b21d2b449df1fd75b1c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981828"
---
# <a name="d3dxfloat16-structure-d3dx9mathh"></a><span data-ttu-id="3d590-103">D3DXFLOAT16 結構 (D3dx9math .h) </span><span class="sxs-lookup"><span data-stu-id="3d590-103">D3DXFLOAT16 structure (D3dx9math.h)</span></span>

<span data-ttu-id="3d590-104">描述16位浮點向量。</span><span class="sxs-lookup"><span data-stu-id="3d590-104">Describes a 16-bit floating point vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d590-105">語法</span><span class="sxs-lookup"><span data-stu-id="3d590-105">Syntax</span></span>


```C++
typedef struct D3DXFLOAT16 {
  WORD Value;
} D3DXFLOAT16, *LPD3DXFLOAT16;
```



## <a name="members"></a><span data-ttu-id="3d590-106">成員</span><span class="sxs-lookup"><span data-stu-id="3d590-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3d590-107">**值**</span><span class="sxs-lookup"><span data-stu-id="3d590-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="3d590-108">類型： **[ **WORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3d590-108">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3d590-109">16位的資料。</span><span class="sxs-lookup"><span data-stu-id="3d590-109">The 16-bit data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d590-110">備註</span><span class="sxs-lookup"><span data-stu-id="3d590-110">Remarks</span></span>

<span data-ttu-id="3d590-111">C + + 程式設計人員可以利用 [**D3DXFLOAT16 擴充**](d3dxfloat16-extensions.md)功能來利用運算子多載和類型轉換，以執行多載的函式和指派、一元和二元 (，包括相等) 運算子。</span><span class="sxs-lookup"><span data-stu-id="3d590-111">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXFLOAT16 Extensions**](d3dxfloat16-extensions.md), which implement overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d590-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d590-112">Requirements</span></span>



| <span data-ttu-id="3d590-113">需求</span><span class="sxs-lookup"><span data-stu-id="3d590-113">Requirement</span></span> | <span data-ttu-id="3d590-114">值</span><span class="sxs-lookup"><span data-stu-id="3d590-114">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d590-115">標頭</span><span class="sxs-lookup"><span data-stu-id="3d590-115">Header</span></span><br/> | <dl> <span data-ttu-id="3d590-116"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="3d590-116"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d590-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d590-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d590-118">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="3d590-118">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
