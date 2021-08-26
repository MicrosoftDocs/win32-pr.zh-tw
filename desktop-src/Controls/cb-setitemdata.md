---
title: 'CB_SETITEMDATA 訊息 (Winuser .h) '
description: 應用程式會傳送 CB \_ SETITEMDATA 訊息，以設定與下拉式方塊中指定之專案相關聯的值。
ms.assetid: 8be9eb57-a635-4c52-9838-556368813c74
keywords:
- CB_SETITEMDATA 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- CB_SETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7abd50db9050178bc5d8d3b8ff556bce90f340fdb8d6692a514b0348aceeeab3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089008"
---
# <a name="cb_setitemdata-message"></a>CB \_ SETITEMDATA 訊息

應用程式會傳送 **CB \_ SETITEMDATA** 訊息，以設定與下拉式方塊中指定之專案相關聯的值。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定專案的以零為基底的索引。

</dd> <dt>

*lParam* 
</dt> <dd>

指定要與專案相關聯的新值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果發生錯誤，傳回值會是 CB \_ ERR。

## <a name="remarks"></a>備註

如果指定的專案在建立時沒有 [**CBS \_ HASSTRINGS**](combo-box-styles.md)樣式的主控描繪下拉式方塊中，則此訊息會取代將專案新增至下拉式方塊的 [**cb \_ ADDSTRING**](cb-addstring.md)或 [**cb \_ INSERTSTRING**](cb-insertstring.md)訊息之 *lParam* 參數中的值。

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

[**CB \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**CB \_ GETITEMDATA**](cb-getitemdata.md)
</dt> <dt>

[**CB \_ INSERTSTRING**](cb-insertstring.md)
</dt> </dl>

 

 





