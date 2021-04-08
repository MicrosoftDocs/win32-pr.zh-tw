---
title: 'CB_GETITEMHEIGHT 訊息 (Winuser .h) '
description: 決定下拉式方塊中清單專案的高度或選取欄位。
ms.assetid: 72fba6ca-0a51-4801-bd45-5f5a7d5ebee2
keywords:
- CB_GETITEMHEIGHT message Windows 控制項
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
ms.openlocfilehash: c4aac9d8f9a430c056f8b91a9306d77c182f4c96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843572"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**CB \_ SETITEMHEIGHT**](cb-setitemheight.md)
</dt> <dt>

[**WM \_ MEASUREITEM**](wm-measureitem.md)
</dt> </dl>

 

 





