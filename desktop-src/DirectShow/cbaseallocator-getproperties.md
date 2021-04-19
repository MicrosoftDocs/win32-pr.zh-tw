---
description: GetProperties 方法會抓取配置器將建立的緩衝區數目，以及緩衝區屬性。 這個方法會實 IMemAllocator：： GetProperties 方法。
ms.assetid: ccee4d69-52fc-4e3c-b6a4-787914708be4
title: 'CBaseAllocator. GetProperties 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abf143b11b6dd67fca6c87f9a31ce69f18951311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994089"
---
# <a name="cbaseallocatorgetproperties-method"></a>CBaseAllocator. GetProperties 方法

方法會抓取配置器 `GetProperties` 將建立的緩衝區數目，以及緩衝區屬性。 這個方法會實 [**IMemAllocator：： GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getproperties) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT GetProperties(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pProps* 
</dt> <dd>

配置器 [**\_ 屬性**](/windows/win32/api/strmif/ns-strmif-allocator_properties) 結構的指標，此結構會接收配置器屬性。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseAllocator 類別**](cbaseallocator.md)
</dt> </dl>

 

 




