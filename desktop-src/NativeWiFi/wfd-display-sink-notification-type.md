---
description: 定義傳遞至 WFD \_ 顯示 \_ 接收 \_ 通知回呼函式的通知類型 \_ 。
ms.assetid: C0AFF80E-A4D2-4FF1-B111-D628AF8755A8
title: 'WFD_DISPLAY_SINK_NOTIFICATION_TYPE 列舉 (Wfdsink .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION_TYPE
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: 25361b0f3529da0293f373117c7bf655635de852
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971780"
---
# <a name="wfd_display_sink_notification_type-enumeration"></a>WFD \_ 顯示 \_ 接收 \_ 通知 \_ 類型列舉

[ **Wfd \_ 顯示 \_ 接收 \_ 通知 \_ 類型** ] 列舉類型會定義傳遞至 [ [**wfd \_ 顯示 \_ 接收] \_ 通知 \_ 回檔**](wfd-display-sink-notification-callback.md) 函式的通知類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum _WFD_DISPLAY_SINK_NOTIFICATION_TYPE { 
  ProvisioningRequestNotification,
  ReconnectRequestNotification,
  ConnectedNotification,
  DisconnectedNotification
} WFD_DISPLAY_SINK_NOTIFICATION_TYPE, *PWFD_DISPLAY_SINK_NOTIFICATION_TYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="ProvisioningRequestNotification"></span><span id="provisioningrequestnotification"></span><span id="PROVISIONINGREQUESTNOTIFICATION"></span>**ProvisioningRequestNotification**
</dt> <dd>

通知是布建要求。

</dd> <dt>

<span id="ReconnectRequestNotification"></span><span id="reconnectrequestnotification"></span><span id="RECONNECTREQUESTNOTIFICATION"></span>**ReconnectRequestNotification**
</dt> <dd>

通知是重新連接要求。

</dd> <dt>

<span id="ConnectedNotification"></span><span id="connectednotification"></span><span id="CONNECTEDNOTIFICATION"></span>**ConnectedNotification**
</dt> <dd>

通知是已連線的通知。

</dd> <dt>

<span id="DisconnectedNotification"></span><span id="disconnectednotification"></span><span id="DISCONNECTEDNOTIFICATION"></span>**DisconnectedNotification**
</dt> <dd>

通知是已中斷連線的通知。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Wfdsink。h</dt> </dl> |



 

 




