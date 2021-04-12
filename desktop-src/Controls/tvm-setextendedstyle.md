---
title: 'TVM_SETEXTENDEDSTYLE 訊息 (Commctrl .h) '
description: 通知樹狀檢視控制項設定擴充樣式。 傳送此訊息或使用宏 TreeView \_ SetExtendedStyle。
ms.assetid: 35cb6ac8-1c1e-4ecd-88b2-878d3f6ccaa5
keywords:
- TVM_SETEXTENDEDSTYLE message Windows 控制項
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
ms.openlocfilehash: 9c450f72f85e40514c35f08284428feec4f7caf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508695"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

