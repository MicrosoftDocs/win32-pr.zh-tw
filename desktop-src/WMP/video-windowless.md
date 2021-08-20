---
title: VIDEO。無視窗
description: 無視窗屬性會指定或抓取值，指出影片控制項是否為視窗化或無視窗;也就是說，控制項的整個矩形是否隨時都可以看見，或是可以裁剪。
ms.assetid: d59e6baf-374b-48f6-b99f-35a83af7feb6
keywords:
- VIDEO：無視窗 Windows Media Player
topic_type:
- apiref
api_name:
- VIDEO.windowless
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c98aefde5aab9837f220ccb7df254e6a592e0d5e9d41de43291b2ab73e287321
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117931738"
---
# <a name="videowindowless"></a>VIDEO。無視窗

**無視窗** 屬性會指定或抓取值，指出影片控制項是否為視窗化或無視窗;也就是說，控制項的整個矩形是否隨時都可以看見，或是可以裁剪。 只能在設計階段設定。

``` syntax
        elementID.windowless
```

## <a name="possible-values"></a>可能的值

這個屬性是在設計階段指定的 **布林值** ，之後是唯讀的。



| 值 | 描述                              |
|-------|------------------------------------------|
| true  | 影片控制項將會是無視窗的。        |
| false | 預設值。 影片控制項將會是視窗化。 |



 

## <a name="remarks"></a>備註

如果需要非矩形的影片視窗，或您想要使用影像來涵蓋影片視窗的任何部分，則必須將此屬性設定為 true。 這會犧牲一些執行必要裁剪的效能。

影片播放已針對播放裁剪進行優化。 在此情況下， **無視窗** 屬性會設定為 false，且一律會顯示整個影片矩形。 會忽略涵蓋影片視窗的任何影像，而影片視窗具有最高層級的迭置順序。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**影片元素**](video-element.md)
</dt> </dl>

 

 





