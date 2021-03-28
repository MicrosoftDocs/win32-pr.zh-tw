---
title: TextureCube：： TextureCube 收集方法
description: 傳回要在雙線性篩選作業中使用的四個材質值。 |TextureCube：： TextureCube 收集方法
ms.assetid: 4891A62A-9D54-4F7E-92C2-9CDDF1453671
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
ms.openlocfilehash: ce58acc01ef87e6d53d829a5c84e7c9c0ff6afb9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974097"
---
# <a name="texturecubegather-methods"></a><span data-ttu-id="b69c7-105">TextureCube：：收集方法</span><span class="sxs-lookup"><span data-stu-id="b69c7-105">TextureCube::Gather methods</span></span>

<span data-ttu-id="b69c7-106">傳回要在雙線性篩選作業中使用的四個材質值。</span><span class="sxs-lookup"><span data-stu-id="b69c7-106">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>

<span data-ttu-id="b69c7-107">如需描述基礎 DXBC 指示的詳細資訊，請參閱 [gather4](./gather4--sm5---asm-.md) 上的檔。</span><span class="sxs-lookup"><span data-stu-id="b69c7-107">See the documentation on [gather4](./gather4--sm5---asm-.md) for more information describing the underlying DXBC instruction.</span></span>

### <a name="overload-list"></a><span data-ttu-id="b69c7-108">多載清單</span><span class="sxs-lookup"><span data-stu-id="b69c7-108">Overload list</span></span>



| <span data-ttu-id="b69c7-109">方法</span><span class="sxs-lookup"><span data-stu-id="b69c7-109">Method</span></span>                                                     | <span data-ttu-id="b69c7-110">描述</span><span class="sxs-lookup"><span data-stu-id="b69c7-110">Description</span></span>                                                                                                              |
|:-----------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b69c7-111">**收集 (S，float)**</span><span class="sxs-lookup"><span data-stu-id="b69c7-111">**Gather(S,float)**</span></span>](dx-graphics-hlsl-to-gather.md)      | <span data-ttu-id="b69c7-112">將材質取樣，並傳回四個樣本 (紅色元件僅) 用於雙線性插補。</span><span class="sxs-lookup"><span data-stu-id="b69c7-112">Samples a texture and returns the four samples (red component only) that are used for bilinear interpolation.</span></span><br/> |
| [<span data-ttu-id="b69c7-113">**收集 (S、float、uint)**</span><span class="sxs-lookup"><span data-stu-id="b69c7-113">**Gather(S,float,uint)**</span></span>](tcube-gather-s-float-uint-.md) | <span data-ttu-id="b69c7-114">取樣材質，並傳回所有四個元件以及作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="b69c7-114">Samples a texture and returns all four components along with status about the operation.</span></span><br/>                      |



## <a name="see-also"></a><span data-ttu-id="b69c7-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b69c7-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b69c7-116">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="b69c7-116">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

