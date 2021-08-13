---
title: 'EM_SETEXTENDEDSTYLE 訊息 (Commctrl .h) '
description: 通知編輯控制項設定擴充樣式。 傳送此訊息或使用巨集編輯 \_ SetExtendedStyle。
ms.assetid: 4ca010c3-2c70-41e5-ade4-11e1895fda26
keywords:
- EM_SETEXTENDEDSTYLE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 710ad6535bd7891f322a4bf02a5fed0f766dd97c2569fa5ec9b961478bf6a457
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118673074"
---
# <a name="em_setextendedstyle-message"></a>EM \_ SETEXTENDEDSTYLE 訊息

通知編輯控制項設定擴充樣式。 傳送此訊息或使用宏 [**編輯 \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setextendedstyle)。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

用來選取要設定之樣式的遮罩。

</dd> <dt>

*lParam* 
</dt> <dd>

指出擴充樣式的值。 如需樣式的詳細資訊，請參閱 [編輯控制項延伸樣式](edit-control-window-extended-styles.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果此訊息成功，則會 **傳回 \_ [確定]**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

編輯控制項的擴充樣式與函數 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 或函數 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)所使用的擴充樣式沒有任何作用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 版本 1809 \[僅限桌面應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2019 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

