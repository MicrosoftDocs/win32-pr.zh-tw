---
description: 描述點陣狀態。
ms.assetid: f7b5b714-8fc8-47b8-adec-1089b8d07081
title: 'D3DRASTER_STATUS 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRASTER_STATUS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e77ab0e6ee164eadae862ed03df5652c21ba7040
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106975683"
---
# <a name="d3draster_status-structure"></a><span data-ttu-id="c64f9-103">D3DRASTER \_ 狀態結構</span><span class="sxs-lookup"><span data-stu-id="c64f9-103">D3DRASTER\_STATUS structure</span></span>

<span data-ttu-id="c64f9-104">描述點陣狀態。</span><span class="sxs-lookup"><span data-stu-id="c64f9-104">Describes the raster status.</span></span>

## <a name="syntax"></a><span data-ttu-id="c64f9-105">語法</span><span class="sxs-lookup"><span data-stu-id="c64f9-105">Syntax</span></span>


```C++
typedef struct D3DRASTER_STATUS {
  BOOL InVBlank;
  UINT ScanLine;
} D3DRASTER_STATUS, *LPD3DRASTER_STATUS;
```



## <a name="members"></a><span data-ttu-id="c64f9-106">成員</span><span class="sxs-lookup"><span data-stu-id="c64f9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c64f9-107">**InVBlank**</span><span class="sxs-lookup"><span data-stu-id="c64f9-107">**InVBlank**</span></span>
</dt> <dd>

<span data-ttu-id="c64f9-108">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c64f9-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c64f9-109">如果點陣處於垂直空白期間，**則為 TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="c64f9-109">**TRUE** if the raster is in the vertical blank period.</span></span> <span data-ttu-id="c64f9-110">如果點陣不在垂直空白句號內，則 **為 FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="c64f9-110">**FALSE** if the raster is not in the vertical blank period.</span></span>

</dd> <dt>

<span data-ttu-id="c64f9-111">**ScanLine**</span><span class="sxs-lookup"><span data-stu-id="c64f9-111">**ScanLine**</span></span>
</dt> <dd>

<span data-ttu-id="c64f9-112">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c64f9-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c64f9-113">如果 InVBlank 為 **FALSE**，則這個值會是大約對應到點陣所繪製之目前掃描行的整數。</span><span class="sxs-lookup"><span data-stu-id="c64f9-113">If InVBlank is **FALSE**, then this value is an integer roughly corresponding to the current scan line painted by the raster.</span></span> <span data-ttu-id="c64f9-114">掃描行的編號方式與 Direct3D 介面座標相同：0是主要表面的頂端，會延伸至顯示器底部)  (高度的值。</span><span class="sxs-lookup"><span data-stu-id="c64f9-114">Scan lines are numbered in the same way as Direct3D surface coordinates: 0 is the top of the primary surface, extending to the value (height of the surface - 1) at the bottom of the display.</span></span>

<span data-ttu-id="c64f9-115">如果 InVBlank 為 **TRUE**，則此值會設定為零，而且可以忽略。</span><span class="sxs-lookup"><span data-stu-id="c64f9-115">If InVBlank is **TRUE**, then this value is set to zero and can be ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c64f9-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="c64f9-116">Requirements</span></span>



| <span data-ttu-id="c64f9-117">需求</span><span class="sxs-lookup"><span data-stu-id="c64f9-117">Requirement</span></span> | <span data-ttu-id="c64f9-118">值</span><span class="sxs-lookup"><span data-stu-id="c64f9-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c64f9-119">標頭</span><span class="sxs-lookup"><span data-stu-id="c64f9-119">Header</span></span><br/> | <dl> <span data-ttu-id="c64f9-120"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="c64f9-120"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c64f9-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c64f9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c64f9-122">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="c64f9-122">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="c64f9-123">**GetRasterStatus**</span><span class="sxs-lookup"><span data-stu-id="c64f9-123">**GetRasterStatus**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrasterstatus)
</dt> </dl>

 

 
