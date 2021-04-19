---
description: SMS \_ 訊息 \_ 類型列舉類型會描述短訊息服務的內容類型 (SMS) 訊息。
ms.assetid: 882886a6-ecce-443f-a7e9-2e4e367ad804
title: 'SMS_MESSAGE_TYPES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMS_MESSAGE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: a2e1ccfd074ff1f5287af22c5a8ebb3c6b3c661d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977658"
---
# <a name="sms_message_types-enumeration"></a>SMS \_ 訊息 \_ 類型列舉

**Sms \_ 訊息 \_ 類型** 列舉類型會描述短訊息服務的內容類型 (SMS) 訊息。

## <a name="syntax"></a>Syntax


```C++
typedef enum SMS_MESSAGE_TYPES { 
  SMS_TEXT_MESSAGE    = 0,
  SMS_BINARY_MESSAGE  = 1
} ;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="SMS_TEXT_MESSAGE"></span><span id="sms_text_message"></span>**SMS \_ 文字 \_ 訊息**
</dt> <dd>

文字訊息。

</dd> <dt>

<span id="SMS_BINARY_MESSAGE"></span><span id="sms_binary_message"></span>**SMS \_ 二進位 \_ 訊息**
</dt> <dd>

二進位訊息。

</dd> </dl>

## <a name="remarks"></a>備註

[**WPD \_ 命令 \_ SMS \_ SEND 命令**](wpd-command-sms-send-command.md)會使用這個列舉。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構和列舉類型**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




