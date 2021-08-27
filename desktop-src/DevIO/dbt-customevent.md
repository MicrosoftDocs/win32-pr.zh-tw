---
description: '\_當驅動程式定義的自訂事件發生時，系統會傳送 DBT CUSTOMEVENT 裝置事件。'
ms.assetid: 6e66fa93-0cd7-4202-83eb-cddc668525ae
title: 'DBT_CUSTOMEVENT (Dbt 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75ec02262e4cf49a7b929f738acce94822aaf67a397a37d6237f4faa57ef7f1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109038"
---
# <a name="dbt_customevent-event"></a>DBT \_ CUSTOMEVENT 事件

\_當驅動程式定義的自訂事件發生時，系統會傳送 DBT CUSTOMEVENT 裝置事件。

若要廣播此裝置事件，系統會使用與 *wParam* 設定為 DBT CUSTOMEVENT 和 lParam 設定的 [**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息， \_ 如下所述。 


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

設定為 DBT \_ CUSTOMEVENT。

</dd> <dt>

*lParam* 
</dt> <dd>

識別裝置之結構的指標。 此結構是由與事件無關的標頭所組成，後面接著描述裝置的事件相依成員。 若要使用此結構，請將結構視為 [**開發 \_ 廣播 \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) 結構，然後檢查其 **dbch \_ devicetype** 成員以判斷裝置類型。

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

[**開發 \_ 廣播 \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[**WM \_ DEVICECHANGE**](wm-devicechange.md)
</dt> </dl>

 

 




