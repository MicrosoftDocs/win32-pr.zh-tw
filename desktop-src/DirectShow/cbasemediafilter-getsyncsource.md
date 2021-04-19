---
description: GetSyncSource 方法會抓取物件正在使用的參考時鐘。 這個方法會實 IMediaFilter：： GetSyncSource 方法。
ms.assetid: 7e74d6ce-cd34-4345-8ff9-174e0acb243a
title: 'CBaseMediaFilter. GetSyncSource 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1e92c9d0fa5e486d7785ff8184ba4ce0dd42e5be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982535"
---
# <a name="cbasemediafiltergetsyncsource-method"></a>CBaseMediaFilter. GetSyncSource 方法

`GetSyncSource`方法會抓取物件正在使用的參考時鐘。 這個方法會實 [**IMediaFilter：： GetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT GetSyncSource(
   IReferenceClock **pClock
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pClock* 
</dt> <dd>

接收時鐘 [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) 介面指標的變數位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK 或 E \_ 指標。

## <a name="remarks"></a>備註

如果物件未使用參考時鐘， *\* pClock* 會設為 **Null**。 當方法傳回時，如果 *\* pClock* 為非 **Null**，則 **IReferenceClock** 介面具有未處理的參考計數。 當您完成時，請務必放開。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseMediaFilter 類別**](cbasemediafilter.md)
</dt> </dl>

 

 




