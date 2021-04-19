---
description: WPD \_ 裝置 \_ 傳輸列舉型別會指定服務的繼承關聯性。 此列舉是由 WPD \_ 裝置 \_ 傳輸屬性所使用。
ms.assetid: a9d48034-3588-4e48-a03a-91cbe679cbc9
title: 'WPD_DEVICE_TRANSPORTS 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_DEVICE_TRANSPORTS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 574c6b0b00980d110f2374e7426dd101c9122854
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985734"
---
# <a name="wpd_device_transports-enumeration"></a>WPD \_ 裝置 \_ 傳輸列舉

[**WPD \_ 裝置 \_ 傳輸**](/windows/desktop/wpd_sdk/wpd-device-transports)列舉型別會指定服務的繼承關聯性。 此列舉是由 **WPD \_ 裝置 \_ 傳輸** 屬性所使用。

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWPD_DEVICE_TRANSPORTS { 
  WPD_DEVICE_TRANSPORT_UNSPECIFIED  = 0,
  WPD_DEVICE_TRANSPORT_USB          = 1,
  WPD_DEVICE_TRANSPORT_IP           = 2,
  WPD_DEVICE_TRANSPORT_BLUETOOTH    = 3
} WPD_DEVICE_TRANSPORTS;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WPD_DEVICE_TRANSPORT_UNSPECIFIED"></span><span id="wpd_device_transport_unspecified"></span>**\_ \_ 未指定 WPD 裝置傳輸 \_**
</dt> <dd>

未指定傳輸類型。

</dd> <dt>

<span id="WPD_DEVICE_TRANSPORT_USB"></span><span id="wpd_device_transport_usb"></span>**WPD \_ 裝置 \_ 傳輸 \_ USB**
</dt> <dd>

裝置透過 USB 連接。

</dd> <dt>

<span id="WPD_DEVICE_TRANSPORT_IP"></span><span id="wpd_device_transport_ip"></span>**WPD \_ 裝置 \_ 傳輸 \_ IP**
</dt> <dd>

裝置會透過網際網路通訊協定 (IP) 進行連線。

</dd> <dt>

<span id="WPD_DEVICE_TRANSPORT_BLUETOOTH"></span><span id="wpd_device_transport_bluetooth"></span>**WPD \_ 裝置 \_ 傳輸 \_ 藍牙**
</dt> <dd>

裝置透過藍牙連線。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



 

