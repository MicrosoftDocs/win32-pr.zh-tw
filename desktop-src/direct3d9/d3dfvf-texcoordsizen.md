---
description: 會建立用來識別 FVF 描述內材質座標格式的位模式。 您可以使用 OR 運算子，將這些宏的結果結合在 FVF 描述內。
ms.assetid: c3076d7c-7935-40ee-b513-7ff6551a535f
title: 'D3DFVF_TEXCOORDSIZEN (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFVF_TEXCOORDSIZEN
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 58288667954e3414aa3d8ae1550e02e7216ffb4e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992327"
---
# <a name="d3dfvf_texcoordsizen"></a><span data-ttu-id="5cec9-104">D3DFVF \_ TEXCOORDSIZEN</span><span class="sxs-lookup"><span data-stu-id="5cec9-104">D3DFVF\_TEXCOORDSIZEN</span></span>

<span data-ttu-id="5cec9-105">會建立用來識別 FVF 描述內材質座標格式的位模式。</span><span class="sxs-lookup"><span data-stu-id="5cec9-105">Constructs bit patterns that are used to identify texture coordinate formats within a FVF description.</span></span> <span data-ttu-id="5cec9-106">您可以使用 OR 運算子，將這些宏的結果結合在 FVF 描述內。</span><span class="sxs-lookup"><span data-stu-id="5cec9-106">The results of these macros can be combined within a FVF description by using the OR operator.</span></span>

``` syntax
#define D3DFVF_TEXCOORDSIZEN(CoordIndex) 
#define D3DFVF_TEXCOORDSIZE1(CoordIndex) (D3DFVF_TEXTUREFORMAT1 << (CoordIndex*2 + 16)) 
#define D3DFVF_TEXCOORDSIZE2(CoordIndex) (D3DFVF_TEXTUREFORMAT2) 
#define D3DFVF_TEXCOORDSIZE3(CoordIndex) (D3DFVF_TEXTUREFORMAT3 << (CoordIndex*2 + 16)) 
#define D3DFVF_TEXCOORDSIZE4(CoordIndex) (D3DFVF_TEXTUREFORMAT4 << (CoordIndex*2 + 16))
```

## <a name="parameters"></a><span data-ttu-id="5cec9-107">參數</span><span class="sxs-lookup"><span data-stu-id="5cec9-107">Parameters</span></span>



| <span data-ttu-id="5cec9-108">參數</span><span class="sxs-lookup"><span data-stu-id="5cec9-108">Parameter</span></span>                                                                                                    | <span data-ttu-id="5cec9-109">Description</span><span class="sxs-lookup"><span data-stu-id="5cec9-109">Description</span></span>                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cec9-110"><span id="CoordIndex"></span><span id="coordindex"></span><span id="COORDINDEX"></span>CoordIndex</span><span class="sxs-lookup"><span data-stu-id="5cec9-110"><span id="CoordIndex"></span><span id="coordindex"></span><span id="COORDINDEX"></span>CoordIndex</span></span><br/> | <span data-ttu-id="5cec9-111">值，這個值會識別材質座標大小 (1-、2-、3或 4Dimensional) 套用的材質座標集合。</span><span class="sxs-lookup"><span data-stu-id="5cec9-111">Value that identifies the texture coordinate set at which the texture coordinate size (1-, 2-, 3-, or 4Dimensional) applies.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="5cec9-112">備註</span><span class="sxs-lookup"><span data-stu-id="5cec9-112">Remarks</span></span>

<span data-ttu-id="5cec9-113">**D3DFVF \_ TEXCOORDSIZEN** 宏會使用下列常數。</span><span class="sxs-lookup"><span data-stu-id="5cec9-113">The **D3DFVF\_TEXCOORDSIZEN** macros use the following constants.</span></span>


```C++
#define D3DFVF_TEXTUREFORMAT1 3 // one floating point value
#define D3DFVF_TEXTUREFORMAT2 0 // two floating point values
#define D3DFVF_TEXTUREFORMAT3 1 // three floating point values
#define D3DFVF_TEXTUREFORMAT4 2 // four floating point values
```



<span data-ttu-id="5cec9-114">下列 FVF 描述會識別具有位置的頂點格式;一般;擴散和反射色彩;以及兩組材質座標。</span><span class="sxs-lookup"><span data-stu-id="5cec9-114">The following FVF description identifies a vertex format that has a position; a normal; diffuse and specular colors; and two sets of texture coordinates.</span></span> <span data-ttu-id="5cec9-115">第一組紋理座標包含單一元素，而第二組則包含兩個元素：</span><span class="sxs-lookup"><span data-stu-id="5cec9-115">The first set of texture coordinates includes a single element, and the second set includes two elements:</span></span>


```C++
DWORD dwFVF = D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_DIFFUSE |
              D3DFVF_SPECULAR | D3DFVF_TEX2 |
              D3DFVF_TEXCOORDSIZE1(0) |  // Uses 1D texture coordinates for
                                         // texture coordinate set 1 (index 0).
              D3DFVF_TEXCOORDSIZE2(1);   // And 2D texture coordinates for 
                                         // texture coordinate set 2 (index 1).
```



## <a name="requirements"></a><span data-ttu-id="5cec9-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="5cec9-116">Requirements</span></span>



| <span data-ttu-id="5cec9-117">需求</span><span class="sxs-lookup"><span data-stu-id="5cec9-117">Requirement</span></span> | <span data-ttu-id="5cec9-118">值</span><span class="sxs-lookup"><span data-stu-id="5cec9-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5cec9-119">標頭</span><span class="sxs-lookup"><span data-stu-id="5cec9-119">Header</span></span><br/> | <dl> <span data-ttu-id="5cec9-120"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="5cec9-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cec9-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5cec9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cec9-122">巨集</span><span class="sxs-lookup"><span data-stu-id="5cec9-122">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="5cec9-123">D3DFVF</span><span class="sxs-lookup"><span data-stu-id="5cec9-123">D3DFVF</span></span>](d3dfvf.md)
</dt> </dl>

 

 




