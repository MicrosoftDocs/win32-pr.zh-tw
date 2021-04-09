---
title: 'WM_DDE_ACK 訊息 (的) '
description: WM \_ dde \_ 通知訊息會通知動態資料交換 (DDE) 應用程式的接收和處理下列訊息： wm dde 傳送 \_ \_ 、WM \_ dde \_ 執行、wm \_ DDE \_ 資料、WM \_ dde \_ 建議、wm \_ dde \_ UNADVISE、wm dde \_ \_ 初始，或 wm \_ dde \_ 要求 (在某些情況下) 。 若要張貼此訊息，請使用下列參數呼叫 PostMessage 函數。
ms.assetid: aca47dbf-e1f2-4725-8364-0aa7fcd98bd9
keywords:
- WM_DDE_ACK 訊息資料交換
topic_type:
- apiref
api_name:
- WM_DDE_ACK
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a407fc6cad7077586539f119dd65be59a507cacd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025016"
---
# <a name="wm_dde_ack-message"></a>WM \_ DDE \_ ACK 訊息

**Wm \_ dde \_** 通知訊息會通知動態資料交換 (DDE) 應用程式接收和處理下列訊息： [**wm \_ dde \_**](wm-dde-poke.md)傳送、 [**wm \_ dde \_ 執行**](wm-dde-execute.md)、 [**wm \_ dde \_ 資料**](wm-dde-data.md)、 [**wm \_ dde \_ 建議**](wm-dde-advise.md)、 [**wm \_ dde \_ UNADVISE**](wm-dde-unadvise.md)、 [**wm dde \_ \_ 起始**](wm-dde-initiate.md)或 [**wm \_ dde \_ 要求**](wm-dde-request.md) (在某些情況下) 。

若要張貼此訊息，請使用下列參數呼叫 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) 函數。


```C++
#define WM_DDE_ACK     0x03E4
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

當回應 [**WM \_ DDE 的 \_ 起始**](wm-dde-initiate.md)時，此參數是傳送訊息之伺服器視窗的控制碼。

當回應 [**WM \_ DDE 的 \_ 執行**](wm-dde-execute.md)時，此參數是伺服器視窗張貼訊息的控制碼。

當您回復所有其他訊息時，此參數是用戶端或伺服器視窗張貼訊息的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

當回應 [**WM \_ DDE 的 \_ 起始**](wm-dde-initiate.md)時，低序位單字包含識別回復應用程式的 atom。 高序位單字包含一個 atom，可識別正在建立交談的主題。

當回應 [**WM \_ DDE 的 \_ 執行**](wm-dde-execute.md)時，低序位單字會指定包含一連串旗標的 [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) 結構，這些旗標表示回應的狀態。 高序位單字是全域記憶體物件的控制碼，其中包含在 **WM \_ DDE \_ 執行** 訊息中收到的命令字串。

當您回復所有其他訊息時，低序位單字會指定 [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) 結構，其中包含一系列指出回應狀態的旗標。 高序位字組包含全域 atom，可識別回應傳送的資料項目名稱。

</dd> </dl>

## <a name="remarks"></a>備註

### <a name="posting"></a>張貼

除了回應 [**WM \_ dde \_ 起始**](wm-dde-initiate.md)訊息之外，應用程式也會呼叫 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)函式，而不是透過呼叫 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)函式，以張貼 **wm \_ dde \_** 通知訊息。 當回應 **WM \_ dde 的 \_ 起始** 時，應用程式會呼叫 **SendMessage** 來傳送 **WM \_ dde \_ ACK** 訊息。 在此情況下，應用程式名稱 atom 和主題名稱 atom 都不應為 **null** (即使是由 **WM \_ DDE \_ 初始化** 訊息指定的 **null** 原子) 。

當您使用隨附的 atom 來確認任何訊息時，應用程式張貼了 **WM \_ DDE \_** 通知可以重複使用伴隨原始訊息的 atom，或是將它刪除並建立新訊息。

當您在確認 [**\_ \_ 執行 wm dde dde**](wm-dde-execute.md)時，張貼了 **wm \_ dde \_** 通知的應用程式應該重複使用原始 **wm \_ dde \_ 執行** 訊息中識別的全域記憶體物件。

所有張貼 **的 \_ WM \_ DDE** 通知訊息都必須藉由呼叫 [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)函數或 [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)函數來建立或重複使用 *lParam* 參數。

如果應用程式已透過張貼 [**WM \_ DDE DDE \_ 終止**](wm-dde-terminate.md) 並等候確認來起始交談的終止，則等待應用程式應該不會認可 (的正面或負面) 其他應用程式傳送的任何後續訊息。 等候中的應用程式應該刪除這些中間訊息中收到的任何原子或共用記憶體物件。 如果在 [**wm \_ dde \_**](wm-dde-poke.md)郵件和 [**wm \_ dde \_ 資料**](wm-dde-data.md)訊息中， **fRelease** 旗標設定為 **FALSE** ，則不應釋放記憶體物件。

### <a name="receiving"></a>接收

接收 **WM \_ DDE \_** 通知訊息的應用程式應該刪除訊息隨附的所有原子。 如果應用程式接收了 **WM \_ DDE \_** 通知，以回應具有伴隨全域記憶體物件的訊息，而且物件是以 **FRelease** 旗標設定為 **FALSE** 來傳送，則應用程式會負責刪除物件。

如果應用程式收到回傳至 [**wm \_ dde \_ 建議**](wm-dde-advise.md)訊息的負 **wm \_ dde dde \_ ACK** 訊息，應用程式應該刪除以原始的 **wm \_ dde \_ 建議** 訊息張貼的全域記憶體物件。 如果應用程式收到回傳至 [**wm \_ dde \_ 資料**](wm-dde-data.md)、 [**wm \_ dde \_**](wm-dde-poke.md)傳送或 [**wm \_ dde \_ 執行**](wm-dde-execute.md)訊息的負 **WM \_ dde \_** 通知訊息，應用程式應該刪除以原始 **WM \_ dde \_ 資料**、 **wm \_ dde \_** 傳送或 **wm dde \_ \_ 執行** 訊息張貼的全域記憶體物件。

接收已張貼之 **WM \_ DDE \_ ACK** 訊息的應用程式，必須使用 [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam)函數釋放 *lParam* 參數。

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

[**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack)
</dt> <dt>

[**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam)
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

[**WM \_ DDE \_ 建議**](wm-dde-advise.md)
</dt> <dt>

[**WM \_ DDE \_ 資料**](wm-dde-data.md)
</dt> <dt>

[**WM \_ DDE \_ 執行**](wm-dde-execute.md)
</dt> <dt>

[**WM \_ DDE \_ 起始**](wm-dde-initiate.md)
</dt> <dt>

[**WM \_ DDE 的進行 \_**](wm-dde-poke.md)
</dt> <dt>

[**WM \_ DDE \_ 要求**](wm-dde-request.md)
</dt> <dt>

[**WM \_ DDE \_ 終止**](wm-dde-terminate.md)
</dt> <dt>

[**WM \_ DDE \_ UNADVISE**](wm-dde-unadvise.md)
</dt> <dt>

**概念**
</dt> <dt>

[關於動態資料交換](about-dynamic-data-exchange.md)
</dt> </dl>

 

