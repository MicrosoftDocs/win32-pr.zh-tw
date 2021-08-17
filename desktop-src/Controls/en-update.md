---
title: 'EN_UPDATE (Winuser 的通知碼) '
description: 當編輯控制項即將重新繪製時傳送。
ms.assetid: 59138736-6cc9-4a3f-95f3-ada9cbf253cb
keywords:
- EN_UPDATE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_UPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c126122336fd878dda633620c395cb86c112de1f5dc89e8e25d2c4e08bd93ebd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436426"
---
# <a name="en_update-notification-code"></a>EN \_ 更新通知碼

當編輯控制項即將重新繪製時傳送。 此通知碼會在控制項格式化文字之後，但在顯示文字之前傳送。 如此一來，就可以視需要調整編輯控制項視窗的大小。 編輯控制項的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。


```C++
EN_UPDATE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含編輯控制項的識別碼。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。

</dd> <dt>

*lParam* 
</dt> <dd>

編輯控制項的控制碼。

</dd> </dl>

## <a name="remarks"></a>備註

**Rich Edit 1.0：** 若要接收 EN \_ 更新通知碼，請在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)訊息傳送的遮罩中指定 [**ENM \_ UPDATE**](rich-edit-control-event-mask-flags.md) 。

**Rich Edit 2.0 和更新版本：** 已忽略 [**ENM \_ 更新**](rich-edit-control-event-mask-flags.md) 旗標。 \_一律會收到 EN 更新通知代碼。 不過，當 Microsoft Rich Edit 3.0 模擬 Microsoft Rich Edit 1.0 時，若要接收 EN-US \_ 更新通知碼，您必須在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)訊息傳送的遮罩中指定 **ENM \_ UPDATE** 。

如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[EN \_ 變更](en-change.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**WM \_ 命令**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

