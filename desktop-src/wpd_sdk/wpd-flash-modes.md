---
description: WPD \_ FLASH \_ 模式列舉類型描述使用裝置來捕捉映射時，所要使用的閃爍模式。
ms.assetid: 4e92c86d-2f35-4bc6-8d37-ec1ab5c518b2
title: 'WPD_FLASH_MODES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FLASH_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 09a2a5b95e86d9d17267cafcfbf723e734ffc74f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977552"
---
# <a name="wpd_flash_modes-enumeration"></a>WPD \_ FLASH \_ 模式列舉

**WPD \_ FLASH \_ 模式** 列舉類型描述使用裝置來捕捉映射時，所要使用的閃爍模式。

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_FLASH_MODES { 
  WPD_FLASH_MODE_UNDEFINED      = 0,
  WPD_FLASH_MODE_AUTO           = 1,
  WPD_FLASH_MODE_OFF            = 2,
  WPD_FLASH_MODE_FILL           = 3,
  WPD_FLASH_MODE_RED_EYE_AUTO   = 4,
  WPD_FLASH_MODE_RED_EYE_FILL   = 5,
  WPD_FLASH_MODE_EXTERNAL_SYNC  = 6
} ;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WPD_FLASH_MODE_UNDEFINED"></span><span id="wpd_flash_mode_undefined"></span>**\_ \_ 未定義 WPD 閃光燈模式 \_**
</dt> <dd>

未指定任何閃爍模式。

</dd> <dt>

<span id="WPD_FLASH_MODE_AUTO"></span><span id="wpd_flash_mode_auto"></span>**\_自動 WPD 閃光燈 \_ 模式 \_**
</dt> <dd>

指定應在自動模式中使用 flash （如裝置所指定）。

</dd> <dt>

<span id="WPD_FLASH_MODE_OFF"></span><span id="wpd_flash_mode_off"></span>**WPD \_ 閃光燈 \_ 模式 \_ 關閉**
</dt> <dd>

指定不應使用任何 flash。

</dd> <dt>

<span id="WPD_FLASH_MODE_FILL"></span><span id="wpd_flash_mode_fill"></span>**WPD \_ 閃光燈 \_ 模式 \_ 填滿**
</dt> <dd>

指定填滿型別 flash。

</dd> <dt>

<span id="WPD_FLASH_MODE_RED_EYE_AUTO"></span><span id="wpd_flash_mode_red_eye_auto"></span>**\_自動 WPD 閃光燈 \_ 模式的 \_ \_ 紅眼 \_**
</dt> <dd>

指定應該使用紅眼降低 flash。

</dd> <dt>

<span id="WPD_FLASH_MODE_RED_EYE_FILL"></span><span id="wpd_flash_mode_red_eye_fill"></span>**WPD \_ 閃光燈 \_ 模式的紅眼 \_ \_ \_ 填滿**
</dt> <dd>

指定應該使用 red 眼睛填滿 flash。

</dd> <dt>

<span id="WPD_FLASH_MODE_EXTERNAL_SYNC"></span><span id="wpd_flash_mode_external_sync"></span>**WPD \_ FLASH \_ 模式 \_ 外部 \_ 同步處理**
</dt> <dd>

指定應該與其他外部 flash 裝置同步 flash。

</dd> </dl>

## <a name="remarks"></a>備註

[WPD \_ 仍然是 \_ IMAGE \_ FLASH \_ 模式](still-image-properties.md)屬性使用此列舉。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構和列舉類型**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




