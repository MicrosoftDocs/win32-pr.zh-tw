---
description: WPD \_ 焦點 \_ 計量 \_ 模式列舉類型會說明裝置應該如何決定要使用的框架部分來設定焦點。
ms.assetid: 0e68d0e8-2ce3-4994-99c2-2ff2293d8a20
title: 'WPD_FOCUS_METERING_MODES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FOCUS_METERING_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: eb37cdd32673c385617d9c0c0ae8616c8dae0ab711d1253391ae2c1e6b2f8789
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703768"
---
# <a name="wpd_focus_metering_modes-enumeration"></a>WPD \_ 焦點 \_ 計量 \_ 模式列舉

**WPD \_ 焦點 \_ 計量 \_ 模式** 列舉類型會說明裝置應該如何決定要使用的框架部分來設定焦點。

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_FOCUS_METERING_MODES { 
  WPD_FOCUS_METERING_MODE_UNDEFINED    = 0,
  WPD_FOCUS_METERING_MODE_CENTER_SPOT  = 1,
  WPD_FOCUS_METERING_MODE_MULTI_SPOT   = 2
} ;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WPD_FOCUS_METERING_MODE_UNDEFINED"></span><span id="wpd_focus_metering_mode_undefined"></span>**\_未定義 WPD 焦點 \_ 計量 \_ 模式 \_**
</dt> <dd>

指出未指定任何焦點模式。

</dd> <dt>

<span id="WPD_FOCUS_METERING_MODE_CENTER_SPOT"></span><span id="wpd_focus_metering_mode_center_spot"></span>**WPD \_ 焦點 \_ 計量 \_ 模式 \_ 中心 \_ 點**
</dt> <dd>

將焦點放在框架區域的中央。

</dd> <dt>

<span id="WPD_FOCUS_METERING_MODE_MULTI_SPOT"></span><span id="wpd_focus_metering_mode_multi_spot"></span>**WPD \_ 焦點 \_ 計量 \_ 模式 \_ 多 \_ 點**
</dt> <dd>

藉由分析框架區域的多個部分來決定焦點。

</dd> </dl>

## <a name="remarks"></a>備註

此列舉是由 [ [WPD \_ 靜止 \_ 影像 \_ 焦點 \_ ] 計量 \_ 模式](still-image-properties.md) 屬性指定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構和列舉類型**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




