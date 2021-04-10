---
title: 'EN_HSCROLL (Winuser 的通知碼) '
description: 當使用者按一下編輯控制項的水準捲軸時傳送。 編輯控制項的父視窗會透過 WM 命令訊息接收此通知碼 \_ 。 在畫面更新之前，父視窗會收到通知。
ms.assetid: beaaa80c-4108-4a8e-aed8-04c9a3a08f3e
keywords:
- EN_HSCROLL 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_HSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f90f6e781409419e39390e64251506b4cc915a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843799"
---
# <a name="en_hscroll-notification-code"></a>EN \_ HSCROLL 通知碼

當使用者按一下編輯控制項的水準捲軸時傳送。 編輯控制項的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。 在畫面更新之前，父視窗會收到通知。


```C++
EN_HSCROLL

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

此通知碼會針對水準捲軸上的下列滑鼠事件傳送：按一下任一箭號按鈕，或在箭號按鈕與 thumb 之間按一下。 不過，在按一下捲軸捲軸時，不會傳送通知碼。 當鍵盤事件在編輯控制項的視圖區域中造成變更時（例如，按下 HOME、END、向左鍵或向右箭號），也會傳送通知碼。

**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。 若要接收 **EN \_ HSCROLL** 通知碼，請在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)訊息傳送的遮罩中指定 [**ENM \_ SCROLL**](rich-edit-control-event-mask-flags.md) 。 如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

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

[EN \_ VSCROLL](en-vscroll.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**WM \_ 命令**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

