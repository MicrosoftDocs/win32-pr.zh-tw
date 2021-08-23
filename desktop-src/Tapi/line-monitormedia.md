---
description: 當偵測到通話媒體類型的變更時，就會傳送 TAPI LINE_MONITORMEDIA 訊息。 此訊息的傳送是使用 lineMonitorMedia 函式來控制
ms.assetid: 1cfba455-9a15-45f3-8d56-74b8348e080e
title: 'LINE_MONITORMEDIA 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fec42f0e8aa630b518f989a9237762edc71281767b281f7af78eb54210138d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519018"
---
# <a name="line_monitormedia-message"></a>行 \_ MONITORMEDIA 訊息

當偵測到通話媒體類型的變更時，就會傳送 TAPI **線路 \_ MONITORMEDIA** 訊息。 此訊息的傳送是使用 [**lineMonitorMedia**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) 函式來控制。


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

開啟行時所提供的回呼實例。

</dd> <dt>

*dwParam1* 
</dt> <dd>

新的媒體類型 (或模式) 。 這個參數必須是一個 [**LINEMEDIAMODE \_ 常數**](linemediamode--constants.md)，而且只能是其中一個。

</dd> <dt>

*dwParam2* 
</dt> <dd>

未使用的。

</dd> <dt>

*dwParam3* 
</dt> <dd>

從偵測到指定媒體的) 開始 Windows 開始，「滴答計數」 (毫秒數。 若是早于2.0 的 TAPI 版本，則不會使用此參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

**線路 \_ MONITORMEDIA** 訊息會傳送至已偵測到媒體類型的媒體監視功能的應用程式。

因為這個時間戳記可能是在執行應用程式的電腦以外的電腦上產生，所以它只會與同一行裝置上產生的其他類似的時間戳記訊息進行比較， ( [**行 \_ GATHERDIGITS**](line-gatherdigits.md)、 [**行 \_ 產生**](line-generate.md)、 [**行 \_ MONITORDIGITS**](line-monitordigits.md)、 [**行 \_ MONITORTONE**](line-monitortone.md)) ），以判斷其相對計時 (事件) 之間的分隔。 在大約49.7 天后，滴答計數可以「換行」;在執行計算時，應用程式必須將這一點列入考慮。

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

[**行 \_ MONITORTONE**](line-monitortone.md)
</dt> </dl>

 

 




