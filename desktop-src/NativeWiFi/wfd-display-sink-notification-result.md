---
description: 描述在 [WFD \_ 顯示 \_ 接收] \_ 通知回呼函式中處理顯示接收器通知之後，您可以選擇性地設定的結果 \_ 。
ms.assetid: 6ED04294-2ED9-455B-9274-8C3DB06D4B21
title: 'WFD_DISPLAY_SINK_NOTIFICATION_RESULT 結構 (Wfdsink .h) '
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
ms.openlocfilehash: d72f444d409a7a3d43103967aff671fa7c808e5a37858e79f175db3511960e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780078"
---
# <a name="wfd_display_sink_notification_result-structure"></a>WFD \_ 顯示 \_ 接收 \_ 通知 \_ 結果結構

[ **Wfd \_ 顯示 \_ 接收 \_ 通知] \_ 結果** 結構描述您可以選擇性地在 [ [**wfd \_ 顯示接收] \_ \_ 通知 \_ 回檔**](wfd-display-sink-notification-callback.md) 函式中處理顯示接收器通知之後設定的結果。

## <a name="syntax"></a>語法


```C++
typedef struct _WFD_DISPLAY_SINK_NOTIFICATION {
  WFD_DISPLAY_SINK_OBJECT_HEADER     Header;
  WFD_DISPLAY_SINK_NOTIFICATION_TYPE type;
  union {
    struct {
      DOT11_WPS_CONFIG_METHOD ConfigMethod;
      UINT32                  uPassKeyLength;
      WCHAR                   Passkey[WFD_SINK_WPS_INFO_MAX_PASSKEY_LENGTH];
    } ProvisioningData;
    struct {
      PWSTR strProfile;
    } ReconnectData;
  };
} WFD_DISPLAY_SINK_NOTIFICATION, *PWFD_DISPLAY_SINK_NOTIFICATION;
```



## <a name="members"></a>成員

<dl> <dt>

**標頭**
</dt> <dd>

可描述通知結果中所含資料的 [**WFD \_ 顯示 \_ 接收器 \_ 物件 \_ 標頭**](wfd-display-sink-object-header.md) 。

</dd> <dt>

**type**
</dt> <dd>

指出通知結果類型的 [ [**WFD \_ 顯示 \_ 接收] \_ 通知 \_ 類型**](wfd-display-sink-notification-type.md) 值。 此參數也會決定要在下聯集內使用的資訊。

</dd> <dt>

**ProvisioningData**
</dt> <dd>

布建要求結果的相關資訊。 如果 *類型* 具有值 **ProvisioningRequestNotification**，請使用此值。

<dl> <dt>

**ConfigMethod**
</dt> <dd>

用於顯示互動式接受之 UI 的方法。

</dd> <dt>

**uPassKeyLength**
</dt> <dd>

*密碼* 中的寬字元數，不計入任何 Null 結束字元。

</dd> <dt>

**金鑰**
</dt> <dd>

以寬字元陣列的形式包含傳遞索引鍵。 WFD \_ 接收 \_ WPS \_ 資訊 \_ 最大 \_ 密碼 \_ 長度會定義為 (8) 的值。

</dd> </dl> </dd> <dt>

**ReconnectData**
</dt> <dd>

重新連接要求結果的相關資訊。 如果 *類型* 具有值 **ReconnectRequestNotification**，請使用此值。

<dl> <dt>

**strProfile**
</dt> <dd>

描述設定檔之以 Null 結束的字串指標。

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Wfdsink。h</dt> </dl> |



 

 




