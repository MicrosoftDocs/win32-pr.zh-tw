---
description: WPD \_ 焦點 \_ 模式列舉類型會說明靜止影像捕獲裝置所使用的焦點模式。
ms.assetid: 3b092391-e4c1-4586-8df4-b58a1dcccc81
title: 'WPD_FOCUS_MODES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FOCUS_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e7e1dc50f115fbd2ace84a3b631d37a42e1c4ba7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994740"
---
# <a name="wpd_focus_modes-enumeration"></a>WPD \_ 焦點 \_ 模式列舉

**WPD \_ 焦點 \_ 模式** 列舉類型會說明靜止影像捕獲裝置所使用的焦點模式。

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_FOCUS_MODES { 
  WPD_FOCUS_UNDEFINED        = 0,
  WPD_FOCUS_MANUAL           = 1,
  WPD_FOCUS_AUTOMATIC        = 2,
  WPD_FOCUS_AUTOMATIC_MACRO  = 3
} ;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WPD_FOCUS_UNDEFINED"></span><span id="wpd_focus_undefined"></span>**\_ \_ 未定義 WPD 焦點**
</dt> <dd>

尚未指定焦點模式。

</dd> <dt>

<span id="WPD_FOCUS_MANUAL"></span><span id="wpd_focus_manual"></span>**WPD \_ 焦點 \_ 手冊**
</dt> <dd>

指定手動焦點。

</dd> <dt>

<span id="WPD_FOCUS_AUTOMATIC"></span><span id="wpd_focus_automatic"></span>**\_自動 WPD 焦點 \_**
</dt> <dd>

指定由裝置控制的自動焦點。

</dd> <dt>

<span id="WPD_FOCUS_AUTOMATIC_MACRO"></span><span id="wpd_focus_automatic_macro"></span>**WPD \_ 焦點 \_ 自動 \_ 宏**
</dt> <dd>

指定裝置應該視需要自動切換宏和一般焦點。

</dd> </dl>

## <a name="remarks"></a>備註

[WPD \_ 仍 \_ 影像 \_ 焦點 \_ 模式](still-image-properties.md)屬性會使用這個列舉。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構和列舉類型**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




