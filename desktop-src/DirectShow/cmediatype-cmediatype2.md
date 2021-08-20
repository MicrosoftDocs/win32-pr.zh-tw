---
description: 深入瞭解 CMediaType. CMediaType (Mtype 的) 方法。 這個方法會使用 ' majortype ' 參數。
ms.assetid: 89356578-0509-46c1-abd4-421688017f1d
title: CMediaType. CMediaType 函式 (Mtype .h) -majortype 參數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b1ebf3cec41c4180a4dcad4a5a7c273996f70bfdb6d052127ff71dd1b929238c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073992"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---majortype-parameter"></a>CMediaType. CMediaType 函式 (Mtype .h) -majortype 參數

函式方法。

## <a name="syntax"></a>語法


```C++
CMediaType(
   const GUID *majortype
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*majortype* 
</dt> <dd>

主要類型 **GUID** 的指標。 此函式會將主要類型 GUID 初始化為此值。

</dd> </dl>

## <a name="remarks"></a>備註

此函式會呼叫 [**CMediaType：： InitMediaType**](cmediatype-initmediatype.md) 方法來初始化媒體類型。

## <a name="requirements"></a>規格需求

| 需求                   | 值                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭  | Mtype (包含： .h)                                                                                      |
| 程式庫 |  (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建)  |

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaType 類別**](cmediatype.md)
</dt> </dl>

 

 




