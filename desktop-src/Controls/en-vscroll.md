---
title: 'EN_VSCROLL (Winuser 的通知碼) '
description: 當使用者按一下編輯控制項的垂直捲動條，或當使用者將滑鼠滾輪滾動至編輯控制項時傳送。
ms.assetid: 46307dee-3c5c-4020-9c2b-ec4638a0cea5
keywords:
- EN_VSCROLL 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_VSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c716ecb36c0d27b445446a30eb0a026edf3fd88641f469e50daef1763cd6ca66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047378"
---
# <a name="en_vscroll-notification-code"></a>EN \_ VSCROLL 通知碼

當使用者按一下編輯控制項的垂直捲動條，或當使用者將滑鼠滾輪滾動至編輯控制項時傳送。 編輯控制項的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。 在畫面更新之前，父視窗會收到通知。


```C++
EN_VSCROLL

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

這則訊息會針對垂直捲動條上的下列滑鼠事件傳送：按一下任一箭號按鈕，或在箭號按鈕與 thumb 之間按一下。 但是，當您按一下捲軸滑鼠本身時，不會傳送訊息。 當鍵盤事件在編輯控制項的視圖區域中造成變更時（例如，按下 HOME、END、PAGE UP、PAGE DOWN、UP 箭號或向下箭號），也會傳送此訊息。

滑鼠滾輪是具有滾動滾輪的滑鼠。 如需詳細資訊，請參閱 [關於滑鼠輸入](/windows/desktop/inputdev/about-mouse-input)的「滑鼠滾輪」。

**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。 若要接收 EN \_ VSCROLL 通知碼，請在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)訊息傳送的遮罩中指定 [**ENM \_ SCROLL**](rich-edit-control-event-mask-flags.md) 。 如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

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

[EN \_ HSCROLL](en-hscroll.md)
</dt> <dt>

**概念**
</dt> <dt>

[使用編輯控制項](using-edit-controls.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**WM \_ 命令**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

