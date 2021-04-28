---
description: D3DXFLOAT16 結構 (D3dx9math) -描述16位浮點向量。
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
ms.openlocfilehash: dc878575de4338a2a399f329362d79ff2e7654f0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094266"
---
# <a name="d3dxfloat16-structure-d3dx9mathh"></a><span data-ttu-id="0e8cf-103">D3DXFLOAT16 結構 (D3dx9math .h) </span><span class="sxs-lookup"><span data-stu-id="0e8cf-103">D3DXFLOAT16 structure (D3dx9math.h)</span></span>

<span data-ttu-id="0e8cf-104">描述16位浮點向量。</span><span class="sxs-lookup"><span data-stu-id="0e8cf-104">Describes a 16-bit floating point vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e8cf-105">語法</span><span class="sxs-lookup"><span data-stu-id="0e8cf-105">Syntax</span></span>


```C++
typedef struct D3DXFLOAT16 {
  WORD Value;
} D3DXFLOAT16, *LPD3DXFLOAT16;
```



## <a name="members"></a><span data-ttu-id="0e8cf-106">成員</span><span class="sxs-lookup"><span data-stu-id="0e8cf-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0e8cf-107">**值**</span><span class="sxs-lookup"><span data-stu-id="0e8cf-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="0e8cf-108">類型： **[ **WORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0e8cf-108">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0e8cf-109">16位的資料。</span><span class="sxs-lookup"><span data-stu-id="0e8cf-109">The 16-bit data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0e8cf-110">備註</span><span class="sxs-lookup"><span data-stu-id="0e8cf-110">Remarks</span></span>

<span data-ttu-id="0e8cf-111">C + + 程式設計人員可以利用 [**D3DXFLOAT16 擴充**](d3dxfloat16-extensions.md)功能來利用運算子多載和類型轉換，以執行多載的函式和指派、一元和二元 (，包括相等) 運算子。</span><span class="sxs-lookup"><span data-stu-id="0e8cf-111">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXFLOAT16 Extensions**](d3dxfloat16-extensions.md), which implement overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e8cf-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e8cf-112">Requirements</span></span>



| <span data-ttu-id="0e8cf-113">需求</span><span class="sxs-lookup"><span data-stu-id="0e8cf-113">Requirement</span></span> | <span data-ttu-id="0e8cf-114">值</span><span class="sxs-lookup"><span data-stu-id="0e8cf-114">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e8cf-115">標頭</span><span class="sxs-lookup"><span data-stu-id="0e8cf-115">Header</span></span><br/> | <dl> <span data-ttu-id="0e8cf-116"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="0e8cf-116"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e8cf-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0e8cf-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e8cf-118">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="0e8cf-118">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
