---
description: Windows 可攜式裝置支援下列 SMS 屬性。
ms.assetid: d821f378-522f-4f0a-825b-6b15295e7b12
title: 'SMS 屬性 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c43917c8c26027713b4e5076e8eb3789b95f08e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978656"
---
# <a name="sms-properties"></a>SMS 屬性

Windows 可攜式裝置支援下列 SMS 屬性。



| 屬性                   | VarType        | Description                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ SMS \_ 編碼**     | **VT \_ LPWSTR** | 值，指定驅動程式將如何編碼用戶端傳送的文字訊息。 這是唯讀屬性;用戶端無法指定裝置用來傳送訊息的編碼類型。 這些值會複製 [**WPD \_ SMS \_ 編碼 \_ 類型**](wpd-sms-encoding-types.md) 的列舉值。 |
| **WPD \_ SMS \_ 最大承載 \_** | **VT \_ UI4**    | 訊息中可包含的最大位元組數目。                                                                                                                                                                                                                                             |
| **WPD \_ SMS \_ 提供者**     | **VT \_ LPWSTR** | 服務提供者的名稱。                                                                                                                                                                                                                                                                                |
| **WPD \_ SMS \_ TIMEOUT**      | **VT \_ UI4**    | 傳回 timeout 之前的毫秒數。                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WPD 屬性和屬性**](properties-and-attributes.md)
</dt> </dl>

 

 




