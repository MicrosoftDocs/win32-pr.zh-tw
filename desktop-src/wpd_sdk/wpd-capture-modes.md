---
description: WPD \_ CAPTURE \_ 模式列舉型別描述靜止影像捕捉的「捕捉計時模式」。
ms.assetid: bfe96176-d018-4b39-a938-035757111784
title: 'WPD_CAPTURE_MODES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_CAPTURE_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e56e3e66cd20abaeb1daf0a674633a36b57a9575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984007"
---
# <a name="wpd_capture_modes-enumeration"></a>WPD \_ CAPTURE \_ 模式列舉

**WPD \_ CAPTURE \_ 模式** 列舉型別描述靜止影像捕捉的「捕捉計時模式」。

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_CAPTURE_MODES { 
  WPD_CAPTURE_MODE_UNDEFINED  = 0,
  WPD_CAPTURE_MODE_NORMAL     = 1,
  WPD_CAPTURE_MODE_BURST      = 2,
  WPD_CAPTURE_MODE_TIMELAPSE  = 3
} ;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WPD_CAPTURE_MODE_UNDEFINED"></span><span id="wpd_capture_mode_undefined"></span>**WPD \_ 捕捉 \_ 模式 \_ 未定義**
</dt> <dd>

尚未定義 capture 模式。

</dd> <dt>

<span id="WPD_CAPTURE_MODE_NORMAL"></span><span id="wpd_capture_mode_normal"></span>**WPD \_ CAPTURE \_ 模式 \_ 正常**
</dt> <dd>

不應使用延遲或高載模式。

</dd> <dt>

<span id="WPD_CAPTURE_MODE_BURST"></span><span id="wpd_capture_mode_burst"></span>**WPD \_ CAPTURE \_ 模式高載 \_**
</dt> <dd>

指定應以定義的間隔來捕捉定義的影像數目。 要捕捉的映射數目以及兩者之間的時間延遲，是由 [WPD \_ 仍為 \_ 影像 \_ \_ ](still-image-properties.md) 高載數目和 [WPD 仍為影像高載 \_ \_ \_ \_ 間隔](still-image-properties.md) 屬性所指定。

</dd> <dt>

<span id="WPD_CAPTURE_MODE_TIMELAPSE"></span><span id="wpd_capture_mode_timelapse"></span>**WPD \_ CAPTURE \_ 模式 \_ TIMELAPSE**
</dt> <dd>

影像捕捉應使用時間間隔攝影。 [WPD \_ 仍 \_ 影像 \_ TIMELAPSE \_ 號碼](still-image-properties.md)和[WPD \_ 仍是 \_ 影像 \_ TIMELAPSE \_ 間隔](still-image-properties.md)屬性描述的影像和間隔數目。

</dd> </dl>

## <a name="remarks"></a>備註

[WPD \_ 仍然是 \_ 影像 \_ 捕捉 \_ 模式](still-image-properties.md)屬性使用此列舉。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WPD 屬性和屬性**](properties-and-attributes.md)
</dt> <dt>

[**結構和列舉類型**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




