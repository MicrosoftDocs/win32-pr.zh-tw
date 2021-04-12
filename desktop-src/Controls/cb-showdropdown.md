---
title: 'CB_SHOWDROPDOWN 訊息 (Winuser .h) '
description: 應用程式傳送 CB \_ SHOWDROPDOWN 訊息，以顯示或隱藏具有 CBS \_ 下拉式清單或 cbs DROPDOWNLIST 樣式之下拉式方塊的清單方塊 \_ 。
ms.assetid: 32b995d7-eed6-4173-8525-0d356dea39b3
keywords:
- CB_SHOWDROPDOWN message Windows 控制項
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
ms.openlocfilehash: fb66e9a0ecf3b6680fce9aca7f680fd6e6fd13e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105605"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CB \_ GETDROPPEDSTATE**](cb-getdroppedstate.md)
</dt> </dl>

 

 





