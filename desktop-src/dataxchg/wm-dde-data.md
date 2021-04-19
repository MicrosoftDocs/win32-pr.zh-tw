---
title: 'WM_DDE_DATA 訊息 (的) '
description: 動態資料交換 (DDE) server 應用程式將 WM \_ DDE 的 \_ 資料訊息張貼至 dde 用戶端應用程式，以將資料項目傳遞給用戶端，或通知用戶端資料項目目的可用性。
ms.assetid: ed6a65d3-b2a3-45f2-9600-291ce2ec8c0a
keywords:
- WM_DDE_DATA 訊息資料交換
topic_type:
- apiref
api_name:
- WM_DDE_DATA
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f045ff07e01023e6535eb00dcb78400e4c9519a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966307"
---
# <a name="wm_dde_data-message"></a>WM \_ DDE \_ 資料訊息

動態資料交換 (DDE) server 應用程式將 **WM \_ DDE 的 \_ 資料** 訊息張貼至 dde 用戶端應用程式，以將資料項目傳遞給用戶端，或通知用戶端資料項目目的可用性。

若要張貼此訊息，請使用下列參數呼叫 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) 函數。


```C++
#define WM_DDE_DATA        0x03E05
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

張貼訊息之伺服器視窗的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

低序位單字是全域記憶體物件的控制碼，其中包含具有資料和其他資訊的 [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) 結構。 如果伺服器通知用戶端資料項目目值在暖資料連結期間已變更，則此控制碼應該設定為 **Null** 。 用戶端會建立一個暖連結，而用戶端會使用 **fDeferUpd** 位組來傳送 [**WM \_ DDE \_ 建議**](wm-dde-advise.md)訊息。

高序位字組包含 atom，可識別資料或通知傳送至的資料項目。

</dd> </dl>

## <a name="remarks"></a>備註

### <a name="posting"></a>張貼

伺服器應用程式會使用 [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) 函數來配置全域記憶體物件。 它會使用 [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) 函數來配置 atom。

伺服器必須藉由呼叫 [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)函數或 [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)函數，來建立或重複使用 **WM \_ DDE \_ DATA** *lParam* 參數。

如果接收 (用戶端) 應用程式以負的 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息回應，則張貼 (伺服器) 應用程式必須刪除全域記憶體物件; 否則，用戶端必須藉由呼叫 [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) 函式來將物件解壓縮之後，才能刪除該物件。

如果伺服器應用程式將 [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata)結構的 **fRelease** 成員設定為 **FALSE**，則伺服器會負責在接收正面或負認可時刪除物件。

伺服器應用程式不應該將 [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata)結構的 **fAckReq** 和 **FRelease** 成員都設為 **FALSE**。 如果這兩個成員都設定為 **FALSE**，則伺服器無法判斷何時刪除該物件。

### <a name="receiving"></a>接收

如果 **fAckReq** 為 **TRUE**，用戶端應用程式應該張貼 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息，以回應正面或負面。 張貼 **WM \_ DDE DDE \_ ACK** 時，用戶端可以重複使用 atom，也可以刪除它並建立新的。

用戶端必須藉由呼叫 [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)函數或 [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)函數來建立或重複使用 [**WM \_ DDE \_ ACK**](wm-dde-ack.md) *lParam* 參數。

如果 **fAckReq** 為 **FALSE**，用戶端應用程式應該刪除 atom。

如果張貼應用程式將全域記憶體物件指定為 **Null**，則接收應用程式可以藉由張貼 [**WM \_ DDE \_ 要求**](wm-dde-request.md) 訊息來要求伺服器傳送資料。

處理在全域記憶體物件不是 **Null** 的 **WM \_ DDE \_ 資料** 訊息之後，除非下列其中一個條件成立，否則用戶端應該釋放物件：

-   **FRelease** 成員為 **FALSE**。
-   **FRelease** 成員是 **TRUE**，但用戶端應用程式會以負的 [**WM \_ DDE \_**](wm-dde-ack.md)通知訊息來回應。

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

[**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata)
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

[**WM \_ DDE \_ 建議**](wm-dde-advise.md)
</dt> <dt>

[**WM \_ DDE 的進行 \_**](wm-dde-poke.md)
</dt> <dt>

[**WM \_ DDE \_ 要求**](wm-dde-request.md)
</dt> <dt>

**概念**
</dt> <dt>

[關於動態資料交換](about-dynamic-data-exchange.md)
</dt> </dl>

 

