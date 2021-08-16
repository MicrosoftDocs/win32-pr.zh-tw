---
title: 'BCM_SETDROPDOWNSTATE 訊息 (Commctrl .h) '
description: 設定具有樣式 TBSTYLE 下拉式清單之按鈕的下拉式狀態 \_ 。 明確地傳送此訊息，或使用按鈕 \_ SetDropDownState 宏。
ms.assetid: 725deff4-0bcb-497d-a6cf-e9c98b05f16e
keywords:
- BCM_SETDROPDOWNSTATE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- BCM_SETDROPDOWNSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 989b4a04502a730c06a906be28a6915a4e604ff22c4b4e5ae9a4b85c8b464f81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117833629"
---
# <a name="bcm_setdropdownstate-message"></a>BCM \_ SETDROPDOWNSTATE 訊息

設定具有樣式 [**TBSTYLE 下拉式 \_ 清單**](toolbar-control-and-button-styles.md)之按鈕的下拉式狀態。 明確地傳送此訊息，或使用 [**按鈕 \_ SetDropDownState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

適用于 BST DROPDOWNPUSHED 狀態的 **布林****值為 TRUE** \_ ，否則為 **FALSE** 。

</dd> <dt>

*lParam* 
</dt> <dd>

必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[按鈕樣式](button-styles.md)
</dt> <dt>

**概念**
</dt> <dt>

[按鈕類型](button-types-and-styles.md)
</dt> </dl>

 

 





