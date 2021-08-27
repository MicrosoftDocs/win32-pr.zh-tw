---
title: 'CB_SETDROPPEDWIDTH 訊息 (Winuser .h) '
description: 應用程式會傳送 CB \_ SETDROPPEDWIDTH 訊息，以使用 cbs \_ 下拉式清單或 cbs DROPDOWNLIST 樣式來設定下拉式方塊清單方塊的最小允許寬度（以圖元為單位） \_ 。
ms.assetid: 89f44733-aebe-44ea-b62d-8bd988f1bd6f
keywords:
- CB_SETDROPPEDWIDTH 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- CB_SETDROPPEDWIDTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05d59aee89c4be18ba8e5013fa1a1e685a56b727d293c833c7f99140b683efeb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089048"
---
# <a name="cb_setdroppedwidth-message"></a>CB \_ SETDROPPEDWIDTH 訊息

應用程式會傳送 **CB \_ SETDROPPEDWIDTH** 訊息，以使用 [**Cbs \_ 下拉式清單**](combo-box-styles.md) 或 [**cbs \_ DROPDOWNLIST**](combo-box-styles.md) 樣式來設定下拉式方塊清單方塊的最小允許寬度（以圖元為單位）。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

清單方塊的允許寬度下限（以圖元為單位）。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果訊息成功，傳回值就是清單方塊的新寬度。

如果訊息失敗，則傳回值為 CB \_ ERR。

## <a name="remarks"></a>備註

根據預設，下拉式清單方塊的最小允許寬度為零。 清單方塊的寬度可以是允許的最小寬度或下拉式方塊寬度（以較大者為准）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CB \_ GETDROPPEDWIDTH**](cb-getdroppedwidth.md)
</dt> </dl>

 

 





