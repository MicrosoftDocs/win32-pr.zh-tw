---
title: Texture2DArray：： Texture2DArray GatherCmp 方法
description: 範例和比較 Texture2DArray 並傳回所有的元件。
ms.assetid: 5b2892f0-be62-4fb2-978e-aabb8ae96e67
keywords:
- GatherCmp 方法 HLSL
topic_type:
- apiref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
api_location: ''
ms.openlocfilehash: 760c6313df2fb50ea821495d9f57933aef5bb0cc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104973892"
---
# <a name="texture2darraygathercmp-methods"></a><span data-ttu-id="4723c-104">Texture2DArray：： GatherCmp 方法</span><span class="sxs-lookup"><span data-stu-id="4723c-104">Texture2DArray::GatherCmp methods</span></span>

<span data-ttu-id="4723c-105">針對要在雙線性篩選作業中使用之 [**Texture2DArray**](sm5-object-texture2darray.md) 的四個材質值，會傳回其與比較值的比較。</span><span class="sxs-lookup"><span data-stu-id="4723c-105">For four texel values of a [**Texture2DArray**](sm5-object-texture2darray.md) that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span>

<span data-ttu-id="4723c-106">如需描述基礎 DXBC 指令的詳細資訊，請參閱 [gather4_c](./gather4-c--sm5---asm-.md) 的相關檔。</span><span class="sxs-lookup"><span data-stu-id="4723c-106">See the documentation on [gather4_c](./gather4-c--sm5---asm-.md) for more information describing the underlying DXBC instruction.</span></span>

### <a name="overload-list"></a><span data-ttu-id="4723c-107">多載清單</span><span class="sxs-lookup"><span data-stu-id="4723c-107">Overload list</span></span>



| <span data-ttu-id="4723c-108">方法</span><span class="sxs-lookup"><span data-stu-id="4723c-108">Method</span></span>                                                                             | <span data-ttu-id="4723c-109">描述</span><span class="sxs-lookup"><span data-stu-id="4723c-109">Description</span></span>                                                                                                      |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4723c-110">**GatherCmp (S、float、float、int)**</span><span class="sxs-lookup"><span data-stu-id="4723c-110">**GatherCmp(S,float,float,int)**</span></span>](sm5-object-texture2darray-gathercmp.md)        | <span data-ttu-id="4723c-111">範例並比較材質，並傳回所有四個元件。</span><span class="sxs-lookup"><span data-stu-id="4723c-111">Samples and compares a texture and returns all four components.</span></span><br/>                                       |
| [<span data-ttu-id="4723c-112">**GatherCmp (S、float、float、int、uint)**</span><span class="sxs-lookup"><span data-stu-id="4723c-112">**GatherCmp(S,float,float,int,uint)**</span></span>](t2d-gathercmp-s-float-float-int-uint-.md) | <span data-ttu-id="4723c-113">範例並比較材質，並傳回所有四個元件以及作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="4723c-113">Samples and compares a texture and returns all four components along with status about the operation.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4723c-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4723c-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4723c-115">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="4723c-115">Texture2DArray</span></span>](sm5-object-texture2darray.md)
</dt> </dl>

 

