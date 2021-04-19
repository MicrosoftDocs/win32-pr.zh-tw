---
description: '\_系統會傳送 TAPI 線路 APPNEWCALL 訊息，以在有新的呼叫控制碼代表時通知應用程式。'
ms.assetid: 0c263025-e719-453e-91c4-a9f2d9321db3
title: 'LINE_APPNEWCALL 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33d24ca816fb69384e90e4215edbc90b9410b887
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993589"
---
# <a name="line_appnewcall-message"></a>行 \_ APPNEWCALL 訊息

系統會傳送 TAPI **線路 \_ APPNEWCALL** 訊息來通知應用程式，而不是透過應用程式中的 API 呼叫，以自發的方式 (建立新的呼叫控制碼，而在此情況下，會透過傳遞至函式) 的指標參數傳回控制碼。


```C++
        
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDevice* 
</dt> <dd>

應用程式對已建立呼叫之線路裝置的控制碼。

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

開啟呼叫的行時所提供的回呼實例。

</dd> <dt>

*dwParam1* 
</dt> <dd>

呼叫出現所在行的位址識別碼。 位址識別碼會永久與位址相關聯;識別碼在作業系統升級之間會維持不變。

</dd> <dt>

*dwParam2* 
</dt> <dd>

應用程式對新呼叫的控制碼。

</dd> <dt>

*dwParam3* 
</dt> <dd>

新呼叫 (LINECALLPRIVILEGE \_ 擁有者或 LINECALLPRIVILEGE 監視器) 的應用程式許可權 \_ 。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

只要應用程式有新呼叫的控制碼，就會傳送 **一行 \_ APPNEWCALL** 訊息給支援 TAPI 2.0 版或更新版本的應用程式。 由於訊息包含呼叫所在的 *hLine* 和 *dwAddressID* 參數，因此應用程式可以輕鬆地在正確的內容中建立新的呼叫物件。 **行 \_ APPNEWCALL** 訊息一律緊接在 [**行 \_ CALLSTATE**](line-callstate.md)訊息中，指出呼叫的初始狀態。

協調早于 2.0) 之 API 版本的繼承應用程式 (只會傳送 [**\_ CALLSTATE**](line-callstate.md) 訊息，如舊版 api 中所述。 這類應用程式會在收到 [**一行 \_ CALLSTATE**](line-callstate.md) 訊息時建立新的呼叫物件，該訊息的 *dwParam3* 設定為非零值，並包含應用程式目前不知道的呼叫控制碼。 缺點是 () 應用程式必須呼叫 [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)來判斷與呼叫相關聯的 *hLine* 和 *dwAddressID* 參數; (b) 應用程式必須掃描所有已知的呼叫控制碼，以判斷呼叫是否為新的呼叫;而且 (c) 有可能，在某些情況下，應用程式會將它視為新的呼叫控制碼，但事實上，它只會將它的控制碼解除配置給呼叫 (例如，應用程式剛剛解除配置了呼叫控制碼，但因為另一個應用程式的 [**lineHandoff**](/windows/desktop/api/Tapi/nf-tapi-linehandoff)已經在應用程式的 TAPI 訊息佇列中，所以提供呼叫應用程式擁有權的 [**行 \_ CALLSTATE**](line-callstate.md)訊息) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**行 \_ CALLSTATE**](line-callstate.md)
</dt> <dt>

[**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)
</dt> <dt>

[**lineHandoff**](/windows/desktop/api/Tapi/nf-tapi-linehandoff)
</dt> </dl>

 

 




