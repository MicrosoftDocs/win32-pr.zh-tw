---
description: 偵測 \_ 到數位時，會傳送 TAPI 線路 MONITORDIGITS 訊息。 此訊息的傳送是使用 lineMonitorDigits 函式來控制。
ms.assetid: 1c1a729c-a6bb-4432-9617-4a892c76cb8d
title: 'LINE_MONITORDIGITS 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c6e85ed515d20c18c6e41cdb185b036312c54ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994716"
---
# <a name="line_monitordigits-message"></a>行 \_ MONITORDIGITS 訊息

偵測到數位時，會傳送 TAPI **線路 \_ MONITORDIGITS** 訊息。 此訊息的傳送是使用 [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) 函式來控制。


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

低序位位元組包含在文字表示中收到的最後一個數位。

</dd> <dt>

*dwParam2* 
</dt> <dd>

偵測到的數位模式。 這個參數必須是一個 [**LINEDIGITMODE \_ 常數**](linedigitmode--constants.md)，而且只能是其中一個。

</dd> <dt>

*dwParam3* 
</dt> <dd>

「滴答計數」 (毫秒數，自 Windows 啟動後偵測到指定數位的) 。 若是早于2.0 的 TAPI 版本，則不會使用此參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

**該行 \_ MONITORDIGITS** 訊息會傳送至已啟用數位監視的應用程式。

因為這個時間戳記可能是在執行應用程式的電腦以外的電腦上產生，所以它只會與同一行裝置上產生的其他類似的時間戳記訊息進行比較， ( [**行 \_ GATHERDIGITS**](line-gatherdigits.md)、 [**行 \_ 產生**](line-generate.md)、 [**行 \_ MONITORMEDIA**](line-monitormedia.md)、 [**行 \_ MONITORTONE**](line-monitortone.md)) ），以判斷其相對計時 (事件) 之間的分隔。 在大約49.7 天后，滴答計數可以「換行」;在執行計算時，應用程式必須將這一點列入考慮。

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

[**行 \_ MONITORMEDIA**](line-monitormedia.md)
</dt> <dt>

[**行 \_ MONITORTONE**](line-monitortone.md)
</dt> <dt>

[**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits)
</dt> </dl>

 

 




