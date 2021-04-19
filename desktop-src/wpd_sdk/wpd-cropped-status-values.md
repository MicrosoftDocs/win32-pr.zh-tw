---
description: WPD \_ 裁剪的 \_ 狀態值 \_ 列舉型別描述影像的裁剪狀態。
ms.assetid: 7ee87fb7-1d17-4e89-aee7-e7abacbd790d
title: 'WPD_CROPPED_STATUS_VALUES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_CROPPED_STATUS_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3f324fd90e58e486a12bffebde9f844d96c3ed83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982263"
---
# <a name="wpd_cropped_status_values-enumeration"></a>WPD \_ 裁剪的 \_ 狀態值 \_ 列舉

**WPD \_ 裁剪的 \_ 狀態值 \_** 列舉型別描述影像的裁剪狀態。

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_CROPPED_STATUS_VALUES { 
  WPD_CROPPED_STATUS_NOT_CROPPED            = 0,
  WPD_CROPPED_STATUS_CROPPED                = 1,
  WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED  = 2
} ;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WPD_CROPPED_STATUS_NOT_CROPPED"></span><span id="wpd_cropped_status_not_cropped"></span>**\_ \_ \_ 未裁剪的 WPD 裁剪狀態 \_**
</dt> <dd>

尚未裁剪影像。

</dd> <dt>

<span id="WPD_CROPPED_STATUS_CROPPED"></span><span id="wpd_cropped_status_cropped"></span>**裁剪的 WPD \_ 裁剪 \_ 狀態 \_**
</dt> <dd>

影像已裁剪。

</dd> <dt>

<span id="WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED"></span><span id="wpd_cropped_status_should_not_be_cropped"></span>**\_ \_ \_ \_ 不應 \_ \_ 裁剪 WPD 裁剪的狀態**
</dt> <dd>

影像尚未經過，也不應該裁剪。

</dd> </dl>

## <a name="remarks"></a>備註

指出影像的裁剪狀態。 [WPD \_ 影像 \_ 裁剪 \_ 狀態](image-properties.md)屬性會使用這個列舉。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構和列舉類型**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




