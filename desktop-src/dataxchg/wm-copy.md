---
title: 'WM_COPY 訊息 (Winuser .h) '
description: 應用程式會將 WM \_ 複製訊息傳送至編輯控制項或下拉式方塊，以 CF 文字格式將目前的選取範圍複製到剪貼簿 \_ 。
ms.assetid: dcac3ad3-1e70-4b71-accd-261587224e60
keywords:
- WM_COPY 訊息資料交換
topic_type:
- apiref
api_name:
- WM_COPY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b298248d75b1d25d1bfef8347347fe2f1a6c7916
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "106986452"
---
# <a name="wm_copy-message"></a>WM \_ 複製訊息

應用程式會將 **WM \_ 複製** 訊息傳送至編輯控制項或下拉式方塊，以 [**CF \_ 文字**](standard-clipboard-formats.md) 格式將目前的選取範圍複製到剪貼簿。


```C++
#define WM_COPY                         0x0301
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

在成功時傳回非零值，否則傳回零。

## <a name="remarks"></a>備註

傳送至下拉式方塊時，會由其編輯控制項來處理 **WM \_ 複製** 訊息。 將此訊息傳送至具有 [**CBS \_ DROPDOWNLIST**](../controls/combo-box-styles.md) 樣式的下拉式方塊時，不會有任何作用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**WM \_ 清除**](wm-clear.md)
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

 

