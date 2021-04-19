---
description: '\_當目前經緩衝處理的數位收集要求終止或取消時，會傳送 TAPI 線路 GATHERDIGITS 訊息。 當應用程式收到此訊息之後，就可以檢查數位緩衝區。'
ms.assetid: 0d27904d-9743-44bf-a7bc-132459351e01
title: 'LINE_GATHERDIGITS 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f0c67c5a9bbd3f798a8f4343b36c311309633ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990190"
---
# <a name="line_gatherdigits-message"></a>行 \_ GATHERDIGITS 訊息

當目前經緩衝處理的數位收集要求終止或取消時，會傳送 TAPI **線路 \_ GATHERDIGITS** 訊息。 當應用程式收到此訊息之後，就可以檢查數位緩衝區。


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

數位收集終止的原因。 這個參數必須是一個 [**LINEGATHERTERM \_ 常數**](linegatherterm--constants.md)，而且只能是其中一個。

</dd> <dt>

*dwParam2* 
</dt> <dd>

未使用的。

</dd> <dt>

*dwParam3* 
</dt> <dd>

「滴答計數」 (從 Windows 開始) 完成數位收集的毫秒數。 若是早于2.0 的 TAPI 版本，則不會使用此參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

這 **行 \_ GATHERDIGITS** 訊息只會傳送至應用程式，該應用程式會使用 [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)在呼叫上起始數位收集。

如果使用 [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits) 函式來取消前一個要求以收集數位，則 TAPI 會傳送 **一行 \_ GATHERDIGITS** 訊息，其中 *dwParam1* 設定為 LINEGATHERTERM \_ cancel 至應用程式，指出原始指定的緩衝區包含收集到取消的數位。

由於 *dwParam3* 所指定的時間戳記可能是在執行應用程式的電腦以外的電腦上產生，因此只適用于與在同一行裝置上產生的其他類似時間戳記的訊息比較， ( [**行 \_ 產生**](line-generate.md)、 [**行 \_ MONITORDIGITS**](line-monitordigits.md)、 [**行 \_ MONITORMEDIA**](line-monitormedia.md)、 [**行 \_ MONITORTONE**](line-monitortone.md)) ，以判斷其相對計時 (事件) 之間的分隔。 在大約49.7 天后，滴答計數可以「換行」;在執行計算時，應用程式必須將這一點列入考慮。

如果服務提供者未產生時間戳記 (例如，如果它是使用舊版的 TAPI) 所建立，則 TAPI 會在最接近服務提供者產生事件的時間點提供時間戳記，讓合成的時間戳記盡可能準確。

> [!Note]  
> 當應用程式叫用將資料寫入至應用程式記憶體的任何非同步作業時，應用程式必須保留該記憶體以供寫入，直到收到 [**一行 \_ 回復**](line-reply.md) 或 **行 \_ GATHERDIGITS** 訊息為止。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**行 \_ 產生**](line-generate.md)
</dt> <dt>

[**行 \_ MONITORDIGITS**](line-monitordigits.md)
</dt> <dt>

[**行 \_ MONITORMEDIA**](line-monitormedia.md)
</dt> <dt>

[**行 \_ MONITORTONE**](line-monitortone.md)
</dt> <dt>

[**行 \_ 回復**](line-reply.md)
</dt> <dt>

[**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)
</dt> </dl>

 

 




