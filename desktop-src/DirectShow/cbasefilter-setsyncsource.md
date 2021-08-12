---
description: SetSyncSource 方法會設定篩選的參考時鐘。 這個方法會實 IMediaFilter：： SetSyncSource 方法。
ms.assetid: 298039fc-dd38-4063-8752-2669b134b8ef
title: 'CBaseFilter. SetSyncSource 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 95e1f1b3578fa88d4616fc9e0b7d0af9fe89ab80c2e93ee32eef305b93d45478
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659584"
---
# <a name="cbasefiltersetsyncsource-method"></a>CBaseFilter. SetSyncSource 方法

**SetSyncSource** 方法會設定篩選的參考時鐘。 這個方法會實 [**IMediaFilter：： SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT SetSyncSource(
   IReferenceClock *pClock
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pClock* 
</dt> <dd>

時鐘 [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) 介面的指標，或 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseFilter 類別**](cbasefilter.md)
</dt> </dl>

 

 




