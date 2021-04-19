---
title: AmbientAttributes 寬度
description: Width 屬性會指定或抓取控制項的寬度。
ms.assetid: f246958a-563c-40c0-8a74-4511103b95b2
keywords:
- AmbientAttributes width Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.width
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c3f91ee47277dc511d54747197edfa44e80e251
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992827"
---
# <a name="ambientattributeswidth"></a>AmbientAttributes 寬度

**Width** 屬性會指定或抓取控制項的寬度。

``` syntax
        elementID.width
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入的16位 **整數** (0 到 32767) 代表控制項的寬度（以圖元為單位）。 預設值為零或控制項 **影像** 屬性中所指定影像的寬度。

## <a name="remarks"></a>備註

如果指定的寬度比提供的影像寬度窄，則會裁剪影像。 如果寬度超過影像的寬度，則按一下區域將會超出影像界限。 無論這個屬性的值為何，影像都不能成長到其父視圖 **或子****視圖** 之外。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**環境屬性**](ambient-attributes.md)
</dt> </dl>

 

 





