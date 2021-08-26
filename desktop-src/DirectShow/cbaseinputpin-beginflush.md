---
description: CBaseInputPin 方法會開始進行清除作業。 這個方法會實 IPin：： BeginFlush 方法。
ms.assetid: 3f149d4f-765b-44c1-87e5-6313f6a4d50d
title: 'CBaseInputPin. BeginFlush 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1b9e5e4e97a3a010523f61cc9efedf224d8dfc7fa373c9514b6d38dc0105d2d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103208"
---
# <a name="cbaseinputpinbeginflush-method"></a>CBaseInputPin. BeginFlush 方法

`CBaseInputPin`方法會開始清除作業。 這個方法會實 [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

這個方法會將 [**CBaseInputPin：： m \_ bFlushing**](cbaseinputpin-m-bflushing.md) 旗標設定為 **TRUE**，這會導致 [**CBaseInputPin：： Receive**](cbaseinputpin-receive.md) 方法拒絕其他任何範例。

衍生的類別必須覆寫這個方法，並執行下列步驟：

1.  對下游輸入 pin 呼叫 [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 方法。 如果 pin 尚未提供任何下游媒體範例，您可以略過此步驟。 如果您的輸出圖釘衍生自 [**CBaseOutputPin**](cbaseoutputpin.md) 類別，您可以呼叫 [**CBaseOutputPin：:D eliverbeginflush**](cbaseoutputpin-deliverbeginflush.md) 方法。
2.  呼叫基類方法。
3.  開始捨棄已排入佇列的資料。
4.  從任何封鎖的呼叫傳回至 **Receive** 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseInputPin 類別**](cbaseinputpin.md)
</dt> </dl>

 

 




