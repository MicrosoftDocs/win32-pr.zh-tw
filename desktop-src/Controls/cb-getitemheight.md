---
title: 'CB_GETITEMHEIGHT 訊息 (Winuser .h) '
description: 決定下拉式方塊中清單專案的高度或選取欄位。
ms.assetid: 72fba6ca-0a51-4801-bd45-5f5a7d5ebee2
keywords:
- CB_GETITEMHEIGHT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- CB_GETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6e3ad9636c32e40bfa95f1f3b2c209eab42023205e0a967cc91804ec314a103
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089188"
---
# <a name="cb_getitemheight-message"></a>CB \_ GETITEMHEIGHT 訊息

決定下拉式方塊中清單專案的高度或選取欄位。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要取出其高度的下拉式方塊元件。 此參數必須是-1，才能取得選取範圍欄位的高度。 除非下拉式方塊具有 [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) 樣式，否則它必須為零才能取出清單專案的高度。 在此情況下， *wParam* 參數是特定清單專案的以零為基底的索引。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是下拉式方塊中清單專案的高度（以圖元為單位）。 如果下拉式方塊具有 [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) 樣式，它就是 *wParam* 參數所指定之專案的高度。 如果 *wParam* 為-1，則傳回值是 (的編輯控制項高度或下拉式方塊的靜態文字) 部分。 如果發生錯誤，傳回值會是 CB \_ ERR。

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

[**CB \_ SETITEMHEIGHT**](cb-setitemheight.md)
</dt> <dt>

[**WM \_ MEASUREITEM**](wm-measureitem.md)
</dt> </dl>

 

 





