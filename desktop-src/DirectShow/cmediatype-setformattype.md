---
description: SetFormatType 方法會指定格式類型。
ms.assetid: e8ed9190-7169-4d51-ace7-597f43ff083e
title: 'CMediaType. SetFormatType 方法 (Mtype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetFormatType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f6a0582a882ffe40a9bd889ff48e70a52a4048bad57e01077263e607f13d9898
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954417"
---
# <a name="cmediatypesetformattype-method"></a>CMediaType. SetFormatType 方法

' ' SetFormatType 方法會指定格式類型。

## <a name="syntax"></a>語法


```C++
void SetFormatType(
   const GUID *pformattype
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pformattype* 
</dt> <dd>

指定格式類型之 **GUID** 的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會設定 **formattype** 成員。 格式類型會定義格式區塊的版面配置。 例如，如果格式類型為 \_ VIDEOINFO 格式，則格式區塊應該包含 **VIDEOINFOHEADER** 結構。 若要設定格式區塊，請呼叫 [**CMediaType：： SetFormat**](cmediatype-setformat.md) 方法。 呼叫端負責確定格式區塊符合格式類型。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Mtype (包含： .h) </dt> </dl>                                                                                     |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaType 類別**](cmediatype.md)
</dt> </dl>

 

 


``
