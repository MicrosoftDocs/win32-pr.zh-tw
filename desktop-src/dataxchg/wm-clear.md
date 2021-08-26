---
title: 'WM_CLEAR 訊息 (Winuser .h) '
description: 應用程式會將 WM \_ 清除訊息傳送至編輯控制項或下拉式方塊，以從編輯控制項中刪除 (清除) 目前的選取專案（如果有的話）。
ms.assetid: 6730a725-01ec-4821-9ffc-1ea267d665b3
keywords:
- WM_CLEAR 訊息資料 Exchange
topic_type:
- apiref
api_name:
- WM_CLEAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6820a9134f112b51474cd5b73e8545583cb02969b02a1bd1428138ebf1049dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029108"
---
# <a name="wm_clear-message"></a>WM \_ 清除訊息

應用程式會將 **WM \_ 清除** 訊息傳送至編輯控制項或下拉式方塊，以從編輯控制項中刪除 (清除) 目前的選取專案（如果有的話）。


```C++
#define WM_CLEAR                        0x0303
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用此參數，且必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用此參數，且必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

藉由傳送 [**EM \_ 復原**](../controls/em-undo.md)訊息的編輯控制項，可復原 **WM \_ 清除** 訊息所執行的刪除作業。

若要刪除目前的選取範圍，並將已刪除的內容放到剪貼簿上，請使用 [**WM \_ 剪**](wm-cut.md) 下訊息。

傳送至下拉式方塊時，會由其編輯控制項來處理 **WM \_ 清除** 訊息。 將此訊息傳送至具有 [**CBS \_ DROPDOWNLIST**](../controls/combo-box-styles.md) 樣式的下拉式方塊時，不會有任何作用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**WM \_ 複製**](wm-copy.md)
</dt> <dt>

[**WM \_ 剪下**](wm-cut.md)
</dt> <dt>

[**WM \_ 貼上**](wm-paste.md)
</dt> <dt>

[**WM \_ 復原**](/windows/desktop/Controls/wm-undo)
</dt> <dt>

**概念**
</dt> <dt>

[剪貼簿](clipboard.md)
</dt> </dl>

 

