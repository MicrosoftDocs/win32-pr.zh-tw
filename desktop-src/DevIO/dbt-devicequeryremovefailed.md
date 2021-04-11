---
description: '\_當移除裝置或媒體片段的要求遭到取消時，系統會廣播 DBT DEVICEQUERYREMOVEFAILED 裝置事件。'
ms.assetid: a24916a9-b67a-4622-b9f3-4b4f26bf4d6b
title: 'DBT_DEVICEQUERYREMOVEFAILED (Dbt 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 848c7378cdbac95729eee70c70a1e323373b8e85
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847287"
---
# <a name="dbt_devicequeryremovefailed-event"></a>DBT \_ DEVICEQUERYREMOVEFAILED 事件

\_當移除裝置或媒體片段的要求遭到取消時，系統會廣播 DBT DEVICEQUERYREMOVEFAILED 裝置事件。

若要廣播此裝置事件，系統會使用與 *wParam* 設定為 DBT DEVICEQUERYREMOVEFAILED 和 lParam 設定的 [**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息， \_ 如下所述。 


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

設定為 DBT \_ DEVICEQUERYREMOVEFAILED。

</dd> <dt>

*lParam* 
</dt> <dd>

識別裝置之結構的指標。 此結構是由與事件無關的標頭所組成，後面接著描述裝置的事件相依成員。 若要使用此結構，請將結構視為 [**開發 \_ 廣播 \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) 結構，然後檢查其 **dbch \_ devicetype** 成員以判斷裝置類型。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **TRUE**。

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

 

 




