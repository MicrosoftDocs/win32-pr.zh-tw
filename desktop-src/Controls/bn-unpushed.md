---
title: 'BN_UNPUSHED (Winuser 的通知碼) '
description: 當按鈕的推送狀態設定為未推送時傳送。
ms.assetid: 1ae7311d-f067-41fe-a117-e0c70d239e9d
keywords:
- BN_UNPUSHED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- BN_UNPUSHED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7eb8c16d8860274c070c31910254311a897c0f1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094076"
---
# <a name="bn_unpushed-notification-code"></a>BN \_ 未推送通知碼

當按鈕的推送狀態設定為未推送時傳送。

> [!Note]  
> 此通知碼僅提供與3.0 版之前的16位 Windows 版本的相容性。 應用程式應該使用這項工作的 [**BS \_ OWNERDRAW**](button-styles.md) 按鈕樣式和 [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) 結構。

 

按鈕的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。


```C++
BN_UNPUSHED

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含按鈕的控制項識別碼。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。

</dd> <dt>

*lParam* 
</dt> <dd>

按鈕的控制碼。

</dd> </dl>

## <a name="remarks"></a>備註

BN \_ 未推送與 [BN \_ UNHILITE](bn-unhilite.md) 通知碼相同。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[BN \_ 推送](bn-pushed.md)
</dt> </dl>

 

