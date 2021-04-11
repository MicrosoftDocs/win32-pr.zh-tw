---
description: 定義效果浮點數。 此範本會取代 EffectFloats 範本。
ms.assetid: 7b41d0dc-209f-4ade-a7ed-aa54f421e520
title: EffectParamFloats
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0954ce7679691920c2e104277d12a48f7a34ddf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025673"
---
# <a name="effectparamfloats"></a><span data-ttu-id="423d3-104">EffectParamFloats</span><span class="sxs-lookup"><span data-stu-id="423d3-104">EffectParamFloats</span></span>

<span data-ttu-id="423d3-105">定義效果浮點數。</span><span class="sxs-lookup"><span data-stu-id="423d3-105">Defines effect floating-point numbers.</span></span> <span data-ttu-id="423d3-106">此範本會取代 [**EffectFloats**](effectfloats.md) 範本。</span><span class="sxs-lookup"><span data-stu-id="423d3-106">This template replaces the [**EffectFloats**](effectfloats.md) template.</span></span>

``` syntax
template EffectParamFloats
{
    < 3014B9A0-62F5-478c-9B86-E4AC9F4E418B >
    STRING ParamName;
    DWORD nFloats;
    array float Floats[nFloats];
} 
```

<span data-ttu-id="423d3-107">其中：</span><span class="sxs-lookup"><span data-stu-id="423d3-107">Where:</span></span>

-   <span data-ttu-id="423d3-108">ParamName：浮點數陣列的名稱。</span><span class="sxs-lookup"><span data-stu-id="423d3-108">ParamName - Name of the array of floats.</span></span>
-   <span data-ttu-id="423d3-109">nFloats-陣列中的浮點值數目。</span><span class="sxs-lookup"><span data-stu-id="423d3-109">nFloats - Number of floating-point values in the array.</span></span>
-   <span data-ttu-id="423d3-110">\[ \] 浮點數 nFloats-浮點值的陣列。</span><span class="sxs-lookup"><span data-stu-id="423d3-110">Floats\[nFloats\] - Array of floating-point values.</span></span>

## <a name="see-also"></a><span data-ttu-id="423d3-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="423d3-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="423d3-112">範本</span><span class="sxs-lookup"><span data-stu-id="423d3-112">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



