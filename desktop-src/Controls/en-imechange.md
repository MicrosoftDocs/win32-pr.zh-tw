---
title: 'EN_IMECHANGE (Richedit 的通知碼) '
description: 通知 rich edit 控制項的父系，IME 轉換狀態已變更。
ms.assetid: 2893e4ef-5904-4a57-95c5-3f6cfbb60d90
keywords:
- EN_IMECHANGE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_IMECHANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fa0e0c8fe4e7d6d8de876a5d1a1fb7a10754096
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025129"
---
# <a name="en_imechange-notification-code"></a>EN \_ IMECHANGE 通知碼

通知 rich edit 控制項的父系，IME 轉換狀態已變更。 此通知碼 *僅* 適用于亞洲語言版本的作業系統。 Rich edit 控制項會以 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息的形式傳送此通知碼。


```C++
EN_IMECHANGE

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含 rich edit 控制項的識別碼。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。

</dd> <dt>

*lParam* 
</dt> <dd>

Rich edit 控制項的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

此通知碼會傳回零。

## <a name="remarks"></a>備註

若要接收 EN \_ IMECHANGE 通知碼，請在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)訊息傳送的遮罩中指定 [**ENM \_ IMECHANGE**](rich-edit-control-event-mask-flags.md) 。

> [!Note]  
> 只有亞洲版 Rich Edit 1.0 支援此通知碼。 較新的版本不支援此功能。 如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**其他資源**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ 命令**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

