---
title: 'WM_PASTE 訊息 (Winuser .h) '
description: 應用程式會將 WM \_ 貼上訊息傳送至編輯控制項或下拉式方塊，以將剪貼簿目前的內容複寫到目前插入號位置的編輯控制項。 只有當剪貼簿包含 CF 文字格式的資料時，才會插入資料 \_ 。
ms.assetid: 6830b511-986f-46ef-a977-7adedffe86ea
keywords:
- WM_PASTE 訊息資料 Exchange
topic_type:
- apiref
api_name:
- WM_PASTE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a3cc1815349a2194d5dd7e2a65eb1c9ae77a2947f41361a90e92bae73357f81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499118"
---
# <a name="wm_paste-message"></a>WM \_ 貼上訊息

應用程式會將 **WM \_ 貼** 上訊息傳送至編輯控制項或下拉式方塊，以將剪貼簿目前的內容複寫到目前插入號位置的編輯控制項。 只有當剪貼簿包含 [**CF \_ 文字**](standard-clipboard-formats.md) 格式的資料時，才會插入資料。


```C++
#define WM_PASTE                        0x0302
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

傳送至下拉式方塊時，會由其編輯控制項來處理 **WM \_ 貼** 上訊息。 將此訊息傳送至具有 [**CBS \_ DROPDOWNLIST**](../controls/combo-box-styles.md) 樣式的下拉式方塊時，不會有任何作用。

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

[**WM \_ 剪下**](wm-cut.md)
</dt> <dt>

[**WM \_ 復原**](/windows/desktop/Controls/wm-undo)
</dt> <dt>

**概念**
</dt> <dt>

[剪貼簿](clipboard.md)
</dt> </dl>

 

