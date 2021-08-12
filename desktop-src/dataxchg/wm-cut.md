---
title: 'WM_CUT 訊息 (Winuser .h) '
description: 應用程式會將 WM \_ 剪下訊息傳送至編輯控制項或下拉式方塊，以刪除 (剪下) 目前的選取專案（如果有的話），並將已刪除的文字複製到 [剪貼簿] 中的 CF \_ 文字格式。
ms.assetid: 6ac45589-3e34-491c-9562-e072ddc478f9
keywords:
- WM_CUT 訊息資料 Exchange
topic_type:
- apiref
api_name:
- WM_CUT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d117e0a942c0d9e24e1a9c40d3d66e605ab8d5cf26bbad0e287e9b03a9b25780
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118304491"
---
# <a name="wm_cut-message"></a>WM \_ 剪下訊息

應用程式會將 **WM \_ 剪** 下訊息傳送至編輯控制項或下拉式方塊，以刪除 (剪下) 目前的選取專案（如果有的話），並將已刪除的文字複製到 [剪貼簿] 中的 [**CF \_ 文字**](standard-clipboard-formats.md) 格式。


```C++
#define WM_CUT                          0x0300
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

藉由傳送 [**EM \_ 復原**](../controls/em-undo.md)訊息的編輯控制項，可復原由 **WM \_ 剪** 下訊息執行的刪除作業。

若要刪除目前的選取範圍，而不將刪除的文字放在剪貼簿上，請使用 [**WM \_ CLEAR**](wm-clear.md) 訊息。

傳送至下拉式方塊時，會由其編輯控制項來處理 **WM \_ 剪** 下訊息。 將此訊息傳送至具有 [**CBS \_ DROPDOWNLIST**](../controls/combo-box-styles.md) 樣式的下拉式方塊時，不會有任何作用。

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

[**WM \_ 清除**](wm-clear.md)
</dt> <dt>

[**WM \_ 複製**](wm-copy.md)
</dt> <dt>

[**WM \_ 貼上**](wm-paste.md)
</dt> <dt>

[**WM \_ 復原**](/windows/desktop/Controls/wm-undo)
</dt> <dt>

**概念**
</dt> <dt>

[剪貼簿](clipboard.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**EM \_ 復原**](../controls/em-undo.md)
</dt> </dl>

 

