---
title: 'CB_SELECTSTRING 訊息 (Winuser .h) '
description: 在下拉式方塊清單中搜尋以指定字串中的字元開頭的專案。 如果找到相符的專案，就會選取它，並將其複製到編輯控制項。
ms.assetid: c08dff72-7e44-40ed-8b64-513359292829
keywords:
- CB_SELECTSTRING 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- CB_SELECTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bedef20646664e37405c97a97f9e49147cad8acc08c05e33172e44a34298f5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019966"
---
# <a name="cb_selectstring-message"></a>CB \_ SELECTSTRING 訊息

在下拉式方塊清單中搜尋以指定字串中的字元開頭的專案。 如果找到相符的專案，就會選取它，並將其複製到編輯控制項。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

在要搜尋的第一個專案之前，專案以零為起始的索引。 當搜尋到達清單底部時，它會從清單頂端繼續至 *wParam* 參數所指定的專案。 如果 *wParam* 為-1，就會從一開始就搜尋整個清單。

</dd> <dt>

*lParam* 
</dt> <dd>

以 null 結束的字串指標，其中包含要搜尋的字元。 搜尋不區分大小寫，因此這個字串可以包含任何大小寫字母的組合。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果找到該字串，則傳回值是所選取專案的索引。 如果搜尋失敗，則傳回值為 CB ERR， \_ 而且目前的選取範圍不會變更。

## <a name="remarks"></a>備註

只有當起始點的字元符合前置詞字串中的字元時，才會選取字串。

如果您建立具有主控描繪樣式的下拉式方塊，但沒有 [**CBS \_ HASSTRINGS**](combo-box-styles.md) 樣式，則 **CB \_ SELECTSTRING** 訊息的作用取決於您是否使用 [**cbs \_ 排序**](combo-box-styles.md) 樣式。 如果使用了 **CBS \_ 排序** 樣式，系統會將 [**WM \_ COMPAREITEM**](wm-compareitem.md) 訊息傳送給下拉式方塊的擁有者，以判斷哪一個專案符合指定的字串。 如果您未使用 **CBS \_ 排序** 樣式，則 **CB \_ SELECTSTRING** 會嘗試比對 **DWORD** 值與 *lParam* 參數的值。

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

[**CB \_ FINDSTRING**](cb-findstring.md)
</dt> <dt>

[**CB \_ FINDSTRINGEXACT**](cb-findstringexact.md)
</dt> <dt>

[**CB \_ SETCURSEL**](cb-setcursel.md)
</dt> <dt>

[**WM \_ COMPAREITEM**](wm-compareitem.md)
</dt> </dl>

 

 





