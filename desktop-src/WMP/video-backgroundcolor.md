---
title: BackgroundColor
description: BackgroundColor 屬性會指定或抓取影片控制項的背景色彩。
ms.assetid: 7acf7dc8-80c3-4620-ad89-4c8de20d17ee
keywords:
- BackgroundColor Windows Media Player
topic_type:
- apiref
api_name:
- VIDEO.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41b5e4f637aa4d15aa9496eb85ee0b60a103ed4db33185e8434b8409173da298
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118830257"
---
# <a name="videobackgroundcolor"></a>BackgroundColor

**BackgroundColor** 屬性會指定或抓取影片控制項的背景色彩。

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a>可能的值

這個屬性是包含任何 Microsoft Internet Explorer 色彩值或值為 "none" 的讀取/寫入 **字串** 。 預設值為 "none"，這表示如果沒有影片與影片控制項相關聯的影片，則影片控制項是透明的，而背景會顯示。

## <a name="remarks"></a>備註

當影片小於視窗而 **stretchToFit** 為 false 時，背景色彩會顯示在影片周圍。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**色彩參考**](color-reference.md)
</dt> <dt>

[**影片元素**](video-element.md)
</dt> <dt>

[**StretchToFit**](video-stretchtofit.md)
</dt> </dl>

 

 





