---
title: 'WM_DDE_TERMINATE 訊息 (的) '
description: 動態資料交換 (DDE) 應用程式 (用戶端或伺服器) 張貼 WM \_ DDE \_ 終止訊息以終止交談。 若要張貼此訊息，請使用下列參數呼叫 PostMessage 函數。
ms.assetid: 4fc162c0-ccc2-44e3-9c07-d49d7426af8b
keywords:
- WM_DDE_TERMINATE 訊息資料交換
topic_type:
- apiref
api_name:
- WM_DDE_TERMINATE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 105b4a7daab87b1311a58a7b5e5805bbd81e73ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094363"
---
# <a name="wm_dde_terminate-message"></a>WM \_ DDE \_ 終止訊息

動態資料交換 (DDE) 應用程式 (用戶端或伺服器) 張貼 **WM \_ DDE \_ 終止** 訊息以終止交談。

若要張貼此訊息，請使用下列參數呼叫 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) 函數。


```C++
#define WM_DDE_TERMINATE       0x03E1
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

張貼訊息之用戶端或伺服器視窗的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="remarks"></a>備註

### <a name="posting"></a>張貼

在等候確認終止時，張貼應用程式不應該將任何其他訊息張貼至接收應用程式。 如果傳送的應用程式接收到來自接收應用程式的 (**WM \_ DDE \_ TERMINATE**) 以外的訊息，則應該刪除伴隨于訊息的任何原子或共用記憶體物件，但不包括與未設定 **fRelease** 成員之 [**wm \_ dde \_**](wm-dde-poke.md)郵件或 [**wm \_ dde \_ 資料**](wm-dde-data.md)訊息相關聯的全域記憶體物件。

### <a name="receiving"></a>接收

用戶端或伺服器應用程式應藉由公佈 **WM \_ DDE \_ 終止** 訊息來回應。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                 |
| 標頭<br/>                   | <dl> <dt> (包含 Windows. h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**WM \_ DDE \_ 資料**](wm-dde-data.md)
</dt> <dt>

[**WM \_ DDE 的進行 \_**](wm-dde-poke.md)
</dt> <dt>

**概念**
</dt> <dt>

[關於動態資料交換](about-dynamic-data-exchange.md)
</dt> </dl>

 

