---
description: 表示用於監視和報告的服務狀態變更類型。
ms.assetid: 7508526c-02ce-4ac2-8616-491390a4afad
title: 'SC_EVENT_TYPE 列舉 (Winsvcp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SC_EVENT_TYPE
api_type:
- HeaderDef
api_location:
- Winsvcp.h
ms.openlocfilehash: 55853d13844d3bb255ab0e84a50e8cbbea2d76ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989009"
---
# <a name="sc_event_type-enumeration"></a>SC \_ 事件 \_ 類型列舉

表示用於監視和報告的服務狀態變更類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum _SC_EVENT_TYPE { 
  SC_EVENT_DATABASE_CHANGE  = 0,
  SC_EVENT_PROPERTY_CHANGE  = 1,
  SC_EVENT_STATUS_CHANGE    = 2
} SC_EVENT_TYPE, *PSC_EVENT_TYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span>**SC \_ 事件 \_ 資料庫 \_ 變更**
</dt> <dd>

已新增或刪除服務。 [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md)函數的 *hService* 參數必須是 SCM 的控制碼。

</dd> <dt>

<span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span>**SC \_ 事件 \_ 屬性 \_ 變更**
</dt> <dd>

已更新一或多個服務屬性。 [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md)函數的 *hService* 參數必須是服務的控制碼。

</dd> <dt>

<span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span>**SC \_ 事件 \_ 狀態 \_ 變更**
</dt> <dd>

服務的狀態已變更。 [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md)函數的 *hService* 參數必須是服務的控制碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Winsvcp。h</dt> </dl> |



 

 




