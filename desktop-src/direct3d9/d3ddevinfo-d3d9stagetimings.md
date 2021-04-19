---
description: 處理著色器資料的時間百分比。
ms.assetid: 388bb943-c25f-4b50-b7e4-d6259f1186c2
title: 'D3DDEVINFO_D3D9STAGETIMINGS 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9STAGETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: cf8c9522decfcbb09a60aff0bee65ca05a0f5eeb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986732"
---
# <a name="d3ddevinfo_d3d9stagetimings-structure"></a><span data-ttu-id="f411e-103">D3DDEVINFO \_ D3D9STAGETIMINGS 結構</span><span class="sxs-lookup"><span data-stu-id="f411e-103">D3DDEVINFO\_D3D9STAGETIMINGS structure</span></span>

<span data-ttu-id="f411e-104">處理著色器資料的時間百分比。</span><span class="sxs-lookup"><span data-stu-id="f411e-104">Percent of time processing shader data.</span></span>

## <a name="syntax"></a><span data-ttu-id="f411e-105">語法</span><span class="sxs-lookup"><span data-stu-id="f411e-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_D3D9STAGETIMINGS {
  FLOAT MemoryProcessingPercent;
  FLOAT ComputationProcessingPercent;
} D3DDEVINFO_D3D9STAGETIMINGS, *LPD3DDEVINFO_D3D9STAGETIMINGS;
```



## <a name="members"></a><span data-ttu-id="f411e-106">成員</span><span class="sxs-lookup"><span data-stu-id="f411e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f411e-107">**MemoryProcessingPercent**</span><span class="sxs-lookup"><span data-stu-id="f411e-107">**MemoryProcessingPercent**</span></span>
</dt> <dd>

<span data-ttu-id="f411e-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f411e-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f411e-109">著色器花費在記憶體存取上的時間百分比。</span><span class="sxs-lookup"><span data-stu-id="f411e-109">Percent of time in shader spent on memory accesses.</span></span>

</dd> <dt>

<span data-ttu-id="f411e-110">**ComputationProcessingPercent**</span><span class="sxs-lookup"><span data-stu-id="f411e-110">**ComputationProcessingPercent**</span></span>
</dt> <dd>

<span data-ttu-id="f411e-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f411e-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f411e-112">時間處理的百分比 (在暫存器中移動資料，或) 執行數學運算。</span><span class="sxs-lookup"><span data-stu-id="f411e-112">Percent of time processing (moving data around in registers or doing mathematical operations).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f411e-113">備註</span><span class="sxs-lookup"><span data-stu-id="f411e-113">Remarks</span></span>

<span data-ttu-id="f411e-114">為了達到最佳效能，建議使用平衡負載。</span><span class="sxs-lookup"><span data-stu-id="f411e-114">For best performance, a balanced load is recommended.</span></span>

## <a name="requirements"></a><span data-ttu-id="f411e-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f411e-115">Requirements</span></span>



| <span data-ttu-id="f411e-116">需求</span><span class="sxs-lookup"><span data-stu-id="f411e-116">Requirement</span></span> | <span data-ttu-id="f411e-117">值</span><span class="sxs-lookup"><span data-stu-id="f411e-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f411e-118">標頭</span><span class="sxs-lookup"><span data-stu-id="f411e-118">Header</span></span><br/> | <dl> <span data-ttu-id="f411e-119"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="f411e-119"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f411e-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f411e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f411e-121">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="f411e-121">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="f411e-122">**GetData**</span><span class="sxs-lookup"><span data-stu-id="f411e-122">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
