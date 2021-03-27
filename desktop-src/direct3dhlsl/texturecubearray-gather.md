---
title: TextureCubeArray：： TextureCubeArray 收集方法
description: 傳回四個材質值的紅色元件，這些值會在雙線性篩選作業中使用。 |TextureCubeArray：： TextureCubeArray 收集方法
ms.assetid: B459E455-EF22-46A7-ADFE-322ED808F83E
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
ms.openlocfilehash: 59a7dfd9170b93e1c253e7558cea7d8fb9b2f8c3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103853819"
---
# <a name="texturecubearraygather-methods"></a><span data-ttu-id="6f2d7-105">TextureCubeArray：：收集方法</span><span class="sxs-lookup"><span data-stu-id="6f2d7-105">TextureCubeArray::Gather methods</span></span>

<span data-ttu-id="6f2d7-106">傳回四個材質值的紅色元件，這些值會在雙線性篩選作業中使用。</span><span class="sxs-lookup"><span data-stu-id="6f2d7-106">Returns the red components of four texel values that would be used in a bi-linear filtering operation.</span></span>

<span data-ttu-id="6f2d7-107">如需描述基礎 DXBC 指示的詳細資訊，請參閱 [gather4](./gather4--sm5---asm-.md) 上的檔。</span><span class="sxs-lookup"><span data-stu-id="6f2d7-107">See the documentation on [gather4](./gather4--sm5---asm-.md) for more information describing the underlying DXBC instruction.</span></span>

### <a name="overload-list"></a><span data-ttu-id="6f2d7-108">多載清單</span><span class="sxs-lookup"><span data-stu-id="6f2d7-108">Overload list</span></span>



| <span data-ttu-id="6f2d7-109">方法</span><span class="sxs-lookup"><span data-stu-id="6f2d7-109">Method</span></span>                                                          | <span data-ttu-id="6f2d7-110">描述</span><span class="sxs-lookup"><span data-stu-id="6f2d7-110">Description</span></span>                                                                                                                                |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f2d7-111">**收集 (S，float)**</span><span class="sxs-lookup"><span data-stu-id="6f2d7-111">**Gather(S,float)**</span></span>](dx-graphics-hlsl-to-gather.md)           | <span data-ttu-id="6f2d7-112">傳回四個材質值的紅色元件， (僅限紅色元件) 將用於雙線性篩選作業。</span><span class="sxs-lookup"><span data-stu-id="6f2d7-112">Returns the red components of four texel values (red component only) that would be used in a bi-linear filtering operation.</span></span> <br/>           |
| [<span data-ttu-id="6f2d7-113">**收集 (S、float、uint)**</span><span class="sxs-lookup"><span data-stu-id="6f2d7-113">**Gather(S,float,uint)**</span></span>](tcubearray-gather-s-float-uint-.md) | <span data-ttu-id="6f2d7-114">傳回四個材質值的紅色元件，這些值會在雙線性篩選作業中使用，以及磚對應狀態。</span><span class="sxs-lookup"><span data-stu-id="6f2d7-114">Returns the red components of four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6f2d7-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f2d7-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f2d7-116">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="6f2d7-116">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

