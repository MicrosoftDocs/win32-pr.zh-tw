---
description: 偵測 \_ 到音調時，會傳送 TAPI 線路 MONITORTONE 訊息。 此訊息的傳送是使用 lineMonitorTones 函式來控制。
ms.assetid: ffdca615-5341-4f02-bb38-b8133cd9477d
title: 'LINE_MONITORTONE 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a57b7e49bcfe47b62002d8000c64b5c03242890250b8286e74470e044727d493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119405278"
---
# <a name="line_monitortone-message"></a>行 \_ MONITORTONE 訊息

偵測到音調時，會傳送 TAPI **線路 \_ MONITORTONE** 訊息。 此訊息的傳送是使用 [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) 函式來控制。


```C++
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDevice* 
</dt> <dd>

呼叫的控制碼。

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

開啟呼叫的行時所提供的回呼實例。

</dd> <dt>

*dwParam1* 
</dt> <dd>

偵測到的色調之 [**LINEMONITORTONE**](/windows/desktop/api/Tapi/ns-tapi-linemonitortone)結構的應用程式特定 **dwAppSpecific** 成員。

</dd> <dt>

*dwParam2* 
</dt> <dd>

未使用的。

</dd> <dt>

*dwParam3* 
</dt> <dd>

「滴答計數」 (Windows 開始) 偵測到色調的毫秒數。 如果是早于2.0 的 API 版本，則不會使用此參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

這 **行 \_ MONITORTONE** 訊息只會傳送至已要求監視其色調的應用程式。

因為這個時間戳記可能是在執行應用程式的電腦以外的電腦上產生，所以它只會與同一行裝置上產生的其他類似的時間戳記訊息進行比較， ( [**行 \_ GATHERDIGITS**](line-gatherdigits.md)、 [**行 \_ 產生**](line-generate.md)、 [**行 \_ MONITORDIGITS**](line-monitordigits.md)、 **行 \_ MONITORTONE**) ），以判斷其相對計時 (事件) 之間的分隔。 在大約49.7 天后，滴答計數可以「換行」;在執行計算時，應用程式必須將這一點列入考慮。

如果服務提供者未產生時間戳記 (例如，如果它是使用舊版的 TAPI) 所建立，則 TAPI 會在最接近服務提供者產生事件的時間點提供時間戳記，讓合成的時間戳記盡可能準確。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**行 \_ GATHERDIGITS**](line-gatherdigits.md)
</dt> <dt>

[**行 \_ 產生**](line-generate.md)
</dt> <dt>

[**行 \_ MONITORDIGITS**](line-monitordigits.md)
</dt> <dt>

[**LINEMONITORTONE**](/windows/desktop/api/Tapi/ns-tapi-linemonitortone)
</dt> <dt>

[**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones)
</dt> </dl>

 

 




