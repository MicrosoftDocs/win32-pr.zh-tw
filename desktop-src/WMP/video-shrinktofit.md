---
title: ShrinkToFit
description: ShrinkToFit 屬性會指定或抓取值，指出影片是否會壓縮成針對影片控制項定義的寬度和高度。
ms.assetid: 94ab33b0-b08c-4063-a3e6-1315bb527e1c
keywords:
- ShrinkToFit Windows Media Player
topic_type:
- apiref
api_name:
- VIDEO.shrinkToFit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 186c43ce664f4da5490168232310a9e4cd640651a035a16097c8875d74270b2e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465658"
---
# <a name="videoshrinktofit"></a>ShrinkToFit

**ShrinkToFit** 屬性會指定或抓取值，指出影片是否會壓縮成針對影片控制項定義的寬度和高度。

``` syntax
        elementID.shrinkToFit
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **布林值**。



| 值 | 描述                                        |
|-------|----------------------------------------------------|
| true  | 預設值。 影片將會縮小以符合控制項。 |
| false | 影片將不會縮小以容納控制項。      |



 

## <a name="remarks"></a>備註

如果未指定寬度或高度，則會忽略這個屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**影片元素**](video-element.md)
</dt> </dl>

 

 





