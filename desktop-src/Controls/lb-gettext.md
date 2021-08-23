---
title: 'LB_GETTEXT 訊息 (Winuser .h) '
description: 從清單方塊中取得字串。
ms.assetid: 6bf7ec3b-237b-4668-9493-40c098a32428
keywords:
- LB_GETTEXT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LB_GETTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b2aa37a2d07e440aac615d1edc1e6f91c6a60e71a96418cd443daff9809ec18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434097"
---
# <a name="lb_gettext-message"></a>LB \_ GETTEXT 訊息

從清單方塊中取得字串。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要抓取之字串的以零為基底的索引。

Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。 這表示清單方塊不能包含超過32767個專案。 雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。

</dd> <dt>

*lParam* 
</dt> <dd>

將接收字串的緩衝區指標;它是 **LPTSTR** 類型，接著會轉換成 **LPARAM**。 緩衝區必須有足夠的空間可供字串和終止的 null 字元使用。 您可以在 **lb \_ GETTEXT** 訊息之前傳送 [**lb \_ GETTEXTLEN**](lb-gettextlen.md)訊息，以取得字串的長度（以 **TCHAR** s 為限）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是字串的長度（在 **TCHAR** s 中），不包括結束的 null 字元。 如果 *wParam* 未指定有效的索引，則傳回值為 LB \_ ERR。

## <a name="remarks"></a>備註

如果清單方塊有擁有者繪製的樣式，而不是 [**磅 \_ HASSTRINGS**](list-box-styles.md) 樣式，則 *lParam* 參數所指向的緩衝區會接收與專案資料)  (專案相關聯的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LB \_ GETTEXTLEN**](lb-gettextlen.md)
</dt> </dl>

 

 





