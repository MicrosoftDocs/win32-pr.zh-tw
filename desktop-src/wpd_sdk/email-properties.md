---
description: Windows 可攜式裝置支援下列電子郵件屬性。
ms.assetid: c886622e-57e7-4bd1-b645-0e979ee7b66a
title: '電子郵件屬性 (PortableDevice) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Email
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: de25d73e9fb331538ecdbf5f22306d85c282b338
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985569"
---
# <a name="email-properties"></a>電子郵件屬性

Windows 可攜式裝置支援下列電子郵件屬性。



| 屬性                         | VarType        | Description                                                                                                                               |
|----------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ 電子郵件 \_ 密件副本 \_ 行**        | **VT \_ LPWSTR** | 電子郵件訊息的密件副本收件者。 密件副本收件者會收到電子郵件的副本，但其名稱不會顯示為收件者。   |
| **WPD \_ 電子郵件 \_ 抄送 \_ 行**         | **VT \_ LPWSTR** | 電子郵件訊息的抄送收件者。 CC 收件者會收到一份電子郵件訊息，而其名稱會顯示為收件者。 |
| **WPD \_ 電子郵件 \_ 有 \_ 附件** | **VT \_ BOOL**   | 布林值，指定此電子郵件訊息是否有附件。                                                               |
| **已 \_ 閱讀 WPD 電子郵件 \_ \_ \_**  | **VT \_ BOOL**   | 指定是否已讀取此電子郵件訊息的布林值。                                                                 |
| **WPD \_ 電子郵件 \_ 收到 \_ 時間**   | **VT \_ 日期**   | 值，指定接收電子郵件訊息的時間。                                                                              |
| **WPD \_ 電子郵件 \_ 寄件者 \_ 位址**  | **VT \_ LPWSTR** | 寄件者的電子郵件地址。                                                                                                         |
| **WPD \_ 電子郵件 \_ 到 \_ 行**         | **VT \_ LPWSTR** | 電子郵件訊息的主要收件者。                                                                                                |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WPD 屬性和屬性**](properties-and-attributes.md)
</dt> </dl>

 

 




