---
title: ResizeBackgroundImage
description: ResizeBackgroundImage 屬性會指定或抓取值，指出背景影像是否可以調整大小。
ms.assetid: d18f3def-777f-4a71-961e-73bae98a4c64
keywords:
- ResizeBackgroundImage Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.resizeBackgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 397929d69cc6ac6ad51c29883898c153218afdca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106974911"
---
# <a name="viewresizebackgroundimage"></a>ResizeBackgroundImage

**ResizeBackgroundImage** 屬性會指定或抓取值，指出背景影像是否可以調整大小。

``` syntax
        elementID.resizeBackgroundImage
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **布林值**。



| 值 | 描述                                      |
|--------|--------------------------------------------------|
| true   | 背景影像可以調整大小。             |
| false  | 預設值。 背景影像無法調整大小。 |



 

## <a name="remarks"></a>備註

如果您將此屬性設定為 true，背景影像會調整大小以符合 **width** 和 **height** 屬性的目前值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**VIEW 元素**](view-element.md)
</dt> <dt>

[**BackgroundImage**](view-backgroundimage.md)
</dt> </dl>

 

 





