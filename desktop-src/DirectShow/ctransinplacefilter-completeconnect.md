---
description: CTransInPlaceFilter. CompleteConnect 方法-CompleteConnect 方法會完成 pin 連接。
ms.assetid: 0c02c455-dbd0-4606-b1b1-f965c2a5805b
title: 'CTransInPlaceFilter. CompleteConnect 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d9cc0bc839a4e35c4ce896acdf50da10f0c2bb0c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084786"
---
# <a name="ctransinplacefiltercompleteconnect-method"></a>CTransInPlaceFilter. CompleteConnect 方法

`CompleteConnect`方法會完成 pin 連接。

## <a name="syntax"></a>語法


```C++
HRESULT CompleteConnect(
   PIN_DIRECTION direction,
   IPin          *pReceivePin
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*direction* 
</dt> <dd>

[**釘選 \_ 方向**](/windows/win32/api/strmif/ne-strmif-pin_direction)列舉類型的成員，指定篩選上的哪個圖釘正在進行連接。

</dd> <dt>

*pReceivePin* 
</dt> <dd>

此連接嘗試中其他 pin 的 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT**。 可能的值包括下表所示的值。



| 傳回碼                                                                                           | Description                                     |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                  | 成功。<br/>                             |
| <dl> <dt>**VFW \_ E \_ NOT \_ IN \_ GRAPH**</dt> </dl> | 篩選不在篩選圖形中。<br/> |



 

## <a name="remarks"></a>備註

這個方法會覆寫 [**CTransformFilter：： CompleteConnect**](ctransformfilter-completeconnect.md) 方法。

篩選器的行為取決於 pin 連接的順序：

-   如果輸入 pin 是先連接的，則連接會使用暫存配置器。 當輸出連接時，篩選器會重新連接輸入的 pin。 重新連接輸入 pin 會導致上游篩選器重新協商配置器。 在該時間點，輸入釘選來自下游篩選器的配置器。 如需詳細資訊，請參閱 [**CTransInPlaceInputPin：： GetAllocator**](ctransinplaceinputpin-getallocator.md)。
-   如果輸出連接是先連接的，則輸出釘選不會選取配置器。 當輸入 pin 連線時，會為這兩個連接協調配置器。 如果輸入和輸出媒體類型不同，則篩選會使用輸入類型重新連接輸出釘選。

篩選器會藉由呼叫 [**CBaseFilter：： ReconnectPin**](cbasefilter-reconnectpin.md) 方法來執行所有 pin 重新連接。 **ReconnectPin** 方法接著會在篩選圖形管理員上呼叫 [**IFilterGraph2：： ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex)方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transip (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransInPlaceFilter 類別**](ctransinplacefilter.md)
</dt> </dl>

 

 




