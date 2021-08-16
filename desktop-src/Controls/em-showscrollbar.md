---
title: 'EM_SHOWSCROLLBAR 訊息 (Richedit .h) '
description: 顯示或隱藏 rich edit 控制項主視窗中的其中一個捲軸。
ms.assetid: 0a6ec010-4870-4faf-9dc2-1da961dc8194
keywords:
- EM_SHOWSCROLLBAR 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_SHOWSCROLLBAR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc3988ced825fed457549fc9f662a418295de7df6085f04c3e71255ca4ad54c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831139"
---
# <a name="em_showscrollbar-message"></a>EM \_ SHOWSCROLLBAR 訊息

顯示或隱藏 rich edit 控制項主視窗中的其中一個捲軸。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

識別要顯示的捲軸：水準或垂直。 此參數必須是 **sb \_ 垂直** 或 **sb \_ HORZ**。

</dd> <dt>

*lParam* 
</dt> <dd>

指定是否要顯示捲軸或隱藏捲軸。 指定 **TRUE** 可顯示捲軸，而 **FALSE** 則會隱藏。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

只有在控制項為就地使用中時，此方法才有效。 控制項處於非使用中狀態時所發出的呼叫可能會失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EM \_ GETSCROLLPOS**](em-getscrollpos.md)
</dt> <dt>

[**EM \_ SETSCROLLPOS**](em-setscrollpos.md)
</dt> </dl>

 

 





