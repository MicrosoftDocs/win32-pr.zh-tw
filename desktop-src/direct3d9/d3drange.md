---
description: 定義範圍。
ms.assetid: 28e8c478-f6ce-4f75-95c6-ea2d08424238
title: 'D3DRANGE 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRANGE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 15ff267528ddfd12f8da77921e2edc2d836e1a39
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997246"
---
# <a name="d3drange-structure"></a><span data-ttu-id="3f043-103">D3DRANGE 結構</span><span class="sxs-lookup"><span data-stu-id="3f043-103">D3DRANGE structure</span></span>

<span data-ttu-id="3f043-104">定義範圍。</span><span class="sxs-lookup"><span data-stu-id="3f043-104">Defines a range.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f043-105">語法</span><span class="sxs-lookup"><span data-stu-id="3f043-105">Syntax</span></span>


```C++
typedef struct D3DRANGE {
  UINT Offset;
  UINT Size;
} D3DRANGE, *LPD3DRANGE;
```



## <a name="members"></a><span data-ttu-id="3f043-106">成員</span><span class="sxs-lookup"><span data-stu-id="3f043-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3f043-107">**Offset**</span><span class="sxs-lookup"><span data-stu-id="3f043-107">**Offset**</span></span>
</dt> <dd>

<span data-ttu-id="3f043-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3f043-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3f043-109">位移（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3f043-109">Offset, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3f043-110">**大小**</span><span class="sxs-lookup"><span data-stu-id="3f043-110">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="3f043-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3f043-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3f043-112">大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3f043-112">Size, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3f043-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="3f043-113">Requirements</span></span>



| <span data-ttu-id="3f043-114">需求</span><span class="sxs-lookup"><span data-stu-id="3f043-114">Requirement</span></span> | <span data-ttu-id="3f043-115">值</span><span class="sxs-lookup"><span data-stu-id="3f043-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f043-116">標頭</span><span class="sxs-lookup"><span data-stu-id="3f043-116">Header</span></span><br/> | <dl> <span data-ttu-id="3f043-117"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="3f043-117"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f043-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3f043-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f043-119">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="3f043-119">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
