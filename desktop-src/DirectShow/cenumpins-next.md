---
description: 下一個方法會抓取列舉序列中指定的 pin 數目。 這個方法會實 IEnumPins：： Next 方法。
ms.assetid: c38fbd32-7d83-43ec-a105-4a7cb515b471
title: 'CEnumPins 下一個方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 683b8eb5beb9946db7f37d4db53a84c96d5bff7fc91fa4864020fffde5554824
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567078"
---
# <a name="cenumpinsnext-method"></a>CEnumPins. Next 方法

下一個方法會抓取列舉序列中指定的 pin 數目。 這個方法會實 [**IEnumPins：： Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT Next(
   ULONG cPins,
   IPin  **ppPins,
   ULONG *pcFetched
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*cPins* 
</dt> <dd>

要取出的 pin 數目。

</dd> <dt>

*ppPins* 
</dt> <dd>

以 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)指標填滿的大小 *cPins* 陣列。

</dd> <dt>

*pcFetched* 
</dt> <dd>

變數的指標，此變數會接收已抓取的 pin 數目。 如果 *cPins* 是1，則可以是 **Null** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                                                | 描述                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>                    | 未依要求抓取多少 pin。<br/>                                 |
| <dl> <dt>**S \_ 確定**</dt> </dl>                       | 成功。<br/>                                                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | 無效引數。<br/>                                                           |
| <dl> <dt>**E \_ 指標**</dt> </dl>                  | **Null** 指標引數。<br/>                                                  |
| <dl> <dt>**VFW \_ E \_ 列舉 \_ 不 \_ \_ 同步**</dt> </dl> | 篩選的狀態已變更，且現在與列舉值不一致。<br/> |



 

## <a name="remarks"></a>備註

這個方法會從列舉中的目前位置開始，將指標指向指定數目的釘選，然後將它們放在指定的陣列中。

這個方法會呼叫篩選器的 [**CBaseFilter：： GetPin**](cbasefilter-getpin.md) 方法來取出釘選。

如果方法成功，則 **IPin** 指標全都具有未完成的參考計數。 當您完成時，請務必釋放它們。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CEnumPins 類別**](cenumpins.md)
</dt> </dl>

 

 




