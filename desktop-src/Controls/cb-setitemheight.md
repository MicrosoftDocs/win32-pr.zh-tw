---
title: 'CB_SETITEMHEIGHT 訊息 (Winuser .h) '
description: 應用程式會傳送 CB \_ SETITEMHEIGHT 訊息，在下拉式方塊中設定清單專案的高度或選擇欄位。
ms.assetid: 25a01170-5ffc-4d86-b696-706f5375570b
keywords:
- CB_SETITEMHEIGHT message Windows 控制項
topic_type:
- apiref
api_name:
- CB_SETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e46be007cdea17857e5d8ec42a12228821539d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967756"
---
# <a name="cb_setitemheight-message"></a>CB \_ SETITEMHEIGHT 訊息

應用程式會傳送 **CB \_ SETITEMHEIGHT** 訊息，在下拉式方塊中設定清單專案的高度或選擇欄位。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定要為其設定高度之下拉式方塊的元件。

此參數必須為1，才能設定選取範圍欄位的高度。 除非下拉式方塊具有 [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) 樣式，否則它必須為零以設定清單專案的高度。 在此情況下， *wParam* 參數是特定清單專案的以零為基底的索引。

</dd> <dt>

*lParam* 
</dt> <dd>

指定 *wParam* 所識別之下拉式方塊元件的高度（以圖元為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果索引或高度無效，則傳回值為 CB \_ ERR。

## <a name="remarks"></a>備註

下拉式方塊中的選取欄位高度會與清單專案的高度分開設定。 應用程式必須確保選取欄位的高度不會小於特定清單專案的高度。

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

[**CB \_ GETITEMHEIGHT**](cb-getitemheight.md)
</dt> <dt>

[**WM \_ MEASUREITEM**](wm-measureitem.md)
</dt> </dl>

 

 





