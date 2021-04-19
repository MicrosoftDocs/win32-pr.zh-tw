---
description: 定義一組兩個布林值，用於 MeshFaceWraps 範本以定義個別臉部的材質拓撲。 當材質座標 (u，v) 範圍介於0到2（而不是0到1）時，請使用而不是 Boolean2d。
ms.assetid: 0d1755fc-66cb-4372-b9d0-fb320c55d6a7
title: MaterialWrap
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6797719919a4f52421751a5cad008aa8a581089a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972737"
---
# <a name="materialwrap"></a><span data-ttu-id="5b130-104">MaterialWrap</span><span class="sxs-lookup"><span data-stu-id="5b130-104">MaterialWrap</span></span>

<span data-ttu-id="5b130-105">定義一組兩個布林值，用於 [**MeshFaceWraps**](meshfacewraps.md) 範本以定義個別臉部的材質拓撲。</span><span class="sxs-lookup"><span data-stu-id="5b130-105">Defines a set of two Boolean values used in the [**MeshFaceWraps**](meshfacewraps.md) template to define the texture topology of an individual face.</span></span> <span data-ttu-id="5b130-106">當材質座標 (u，v) 範圍介於0到2（而不是0到1）時，請使用而不是 [**Boolean2d**](boolean2d.md) 。</span><span class="sxs-lookup"><span data-stu-id="5b130-106">Use instead of [**Boolean2d**](boolean2d.md) when the texture coordinates (u, v) span the range of 0 to 2 instead of 0 to 1.</span></span>

``` syntax
template MaterialWrap
{
    < 4885ae60-78e8-11cf-8f52-0040333594a3 >
    Boolean u;
    Boolean v;
} 
```

<span data-ttu-id="5b130-107">其中：</span><span class="sxs-lookup"><span data-stu-id="5b130-107">Where:</span></span>

-   <span data-ttu-id="5b130-108">u-布林值。</span><span class="sxs-lookup"><span data-stu-id="5b130-108">u - Boolean value.</span></span> <span data-ttu-id="5b130-109">請參閱 [**布林值**](boolean.md)。</span><span class="sxs-lookup"><span data-stu-id="5b130-109">See [**Boolean**](boolean.md).</span></span>
-   <span data-ttu-id="5b130-110">v 布林值。</span><span class="sxs-lookup"><span data-stu-id="5b130-110">v - Boolean value.</span></span> <span data-ttu-id="5b130-111">請參閱 [**布林值**](boolean.md)。</span><span class="sxs-lookup"><span data-stu-id="5b130-111">See [**Boolean**](boolean.md).</span></span>

> [!Note]  
> <span data-ttu-id="5b130-112">不再使用 [**MeshFaceWraps**](meshfacewraps.md) 範本。</span><span class="sxs-lookup"><span data-stu-id="5b130-112">The [**MeshFaceWraps**](meshfacewraps.md) template is no longer used.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="5b130-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b130-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b130-114">範本</span><span class="sxs-lookup"><span data-stu-id="5b130-114">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



