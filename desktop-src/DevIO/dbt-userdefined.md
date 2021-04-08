---
description: DBT 的使用者 \_ 定義裝置事件會識別使用者定義的事件。
ms.assetid: b42feda9-5fe7-4e54-aad9-28c61d2f29b6
title: 'DBT_USERDEFINED (Dbt 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d57ed3ebb801da4ae1ed7a7964cb7aac4f411a35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025919"
---
# <a name="dbt_userdefined-event"></a>DBT \_ 使用者的事件

DBT 的使用者 \_ 定義裝置事件會識別使用者定義的事件。

若要廣播此裝置事件，請使用 [**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息來呼叫 [**BroadcastSystemMessage**](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage)函數。 將 *wParam* 設定為 DBT 的 \_ 使用者，並設定 *lParam* ，如下所述。


```C++
LRESULT CALLBACK WindowProc( HWND   hwnd,     // handle to window
                             UINT   uMsg,     // WM_DEVICECHANGE
                             WPARAM wParam,   // DBT_USERDEFINED
                             LPARAM lParam ); // event-specific data
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwnd* 
</dt> <dd>

視窗的控點。

</dd> <dt>

*uMsg* 
</dt> <dd>

[**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息識別碼。

</dd> <dt>

*wParam* 
</dt> <dd>

設定為 DBT 的 \_ 使用者。

</dd> <dt>

*lParam* 
</dt> <dd>

[**\_ 開發人員 \_ 廣播 \_**](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined)的使用者定義結構指標，描述正在進行的使用者定義廣播。 **Dbud \_ >szname** 成員包含使用者自訂訊息的名稱，後面接著任何使用者定義的資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **TRUE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows XP<br/>                                                            |
| 最低支援的伺服器<br/> | Windows Server 2003<br/>                                                   |
| 標頭<br/>                   | <dl> <dt>Dbt。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[裝置事件](device-events.md)
</dt> <dt>

[裝置管理事件](device-management-events.md)
</dt> <dt>

[**\_開發人員 \_ 廣播的 \_ 使用者**](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined)
</dt> <dt>

[**WM \_ DEVICECHANGE**](wm-devicechange.md)
</dt> <dt>

[**BroadcastSystemMessage**](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage)
</dt> </dl>

 

