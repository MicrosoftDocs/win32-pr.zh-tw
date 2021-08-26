---
title: 'CB_DELETESTRING 訊息 (Winuser .h) '
description: 刪除下拉式方塊的清單方塊中的字串。
ms.assetid: 8d526796-04ef-4c01-94d6-fb50e6fef27b
keywords:
- CB_DELETESTRING 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- CB_DELETESTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0bed1d654b86ffeb4a02c780678822e1999847ef0e163e35ecba081af099f66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120063578"
---
# <a name="cb_deletestring-message"></a>CB \_ DELETESTRING 訊息

刪除下拉式方塊的清單方塊中的字串。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要刪除之字串的以零為基底的索引。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是清單中剩餘字串的計數。 如果 *wParam* 參數指定的索引大於清單中的專案數，則傳回值為 CB \_ ERR。

## <a name="remarks"></a>備註

如果您建立具有主控描繪樣式但沒有 [**CBS \_ HASSTRINGS**](combo-box-styles.md) 樣式的下拉式方塊，系統會將 [**WM \_ DELETEITEM**](wm-deleteitem.md) 訊息傳送給下拉式方塊的擁有者，讓應用程式可以釋出與該專案相關聯的任何其他資料。

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

[**CB \_ RESETCONTENT**](cb-resetcontent.md)
</dt> <dt>

[**WM \_ DELETEITEM**](wm-deleteitem.md)
</dt> </dl>

 

 





