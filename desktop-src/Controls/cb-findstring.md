---
title: 'CB_FINDSTRING 訊息 (Winuser .h) '
description: 在下拉式方塊的清單方塊中，搜尋以指定字串中的字元開頭的專案。
ms.assetid: 872a72d5-4d8e-41c7-ac6b-eeb571403623
keywords:
- CB_FINDSTRING message Windows 控制項
topic_type:
- apiref
api_name:
- CB_FINDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 295300790a27a956bce953e4e293c07c22ec0d81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094580"
---
# <a name="cb_findstring-message"></a>CB \_ FINDSTRING 訊息

在下拉式方塊的清單方塊中，搜尋以指定字串中的字元開頭的專案。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

在要搜尋的第一個專案之前，專案以零為起始的索引。 當搜尋到達清單方塊的底部時，它會從清單方塊的頂端繼續移回 *wParam* 參數所指定的專案。 如果 *wParam* 為-1，就會從一開始就搜尋整個清單方塊。

</dd> <dt>

*lParam* 
</dt> <dd>

以 null 結束的字串指標，其中包含要搜尋的字元。 搜尋不區分大小寫，因此這個字串可以包含任何大小寫字母的組合。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是相符專案的以零為基底的索引。 如果搜尋失敗，則為 CB \_ 錯誤。

## <a name="remarks"></a>備註

如果您建立具有主控描繪樣式的下拉式方塊，但沒有 [**CBS \_ HASSTRINGS**](combo-box-styles.md) 樣式，則 **CB \_ FINDSTRING** 訊息的作用取決於您的應用程式是否使用 [**cbs \_ 排序**](combo-box-styles.md) 樣式。 如果您使用 **CBS \_ 排序** 樣式，則會將 [**WM \_ COMPAREITEM**](wm-compareitem.md) 訊息傳送給下拉式方塊的擁有者，以判斷哪一個專案符合指定的字串。 如果您未使用 **CBS \_ 排序** 樣式， **CB \_ FINDSTRING** 訊息會搜尋符合 *lParam* 參數值的清單專案。

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

[**CB \_ FINDSTRINGEXACT**](cb-findstringexact.md)
</dt> <dt>

[**CB \_ SELECTSTRING**](cb-selectstring.md)
</dt> <dt>

[**CB \_ SETCURSEL**](cb-setcursel.md)
</dt> <dt>

[**WM \_ COMPAREITEM**](wm-compareitem.md)
</dt> </dl>

 

 





