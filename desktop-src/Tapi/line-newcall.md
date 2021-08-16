---
description: '\_每當 tapi 未產生的新呼叫抵達 tapi 開啟的行時，就會將 TSPI LINE NEWCALL 訊息傳送至 LINEEVENT 回呼函式。'
ms.assetid: 36122dfb-1ed6-459d-aa2b-69c86daaddd8
title: 'LINE_NEWCALL 訊息 (Tspi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f541f7535e9b41dc66a83b8d033d3ff7adf4d51f6e78f275d2695cb5ae7a35b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761904"
---
# <a name="line_newcall-message"></a>行 \_ NEWCALL 訊息

每當 tapi 未產生的新呼叫抵達 TAPI 開啟的行時，就會將 TSPI **LINE \_ NEWCALL** 訊息傳送至 [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) 回呼函式。 這必須是第一個針對該呼叫傳送的訊息。 TAPI 會將 *htCall* 的不透明控制碼寫入服務提供者以 *dwParam2* 形式傳遞的位置。 這會提供服務提供者要在後續訊息中使用的 *htCall* 值。


```C++
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*htLine* 
</dt> <dd>

線路裝置的 TAPI 不透明物件控制碼。

</dd> <dt>

*htCall* 
</dt> <dd>

未使用的。

</dd> <dt>

*dwMsg* 
</dt> <dd>

值行 \_ NEWCALL。

</dd> <dt>

*dwParam1* 
</dt> <dd>

服務提供者的呼叫不透明控制碼，屬於 [**HDRVCALL**](hdrvline.md)型別。 TAPI 會將此值傳遞為 *hdCall* 參數，以識別在後續程式中叫用以在呼叫上操作的呼叫。

</dd> <dt>

*dwParam2* 
</dt> <dd>

指向 LPHTAPICALL 的類型指標，指向 [**HTAPICALL**](htapicall.md)。 TAPI 會針對指定位置的呼叫，寫入 TAPI 不透明控制碼。 服務提供者必須儲存此值，並將其傳遞為 *htCall* 參數，以識別在其回報給呼叫的後續事件中的呼叫。

此參數也可以取得 **Null** 值 (請參閱) 的下列備註區段。

</dd> <dt>

*dwParam3* 
</dt> <dd>

未使用的。

</dd> </dl>

## <a name="remarks"></a>備註

服務提供者應該傳送 [**該行 \_ CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) 訊息作為此呼叫的下一則訊息。 **LINE \_ NEWCALL** 事件不尋常，因為它也會傳回值給服務提供者。

此函式會報告源自服務提供者的任何新呼叫， (輸入、輸出、在電話上起始，以及在 TAPI 和服務提供者尚未交換不透明控制碼的) 上。 系統會交換這些控制碼，讓 TAPI 和服務提供者可以接著提出要求，並報告與呼叫相關的事件。 由於這些新的呼叫不一定是輸入，因此呼叫一開始可能會處於任何狀態，而不一定是 *提供* 狀態。 如果服務提供者啟動，併發現該行有一或多個呼叫已在使用中，它就會使用 **行 \_ NEWCALL** 訊息來通知 TAPI，然後以 [**行 \_ CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) 訊息指出目前的狀態。 由使用者在電話上起始的新撥出電話，將會以 **行 \_ NEWCALL** 訊息來回報，而初始 **行 \_ CALLSTATE** 訊息會指出通話處於 **撥號撥號** 狀態 (然後繼續進行) 。

如果服務提供者在很短的時間內將大量呼叫傳遞給 TAPI (在相同的插斷週期) 期間，TAPI 可能會在處理這些呼叫時累積。 當發生這種情況時，TAPI 會向服務提供者指出在傳送任何其他呼叫之前，會先等候一小段時間。 它會藉由將 **Null** 值（而不是有效的 [**HTAPICALL**](htapicall.md)）寫入至 **\_ NEWCALL 行** *dwParam2* 參數所指向的位置來發出信號。 這表示嘗試處理新提供的呼叫控制碼失敗，最有可能是因為暫時無法配置記憶體。 服務提供者可以藉由卸載呼叫來回應，或是在排程延遲之後重新傳送 **行 \_ NEWCALL** 訊息來回應 (在這段期間，服務提供者應該產生處理器以允許 TAPI 處理其他擱置中的動作) 。 在任何情況下，您可以將新呼叫的相關訊息傳遞給 TAPI，直到控制碼交換成功為止。 當 *dwParam2* 所指向的位置取得非 **Null** 值時，服務提供者會知道此值是對呼叫的有效 [**HTAPICALL**](htapicall.md) 控制碼。

TAPI 層級沒有直接對應的訊息。 此訊息是在 TSPI 層級上使用，以獨特且明確的方式引入新的 TAPI 來電，並取得 TAPI 不透明識別碼進行呼叫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tspi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**行 \_ CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85))
</dt> <dt>

[**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent)
</dt> </dl>

 

