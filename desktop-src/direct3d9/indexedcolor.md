---
description: 是由索引參數和 RGBA 色彩所組成，用來定義網格頂點色彩。 索引會定義要套用色彩的頂點。
ms.assetid: 63909c54-c2de-4065-9882-58fca2b4e893
title: IndexedColor
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c895cf56efedfa7214bcfa6acafd32ab9324bbe8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317659"
---
# <a name="indexedcolor"></a><span data-ttu-id="6f772-104">IndexedColor</span><span class="sxs-lookup"><span data-stu-id="6f772-104">IndexedColor</span></span>

<span data-ttu-id="6f772-105">是由索引參數和 RGBA 色彩所組成，用來定義網格頂點色彩。</span><span class="sxs-lookup"><span data-stu-id="6f772-105">Consists of an index parameter and an RGBA color and is used for defining mesh vertex colors.</span></span> <span data-ttu-id="6f772-106">索引會定義要套用色彩的頂點。</span><span class="sxs-lookup"><span data-stu-id="6f772-106">The index defines the vertex to which the color is applied.</span></span>

``` syntax
template IndexedColor
{
    < 1630B820-7842-11cf-8F52-0040333594A3 >
    DWORD index;
    ColorRGBA indexColor;
} 
```

<span data-ttu-id="6f772-107">其中：</span><span class="sxs-lookup"><span data-stu-id="6f772-107">Where:</span></span>

-   <span data-ttu-id="6f772-108">index-DWORD。</span><span class="sxs-lookup"><span data-stu-id="6f772-108">index - A DWORD.</span></span> <span data-ttu-id="6f772-109">請參閱上述的說明。</span><span class="sxs-lookup"><span data-stu-id="6f772-109">See the description above.</span></span>
-   <span data-ttu-id="6f772-110">indexColor-ColorRGBA 範本。</span><span class="sxs-lookup"><span data-stu-id="6f772-110">indexColor - A ColorRGBA template.</span></span> <span data-ttu-id="6f772-111">請參閱 [**ColorRGBA**](colorrgba.md)。</span><span class="sxs-lookup"><span data-stu-id="6f772-111">See [**ColorRGBA**](colorrgba.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="6f772-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f772-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f772-113">範本</span><span class="sxs-lookup"><span data-stu-id="6f772-113">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



