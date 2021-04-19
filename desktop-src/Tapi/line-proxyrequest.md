---
description: TAPI 線路 \_ PROXYREQUEST 訊息會將要求傳遞給已註冊的 proxy 函式處理常式。
ms.assetid: 7f33de55-2482-4558-bd86-ee2ac1e31269
title: 'LINE_PROXYREQUEST 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d536e85a9c773626bb5aacc4745d9d82817fe3c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992920"
---
# <a name="line_proxyrequest-message"></a>行 \_ PROXYREQUEST 訊息

TAPI **線路 \_ PROXYREQUEST** 訊息會將要求傳遞給已註冊的 proxy 函式處理常式。


```C++
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDevice* 
</dt> <dd>

應用程式狀態已變更之線路裝置的應用程式控制碼。

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

開啟呼叫的行時所提供的回呼實例。

</dd> <dt>

*dwParam1* 
</dt> <dd>

[**LINEPROXYREQUEST**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest)結構的指標，其中包含 proxy 處理常式應用程式要處理的要求。

</dd> <dt>

*dwParam2* 
</dt> <dd>

保留的。

</dd> <dt>

*dwParam3* 
</dt> <dd>

保留的。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

**該行 \_ PROXYREQUEST** 訊息只會傳送至第一個註冊的應用程式，以處理傳遞之類型的 proxy 要求。

應用程式應該處理 proxy 緩衝區中包含的要求，並呼叫 [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) 來傳回資料或傳遞結果。 只有在應用程式的 TAPI 回呼函數可以立即執行時，才需要在應用程式的 TAPI 回呼函式內容中處理要求，而不需要等待任何其他實體的回應。 如果應用程式需要與其他實體通訊 (例如，用來處理 PBX 型 ACD 的服務提供者，或可能導致封鎖) 的任何其他系統服務，則要求應該在應用程式中排入佇列，而且回呼函式會結束，以避免應用程式延遲接收到其他的 TAPI 訊息。

當 **行 \_ PROXYREQUEST** 傳遞至 proxy 處理常式時，TAPI 已經將正面的 *dwRequestID* 函式結果傳回至原始應用程式，並解除封鎖呼叫執行緒以繼續執行。 應用程式正在等候 [**行 \_ 回復**](line-reply.md) 訊息，此訊息會在 proxy 處理常式應用程式呼叫 [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse)時自動產生。

應用程式不應釋放 *lpProxyRequest* 所指向的記憶體。 TAPI 會在執行 [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse)期間釋出記憶體。 應用程式可以針對每 **一行 \_ PROXYREQUEST** 訊息只呼叫 [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse)一次。

如果應用程式在有擱置的 proxy 要求時收到 [**行 \_ 關閉**](line-close.md) 訊息，則應該為每個擱置中的要求呼叫 [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) ，並傳入適當的 *dwResult* 值 (例如 LINEERR \_ OPERATIONFAILED) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**行 \_ 關閉**](line-close.md)
</dt> <dt>

[**行 \_ 回復**](line-reply.md)
</dt> <dt>

[**LINEPROXYREQUEST**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest)
</dt> <dt>

[**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse)
</dt> </dl>

 

 




