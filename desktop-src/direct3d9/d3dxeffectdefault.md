---
description: 效果預設參數。
ms.assetid: a8a24cf2-0ecd-4429-97d3-086ff49540a1
title: 'D3DXEFFECTDEFAULT 結構 (D3dx9mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTDEFAULT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: fee415cbd7d8ec28daa079dd2f224949402a813b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991461"
---
# <a name="d3dxeffectdefault-structure"></a><span data-ttu-id="215a0-103">D3DXEFFECTDEFAULT 結構</span><span class="sxs-lookup"><span data-stu-id="215a0-103">D3DXEFFECTDEFAULT structure</span></span>

<span data-ttu-id="215a0-104">效果預設參數。</span><span class="sxs-lookup"><span data-stu-id="215a0-104">Effect default parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="215a0-105">語法</span><span class="sxs-lookup"><span data-stu-id="215a0-105">Syntax</span></span>


```C++
typedef struct D3DXEFFECTDEFAULT {
  LPSTR                 pParamName;
  D3DXEFFECTDEFAULTTYPE Type;
  DWORD                 NumBytes;
  LPVOID                pValue;
} D3DXEFFECTDEFAULT, *LPD3DXEFFECTDEFAULT;
```



## <a name="members"></a><span data-ttu-id="215a0-106">成員</span><span class="sxs-lookup"><span data-stu-id="215a0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="215a0-107">**pParamName**</span><span class="sxs-lookup"><span data-stu-id="215a0-107">**pParamName**</span></span>
</dt> <dd>

<span data-ttu-id="215a0-108">類型： **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="215a0-108">Type: **LPSTR**</span></span>

</dd> <dd>

<span data-ttu-id="215a0-109">參數名稱。</span><span class="sxs-lookup"><span data-stu-id="215a0-109">Parameter name.</span></span>

</dd> <dt>

<span data-ttu-id="215a0-110">**型別**</span><span class="sxs-lookup"><span data-stu-id="215a0-110">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="215a0-111">類型： **[ **D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)**</span><span class="sxs-lookup"><span data-stu-id="215a0-111">Type: **[**D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="215a0-112">PValue 中的資料類型。</span><span class="sxs-lookup"><span data-stu-id="215a0-112">Data type in pValue.</span></span> <span data-ttu-id="215a0-113">如需詳細資訊，請參閱 [ **D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)</span><span class="sxs-lookup"><span data-stu-id="215a0-113">For more information, see [**D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)</span></span>

</dd> <dt>

<span data-ttu-id="215a0-114">**NumBytes**</span><span class="sxs-lookup"><span data-stu-id="215a0-114">**NumBytes**</span></span>
</dt> <dd>

<span data-ttu-id="215a0-115">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="215a0-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="215a0-116">PValue 所指向之資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="215a0-116">Size, in bytes, of the data pointed to by pValue.</span></span>

</dd> <dt>

<span data-ttu-id="215a0-117">**pValue**</span><span class="sxs-lookup"><span data-stu-id="215a0-117">**pValue**</span></span>
</dt> <dd>

<span data-ttu-id="215a0-118">類型： **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="215a0-118">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="215a0-119">包含資料之記憶體位置的指標。</span><span class="sxs-lookup"><span data-stu-id="215a0-119">Pointer to the memory location that contains the data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="215a0-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="215a0-120">Requirements</span></span>



| <span data-ttu-id="215a0-121">需求</span><span class="sxs-lookup"><span data-stu-id="215a0-121">Requirement</span></span> | <span data-ttu-id="215a0-122">值</span><span class="sxs-lookup"><span data-stu-id="215a0-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="215a0-123">標頭</span><span class="sxs-lookup"><span data-stu-id="215a0-123">Header</span></span><br/> | <dl> <span data-ttu-id="215a0-124"><dt>D3dx9mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="215a0-124"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="215a0-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="215a0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="215a0-126">效果結構</span><span class="sxs-lookup"><span data-stu-id="215a0-126">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
