---
description: CheckMediaType 方法會判斷 pin 是否接受特定的媒體類型。 這個方法會實作為純虛擬 CBasePin：： CheckMediaType 方法。
ms.assetid: 3db7c74c-a6aa-4b49-b2a5-9bf8db35fd7e
title: 'CSourceStream. CheckMediaType 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4cb900d4de448b59eadb4cfd4de28aebf3ac07845fff6a2769c003d37cac846a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633928"
---
# <a name="csourcestreamcheckmediatype-method"></a>CSourceStream. CheckMediaType 方法

`CheckMediaType`方法會判斷 pin 是否接受特定的媒體類型。 這個方法會實作為純虛擬 [**CBasePin：： CheckMediaType**](cbasepin-checkmediatype.md) 方法。

## <a name="syntax"></a>語法


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pMediaType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMediaType* 
</dt> <dd>

[**CMediaType**](cmediatype.md)物件的指標，該物件包含建議的媒體類型。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                            | 描述                                          |
|----------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>   | 此 pin 支援此媒體類型。<br/>        |
| <dl> <dt>**E \_ 失敗**</dt> </dl> | Pin 不支援此媒體類型。<br/> |



 

## <a name="remarks"></a>備註

根據預設，pin 支援單一媒體類型。 這個方法會呼叫 [**CSourceStream：： GetMediaType**](csourcestream-getmediatype.md) 方法的單一參數版本，以抓取支援的型別，並將它與建議的型別進行比較。 如果您的 pin 支援一個以上的媒體類型，請覆寫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>來源 .h (包含) 的資料流程 </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceStream 類別**](csourcestream.md)
</dt> </dl>

 

 




