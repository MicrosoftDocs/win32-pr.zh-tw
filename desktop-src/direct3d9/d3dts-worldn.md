---
description: 識別後續的轉換矩陣，這些矩陣可以用來 blend 頂點，方法是使用對應的矩陣，以及在頂點格式中指定的混合 (搶鮮版（Beta）) 加權值。
ms.assetid: cab444c2-b245-4d1a-a90c-745c92a2ea89
title: 'D3DTS_WORLDn (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTS_WORLDn
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 004435d278538c788e21ed7dc3482fd5e248895b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976693"
---
# <a name="d3dts_worldn"></a><span data-ttu-id="fb627-103">D3DTS \_ WORLDn</span><span class="sxs-lookup"><span data-stu-id="fb627-103">D3DTS\_WORLDn</span></span>

<span data-ttu-id="fb627-104">識別後續的轉換矩陣，這些矩陣可以用來 blend 頂點，方法是使用對應的矩陣，以及在頂點格式中指定的混合 (搶鮮版（Beta）) 加權值。</span><span class="sxs-lookup"><span data-stu-id="fb627-104">Identifies subsequent transformation matrices that can be used to blend vertices by using the corresponding matrix and a blending (beta) weight value specified in the vertex format.</span></span>

``` syntax
#define D3DTS_WORLDn 
#define D3DTS_WORLD1 D3DTS_WORLDMATRIX(1)
#define D3DTS_WORLD2 D3DTS_WORLDMATRIX(2)
#define D3DTS_WORLD3 D3DTS_WORLDMATRIX(3)
```

## <a name="remarks"></a><span data-ttu-id="fb627-105">備註</span><span class="sxs-lookup"><span data-stu-id="fb627-105">Remarks</span></span>

<span data-ttu-id="fb627-106">這些宏是為了促進現有的應用程式與 Direct3D 9 的移植而提供。</span><span class="sxs-lookup"><span data-stu-id="fb627-106">These macros are provided to facilitate porting existing applications to Direct3D 9.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb627-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb627-107">Requirements</span></span>



| <span data-ttu-id="fb627-108">需求</span><span class="sxs-lookup"><span data-stu-id="fb627-108">Requirement</span></span> | <span data-ttu-id="fb627-109">值</span><span class="sxs-lookup"><span data-stu-id="fb627-109">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb627-110">標頭</span><span class="sxs-lookup"><span data-stu-id="fb627-110">Header</span></span><br/> | <dl> <span data-ttu-id="fb627-111"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="fb627-111"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb627-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb627-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb627-113">巨集</span><span class="sxs-lookup"><span data-stu-id="fb627-113">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="fb627-114">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="fb627-114">**SetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[<span data-ttu-id="fb627-115">**D3DTS \_ WORLDMATRIX**</span><span class="sxs-lookup"><span data-stu-id="fb627-115">**D3DTS\_WORLDMATRIX**</span></span>](d3dts-worldmatrix.md)
</dt> </dl>

 

 
