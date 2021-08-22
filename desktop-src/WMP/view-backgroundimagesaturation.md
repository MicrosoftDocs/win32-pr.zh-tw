---
title: BackgroundImageSaturation
description: BackgroundImageSaturation 屬性會指定或抓取背景影像的飽和度值。
ms.assetid: 9e1f205b-6366-4816-9430-1153f57d686c
keywords:
- BackgroundImageSaturation Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.backgroundImageSaturation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 934c10ee090f99d456c38a5eb56512d3adb9b748d45b166167b49f3249d819e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119506858"
---
# <a name="viewbackgroundimagesaturation"></a>BackgroundImageSaturation

**BackgroundImageSaturation** 屬性會指定或抓取背景影像的飽和度值。

``` syntax
        elementID.backgroundImageSaturation
```

## <a name="possible-values"></a>可能的值

這個屬性是一個讀/寫 **編號** (**float**) ，其值範圍從0.0 到2.0，預設值為1.0。

## <a name="remarks"></a>備註

這個屬性會變更 **backgroundImage** 屬性所指定之影像的飽和度值（如果已指定），而且它是指8位的 BMP 影像。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**VIEW 元素**](view-element.md)
</dt> <dt>

[**BackgroundImage**](view-backgroundimage.md)
</dt> <dt>

[**BackgroundImageHueShift**](view-backgroundimagehueshift.md)
</dt> </dl>

 

 





