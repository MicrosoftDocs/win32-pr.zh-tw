---
description: 系統會廣播 DBT \_ QUERYCHANGECONFIG 裝置事件，以要求 (dock 或取消停駐) 變更目前設定的許可權。 任何應用程式都可以拒絕此要求，並取消變更。
ms.assetid: 2e452ea7-e2bf-4500-952a-ee7d891533a0
title: 'DBT_QUERYCHANGECONFIG (Dbt 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48367da1788ae2985b21fad6e960153008e9ffd2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510574"
---
# <a name="dbt_querychangeconfig-event"></a>DBT \_ QUERYCHANGECONFIG 事件

系統會廣播 DBT \_ QUERYCHANGECONFIG 裝置事件，以要求 (dock 或取消停駐) 變更目前設定的許可權。 任何應用程式都可以拒絕此要求，並取消變更。

若要廣播此裝置事件，系統會使用 *wParam* 設定為 DBT QUERYCHANGECONFIG 且 lParam 設定為零的 [**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息 \_ 。 


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

設定為 DBT \_ QUERYCHANGECONFIG。

</dd> <dt>

*lParam* 
</dt> <dd>

設定為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **TRUE** 以授與變更設定的許可權。

傳回「廣播 \_ 查詢 \_ 拒絕」以拒絕變更設定的許可權。

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

[**WM \_ DEVICECHANGE**](wm-devicechange.md)
</dt> </dl>

 

 




