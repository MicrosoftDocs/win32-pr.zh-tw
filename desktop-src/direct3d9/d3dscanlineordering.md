---
description: 旗標，指出轉譯器用來在介面上建立影像的方法。
ms.assetid: 55cf790e-ebe9-4791-a2be-a90fc76bae57
title: 'D3DSCANLINEORDERING 列舉 (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSCANLINEORDERING
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2eaed36577f881266c12b0a927cfcdc2494f0d57
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106975711"
---
# <a name="d3dscanlineordering-enumeration"></a><span data-ttu-id="f4f31-103">D3DSCANLINEORDERING 列舉</span><span class="sxs-lookup"><span data-stu-id="f4f31-103">D3DSCANLINEORDERING enumeration</span></span>

<span data-ttu-id="f4f31-104">旗標，指出轉譯器用來在介面上建立影像的方法。</span><span class="sxs-lookup"><span data-stu-id="f4f31-104">Flags indicating the method the rasterizer uses to create an image on a surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4f31-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4f31-105">Syntax</span></span>


```C++
typedef enum D3DSCANLINEORDERING { 
  D3DSCANLINEORDERING_PROGRESSIVE  = 1,
  D3DSCANLINEORDERING_INTERLACED   = 2
} D3DSCANLINEORDERING, *LPD3DSCANLINEORDERING;
```



## <a name="constants"></a><span data-ttu-id="f4f31-106">常數</span><span class="sxs-lookup"><span data-stu-id="f4f31-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f4f31-107"><span id="D3DSCANLINEORDERING_PROGRESSIVE"></span><span id="d3dscanlineordering_progressive"></span>**D3DSCANLINEORDERING \_ 漸進式**</span><span class="sxs-lookup"><span data-stu-id="f4f31-107"><span id="D3DSCANLINEORDERING_PROGRESSIVE"></span><span id="d3dscanlineordering_progressive"></span>**D3DSCANLINEORDERING\_PROGRESSIVE**</span></span>
</dt> <dd>

<span data-ttu-id="f4f31-108">映射會從第一個 scanline 建立到最後一個，而不會略過任何。</span><span class="sxs-lookup"><span data-stu-id="f4f31-108">The image is created from the first scanline to the last without skipping any.</span></span>

</dd> <dt>

<span data-ttu-id="f4f31-109"><span id="D3DSCANLINEORDERING_INTERLACED"></span><span id="d3dscanlineordering_interlaced"></span>**交錯式 D3DSCANLINEORDERING \_**</span><span class="sxs-lookup"><span data-stu-id="f4f31-109"><span id="D3DSCANLINEORDERING_INTERLACED"></span><span id="d3dscanlineordering_interlaced"></span>**D3DSCANLINEORDERING\_INTERLACED**</span></span>
</dt> <dd>

<span data-ttu-id="f4f31-110">影像是使用交錯的方法所建立，在奇數的行程上繪製奇數行，甚至是在偶數的階段繪製。</span><span class="sxs-lookup"><span data-stu-id="f4f31-110">The image is created using the interlaced method in which odd-numbered lines are drawn on odd-numbered passes and even lines are drawn on even-numbered passes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4f31-111">備註</span><span class="sxs-lookup"><span data-stu-id="f4f31-111">Remarks</span></span>

<span data-ttu-id="f4f31-112">此列舉會用來做為 [**D3DDISPLAYMODEFILTER**](d3ddisplaymodefilter.md) 和 [**D3DDISPLAYMODEEX**](d3ddisplaymodeex.md)中的成員。</span><span class="sxs-lookup"><span data-stu-id="f4f31-112">This enumeration is used as a member in [**D3DDISPLAYMODEFILTER**](d3ddisplaymodefilter.md) and [**D3DDISPLAYMODEEX**](d3ddisplaymodeex.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4f31-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4f31-113">Requirements</span></span>



| <span data-ttu-id="f4f31-114">需求</span><span class="sxs-lookup"><span data-stu-id="f4f31-114">Requirement</span></span> | <span data-ttu-id="f4f31-115">值</span><span class="sxs-lookup"><span data-stu-id="f4f31-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4f31-116">標頭</span><span class="sxs-lookup"><span data-stu-id="f4f31-116">Header</span></span><br/> | <dl> <span data-ttu-id="f4f31-117"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="f4f31-117"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4f31-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4f31-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4f31-119">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="f4f31-119">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




