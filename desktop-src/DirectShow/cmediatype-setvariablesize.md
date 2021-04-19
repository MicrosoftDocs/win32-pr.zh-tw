---
description: SetVariableSize 方法指定範例沒有固定的大小。
ms.assetid: 2a207cdb-f8e6-44aa-8bf6-868267aeb42d
title: 'CMediaType. SetVariableSize 方法 (Mtype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetVariableSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4621a639b3bc18382bc41ae9425c4de50db920ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987962"
---
# <a name="cmediatypesetvariablesize-method"></a>CMediaType. SetVariableSize 方法

`SetVariableSize`方法指定範例沒有固定的大小。

## <a name="syntax"></a>語法


```C++
void SetVariableSize();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會將 **bFixedSizeSamples** 成員設定為 **FALSE**。 [**CMediaType：： GetSampleSize**](cmediatype-getsamplesize.md)方法的後續呼叫會傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Mtype (包含： .h) </dt> </dl>                                                                                     |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaType 類別**](cmediatype.md)
</dt> </dl>

 

 




