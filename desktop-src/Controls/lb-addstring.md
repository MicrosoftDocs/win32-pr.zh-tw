---
title: 'LB_ADDSTRING 訊息 (Winuser .h) '
description: 將字串加入至清單方塊。 如果清單方塊沒有磅 \_ 排序樣式，則會將字串加入至清單結尾。 否則，會將字串插入清單中，並排序清單。
ms.assetid: 924d9232-6e38-49c3-aa3e-19efd46b01ba
keywords:
- LB_ADDSTRING 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LB_ADDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 552e3c344a730ad1fc00337cafa71a19a6586b9a4c95f2ed1ebce352d9d909aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118671684"
---
# <a name="lb_addstring-message"></a>LB \_ ADDSTRING 訊息

將字串加入至清單方塊。 如果清單方塊沒有 [**磅 \_ 排序**](list-box-styles.md) 樣式，則會將字串加入至清單結尾。 否則，會將字串插入清單中，並排序清單。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

要加入之以 null 結束的字串指標。

如果清單方塊有擁有者繪製的樣式，而不是 [**磅 \_ HASSTRINGS**](list-box-styles.md) 樣式，則此參數會儲存為專案資料，而不是字串。 您可以傳送 **LB \_ GETITEMDATA** 和 **lb \_ SETITEMDATA** 訊息來取得或修改專案資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是清單方塊中字串以零為基底的索引。 如果發生錯誤，傳回值為 LB \_ ERR。 如果空間不足，無法儲存新的字串，則傳回值為 LB \_ ERRSPACE。

## <a name="remarks"></a>備註

如果清單方塊具有主控描繪樣式和 [**磅 \_ 排序**](list-box-styles.md) 樣式（而不是 [**磅 \_ HASSTRINGS**](list-box-styles.md) 樣式），系統會將 [**WM \_ COMPAREITEM**](wm-compareitem.md) 訊息一次或多次傳送給清單方塊的擁有者，以便在清單方塊中正確地放置新專案。

[**LB \_ INITSTORAGE**](lb-initstorage.md)訊息有助於加速初始化具有大量專案 (超過 100) 的清單方塊。 它會保留指定的記憶體數量，讓後續的 **LB \_ ADDSTRING** 訊息能以最短的時間進行。 您可以使用 *wParam* 和 *lParam* 參數的估計值。 如果您高估值，則會配置額外的記憶體;如果您低估了，一般配置會用於超出要求數量的專案。

如果清單方塊具有 [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) 樣式，而且您新增的字串範圍超出清單方塊，請傳送 [**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) 訊息，以確保會顯示水準捲軸。

若為 ANSI 應用程式，系統會使用 CP ACP 將清單方塊中的文字轉換成 Unicode \_ 。 這可能會造成問題。 例如，日文 Windows 的非 Unicode 清單方塊中有重音的羅馬字元，將會出現混亂。 若要修正此問題，請將應用程式編譯為 Unicode 或使用主控描繪清單方塊。

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

[**LB \_ DELETESTRING**](lb-deletestring.md)
</dt> <dt>

[**LB \_ INSERTSTRING**](lb-insertstring.md)
</dt> <dt>

[**LB \_ SELECTSTRING**](lb-selectstring.md)
</dt> <dt>

[**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)
</dt> <dt>

[**WM \_ COMPAREITEM**](wm-compareitem.md)
</dt> </dl>

 

