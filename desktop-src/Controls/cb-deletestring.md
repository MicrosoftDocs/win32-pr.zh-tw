---
title: 'CB_DELETESTRING 訊息 (Winuser .h) '
description: 刪除下拉式方塊的清單方塊中的字串。
ms.assetid: 8d526796-04ef-4c01-94d6-fb50e6fef27b
keywords:
- CB_DELETESTRING message Windows 控制項
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
ms.openlocfilehash: eb0d3900c86874db1113c219fd9f7967c5f6bb6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106002"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**CB \_ RESETCONTENT**](cb-resetcontent.md)
</dt> <dt>

[**WM \_ DELETEITEM**](wm-deleteitem.md)
</dt> </dl>

 

 





