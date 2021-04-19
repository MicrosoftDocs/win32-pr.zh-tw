---
description: 管線中處理資料的時間百分比。
ms.assetid: eb9dec27-2e45-4897-92af-8415c8fa08d4
title: 'D3DDEVINFO_D3D9PIPELINETIMINGS 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9PIPELINETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 627eec0ea93181b14c308ab229ed603412511a91
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106989188"
---
# <a name="d3ddevinfo_d3d9pipelinetimings-structure"></a><span data-ttu-id="617f7-103">D3DDEVINFO \_ D3D9PIPELINETIMINGS 結構</span><span class="sxs-lookup"><span data-stu-id="617f7-103">D3DDEVINFO\_D3D9PIPELINETIMINGS structure</span></span>

<span data-ttu-id="617f7-104">管線中處理資料的時間百分比。</span><span class="sxs-lookup"><span data-stu-id="617f7-104">Percent of time processing data in the pipeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="617f7-105">語法</span><span class="sxs-lookup"><span data-stu-id="617f7-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_D3D9PIPELINETIMINGS {
  FLOAT VertexProcessingTimePercent;
  FLOAT PixelProcessingTimePercent;
  FLOAT OtherGPUProcessingTimePercent;
  FLOAT GPUIdleTimePercent;
} D3DDEVINFO_D3D9PIPELINETIMINGS, *LPD3DDEVINFO_D3D9PIPELINETIMINGS;
```



## <a name="members"></a><span data-ttu-id="617f7-106">成員</span><span class="sxs-lookup"><span data-stu-id="617f7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="617f7-107">**VertexProcessingTimePercent**</span><span class="sxs-lookup"><span data-stu-id="617f7-107">**VertexProcessingTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="617f7-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="617f7-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="617f7-109">執行頂點著色器所花費的時間百分比。</span><span class="sxs-lookup"><span data-stu-id="617f7-109">Percent of time spent running vertex shaders.</span></span>

</dd> <dt>

<span data-ttu-id="617f7-110">**PixelProcessingTimePercent**</span><span class="sxs-lookup"><span data-stu-id="617f7-110">**PixelProcessingTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="617f7-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="617f7-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="617f7-112">花費在執行圖元著色器的時間百分比。</span><span class="sxs-lookup"><span data-stu-id="617f7-112">Percent of time spent running pixel shaders.</span></span>

</dd> <dt>

<span data-ttu-id="617f7-113">**OtherGPUProcessingTimePercent**</span><span class="sxs-lookup"><span data-stu-id="617f7-113">**OtherGPUProcessingTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="617f7-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="617f7-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="617f7-115">執行其他處理所花費的時間百分比。</span><span class="sxs-lookup"><span data-stu-id="617f7-115">Percent of time spent doing other processing.</span></span>

</dd> <dt>

<span data-ttu-id="617f7-116">**GPUIdleTimePercent**</span><span class="sxs-lookup"><span data-stu-id="617f7-116">**GPUIdleTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="617f7-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="617f7-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="617f7-118">未處理任何時間的時間百分比。</span><span class="sxs-lookup"><span data-stu-id="617f7-118">Percent of time not processing anything.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="617f7-119">備註</span><span class="sxs-lookup"><span data-stu-id="617f7-119">Remarks</span></span>

<span data-ttu-id="617f7-120">為了達到最佳效能，建議使用平衡負載。</span><span class="sxs-lookup"><span data-stu-id="617f7-120">For best performance, a balanced load is recommended.</span></span>

## <a name="requirements"></a><span data-ttu-id="617f7-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="617f7-121">Requirements</span></span>



| <span data-ttu-id="617f7-122">需求</span><span class="sxs-lookup"><span data-stu-id="617f7-122">Requirement</span></span> | <span data-ttu-id="617f7-123">值</span><span class="sxs-lookup"><span data-stu-id="617f7-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="617f7-124">標頭</span><span class="sxs-lookup"><span data-stu-id="617f7-124">Header</span></span><br/> | <dl> <span data-ttu-id="617f7-125"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="617f7-125"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="617f7-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="617f7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="617f7-127">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="617f7-127">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="617f7-128">**GetData**</span><span class="sxs-lookup"><span data-stu-id="617f7-128">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
