---
description: CMediaType 方法 (Mtype 會) 設定另一種媒體類型的媒體類型。 方法使用 ' cmtype ' 參數。
ms.assetid: 71c19d0f-93b6-41db-8659-c64411b83e7c
title: CMediaType： Set 方法 (Mtype .h) -cmtype [ref] 參數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9bf14132660045afbd171173a38d3ea320ba1aa
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/19/2021
ms.locfileid: "106992761"
---
# <a name="cmediatypeset-method-mtypeh---cmtype-ref-parameter"></a>CMediaType： Set 方法 (Mtype .h) -cmtype [ref] 參數

`Set`方法會設定另一種媒體類型的媒體類型。

## <a name="syntax"></a>語法


```C++
HRESULT Set(
  [ref] const CMediaType &cmtype
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*cmtype* \[裁判\]
</dt> <dd>

[**CMediaType**](cmediatype.md)物件的參考。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 \_ [確定] 或 [E \_ OUTOFMEMORY]。

## <a name="remarks"></a>備註

這個方法會從 *cmtype* 複製整個媒體類型。

## <a name="requirements"></a>規格需求

| 需求                   | 值                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭  | Mtype (包含： .h)                                                                                      |
| 程式庫 |  (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建)  |

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaType 類別**](cmediatype.md)
</dt> </dl>

 

 




