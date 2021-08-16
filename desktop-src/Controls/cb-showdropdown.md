---
title: 'CB_SHOWDROPDOWN 訊息 (Winuser .h) '
description: 應用程式傳送 CB \_ SHOWDROPDOWN 訊息，以顯示或隱藏具有 CBS \_ 下拉式清單或 cbs DROPDOWNLIST 樣式之下拉式方塊的清單方塊 \_ 。
ms.assetid: 32b995d7-eed6-4173-8525-0d356dea39b3
keywords:
- CB_SHOWDROPDOWN 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- CB_SHOWDROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c820c65c053f7acbcffb379228ea5f7720476b6d2165ac4988ce8789e912cdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117832236"
---
# <a name="cb_showdropdown-message"></a>CB \_ SHOWDROPDOWN 訊息

應用程式傳送 **CB \_ SHOWDROPDOWN** 訊息，以顯示或隱藏具有 [**CBS \_ 下拉式清單**](combo-box-styles.md) 或 [**cbs \_ DROPDOWNLIST**](combo-box-styles.md) 樣式之下拉式方塊的清單方塊。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定是否要顯示或隱藏下拉式清單方塊的 **布林** 值。 值為 **TRUE** 會顯示清單方塊; **FALSE** 值會將它隱藏。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值一律為 **TRUE**。

## <a name="remarks"></a>備註

此訊息不會影響以 [**CBS \_ 簡單**](combo-box-styles.md) 樣式建立的下拉式方塊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CB \_ GETDROPPEDSTATE**](cb-getdroppedstate.md)
</dt> </dl>

 

 





