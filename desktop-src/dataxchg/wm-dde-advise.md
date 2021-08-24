---
title: 'WM_DDE_ADVISE 訊息 (的) '
description: 動態資料交換 (dde) 用戶端應用程式會將 WM \_ DDE \_ 建議訊息張貼至 dde 伺服器應用程式，要求伺服器在專案變更時，提供資料項目的更新。
ms.assetid: b00db740-36a7-4487-abbf-d74b12f5212a
keywords:
- WM_DDE_ADVISE 訊息資料 Exchange
topic_type:
- apiref
api_name:
- WM_DDE_ADVISE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c651144b4f09cf53f07c0f1860625cab8277e5c8a9532ee864b9ec1b1c927323
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636218"
---
# <a name="wm_dde_advise-message"></a>WM \_ DDE \_ 建議訊息

動態資料交換 (dde) 用戶端應用程式會將 **WM \_ DDE \_ 建議** 訊息張貼至 dde 伺服器應用程式，要求伺服器在專案變更時，提供資料項目的更新。

若要張貼此訊息，請使用下列參數呼叫 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) 函數。


```C++
#define WM_DDE_ADVISE      0x03E2
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

張貼訊息之用戶端視窗的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

低序位單字是全域記憶體物件的控制碼，其中包含指定如何傳送資料的 [**DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise) 結構。

高序位字包含識別所要求資料項目的 atom。

</dd> </dl>

## <a name="remarks"></a>備註

如果用戶端應用程式支援單一主題和專案的多個剪貼簿格式，它可以張貼主題和專案的多個 **WM \_ DDE \_ 建議** 訊息，並指定每個訊息的不同剪貼簿格式。 請注意，伺服器只能針對經常性存取資料連結支援多種格式，而不支援暖資料連結。

### <a name="posting"></a>張貼

用戶端應用程式會呼叫 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)函式，而不是 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)函式，以張貼 **WM \_ DDE \_ 建議** 訊息。

用戶端應用程式會使用 [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) 函數來配置全域記憶體物件。 它會使用 [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) 函數來配置 atom。

用戶端應用程式必須藉由呼叫 [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)函數或 [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)函數，來建立或重複使用 **WM \_ DDE \_ 建議** *lParam* 參數。

如果接收 (伺服器) 應用程式以負的 [**WM \_ DDE \_ 確認**](wm-dde-ack.md) 訊息回應，則張貼應用程式必須刪除物件。

**FRelease** 旗標不會用於 **wm \_ dde \_ 建議** 訊息中，但其資料釋出行為類似于 [**wm \_ Dde \_ 資料**](wm-dde-data.md)和 [**wm \_ dde \_**](wm-dde-poke.md)訊息（其中 **fRelease** 為 **TRUE**）。

### <a name="receiving"></a>接收

伺服器應用程式會張貼 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息，以回應正面或負面。 張貼 **WM \_ DDE \_** 通知時，應用程式可以重複使用 atom 或將它刪除，然後建立一個新的。 如果 **WM \_ DDE \_** 通知訊息是正數，則應用程式應該刪除全域記憶體物件，否則應用程式不應該刪除物件。

伺服器必須藉由呼叫 [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)函數或 [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)函數，來建立或重複使用 [**WM \_ DDE \_ ACK**](wm-dde-ack.md) *lParam* 參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                 |
| 標頭<br/>                   | <dl> <dt>Dde. h (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise)
</dt> <dt>

[**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[**WM \_ DDE \_ ACK**](wm-dde-ack.md)
</dt> <dt>

[**WM \_ DDE \_ 資料**](wm-dde-data.md)
</dt> <dt>

[**WM \_ DDE 的進行 \_**](wm-dde-poke.md)
</dt> <dt>

[**WM \_ DDE \_ 要求**](wm-dde-request.md)
</dt> <dt>

**概念**
</dt> <dt>

[關於動態資料交換](about-dynamic-data-exchange.md)
</dt> </dl>

 

