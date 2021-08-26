---
title: 'EN_STOPNOUNDO (Richedit 的通知碼) '
description: 通知 rich edit 控制項的父視窗，表示控制項無法配置足夠的記憶體來維持復原狀態。 Rich edit 控制項會以 WM 通知訊息的形式傳送此通知碼 \_ 。
ms.assetid: 5608f6dd-83dc-4712-b485-dd9bc17dea24
keywords:
- EN_STOPNOUNDO 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_STOPNOUNDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e2bd22161f215e9544db08f845eb144fe94ec083b8a887a3db6fc46220d822d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047388"
---
# <a name="en_stopnoundo-notification-code"></a>EN \_ STOPNOUNDO 通知碼

通知 rich edit 控制項的父視窗，表示控制項無法配置足夠的記憶體來維持復原狀態。 Rich edit 控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。


```C++
EN_STOPNOUNDO

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回零以繼續執行 **復原** 操作。

傳回非零值以停止 **復原** 作業。

## <a name="remarks"></a>備註

父視窗一律會取得這個事件的 [**WM \_ 通知**](wm-notify.md) 訊息，不需要以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)傳送通知遮罩。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)
</dt> <dt>

[**WM \_ 通知**](wm-notify.md)
</dt> </dl>

 

 





