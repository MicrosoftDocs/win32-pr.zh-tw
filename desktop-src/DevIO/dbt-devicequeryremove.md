---
description: 系統會廣播 DBT \_ DEVICEQUERYREMOVE 裝置事件，以要求移除裝置或媒體部分的許可權。
ms.assetid: a0e9aa57-da0e-4e9c-99d0-5502040d2664
title: 'DBT_DEVICEQUERYREMOVE (Dbt 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8c9dbdee13318f9a664582fdba8f9e3f9bfc5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981124"
---
# <a name="dbt_devicequeryremove-event"></a>DBT \_ DEVICEQUERYREMOVE 事件

系統會廣播 DBT \_ DEVICEQUERYREMOVE 裝置事件，以要求移除裝置或媒體部分的許可權。 這則訊息是應用程式和驅動程式的最後機會，以準備進行移除。 不過，任何應用程式都可以拒絕此要求，並取消作業。

若要廣播此裝置事件，系統會使用與 *wParam* 設定為 DBT DEVICEQUERYREMOVE 和 lParam 設定的 [**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息， \_ 如下所述。 


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

設定為 DBT \_ DEVICEQUERYREMOVE。

</dd> <dt>

*lParam* 
</dt> <dd>

結構的指標，此結構識別要移除的裝置。 此結構是由與事件無關的標頭所組成，後面接著描述裝置的事件相依成員。 若要使用此結構，請將結構視為 [**開發 \_ 廣播 \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) 結構，然後檢查其 **dbch \_ devicetype** 成員以判斷裝置類型。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **TRUE** 以授與移除裝置的許可權。

傳回「廣播 \_ 查詢 \_ 拒絕」以拒絕移除裝置的許可權。

## <a name="remarks"></a>備註

您必須關閉裝置的所有控制碼，否則裝置移除將會失敗。

## <a name="examples"></a>範例

如需範例，請參閱 [處理移除裝置的要求](processing-a-request-to-remove-a-device.md)。

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

 

 




