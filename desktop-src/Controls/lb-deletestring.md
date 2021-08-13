---
title: 'LB_DELETESTRING 訊息 (Winuser .h) '
description: 刪除清單方塊中的字串。
ms.assetid: 3f360e07-b70d-4bfc-89d4-18d3b18b0fcf
keywords:
- LB_DELETESTRING 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LB_DELETESTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3329f82babea73a6392f7c360623fdeadec843dfcfd62e70106e7fb1cb0367ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118671673"
---
# <a name="lb_deletestring-message"></a>LB \_ DELETESTRING 訊息

刪除清單方塊中的字串。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要刪除之字串的以零為基底的索引。

Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。 這表示清單方塊不能包含超過32767個專案。 雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是清單中剩餘字串的計數。 \_如果 *wParam* 參數指定的索引大於清單中的專案數，則傳回值為 LB ERR。

## <a name="remarks"></a>備註

如果應用程式建立具有主控描繪樣式但沒有 [**磅 \_ HASSTRINGS**](list-box-styles.md) 樣式的清單方塊，系統會將 [**WM \_ DELETEITEM**](wm-deleteitem.md) 訊息傳送給清單方塊的擁有者，讓應用程式可以釋出與該專案相關聯的任何其他資料。

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

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**LB \_ INSERTSTRING**](lb-insertstring.md)
</dt> <dt>

[**WM \_ DELETEITEM**](wm-deleteitem.md)
</dt> </dl>

 

 





