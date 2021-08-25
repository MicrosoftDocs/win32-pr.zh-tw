---
description: '\_當 (停駐或取消停駐) 變更目前設定的要求時，系統會廣播 DBT CONFIGCHANGECANCELED 裝置事件。'
ms.assetid: b4b1455c-9a04-4fa0-a3fa-ed991f278c0c
title: 'DBT_CONFIGCHANGECANCELED (Dbt 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 624144ccd5a87d983d453c8d6a3c0667376c2a1b9340bba83f229a29882bffe4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874538"
---
# <a name="dbt_configchangecanceled-event"></a>DBT \_ CONFIGCHANGECANCELED 事件

\_當 (停駐或取消停駐) 變更目前設定的要求時，系統會廣播 DBT CONFIGCHANGECANCELED 裝置事件。

若要廣播此裝置事件，系統會使用 *wParam* 設定為 DBT CONFIGCHANGECANCELED 且 lParam 設定為零的 [**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息 \_ 。 


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

設定為 DBT \_ CONFIGCHANGECANCELED。

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

 

 




