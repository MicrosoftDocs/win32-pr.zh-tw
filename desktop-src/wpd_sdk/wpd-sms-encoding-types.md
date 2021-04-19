---
description: WPD \_ sms \_ 編碼 \_ 類型列舉類型會描述短訊息服務 (SMS) 訊息的編碼類型。
ms.assetid: 5a9752e5-4e09-42a4-8fed-b4ea551fa36f
title: 'WPD_SMS_ENCODING_TYPES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_SMS_ENCODING_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: f7deae3cdc560e27e19b5ff7664e5566cff6d7e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994836"
---
# <a name="wpd_sms_encoding_types-enumeration"></a>WPD \_ SMS \_ 編碼 \_ 類型列舉

**WPD \_ sms \_ 編碼 \_ 類型** 列舉類型會描述短訊息服務 (SMS) 訊息的編碼類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_SMS_ENCODING_TYPES { 
  SMS_ENCODING_7_BIT   = 0,
  SMS_ENCODING_8_BIT   = 1,
  SMS_ENCODING_UTF_16  = 2
} ;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="SMS_ENCODING_7_BIT"></span><span id="sms_encoding_7_bit"></span>**SMS \_ 編碼 \_ 7 \_ 位**
</dt> <dd>

七位編碼。

</dd> <dt>

<span id="SMS_ENCODING_8_BIT"></span><span id="sms_encoding_8_bit"></span>**SMS \_ 編碼 \_ 8 \_ 位**
</dt> <dd>

八位編碼。

</dd> <dt>

<span id="SMS_ENCODING_UTF_16"></span><span id="sms_encoding_utf_16"></span>**SMS \_ 編碼 \_ utf-16 \_**
</dt> <dd>

 (UTF) 的十六位編碼。

</dd> </dl>

## <a name="remarks"></a>備註

此列舉是由 [WPD \_ SMS \_ ENCODING](sms-properties.md) 屬性所使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構和列舉類型**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




