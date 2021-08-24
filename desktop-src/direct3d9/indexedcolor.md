---
description: 是由索引參數和 RGBA 色彩所組成，用來定義網格頂點色彩。 索引會定義要套用色彩的頂點。
ms.assetid: 63909c54-c2de-4065-9882-58fca2b4e893
title: IndexedColor
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b0dcaf850786a18e5fc317276939436b93c3a49765d520aa40f88cd53707d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563728"
---
# <a name="indexedcolor"></a>IndexedColor

是由索引參數和 RGBA 色彩所組成，用來定義網格頂點色彩。 索引會定義要套用色彩的頂點。

``` syntax
template IndexedColor
{
    < 1630B820-7842-11cf-8F52-0040333594A3 >
    DWORD index;
    ColorRGBA indexColor;
} 
```

其中：

-   index-DWORD。 請參閱上述的說明。
-   indexColor-ColorRGBA 範本。 請參閱 [**ColorRGBA**](colorrgba.md)。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[範本](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



