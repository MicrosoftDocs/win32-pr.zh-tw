---
description: WPD \_ 色彩 \_ 更正的 \_ 狀態值 \_ 列舉類型描述影像或影片檔案的色彩更正狀態。
ms.assetid: af129a1b-7760-4339-adf7-3f3c17cebde2
title: 'WPD_COLOR_CORRECTED_STATUS_VALUES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COLOR_CORRECTED_STATUS_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: ec6bfcaa3933bb70c3064f829e701509e3ff32f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981650"
---
# <a name="wpd_color_corrected_status_values-enumeration"></a>WPD \_ 色彩 \_ 更正的 \_ 狀態值 \_ 列舉

**WPD \_ 色彩更正 \_ 的 \_ 狀態值 \_** 列舉類型描述影像或影片檔案的色彩更正狀態。

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_COLOR_CORRECTED_STATUS_VALUES { 
  WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED            = 0,
  WPD_COLOR_CORRECTED_STATUS_CORRECTED                = 1,
  WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED  = 2
} ;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED"></span><span id="wpd_color_corrected_status_not_corrected"></span>**\_ \_ \_ \_ 未更正 WPD 色彩更正 \_ 狀態**
</dt> <dd>

尚未校正影像的色彩。

</dd> <dt>

<span id="WPD_COLOR_CORRECTED_STATUS_CORRECTED"></span><span id="wpd_color_corrected_status_corrected"></span>**已 \_ 更正 WPD 色彩 \_ 更正 \_ 狀態 \_**
</dt> <dd>

影像已經過色彩校正。

</dd> <dt>

<span id="WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED"></span><span id="wpd_color_corrected_status_should_not_be_corrected"></span>**\_ \_ \_ \_ \_ 不應 \_ \_ 更正 WPD 色彩更正狀態**
</dt> <dd>

影像尚未經過修正，因此不應校正色彩。

</dd> </dl>

## <a name="remarks"></a>備註

指出影像的色彩更正狀態。 此列舉是由 [WPD \_ IMAGE \_ COLOR \_ 校正 \_ STATUS](image-properties.md) 屬性所使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構和列舉類型**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




