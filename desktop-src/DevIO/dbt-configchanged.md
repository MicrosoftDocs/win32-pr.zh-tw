---
description: 系統會廣播 DBT \_ CONFIGCHANGED 裝置事件，以指出目前的設定已變更，因為 dock 或取消停駐。 將資料儲存在登錄中的應用程式或驅動程式 HKEY \_ 目前的設定 \_ 金鑰應該會更新資料。
ms.assetid: e5e33970-b17e-4723-98aa-e242f90fe4e7
title: 'DBT_CONFIGCHANGED (Dbt 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d242832378ba9ca3d3006965719942aa41ecff93
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187721"
---
# <a name="dbt_configchanged-event"></a>DBT \_ CONFIGCHANGED 事件

系統會廣播 DBT \_ CONFIGCHANGED 裝置事件，以指出目前的設定已變更，因為 dock 或取消停駐。 將資料儲存在登錄中的應用程式或驅動程式 HKEY \_ 目前的設定 \_ 金鑰應該會更新資料。

若要廣播此裝置事件，系統會使用 *wParam* 設定為 DBT CONFIGCHANGED 且 lParam 設定為零的 [**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息 \_ 。 


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

設定為 DBT \_ CONFIGCHANGED。

</dd> <dt>

*lParam* 
</dt> <dd>

設定為零。

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

[**WM \_ DEVICECHANGE**](wm-devicechange.md)
</dt> </dl>

 

 




