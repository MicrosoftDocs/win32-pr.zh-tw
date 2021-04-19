---
description: 描述傳遞至 WFD \_ 顯示 \_ 接收 \_ 通知回呼函式的通知 \_ 。
ms.assetid: 1CB91DD9-5B58-4FE0-B7B0-E6189760511A
title: 'WFD_DISPLAY_SINK_NOTIFICATION 結構 (Wfdsink .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: d4c2a15bbe6ef0df62fc0d607c97ecb3a2b54ec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981558"
---
# <a name="wfd_display_sink_notification-structure"></a>WFD \_ 顯示 \_ 接收 \_ 通知結構

[ **Wfd \_ 顯示 \_ 接收] \_ 通知** 結構描述傳遞至 [ [**wfd \_ 顯示接收] \_ \_ 通知 \_ 回檔**](wfd-display-sink-notification-callback.md) 函式的通知。

## <a name="syntax"></a>語法


```C++
typedef struct _WFD_DISPLAY_SINK_NOTIFICATION {
  WFD_DISPLAY_SINK_OBJECT_HEADER     Header;
  WFD_DISPLAY_SINK_NOTIFICATION_TYPE type;
  WCHAR                              strRemoteDeviceName[WFD_SINK_MAX_DEVICE_NAME_LENGTH + 1];
  DOT11_MAC_ADDRESS                  RemoteDeviceAddress;
  union {
    struct {
      HANDLE                  hSessionHandle;
      DOT11_WPS_CONFIG_METHOD PossibleConfigMethods;
    } ProvisioningRequestInfo;
    struct {
      DOT11_WFD_GROUP_ID GroupID;
    } ReconnectRequestInfo;
    struct {
      HANDLE             hSessionHandle;
      GUID               guidSessionInterface;
      DOT11_WFD_GROUP_ID GroupID;
      PWSTR              strProfile;
      SOCKADDR_STORAGE   LocalAddress;
      SOCKADDR_STORAGE   RemoteAddress;
      USHORT             uRTSPPort;
    } ConnectedInfo;
  };
} WFD_DISPLAY_SINK_NOTIFICATION, *PWFD_DISPLAY_SINK_NOTIFICATION;
```



## <a name="members"></a>成員

<dl> <dt>

**標頭**
</dt> <dd>

可描述通知中所含資料的 [**WFD \_ 顯示 \_ 接收器 \_ 物件 \_ 標頭**](wfd-display-sink-object-header.md) 。

</dd> <dt>

**type**
</dt> <dd>

指出通知類型的 [ [**WFD \_ 顯示 \_ 接收] \_ 通知 \_ 類型**](wfd-display-sink-notification-type.md) 值。 此參數也會決定要在下聯集內使用的資訊。

</dd> <dt>

**strRemoteDeviceName**
</dt> <dd>

包含以 Null 終止的字串，其中包含遠端裝置的名稱。 [WFD \_ 接收器 \_ 最大 \_ 裝置 \_ 名稱長度] \_ 定義為 (32) 的值。

</dd> <dt>

**RemoteDeviceAddress**
</dt> <dd>

[**DOT11 \_ MAC \_ 位址**](dot11-mac-address-type.md)，其中包含遠端裝置的 BSSID。

</dd> <dt>

**ProvisioningRequestInfo**
</dt> <dd>

布建要求的相關資訊。 如果 *類型* 具有值 **ProvisioningRequestNotification**，請使用此值。

<dl> <dt>

**hSessionHandle**
</dt> <dd>

會話控制碼。

</dd> <dt>

**PossibleConfigMethods**
</dt> <dd>

顯示 UI 以進行互動式接受的可能方法。

</dd> </dl> </dd> <dt>

**ReconnectRequestInfo**
</dt> <dd>

重新連接要求的相關資訊。 如果 *類型* 具有值 **ReconnectRequestNotification**，請使用此值。

<dl> <dt>

**GroupID**
</dt> <dd>

群組識別碼。

</dd> </dl> </dd> <dt>

**ConnectedInfo**
</dt> <dd>

連線通知的相關資訊。 如果 *類型* 具有值 **ConnectedNotification**，請使用此值。

<dl> <dt>

**hSessionHandle**
</dt> <dd>

會話控制碼。

</dd> <dt>

**guidSessionInterface**
</dt> <dd>

指出會話介面的 GUID。

</dd> <dt>

**GroupID**
</dt> <dd>

群組識別碼。

</dd> <dt>

**strProfile**
</dt> <dd>

描述設定檔之以 Null 結束的字串指標。

</dd> <dt>

**LocalAddress**
</dt> <dd>

本機位址。

</dd> <dt>

**RemoteAddress**
</dt> <dd>

遠端位址。

</dd> <dt>

**uRTSPPort**
</dt> <dd>

RTSP 埠。

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Wfdsink。h</dt> </dl> |



 

 




