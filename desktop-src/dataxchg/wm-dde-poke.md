---
title: 'WM_DDE_POKE 訊息 (的) '
description: 動態資料交換 (的 DDE) 用戶端應用程式會將 WM \_ DDE \_ 郵件訊息張貼至 DDE 伺服器應用程式。
ms.assetid: 848142b7-a7ef-4206-9bb3-b511388cfaaa
keywords:
- WM_DDE_POKE 訊息資料交換
topic_type:
- apiref
api_name:
- WM_DDE_POKE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 001697cbd5328b9c8d9eb72ebddff5f86ef6381c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686524"
---
# <a name="wm_dde_poke-message"></a>WM \_ DDE \_ 訊息

動態資料交換 (的 DDE) 用戶端應用程式會將 **WM \_ DDE \_** 郵件訊息張貼至 DDE 伺服器應用程式。 用戶端會使用此訊息要求伺服器接受未請求的資料項目。 伺服器預期會以 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息來回複，指出它是否接受該資料項目。

若要張貼此訊息，請使用下列參數呼叫 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) 函數。


```C++
#define WM_DDE_POKE        0x03E7
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

張貼訊息之用戶端視窗的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

低序位單字是全域記憶體物件的控制碼，其中包含具有資料和其他資訊的 [**DDEPOKE**](/windows/desktop/api/Dde/ns-dde-ddepoke) 結構。

高序位單字包含全域 atom，可識別要傳送資料或通知的資料項目。

</dd> </dl>

## <a name="remarks"></a>備註

### <a name="posting"></a>張貼

用戶端應用程式必須使用 [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) 函式來配置全域記憶體物件的記憶體。 如果下列任一條件成立，用戶端應用程式必須刪除物件：

-   伺服器應用程式會以負的 [**WM \_ DDE \_ 確認**](wm-dde-ack.md) 訊息來回應。
-   **FRelease** 成員為 **FALSE**，但伺服器應用程式會以正面或負的 WM 的 [**WM \_ DDE \_ ACK**](wm-dde-ack.md)來回應。

用戶端應用程式必須使用 [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) 函數來建立 atom。

用戶端應用程式必須藉由呼叫 [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)函數或 [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)函式，來建立或重複使用 **WM \_ \_ DDE** 的 *lParam* 參數。

### <a name="receiving"></a>接收

伺服器應用程式應該張貼 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息，以回應正面或負面。 在張貼 **WM \_ DDE \_** 通知時，伺服器可以重複使用 atom，也可以將它刪除並建立一個新的。

伺服器必須藉由呼叫 [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)函數或 [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)函數，來建立或重複使用 [**WM \_ DDE \_ ACK**](wm-dde-ack.md) *lParam* 參數。

若要釋放全域記憶體物件，伺服器應該呼叫 [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) 函數。 此外，如果資料格式為 [**cf \_ DSPMETAFILEPICT**](clipboard-formats.md) 或 **cf \_ METAFILEPICT**，則伺服器也必須使用內嵌的中繼檔控制碼來呼叫 [**DeleteMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile) 。 這兩種格式具有額外的間接取值層級;亦即，應用程式必須鎖定物件以取得控制碼的指標，然後鎖定該控制碼以取得 [**METAFILEPICT**](/windows/win32/api/wingdi/ns-wingdi-metafilepict)結構的指標，最後使用 **METAFILEPICT** 結構 **hMF** 成員的控制碼來呼叫 **DeleteMetaFile** 。

若要釋放物件，伺服器應該呼叫 [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) 函數。

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

[**DDEPOKE**](/windows/desktop/api/Dde/ns-dde-ddepoke)
</dt> <dt>

[**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[**METAFILEPICT**](/windows/win32/api/wingdi/ns-wingdi-metafilepict)
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

**概念**
</dt> <dt>

[關於動態資料交換](about-dynamic-data-exchange.md)
</dt> </dl>

 

