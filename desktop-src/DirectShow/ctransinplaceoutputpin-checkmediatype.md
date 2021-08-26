---
description: CTransInPlaceOutputPin. CheckMediaType 方法-CheckMediaType 方法會判斷 pin 是否接受特定的媒體類型。
ms.assetid: be720021-ef7b-4281-a9f4-93abbdafc75d
title: 'CTransInPlaceOutputPin. CheckMediaType 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2816d148af2a7514dc28a71036402f3781e47a0144848a2ea81bbb94d339f961
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999028"
---
# <a name="ctransinplaceoutputpincheckmediatype-method"></a>CTransInPlaceOutputPin. CheckMediaType 方法

`CheckMediaType`方法會判斷 pin 是否接受特定的媒體類型。

## <a name="syntax"></a>語法


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Pmt* 
</dt> <dd>

[**CMediaType**](cmediatype.md)物件的指標，該物件包含建議的媒體類型。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                                                | 描述                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                       | 成功。<br/>                 |
| <dl> <dt>**\_ \_ \_ 未接受 VFW E \_ 類型**</dt> </dl> | 媒體類型不被接受。<br/> |



 

## <a name="remarks"></a>備註

這個方法會覆寫 [**CTransformOutputPin：： CheckMediaType**](ctransformoutputpin-checkmediatype.md) 方法。

如果篩選已經進行串流處理，而且使用兩個配置器，這個方法會拒絕任何格式變更。 否則，這個方法會呼叫篩選器的 [**CTransformFilter：： CheckInputType**](ctransformfilter-checkinputtype.md) 方法來檢查媒體類型。 如果輸入連接已連線，它也會在上游輸出 pin 上呼叫 [**IPin：： QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transip (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransInPlaceOutputPin 類別**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




