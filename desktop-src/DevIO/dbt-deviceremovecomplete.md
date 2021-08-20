---
description: '\_當實際移除裝置或媒體時，系統會廣播 DBT DEVICEREMOVECOMPLETE 裝置事件。'
ms.assetid: e25d35b9-f8f1-4850-996c-e1cb393cca66
title: 'DBT_DEVICEREMOVECOMPLETE (Dbt 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5998742d823d710bfb91cd10579a3fb1ec65bec42b615fc7fdac3ac35545b24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539188"
---
# <a name="dbt_deviceremovecomplete-event"></a>DBT \_ DEVICEREMOVECOMPLETE 事件

\_當實際移除裝置或媒體時，系統會廣播 DBT DEVICEREMOVECOMPLETE 裝置事件。

若要廣播此裝置事件，系統會使用與 *wParam* 設定為 DBT DEVICEREMOVECOMPLETE 和 lParam 設定的 [**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息， \_ 如下所述。 


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

設定為 DBT \_ DEVICEREMOVECOMPLETE

</dd> <dt>

*lParam* 
</dt> <dd>

識別已移除裝置之結構的指標。 此結構是由與事件無關的標頭所組成，後面接著描述裝置的事件相依成員。 若要使用此結構，請將結構視為 [**開發 \_ 廣播 \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) 結構，然後檢查其 **dbch \_ devicetype** 成員以判斷裝置類型。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **TRUE**。

## <a name="remarks"></a>備註

系統可能會廣播 DBT \_ DEVICEREMOVECOMPLETE 訊息，而不會傳送對應的 [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) 和 [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) 訊息。 在這種情況下，應用程式和驅動程式必須盡可能地從裝置遺失中復原。

如果正在移除媒體，則抵達的裝置類型為磁片區， (**dbch \_ devicetype** 成員是 DBT \_ DEVTYP \_ volume) ，而 **dbcv \_ 旗標** 成員 (媒體) 的變更效果 \_ 。

## <a name="examples"></a>範例

如需範例，請參閱偵測 [媒體插入或移除](detecting-media-insertion-or-removal.md) 或 [處理移除裝置的要求](processing-a-request-to-remove-a-device.md)。

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

 

 




