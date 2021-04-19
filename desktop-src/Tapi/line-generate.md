---
description: '\_會傳送 TAPI 線路產生訊息，以通知應用程式目前的數位或語氣產生已終止。'
ms.assetid: 375823c5-22c2-4010-bfb4-5b8b46141c72
title: 'LINE_GENERATE 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b916dc95d1a6343b0f8ebc0eef9e589b04aa2112
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990733"
---
# <a name="line_generate-message"></a>行 \_ 產生訊息

會傳送 TAPI **線路 \_ 產生** 訊息，以通知應用程式目前的數位或語氣產生已終止。 每次只有一個這類世代要求可以進行指定的呼叫。 當數位或語氣產生取消時，也會傳送此訊息。


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

數位或語氣產生終止的原因。 這個參數必須是一個 [**LINEGENERATETERM \_ 常數**](linegenerateterm--constants.md)，而且只能是其中一個。

</dd> <dt>

*dwParam2* 
</dt> <dd>

未使用的。

</dd> <dt>

*dwParam3* 
</dt> <dd>

「滴答計數」 (從 Windows 開始) 數位或語氣產生完成的毫秒數。 如果是早于2.0 的 API 版本，則不會使用此參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

**該行 \_ 產生** 訊息只會傳送至要求數位或語氣產生的應用程式。

由於 *dwParam3* 所指定的時間戳記可能是在執行應用程式的電腦以外的電腦上產生，因此只適用于與在同一行裝置上產生的其他類似時間戳記的訊息比較， ( [**行 \_ GATHERDIGITS**](line-gatherdigits.md)、 [**行 \_ MONITORDIGITS**](line-monitordigits.md)、 [**行 \_ MONITORMEDIA**](line-monitormedia.md)、 [**行 \_ MONITORTONE**](line-monitortone.md)) ，以判斷其相對計時 (事件) 之間的分隔。 在大約49.7 天后，滴答計數可以「換行」;在執行計算時，應用程式必須將這一點列入考慮。

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

[**行 \_ MONITORDIGITS**](line-monitordigits.md)
</dt> <dt>

[**行 \_ MONITORMEDIA**](line-monitormedia.md)
</dt> <dt>

[**行 \_ MONITORTONE**](line-monitortone.md)
</dt> </dl>

 

 




