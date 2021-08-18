---
title: 'LB_GETITEMDATA 訊息 (Winuser .h) '
description: 取得與指定清單方塊專案相關聯的應用程式定義值。
ms.assetid: 3a3f7fa5-ce04-4e95-86e1-5c7de796d1b6
keywords:
- LB_GETITEMDATA 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LB_GETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bbfdb091fb98c0cf448af1cf5f554f7d0db2b03f53826154f7d62f2f6b27b62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019336"
---
# <a name="lb_getitemdata-message"></a>LB \_ GETITEMDATA 訊息

取得與指定清單方塊專案相關聯的應用程式定義值。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

項目的索引。

Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。 這表示清單方塊不能包含超過32767個專案。 雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是與專案相關聯的值，如果發生錯誤，則為 LB \_ ERR。 如果專案是在主控描繪清單方塊中，而且是以 [**磅 \_ HASSTRINGS**](list-box-styles.md)樣式建立的，則此值會在將專案新增至清單方塊的 [**lb \_ ADDSTRING**](lb-addstring.md)或 [**lb \_ INSERTSTRING**](lb-insertstring.md)訊息的 *lParam* 參數中。 否則，它是 [**LB \_ SETITEMDATA**](lb-setitemdata.md)訊息 *lParam* 中的值。

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

[**LB \_ SETITEMDATA**](lb-setitemdata.md)
</dt> </dl>

 

 





