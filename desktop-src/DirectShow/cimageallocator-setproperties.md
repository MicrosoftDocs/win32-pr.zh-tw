---
description: SetProperties 方法會指定要配置的緩衝區數目和每個緩衝區的大小。 這個方法會覆寫 CBaseAllocator：： SetProperties 方法。
ms.assetid: 8d419432-a9a7-44fb-b916-8dacd08eb6ec
title: 'CImageAllocator. SetProperties 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c04501fe3511d9cdd45f3513c68082d2ffece0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984818"
---
# <a name="cimageallocatorsetproperties-method"></a>CImageAllocator. SetProperties 方法

`SetProperties`方法會指定要配置的緩衝區數目和每個緩衝區的大小。 這個方法會覆寫 [**CBaseAllocator：： SetProperties**](cbaseallocator-setproperties.md) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT SetProperties(
   ALLOCATOR_PROPERTIES *pRequest,
   ALLOCATOR_PROPERTIES *pActual
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pRequest* 
</dt> <dd>

配置器 [**\_ 屬性**](/windows/win32/api/strmif/ns-strmif-allocator_properties) 結構的指標，其中包含緩衝區需求。

</dd> <dt>

*pActual* 
</dt> <dd>

配置器 **\_ 屬性** 結構的指標，此結構會接收實際的緩衝區屬性。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

這個方法會呼叫 [**CImageAllocator：： CheckSizes**](cimageallocator-checksizes.md) 來驗證要求的緩衝區大小。 它也會呼叫的基類版本 `SetProperties` 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CImageAllocator 類別**](cimageallocator.md)
</dt> </dl>

 

 




