---
description: WPD \_ 效果 \_ 模式列舉型別描述可套用至影像的各種視覺效果。
ms.assetid: 7624fccb-e416-4db4-978e-410c4c236328
title: 'WPD_EFFECT_MODES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EFFECT_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 7e29f89207a74d335fbe1c2561f8dcf9cec3e923
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993947"
---
# <a name="wpd_effect_modes-enumeration"></a>WPD \_ 效果 \_ 模式列舉

**WPD \_ 效果 \_ 模式** 列舉型別描述可套用至影像的各種視覺效果。

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_EFFECT_MODES { 
  WPD_EFFECT_MODE_UNDEFINED        = 0,
  WPD_EFFECT_MODE_COLOR            = 1,
  WPD_EFFECT_MODE_BLACK_AND_WHITE  = 2,
  WPD_EFFECT_MODE_SEPIA            = 3
} ;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WPD_EFFECT_MODE_UNDEFINED"></span><span id="wpd_effect_mode_undefined"></span>**\_ \_ 未定義 WPD 效果模式 \_**
</dt> <dd>

未指定任何效果。

</dd> <dt>

<span id="WPD_EFFECT_MODE_COLOR"></span><span id="wpd_effect_mode_color"></span>**WPD \_ 效果 \_ 模式 \_ 色彩**
</dt> <dd>

影像應該為色彩。

</dd> <dt>

<span id="WPD_EFFECT_MODE_BLACK_AND_WHITE"></span><span id="wpd_effect_mode_black_and_white"></span>**WPD \_ 效果 \_ 模式 \_ 黑色 \_ 和 \_ 白色**
</dt> <dd>

影像應該是黑色和白色。

</dd> <dt>

<span id="WPD_EFFECT_MODE_SEPIA"></span><span id="wpd_effect_mode_sepia"></span>**WPD \_ 效果 \_ 模式 \_ 棕褐色**
</dt> <dd>

影像應該是棕褐色。

</dd> </dl>

## <a name="remarks"></a>備註

此列舉是由 [ [WPD \_ 仍然 \_ 影像 \_ 效果 \_ 模式]](still-image-properties.md) 屬性所使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構和列舉類型**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




