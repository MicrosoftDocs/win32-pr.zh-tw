---
description: CBaseInputPin 接收方法-Receive 方法會接收資料流程中的下一個媒體範例。 這個方法會實 IMemInputPin：： Receive 方法。
ms.assetid: 30fefc7b-7c9c-44cd-b58b-2b275dfa2520
title: 'CBaseInputPin 的 Receive 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fe88913ad374923c11cf058a3dc0aa70580411e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099686"
---
# <a name="cbaseinputpinreceive-method"></a>CBaseInputPin 接收方法

`Receive`方法會接收資料流程中的下一個媒體範例。 這個方法會實 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSample* 
</dt> <dd>

範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所列的值。



| 傳回碼                                                                                             | Description                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                    | 成功。<br/>                                        |
| <dl> <dt>**S \_ FALSE**</dt> </dl>                 | Pin 目前正在排清;已拒絕範例。<br/> |
| <dl> <dt>**E \_ 指標**</dt> </dl>               | **Null** 指標引數。<br/>                      |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | 媒體類型無效。<br/>                             |
| <dl> <dt>**VFW \_ E \_ 運行時 \_ 錯誤**</dt> </dl>   | 發生執行階段錯誤。<br/>                      |
| <dl> <dt>**VFW \_ E \_ 錯誤的 \_ 狀態**</dt> </dl>     | 已停止 pin。<br/>                             |



 

## <a name="remarks"></a>備註

上游輸出圖釘會呼叫這個方法，以將範例傳遞給輸入的 pin。 輸入 pin 必須執行下列其中一項：

-   在傳回之前處理範例。
-   傳回並處理工作者執行緒中的範例。
-   拒絕範例。

如果 pin 使用背景工作執行緒來處理範例，請在此方法內的範例中新增參考計數。 在方法傳回之後，上游 pin 會釋放範例。 當範例的參考計數到達零時，此範例會回到配置器以供重複使用。

這個方法是同步的，而且可以封鎖。 如果此方法可能會封鎖，pin 的 [**CBaseInputPin：： ReceiveCanBlock**](cbaseinputpin-receivecanblock.md) 方法應該會傳回 s \_ OK。

在基類中，這個方法會執行下列步驟：

1.  呼叫 [**CBaseInputPin：： CheckStreaming**](cbaseinputpin-checkstreaming.md) 方法，以確認釘選可以立即處理範例。 如果無法這樣做，例如，如果已停止 pin，方法將會失敗。
2.  抓取範例屬性，並檢查格式是否已變更 (請參閱下面的) 。
3.  如果格式已變更，則方法會呼叫 [**CBasePin：： CheckMediaType**](cbasepin-checkmediatype.md) 方法，以判斷是否可接受新的格式。
4.  如果無法接受新的格式，方法會呼叫 [**CBasePin：： EndOfStream**](cbasepin-endofstream.md) 方法、張貼 EC \_ ERRORABORT 事件，並傳回錯誤碼。
5.  假設沒有任何錯誤，則方法會傳回 S \_ OK。

測試格式變更，如下所示：

-   如果範例支援 [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2)介面，請檢查 [**AM \_ Sample2.xml \_ 屬性**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties)結構的 **dwSampleFlags** 成員。 如果有 AM \_ 範例 \_ TYPECHANGED 旗標，則格式已變更。
-   否則，如果範例不支援 **IMediaSample2**，請呼叫 [**IMediaSample：： GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) 方法。 如果此方法傳回非 **Null** 值，則格式已變更。

在基類中，此方法不會處理範例。 衍生的類別必須覆寫這個方法以執行處理。  (這牽涉到的內容完全取決於篩選器。 ) 衍生類別應該呼叫基類方法，以檢查先前所述的錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseInputPin 類別**](cbaseinputpin.md)
</dt> </dl>

 

 




