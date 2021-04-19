---
title: 'CBN_SELENDOK (Winuser 的通知碼) '
description: 當使用者選取清單專案時傳送，或選取專案然後關閉清單。 這表示會處理使用者的選取專案。 下拉式方塊的父視窗會透過 WM 命令訊息接收此通知碼 \_ 。
ms.assetid: ef0ac46f-2db9-40d6-ba82-7e90d71fdd37
keywords:
- CBN_SELENDOK 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- CBN_SELENDOK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0b04fcce0ec2b3f6a2bf5b5e04fa4110ad6ceb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965905"
---
# <a name="cbn_selendok-notification-code"></a>CBN \_ SELENDOK 通知碼

當使用者選取清單專案時傳送，或選取專案然後關閉清單。 這表示會處理使用者的選取專案。 下拉式方塊的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。


```C++
CBN_SELENDOK

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含下拉式方塊的控制項識別碼。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。

</dd> <dt>

*lParam* 
</dt> <dd>

下拉式方塊的控制碼。

</dd> </dl>

## <a name="remarks"></a>備註

在具有 [**CBS \_ 簡單**](combo-box-styles.md) 樣式的下拉式方塊中，CBN \_ SELENDOK 通知碼會在每個 [CBN \_ SELCHANGE](cbn-selchange.md) 通知程式碼之前立即傳送。

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

[CBN \_ SELCHANGE](cbn-selchange.md)
</dt> <dt>

[CBN \_ SELENDCANCEL](cbn-selendcancel.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ 命令**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

