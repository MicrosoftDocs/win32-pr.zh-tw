---
description: 描述效果物件。
ms.assetid: 161d3e7a-213a-4a83-a1b5-837b0aab96bf
title: 'D3DXEFFECT_DESC 結構 (D3dx9effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: c8e7a3a2adf19514e2e4d1c6f61dbea888ce033d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696647"
---
# <a name="d3dxeffect_desc-structure"></a><span data-ttu-id="d0c6a-103">D3DXEFFECT \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="d0c6a-103">D3DXEFFECT\_DESC structure</span></span>

<span data-ttu-id="d0c6a-104">描述效果物件。</span><span class="sxs-lookup"><span data-stu-id="d0c6a-104">Describes an effect object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0c6a-105">語法</span><span class="sxs-lookup"><span data-stu-id="d0c6a-105">Syntax</span></span>


```C++
typedef struct D3DXEFFECT_DESC {
  LPCSTR Creator;
  UINT   Parameters;
  UINT   Techniques;
  UINT   Functions;
} D3DXEFFECT_DESC, *LPD3DXEFFECT_DESC;
```



## <a name="members"></a><span data-ttu-id="d0c6a-106">成員</span><span class="sxs-lookup"><span data-stu-id="d0c6a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d0c6a-107">**建立者**</span><span class="sxs-lookup"><span data-stu-id="d0c6a-107">**Creator**</span></span>
</dt> <dd>

<span data-ttu-id="d0c6a-108">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d0c6a-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d0c6a-109">字串，其中包含效果建立者的名稱。</span><span class="sxs-lookup"><span data-stu-id="d0c6a-109">String that contains the name of the effect creator.</span></span>

</dd> <dt>

<span data-ttu-id="d0c6a-110">**參數**</span><span class="sxs-lookup"><span data-stu-id="d0c6a-110">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="d0c6a-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d0c6a-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d0c6a-112">用於效果的參數數目。</span><span class="sxs-lookup"><span data-stu-id="d0c6a-112">Number of parameters used for effect.</span></span>

</dd> <dt>

<span data-ttu-id="d0c6a-113">**技術**</span><span class="sxs-lookup"><span data-stu-id="d0c6a-113">**Techniques**</span></span>
</dt> <dd>

<span data-ttu-id="d0c6a-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d0c6a-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d0c6a-115">可以呈現效果的技術數目。</span><span class="sxs-lookup"><span data-stu-id="d0c6a-115">Number of techniques that can render the effect.</span></span>

</dd> <dt>

<span data-ttu-id="d0c6a-116">**函數**</span><span class="sxs-lookup"><span data-stu-id="d0c6a-116">**Functions**</span></span>
</dt> <dd>

<span data-ttu-id="d0c6a-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d0c6a-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d0c6a-118">可以呈現效果的函式數目。</span><span class="sxs-lookup"><span data-stu-id="d0c6a-118">Number of functions that can render the effect.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d0c6a-119">備註</span><span class="sxs-lookup"><span data-stu-id="d0c6a-119">Remarks</span></span>

<span data-ttu-id="d0c6a-120">效果物件可以包含相同效果的多種轉譯技巧和參數。</span><span class="sxs-lookup"><span data-stu-id="d0c6a-120">An effect object can contain multiple rendering techniques and parameters for the same effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0c6a-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0c6a-121">Requirements</span></span>



| <span data-ttu-id="d0c6a-122">需求</span><span class="sxs-lookup"><span data-stu-id="d0c6a-122">Requirement</span></span> | <span data-ttu-id="d0c6a-123">值</span><span class="sxs-lookup"><span data-stu-id="d0c6a-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0c6a-124">標頭</span><span class="sxs-lookup"><span data-stu-id="d0c6a-124">Header</span></span><br/> | <dl> <span data-ttu-id="d0c6a-125"><dt>D3dx9effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="d0c6a-125"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0c6a-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0c6a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0c6a-127">效果結構</span><span class="sxs-lookup"><span data-stu-id="d0c6a-127">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
