---
description: 指定要篩選出的顯示模式類型。
ms.assetid: 4a03d0f0-dec5-4209-8c99-b58cc13064f5
title: 'D3DDISPLAYMODEFILTER 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODEFILTER
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b60c283405bead7b2618b91d6de76158841ff27f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322763"
---
# <a name="d3ddisplaymodefilter-structure"></a><span data-ttu-id="03793-103">D3DDISPLAYMODEFILTER 結構</span><span class="sxs-lookup"><span data-stu-id="03793-103">D3DDISPLAYMODEFILTER structure</span></span>

<span data-ttu-id="03793-104">指定要篩選出的顯示模式類型。</span><span class="sxs-lookup"><span data-stu-id="03793-104">Specifies types of display modes to filter out.</span></span>

## <a name="syntax"></a><span data-ttu-id="03793-105">語法</span><span class="sxs-lookup"><span data-stu-id="03793-105">Syntax</span></span>


```C++
typedef struct {
  UINT                Size;
  D3DFORMAT           Format;
  D3DSCANLINEORDERING ScanLineOrdering;
} D3DDISPLAYMODEFILTER;
```



## <a name="members"></a><span data-ttu-id="03793-106">成員</span><span class="sxs-lookup"><span data-stu-id="03793-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="03793-107">**大小**</span><span class="sxs-lookup"><span data-stu-id="03793-107">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="03793-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="03793-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="03793-109">此結構的大小。</span><span class="sxs-lookup"><span data-stu-id="03793-109">The size of this structure.</span></span> <span data-ttu-id="03793-110">這應該一律設定為 sizeof (D3DDISPLAYMODEFILTER) 。</span><span class="sxs-lookup"><span data-stu-id="03793-110">This should always be set to sizeof(D3DDISPLAYMODEFILTER).</span></span>

</dd> <dt>

<span data-ttu-id="03793-111">**格式**</span><span class="sxs-lookup"><span data-stu-id="03793-111">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="03793-112">類型： **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="03793-112">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="03793-113">要篩選出的顯示模式格式。請參閱 [D3DFORMAT](d3dformat.md)。</span><span class="sxs-lookup"><span data-stu-id="03793-113">The display mode format to filter out. See [D3DFORMAT](d3dformat.md).</span></span>

</dd> <dt>

<span data-ttu-id="03793-114">**ScanLineOrdering**</span><span class="sxs-lookup"><span data-stu-id="03793-114">**ScanLineOrdering**</span></span>
</dt> <dd>

<span data-ttu-id="03793-115">類型： **[ **D3DSCANLINEORDERING**](./d3dscanlineordering.md)**</span><span class="sxs-lookup"><span data-stu-id="03793-115">Type: **[**D3DSCANLINEORDERING**](./d3dscanlineordering.md)**</span></span>

</dd> <dd>

<span data-ttu-id="03793-116">Scanline 順序是否為交錯式或漸進式。</span><span class="sxs-lookup"><span data-stu-id="03793-116">Whether the scanline ordering is interlaced or progressive.</span></span> <span data-ttu-id="03793-117">請參閱 [**D3DSCANLINEORDERING**](./d3dscanlineordering.md)。</span><span class="sxs-lookup"><span data-stu-id="03793-117">See [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="03793-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="03793-118">Requirements</span></span>



| <span data-ttu-id="03793-119">需求</span><span class="sxs-lookup"><span data-stu-id="03793-119">Requirement</span></span> | <span data-ttu-id="03793-120">值</span><span class="sxs-lookup"><span data-stu-id="03793-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="03793-121">標頭</span><span class="sxs-lookup"><span data-stu-id="03793-121">Header</span></span><br/> | <dl> <span data-ttu-id="03793-122"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="03793-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03793-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03793-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03793-124">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="03793-124">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
