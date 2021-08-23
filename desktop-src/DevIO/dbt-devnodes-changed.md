---
description: 系統已 \_ 新增或移除裝置時，系統會將 DBT DEVNODES \_ 變更裝置事件廣播。 維護系統中裝置清單的應用程式應該重新整理其清單。
ms.assetid: 62acc633-7dad-4792-a5a2-1f95356479d1
title: 'DBT_DEVNODES_CHANGED (Dbt 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00d43873241c3f72336dd996fb9fa3486229d9ffcf522923d68ab606313afb7e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539158"
---
# <a name="dbt_devnodes_changed-event"></a>DBT \_ DEVNODES \_ 已變更事件

系統已 \_ 新增或移除裝置時，系統會將 DBT DEVNODES \_ 變更裝置事件廣播。 維護系統中裝置清單的應用程式應該重新整理其清單。

若要廣播此裝置事件，系統會使用 *wParam* 設定為 DBT DEVNODES [**\_**](wm-devicechange.md) \_ \_ 變更且 *lParam* 設定為零的 WM DEVICECHANGE 訊息。


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
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

設定為 DBT \_ DEVNODES \_ 已變更。

</dd> <dt>

*lParam* 
</dt> <dd>

設定為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **TRUE**。

## <a name="remarks"></a>備註

在系統中新增或移除的裝置沒有其他相關資訊。 需要詳細資訊的應用程式應該使用 [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) 函式來註冊裝置通知。

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

[**開發 \_ 廣播 \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[**WM \_ DEVICECHANGE**](wm-devicechange.md)
</dt> </dl>

 

 




