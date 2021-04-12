---
title: 'CB_INSERTSTRING 訊息 (Winuser .h) '
description: 將字串或專案資料插入下拉式方塊的清單中。 與 CB ADDSTRING 訊息不同的是 \_ ，cb \_ INSERTSTRING 訊息並不會讓您排序包含 CBS \_ 排序樣式的清單。
ms.assetid: b9067b4e-afca-4c78-9ca2-c717b99c7459
keywords:
- CB_INSERTSTRING message Windows 控制項
topic_type:
- apiref
api_name:
- CB_INSERTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d050980137bc34652cb2fce39b9f188f4d5cd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465264"
---
# <a name="cb_insertstring-message"></a>CB \_ INSERTSTRING 訊息

將字串或專案資料插入下拉式方塊的清單中。 與 [**cb \_ ADDSTRING**](cb-addstring.md) 訊息不同的是， **cb \_ INSERTSTRING** 訊息並不會讓您排序包含 [**CBS \_ 排序**](combo-box-styles.md) 樣式的清單。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

以零為基底的索引，這是插入字串的位置。 如果此參數為-1，則會將字串加入至清單結尾。

</dd> <dt>

*lParam* 
</dt> <dd>

要插入之以 null 終止之字串的指標。 如果您建立具有主控描繪樣式的下拉式方塊，但沒有 [**CBS \_ HASSTRINGS**](combo-box-styles.md) 樣式，則會儲存 *lParam* 參數的值，而不是它所指向的字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是插入字串之位置的索引。 如果發生錯誤，傳回值會是 CB \_ ERR。 如果沒有足夠的可用空間來儲存新的字串，則它是 CB \_ ERRSPACE。

如果下拉式方塊具有 [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) 樣式，而且您插入的字串範圍超過下拉式方塊，您應該傳送 [**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) 訊息，以確保會顯示水準捲軸。

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

[**CB \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)
</dt> <dt>

[**CB \_ 目錄**](cb-dir.md)
</dt> </dl>

 

