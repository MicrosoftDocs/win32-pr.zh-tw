---
title: AmbientAttributes. verticalAlignment
description: VerticalAlignment 屬性會指定或抓取值，指出當視圖或父子視圖伸展時，控制項的垂直位置。
ms.assetid: 08ef483a-58ee-4a35-9973-2567076d07f7
keywords:
- AmbientAttributes. verticalAlignment Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.verticalAlignment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88de2f5f54b95b14827fabb2bafb89ff6974966b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996458"
---
# <a name="ambientattributesverticalalignment"></a>AmbientAttributes. verticalAlignment

**VerticalAlignment** 屬性會指定或抓取值，指出當 **視圖** 或父子 **視圖** 伸展時，控制項的垂直位置。

``` syntax
        elementID.verticalAlignment
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **字串**。



| 值   | 描述                                                                                                                                                                                                                                                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| top     | 預設值。 當調整視圖大小時，會維護控制項相對於 **view** 或 parent 子 **視圖頂端** 的位置。                                                                                                                                                                                                             |
| 下  | 當調整視圖大小時，會維護控制項相對於 **視圖** 或父子 **視圖** 底部的位置。                                                                                                                                                                                                                   |
| 中心  | 當調整視圖大小時，會維護控制項相對於 **view** 或 parent **子視圖垂直** 中心的位置。                                                                                                                                                                                                          |
| Stretch - 自動縮放 | 將控制項的放置位置維持在調整大小時，相對於視圖的上邊界和下邊界。 當 **視圖** 或父項子 **視圖** 伸展時，控制項會延展到適當的大小。 實際的影像除非可以調整大小，否則不會增加或縮小，但如果未受 **clippingImage** 限制，可按一下的區域會擴大或縮小。 |



 

## <a name="remarks"></a>備註

除非 **verticalAlignment** 設為 "center"，否則控制項會保留其與指定邊緣之間的原始距離，如果指定了 "stretch" 且控制項可以調整大小，則會從兩個邊緣保留原始距離。 如果無法調整控制項的大小，且指定了「延展」，則會改為按一下可按一下的區域。

您可以設定 **>horizontalalignment** 和 **verticalAlignment** 屬性的任何組合。 例如，如果您想要以水準和垂直方式置中控制項，請將 **>horizontalalignment** 設定為 "center"，並將 **verticalAlignment** 設為 "center"。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**環境屬性**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes. >horizontalalignment**](ambientattributes-horizontalalignment.md)
</dt> </dl>

 

 





