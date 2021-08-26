---
title: 'BM_SETSTATE 訊息 (Winuser .h) '
description: 設定按鈕的醒目提示狀態。 醒目提示狀態會指出按鈕是否反白顯示，如同使用者是否已推送按鈕。 您可以明確地傳送此訊息，或使用按鈕 \_ SetState 宏。
ms.assetid: 675ebe8d-b381-46ca-b328-ebe9f25d864a
keywords:
- BM_SETSTATE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- BM_SETSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e3bb9451041c602541f039afcd85a895af2f02302dc5d55d64fbefb5bc6e3ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921208"
---
# <a name="bm_setstate-message"></a>BM \_ SETSTATE 訊息

設定按鈕的醒目提示狀態。 醒目提示狀態會指出按鈕是否反白顯示，如同使用者是否已推送按鈕。 您可以明確地傳送此訊息，或使用 [**按鈕 \_ SetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定是否要反白顯示按鈕的 **布林** 值。 值為 **TRUE** 時，會反白顯示按鈕。 **FALSE** 值會移除任何反白顯示。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息一律會傳回零。

## <a name="remarks"></a>備註

醒目提示只會影響按鈕的外觀。 它不會影響選項按鈕或核取方塊的核取狀態。

當使用者將游標放在其上方，然後按下並按住滑鼠左鍵時，按鈕就會自動反白顯示。 當使用者放開滑鼠按鍵時，就會移除反白顯示。

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

[**BM \_ >GETSTATE**](bm-getstate.md)
</dt> <dt>

[**BM \_ SETCHECK**](bm-setcheck.md)
</dt> </dl>

 

 





