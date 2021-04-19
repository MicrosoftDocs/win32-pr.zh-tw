---
title: AmbientAttributes 高度
description: Height 屬性會指定或抓取控制項的高度。
ms.assetid: a5c85d86-15d4-451d-b8bc-ed3b6e0dfd7d
keywords:
- AmbientAttributes 高度 Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.height
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 662268bfeaf00b3185d531ff10d8dd17c9127a66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999661"
---
# <a name="ambientattributesheight"></a>AmbientAttributes 高度

**Height** 屬性會指定或抓取控制項的高度。

``` syntax
        elementID.height
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **號碼** (**long**) 代表控制項的高度（以圖元為單位）。 預設值為零或控制項 **影像** 屬性中所指定影像的高度。

## <a name="remarks"></a>備註

如果指定的高度小於所提供影像的高度，則會裁剪影像。 如果高度大於影像的高度，則按一下區域會超出影像界限。 無論這個屬性的值為何，影像都不能成長到其父視圖 **或子****視圖** 之外。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**環境屬性**](ambient-attributes.md)
</dt> </dl>

 

 





