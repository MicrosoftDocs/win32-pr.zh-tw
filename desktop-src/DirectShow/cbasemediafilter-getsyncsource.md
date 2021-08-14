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
ms.openlocfilehash: 03bceee63109dedbf3b2fa9a855ddbfb410014d48de613f95c7bbfb98d6b0894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658871"
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

 

 




