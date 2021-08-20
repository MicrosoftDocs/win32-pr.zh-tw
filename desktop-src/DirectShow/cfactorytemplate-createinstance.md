---
description: CreateInstance 方法會呼叫類別的物件建立函數。
ms.assetid: 8a7d5c56-867d-432d-a0c2-97b8e3cf8a69
title: CFactoryTemplate (Combase) 的 CreateInstance 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 816d690a7e57df83b3f521f4591c3334269d0fccebbaeac480e7aacb46253273
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074202"
---
# <a name="cfactorytemplatecreateinstance-method"></a>CFactoryTemplate CreateInstance 方法

`CreateInstance`方法會呼叫類別的物件建立函數。

## <a name="syntax"></a>語法


```C++
CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*朋 克* 
</dt> <dd>

匯總 **IUnknown** 介面的指標。

</dd> <dt>

*phr* 
</dt> <dd>

變數的指標，此變數會接收 **HRESULT** 值，指出方法的成功或失敗。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回類別物件的實例。

## <a name="remarks"></a>備註

**IClassFactory：： CreateInstance** 方法會呼叫這個類別方法。 這個方法會呼叫 [**CFactoryTemplate：： m \_ lpfnNew**](cfactorytemplate-m-lpfnnew.md) 成員變數所指向的函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Combase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CFactoryTemplate 類別**](cfactorytemplate.md)
</dt> </dl>

 

 




