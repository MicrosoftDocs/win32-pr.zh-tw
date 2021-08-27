---
title: 'LVM_GETITEM 訊息 (Commctrl .h) '
description: 抓取部分或全部清單視圖專案的屬性。 您可以明確地傳送此訊息，或使用 ListView \_ GetItem 宏來傳送。
ms.assetid: 684ad96a-2c3b-4148-b66c-41f8322500bb
keywords:
- LVM_GETITEM 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETITEM
- LVM_GETITEMA
- LVM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05338abce0396c5cc527c8a1c04176b3b59243a684c66a263cb190d59ac68b98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088898"
---
# <a name="lvm_getitem-message"></a>LVM \_ GETITEM 訊息

抓取部分或全部清單視圖專案的屬性。 您可以明確地傳送此訊息，或使用 [**ListView \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的指標，此結構會指定要取出的資訊，並接收清單視圖專案的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

當 **LVM \_ GETITEM** 訊息傳送時， **iItem** 和 **iSubItem** 成員會識別要抓取相關資訊的專案或子專案，而 **遮罩** 成員會指定要取出哪些屬性。 如需可能值的清單，請參閱 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) 結構的描述。

如果 LVIF \_ 文字旗標是在 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的 **mask** 成員中設定，則 **pszText** 成員必須指向有效的緩衝區，而且 **cchTextMax** 成員必須設定為該緩衝區中的字元數。 應用程式不應假設文字一定會放在指定的緩衝區中。 控制項可以改為將結構的 **pszText** 成員變更為指向新的文字，而不是將它放在緩衝區中。

如果 **mask** 成員指定 LVIF \_ 狀態值， **stateMask** 成員就必須指定要取出的專案狀態位。 在輸出時， **狀態** 成員會包含指定之狀態位的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **LVM \_GETITEMW** (Unicode) 和 **LVM \_ GETITEMA** (ANSI) <br/>                   |



 

 





