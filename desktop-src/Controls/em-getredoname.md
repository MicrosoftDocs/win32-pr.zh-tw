---
title: 'EM_GETREDONAME 訊息 (Richedit .h) '
description: 在 rich edit 控制項的重做佇列中，抓取下一個動作的型別（如果有的話）。
ms.assetid: 8649236f-32dc-45d3-847e-c9f65ffba44c
keywords:
- EM_GETREDONAME message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETREDONAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ea44257344b9ebdb8ffe91ad97e939aae0db9b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934488"
---
# <a name="em_getredoname-message"></a>EM \_ GETREDONAME 訊息

在 rich edit 控制項的重做佇列中，抓取下一個動作的型別（如果有的話）。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用;必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用;必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果控制項的重做佇列不是空的，則傳回的值會是 [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) 列舉值，指出控制項的重做佇列中下一個動作的類型。

如果沒有 redoable 的動作，或下一個 redoable 動作的型別未知，則傳回值為零。

## <a name="remarks"></a>備註

可以復原或重做的動作類型包括輸入、刪除、拖放、剪下和貼上作業。 這項資訊適用于提供復原和重做作業之擴充使用者介面的應用程式，例如 redoable 動作的下拉式清單方塊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EM \_ GETUNDONAME**](em-getundoname.md)
</dt> <dt>

[**EM \_ 重做**](em-redo.md)
</dt> <dt>

[**EM \_ 復原**](em-undo.md)
</dt> <dt>

[**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 





