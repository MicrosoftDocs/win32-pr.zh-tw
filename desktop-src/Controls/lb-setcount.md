---
title: 'LB_SETCOUNT 訊息 (Winuser .h) '
description: 設定清單方塊中以磅 NODATA 樣式建立的專案計數 \_ ，而不是以磅 HASSTRINGS 樣式建立的專案計數 \_ 。
ms.assetid: 3ebc4237-24d3-443f-86d5-bdcd66a31baf
keywords:
- LB_SETCOUNT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LB_SETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e1b3f68a67de2b7caa77cfd7c9e6f2a5b164e20af42100882fef1aad04eca14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119433940"
---
# <a name="lb_setcount-message"></a>LB \_ SETCOUNT 訊息

設定清單方塊中以 [**磅 \_ NODATA**](list-box-styles.md) 樣式建立的專案計數，而不是以 [**磅 \_ HASSTRINGS**](list-box-styles.md) 樣式建立的專案計數。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定清單方塊中新的專案計數。

Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。 這表示清單方塊不能包含超過32767個專案。 雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果發生錯誤，傳回值為 LB \_ ERR。 如果記憶體不足，無法儲存專案，則傳回值為 LB \_ ERRSPACE。

## <a name="remarks"></a>備註

只有使用 [**磅 \_ NODATA**](list-box-styles.md)樣式建立的清單方塊才支援 **LB \_ SETCOUNT** 訊息，且不會以 [**磅 \_ HASSTRINGS**](list-box-styles.md)樣式建立。 所有其他清單方塊都會傳回 LB \_ ERR。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LB \_ GETCOUNT**](lb-getcount.md)
</dt> </dl>

 

 





