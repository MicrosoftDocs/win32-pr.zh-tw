---
title: 'TVM_SETEXTENDEDSTYLE 訊息 (Commctrl .h) '
description: 通知樹狀檢視控制項設定擴充樣式。 傳送此訊息或使用宏 TreeView \_ SetExtendedStyle。
ms.assetid: 35cb6ac8-1c1e-4ecd-88b2-878d3f6ccaa5
keywords:
- TVM_SETEXTENDEDSTYLE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d13d99a2f7a27475c30867f007f45d7525118d3077ebdce235c6bd33e1f8aafe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750958"
---
# <a name="tvm_setextendedstyle-message"></a>TVM \_ SETEXTENDEDSTYLE 訊息

通知樹狀檢視控制項設定擴充樣式。 傳送此訊息或使用宏 [**TreeView \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setextendedstyle)。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

用來選取要設定之樣式的遮罩。

</dd> <dt>

*lParam* 
</dt> <dd>

指出擴充樣式的值。 如需樣式的詳細資訊，請參閱 [樹狀檢視控制項擴充樣式](tree-view-control-window-extended-styles.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果此訊息成功，則會 **傳回 \_ [確定]**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

樹狀檢視控制項的擴充樣式與函數 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 或函數 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)所使用的擴充樣式沒有任何作用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

