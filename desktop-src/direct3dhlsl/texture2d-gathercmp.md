---
title: Texture2D：： Texture2D GatherCmp 方法
description: 範例和比較 Texture2D 並傳回所有的元件。
ms.assetid: d520b113-77af-486e-8d3d-8276f72df18f
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
ms.openlocfilehash: 18455f33ba97c9d5a0180a59e39891cd617a09af
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104973900"
---
# <a name="texture2dgathercmp-methods"></a><span data-ttu-id="d2852-104">Texture2D：： GatherCmp 方法</span><span class="sxs-lookup"><span data-stu-id="d2852-104">Texture2D::GatherCmp methods</span></span>

<span data-ttu-id="d2852-105">針對要在雙線性篩選作業中使用之 [**Texture2D**](sm5-object-texture2d.md) 的四個材質值，會傳回其與比較值的比較。</span><span class="sxs-lookup"><span data-stu-id="d2852-105">For four texel values of a [**Texture2D**](sm5-object-texture2d.md) that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span>

<span data-ttu-id="d2852-106">如需描述基礎 DXBC 指令的詳細資訊，請參閱 [gather4_c](./gather4-c--sm5---asm-.md) 的相關檔。</span><span class="sxs-lookup"><span data-stu-id="d2852-106">See the documentation on [gather4_c](./gather4-c--sm5---asm-.md) for more information describing the underlying DXBC instruction.</span></span>

### <a name="overload-list"></a><span data-ttu-id="d2852-107">多載清單</span><span class="sxs-lookup"><span data-stu-id="d2852-107">Overload list</span></span>



| <span data-ttu-id="d2852-108">方法</span><span class="sxs-lookup"><span data-stu-id="d2852-108">Method</span></span>                                                                             | <span data-ttu-id="d2852-109">描述</span><span class="sxs-lookup"><span data-stu-id="d2852-109">Description</span></span>                                                                                                      |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2852-110">**GatherCmp (S、float、float、int)**</span><span class="sxs-lookup"><span data-stu-id="d2852-110">**GatherCmp(S,float,float,int)**</span></span>](sm5-object-texture2d-gathercmp.md)             | <span data-ttu-id="d2852-111">範例並比較材質，並傳回所有四個元件。</span><span class="sxs-lookup"><span data-stu-id="d2852-111">Samples and compares a texture and returns all four components.</span></span><br/>                                       |
| [<span data-ttu-id="d2852-112">**GatherCmp (S、float、float、int、uint)**</span><span class="sxs-lookup"><span data-stu-id="d2852-112">**GatherCmp(S,float,float,int,uint)**</span></span>](t2d-gathercmp-s-float-float-int-uint-.md) | <span data-ttu-id="d2852-113">範例並比較材質，並傳回所有四個元件以及作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="d2852-113">Samples and compares a texture and returns all four components along with status about the operation.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d2852-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d2852-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2852-115">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d2852-115">Texture2D</span></span>](sm5-object-texture2d.md)
</dt> </dl>

 

