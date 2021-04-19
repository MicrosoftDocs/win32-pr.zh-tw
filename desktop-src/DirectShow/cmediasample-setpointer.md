---
description: SetPointer 方法會將指標設定為記憶體緩衝區。
ms.assetid: 60627600-c982-462e-b540-327a58e57615
title: 'CMediaSample. SetPointer 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetPointer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67d9fc5d260cc627919a458593328c36f0de9a94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999123"
---
# <a name="cmediasamplesetpointer-method"></a>CMediaSample. SetPointer 方法

`SetPointer`方法會將指標設定為記憶體緩衝區。

## <a name="syntax"></a>語法


```C++
HRESULT SetPointer(
   BYTE *ptr,
   LONG cBytes
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ptr* 
</dt> <dd>

呼叫端所配置的記憶體緩衝區指標，大小為 *cBytes*。

</dd> <dt>

*cBytes* 
</dt> <dd>

緩衝區的長度（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

此方法可讓配置器設定範例的新指標。

這個方法無法透過 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面使用。 建立範例的物件可以透過 **CMediaSample**) 存取此方法 (，但其他物件則不能。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaSample 類別**](cmediasample.md)
</dt> </dl>

 

 




