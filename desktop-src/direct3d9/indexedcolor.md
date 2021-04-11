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

 

 



