---
description: CreateImageSample 方法會建立媒體範例。
ms.assetid: dae71692-5cbc-4bc7-a363-41766ef17c58
title: 'CImageAllocator. CreateImageSample 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CreateImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57463a7025ea816b6fe6bcaa8b964231458903de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995355"
---
# <a name="cimageallocatorcreateimagesample-method"></a>CImageAllocator. CreateImageSample 方法

`CreateImageSample`方法會建立媒體範例。

## <a name="syntax"></a>語法


```C++
virtual CImageSample* CreateImageSample(
   LPBYTE pData,
   LONG   Length
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*.Pdata* 
</dt> <dd>

大小 *長度* 緩衝區的指標，由呼叫端配置。

</dd> <dt>

*長度* 
</dt> <dd>

緩衝區的長度。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 [**CImageSample**](cimagesample.md) 物件。

## <a name="remarks"></a>備註

這個方法會建立新的媒體範例，實作為 **CImageSample** 物件。 範例的 [**IMediaSample：： GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) 方法會傳回 *.pdata* 參數中所指定之緩衝區的指標。

如果您從 [**CImageAllocator**](cimageallocator.md) 衍生新的配置器類別，並從 [**CImageSample**](cimagesample.md)衍生新的媒體範例類別，您應該覆寫這個方法，以建立媒體範例類別的實例。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CImageAllocator 類別**](cimageallocator.md)
</dt> <dt>

[**CImageAllocator：：配置**](cimageallocator-alloc.md)
</dt> </dl>

 

 




