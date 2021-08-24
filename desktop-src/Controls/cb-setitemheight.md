---
title: 'CB_SETITEMHEIGHT 訊息 (Winuser .h) '
description: 應用程式會傳送 CB \_ SETITEMHEIGHT 訊息，在下拉式方塊中設定清單專案的高度或選擇欄位。
ms.assetid: 25a01170-5ffc-4d86-b696-706f5375570b
keywords:
- CB_SETITEMHEIGHT 訊息 Windows 控制項
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
ms.openlocfilehash: b97e83d13e66d0a8252fdc1974c775188f8009958a3f286916b0e46ea4f0e88c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119699438"
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
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**CB \_ GETITEMHEIGHT**](cb-getitemheight.md)
</dt> <dt>

[**WM \_ MEASUREITEM**](wm-measureitem.md)
</dt> </dl>

 

 





