---
description: StartUsingOutputPin 方法會取得串流作業的釘選存取權。
ms.assetid: afa627a9-00fd-4ad0-b674-9c54a5a1be55
title: 'CDynamicOutputPin. StartUsingOutputPin 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.StartUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1c5ea7386c896f6b989a47c2574dfa4d61eacb5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001178"
---
# <a name="cdynamicoutputpinstartusingoutputpin-method"></a>CDynamicOutputPin. StartUsingOutputPin 方法

`StartUsingOutputPin`方法會取得串流作業的釘選存取權。

## <a name="syntax"></a>語法


```C++
virtual HRESULT StartUsingOutputPin();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                                           | Description                                                       |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                  | 成功。<br/>                                               |
| <dl> <dt>**E 未 \_ 預期**</dt> </dl>          | 非預期的錯誤。<br/>                                      |
| <dl> <dt>**VFW \_ E \_ 狀態 \_ 已變更**</dt> </dl> | 篩選已停止，或 pin 已開始排清。<br/> |



 

## <a name="remarks"></a>備註

呼叫這個方法之前，請先呼叫這個方法，然後再呼叫任何方法，將資料傳遞到連接的輸入 pin 或變更連接的媒體類型。 例如，此規則適用于下列方法：

-   [**CDynamicOutputPin::ChangeOutputFormat**](cdynamicoutputpin-changeoutputformat.md)
-   [**CDynamicOutputPin::ChangeMediaType**](cdynamicoutputpin-changemediatype.md)
-   [**CDynamicOutputPin：:D ynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md)
-   [**CBaseOutputPin：:D eliver**](cbaseoutputpin-deliver.md)
-   [**CBaseOutputPin：:D eliverEndOfStream**](cbaseoutputpin-deliverendofstream.md)
-   [**CBaseOutputPin：:D eliverNewSegment**](cbaseoutputpin-delivernewsegment.md)
-   [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

之後，請呼叫 [**CDynamicOutputPin：： StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) 方法來釋放對 pin 的存取。

如果釘選了 pin，會 `StartUsingOutputPin` 等候 pin 變成解除封鎖。 如果在方法等候時，篩選準則停止，方法會立即傳回 VFW \_ E \_ 狀態 \_ 變更。 Pin 會維護已呼叫的次數， `StartUsingOutputPin` 而不需要對應的 **StopUsingOutputPin** 呼叫數目。 如果另一個執行緒嘗試在此計數為非零時封鎖 pin，則會將其封鎖狀態設為「擱置」。 一旦所有串流作業都已完成，最後呼叫 **StopUsingOutputPin** 時，就會封鎖該 pin。

當您呼叫這個方法時，請勿保留 [**CDynamicOutputPin：： m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical 區段。 否則，如果 pin 遭到封鎖，則永遠不會解除封鎖，造成鎖死。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDynamicOutputPin 類別**](cdynamicoutputpin.md)
</dt> </dl>

 

 




