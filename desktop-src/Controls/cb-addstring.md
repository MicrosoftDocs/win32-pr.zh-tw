---
title: 'CB_ADDSTRING 訊息 (Winuser .h) '
description: 將字串加入下拉式方塊的清單方塊中。 如果下拉式方塊沒有 CBS \_ 排序樣式，則會將字串加入至清單結尾。 否則，會將字串插入清單中，並排序清單。
ms.assetid: 201bcb7b-e7d1-41e6-8eb7-a5864b659a52
keywords:
- CB_ADDSTRING message Windows 控制項
topic_type:
- apiref
api_name:
- CB_ADDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dda16367ec24e869f6cb664e89751d7a13efec3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934917"
---
# <a name="cb_addstring-message"></a>CB \_ ADDSTRING 訊息

將字串加入下拉式方塊的清單方塊中。 如果下拉式方塊沒有 [**CBS \_ 排序**](combo-box-styles.md) 樣式，則會將字串加入至清單結尾。 否則，會將字串插入清單中，並排序清單。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

要加入之以 null 終止之字串的 **LPCTSTR** 指標。 如果您建立具有主控描繪樣式的下拉式方塊，但沒有 [**CBS \_ HASSTRINGS**](combo-box-styles.md) 樣式，則 *lParam* 參數的值會儲存為專案資料，而不是另一個指向的字串。 您可以藉由傳送 [**CB \_ GETITEMDATA**](cb-getitemdata.md) 或 [**cb \_ SETITEMDATA**](cb-setitemdata.md) 訊息來取出或修改專案資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是下拉式方塊清單方塊中字串的以零為基底的索引。 如果發生錯誤，傳回值會是 CB \_ ERR。 如果空間不足，無法存放新的字串，它就是 CB \_ ERRSPACE。

## <a name="remarks"></a>備註

如果您建立具有 [**cbs \_ 排序**](combo-box-styles.md) 樣式但沒有 [**cbs \_ HASSTRINGS**](combo-box-styles.md) 樣式的主控描繪下拉式列示方塊，則會將 [**WM \_ COMPAREITEM**](wm-compareitem.md) 訊息傳送一或多次至下拉式方塊的擁有者，以便將新專案正確地放在清單中。

若要將字串插入清單中的特定位置，請使用 [**CB \_ INSERTSTRING**](cb-insertstring.md) 訊息。

如果下拉式方塊具有 [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) 樣式，而且您新增的字串範圍超過下拉式方塊，請傳送 [**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) 訊息，以確保會顯示水準捲軸。

**Comclt32.dll 5.0 版或更新版本：** 如果設定了 [ [**cbs \_ 小寫**](combo-box-styles.md) ] 或 [ [**cbs \_ 大寫**](combo-box-styles.md) ]，則 Unicode 版本的 **CB \_ ADDSTRING** 會改變字串。 如果使用唯讀的全域記憶體，這會導致應用程式失敗。

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

[**CB \_ 目錄**](cb-dir.md)
</dt> <dt>

[**CB \_ INSERTSTRING**](cb-insertstring.md)
</dt> <dt>

[**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)
</dt> <dt>

[**WM \_ COMPAREITEM**](wm-compareitem.md)
</dt> </dl>

 

