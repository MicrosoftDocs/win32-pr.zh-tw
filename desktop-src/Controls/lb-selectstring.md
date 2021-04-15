---
title: 'LB_SELECTSTRING 訊息 (Winuser .h) '
description: 在清單方塊中搜尋以指定字串中的字元開頭的專案。 如果找到相符的專案，就會選取該專案。
ms.assetid: fd443ade-665d-439a-8951-3d9fed50695b
keywords:
- LB_SELECTSTRING message Windows 控制項
topic_type:
- apiref
api_name:
- LB_SELECTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5963ea6530038e17bc7f23d9ab66eba14ca0b05d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466529"
---
# <a name="lb_selectstring-message"></a>LB \_ SELECTSTRING 訊息

在清單方塊中搜尋以指定字串中的字元開頭的專案。 如果找到相符的專案，就會選取該專案。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

搜尋第一個項目之前，項目以零為起始的索引。 當搜尋到達清單方塊的底部時，它會從清單方塊的頂端繼續移回 *wParam* 參數所指定的專案。 如果 *wParam* 為-1，就會從一開始就搜尋整個清單方塊。

Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。 這表示清單方塊不能包含超過32767個專案。 雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。

</dd> <dt>

*lParam* 
</dt> <dd>

以 null 結束的字串指標，其中包含要搜尋的前置詞。 搜尋不會區分大小寫，因此這個字串可以包含任何大小寫字母的組合。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果搜尋成功，傳回值就是所選取專案的索引。 如果搜尋失敗，則傳回值為 LB ERR， \_ 而且目前的選取範圍不會變更。

## <a name="remarks"></a>備註

如有必要，會滾動清單方塊以將選取的專案帶到視野中。

請勿將此訊息與具有 [**磅 \_ MULTIPLESEL**](list-box-styles.md) 或 [**磅 \_ EXTENDEDSEL**](list-box-styles.md) 樣式的清單方塊一起使用。

只有當專案的初始字元與 *lParam* 參數所指定之字串中的字元相符時，才會選取該專案。

如果清單方塊具有擁有者繪製的樣式，而不是 [**磅 \_ HASSTRINGS**](list-box-styles.md) 樣式，則 **LB \_ SELECTSTRING** 所採取的動作取決於是否使用 [**磅 \_ 排序**](list-box-styles.md) 樣式。 如果使用了 **磅 \_ 排序** ，系統會將 [**WM \_ COMPAREITEM**](wm-compareitem.md) 訊息傳送給清單方塊擁有者，以判斷哪一個專案符合指定的字串。 否則， **LB \_ SELECTSTRING** 會嘗試尋找具有 long 值的專案， (提供為符合 *lParam* 參數的 [**lb \_ ADDSTRING**](lb-addstring.md)或 [**lb \_ INSERTSTRING**](lb-insertstring.md) message) 的 *lParam* 參數。

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

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**LB \_ FINDSTRING**](lb-findstring.md)
</dt> <dt>

[**LB \_ INSERTSTRING**](lb-insertstring.md)
</dt> </dl>

 

 





