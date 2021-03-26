---
title: Texture2DArray：： Texture2DArray 收集方法
description: 範例 Texture2DArray 並傳回所有四個元件。
ms.assetid: eea1dd00-0061-4601-a218-979eb0ecd36d
keywords:
- 收集方法 HLSL
topic_type:
- apiref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
api_location: ''
ms.openlocfilehash: cd10959490a85583cab01814f9cdb012859317a4
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104973884"
---
# <a name="texture2darraygather-methods"></a><span data-ttu-id="59f7b-104">Texture2DArray：：收集方法</span><span class="sxs-lookup"><span data-stu-id="59f7b-104">Texture2DArray::Gather methods</span></span>

<span data-ttu-id="59f7b-105">傳回 [**Texture2DArray**](sm5-object-texture2darray.md) 的四個材質值，這些值會在雙線性篩選作業中使用。</span><span class="sxs-lookup"><span data-stu-id="59f7b-105">Returns the four texel values of a [**Texture2DArray**](sm5-object-texture2darray.md) that would be used in a bi-linear filtering operation.</span></span>

<span data-ttu-id="59f7b-106">如需描述基礎 DXBC 指示的詳細資訊，請參閱 [gather4](./gather4--sm5---asm-.md) 上的檔。</span><span class="sxs-lookup"><span data-stu-id="59f7b-106">See the documentation on [gather4](./gather4--sm5---asm-.md) for more information describing the underlying DXBC instruction.</span></span>

### <a name="overload-list"></a><span data-ttu-id="59f7b-107">多載清單</span><span class="sxs-lookup"><span data-stu-id="59f7b-107">Overload list</span></span>



| <span data-ttu-id="59f7b-108">方法</span><span class="sxs-lookup"><span data-stu-id="59f7b-108">Method</span></span>                                                                | <span data-ttu-id="59f7b-109">描述</span><span class="sxs-lookup"><span data-stu-id="59f7b-109">Description</span></span>                                                                                                               |
|:----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="59f7b-110">**收集 (S、float、int)**</span><span class="sxs-lookup"><span data-stu-id="59f7b-110">**Gather(S,float,int)**</span></span>](sm5-object-texture2darray-gather.md)        | <span data-ttu-id="59f7b-111">傳回要在雙線性篩選作業中使用的四個材質值。</span><span class="sxs-lookup"><span data-stu-id="59f7b-111">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                 |
| [<span data-ttu-id="59f7b-112">**收集 (S、float、int、uint)**</span><span class="sxs-lookup"><span data-stu-id="59f7b-112">**Gather(S,float,int,uint)**</span></span>](t2darray-gather-s-float-int-uint-.md)  | <span data-ttu-id="59f7b-113">傳回四個材質值，這些值會在雙線性篩選作業中使用，以及磚對應狀態。</span><span class="sxs-lookup"><span data-stu-id="59f7b-113">Returns the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="59f7b-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59f7b-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59f7b-115">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="59f7b-115">Texture2DArray</span></span>](sm5-object-texture2darray.md)
</dt> </dl>

 

