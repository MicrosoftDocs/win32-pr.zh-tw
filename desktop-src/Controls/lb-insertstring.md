---
title: 'LB_INSERTSTRING 訊息 (Winuser .h) '
description: 將字串或專案資料插入清單方塊中。 與 LB ADDSTRING 訊息不同的是 \_ ，lb \_ INSERTSTRING 訊息並不會造成具有磅排序樣式的清單進行 \_ 排序。
ms.assetid: dfaa742d-2f42-4485-aed5-cda8ca9ba66c
keywords:
- LB_INSERTSTRING message Windows 控制項
topic_type:
- apiref
api_name:
- LB_INSERTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5858af0e0229f90a5ed9928e7478d0ac9a71c8f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105545"
---
# <a name="lb_insertstring-message"></a>LB \_ INSERTSTRING 訊息

將字串或專案資料插入清單方塊中。 與 [**lb \_ ADDSTRING**](lb-addstring.md) 訊息不同的是， **lb \_ INSERTSTRING** 訊息並不會造成具有 [**磅 \_ 排序**](list-box-styles.md) 樣式的清單進行排序。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

以零為基底的索引，這是插入字串的位置。 如果此參數為-1，則會將字串加入至清單結尾。

</dd> <dt>

*lParam* 
</dt> <dd>

要插入之以 null 終止之字串的指標。 如果清單方塊有擁有者繪製的樣式，而不是 [**磅 \_ HASSTRINGS**](list-box-styles.md) 樣式，則此參數會儲存為專案資料，而不是字串。 您可以傳送 [**LB \_ GETITEMDATA**](lb-getitemdata.md) 和 [**lb \_ SETITEMDATA**](lb-setitemdata.md) 訊息來取得或修改專案資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是插入字串之位置的索引。 如果發生錯誤，傳回值為 LB \_ ERR。 如果空間不足，無法儲存新的字串，則傳回值為 LB \_ ERRSPACE。

## <a name="remarks"></a>備註

[**LB \_ INITSTORAGE**](lb-initstorage.md)訊息有助於加速初始化具有大量專案 (超過 100) 的清單方塊。 它會保留指定的記憶體數量，讓後續的 **LB \_ INSERTSTRING** 訊息能以最短的時間進行。 您可以使用 *wParam* 和 *lParam* 參數的估計值。 如果您高估值，則會配置額外的記憶體;如果您低估了，一般配置會用於超出要求數量的專案。

如果清單方塊具有 [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) 樣式，而且您插入的字串範圍超出清單方塊，請傳送 [**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) 訊息以確保水準捲軸出現。

若為 ANSI 應用程式，系統會使用 CP ACP 將清單方塊中的文字轉換成 Unicode \_ 。 這可能會造成問題。 例如，在日文視窗的非 Unicode 清單方塊中，重音的羅馬字元將會出現模糊。 若要修正此問題，請將應用程式編譯為 Unicode 或使用主控描繪清單方塊。

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

[**LB \_ SELECTSTRING**](lb-selectstring.md)
</dt> <dt>

[**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)
</dt> </dl>

 

