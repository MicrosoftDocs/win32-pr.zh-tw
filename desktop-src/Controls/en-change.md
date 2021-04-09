---
title: 'EN_CHANGE (Winuser 的通知碼) '
description: 當使用者採取的動作可能已更改編輯控制項中的文字時傳送。
ms.assetid: 8a04e6fb-ae9d-4d94-8047-6de96df899f5
keywords:
- EN_CHANGE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8ef26d1ec4f8ec1dc93e54d46b88c4fe7cc872b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843356"
---
# <a name="en_change-notification-code"></a>EN \_ 變更通知碼

當使用者採取的動作可能已更改編輯控制項中的文字時傳送。 不同于 [EN \_ 更新](en-update.md) 通知碼，系統會在系統更新畫面之後傳送此通知碼。 編輯控制項的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。


```C++
EN_CHANGE

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

**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。 若要接收 EN-US \_ 變更通知碼，請在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)訊息傳送的遮罩中指定 [**ENM \_ 變更**](rich-edit-control-event-mask-flags.md)。 如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

\_使用 [**ES \_ 多行**](edit-control-styles.md)樣式，並透過 [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)傳送文字時，不會傳送 EN 變更通知碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[EN \_ 更新](en-update.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**WM \_ 命令**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

