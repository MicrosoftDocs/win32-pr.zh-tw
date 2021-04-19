---
title: AmbientAttributes. >horizontalalignment
description: '>horizontalalignment 屬性會指定或抓取值，指出調整視圖或父子視圖大小時，控制項的水準位置。'
ms.assetid: 97ca23b9-2046-45ee-b2da-ea388e7ab8d8
keywords:
- AmbientAttributes. >horizontalalignment Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.horizontalAlignment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f946f0d095526c9fc0894cdf0270cbf7cc0c81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994579"
---
# <a name="ambientattributeshorizontalalignment"></a>AmbientAttributes. >horizontalalignment

**>horizontalalignment** 屬性會指定或抓取值，指出調整 **視圖** 或父子 **視圖** 大小時，控制項的水準位置。

``` syntax
        elementID.horizontalAlignment
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **字串**。



| 值   | 描述                                                                                                                                                                                                                                                                                                                                                        |
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| left    | 預設值。 當調整視圖大小時，會維護控制項相對於 **view** 或 parent 子 **視圖左邊** 的位置。                                                                                                                                                                                                                               |
| 向右   | 當調整視圖大小時，會維護控制項相對於 **view** 或 Parent 子 **視圖** 右邊的位置。                                                                                                                                                                                                                                       |
| 中心  | 當調整視圖大小時，會維護控制項相對於 **視圖** 或父子 **視圖** 水準中心的位置。                                                                                                                                                                                                                           |
| Stretch - 自動縮放 | 當調整大小時，會維護控制項相對於 **視圖** 或父子 **視圖** 左右邊界的位置。 當 **視圖** 或子 **視圖** 伸展時，控制項會擴展至適當的大小。 實際的影像除非可以調整大小，否則不會增加或縮小，但如果未受 **clippingImage** 限制，可按一下的區域會擴大或縮小。 |



 

## <a name="remarks"></a>備註

除非 **>horizontalalignment** 設為 "center"，否則控制項會保留其與指定邊緣之間的原始距離，如果指定了 "stretch" 且控制項可以調整大小，則會從兩個邊緣保留原始距離。 如果無法調整控制項的大小，且指定了「延展」，則會改為按一下可按一下的區域。

您可以設定 **>horizontalalignment** 和 **verticalAlignment** 的任何組合。 例如，如果您想要以水準和垂直方式置中控制項，請設定 >horizontalalignment = "center" verticalAlignment = "center"。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**環境屬性**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes. verticalAlignment**](ambientattributes-verticalalignment.md)
</dt> <dt>

[**AmbientAttributes.clippingImage**](ambientattributes-clippingimage.md)
</dt> </dl>

 

 





