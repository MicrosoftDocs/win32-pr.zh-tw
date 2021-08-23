---
description: CBaseFilter. StreamTime 方法-StreamTime 方法會抓取目前的資料流程時間。
ms.assetid: 88a2939d-fb51-49fd-af71-21c99511de43
title: 'CBaseFilter. StreamTime 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.StreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: af266e22cb8ee5a2ff5d5d233dc6cfc623e37cd0d34c073db4dbab71d9c221ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635478"
---
# <a name="cbasefilterstreamtime-method"></a>CBaseFilter. StreamTime 方法

**StreamTime** 方法會抓取目前的資料流程時間。

## <a name="syntax"></a>語法


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*rtStream* \[裁判\]
</dt> <dd>

[**CRefTime**](creftime.md)物件的參考，該物件會接收目前的資料流程時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所列的值。



| 傳回碼                                                                                      | 描述                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>             | 成功。<br/>                         |
| <dl> <dt>**VFW \_ E \_ NO \_ CLOCK**</dt> </dl> | 沒有可用的參考時鐘。<br/> |



 

## <a name="remarks"></a>備註

資料流程時間定義為目前的參考時間 (如參考時鐘所指定) 減去 [**CBaseFilter：： m \_ tStart**](cbasefilter-m-tstart.md)) 所指定的開始時間 (。 媒體範例的 *時間戳記* 會指定應呈現的資料流程時間。 如果時間戳記小於目前資料流程時間的樣本尚未轉譯，則會延遲。

這個方法會藉由呼叫 [**IReferenceClock：： GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) 取得目前的參考時間，然後減去初始開始時間，來取得資料流程時間。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectShow 中的時間和時鐘](time-and-clocks-in-directshow.md)
</dt> <dt>

[**CBaseFilter 類別**](cbasefilter.md)
</dt> </dl>

 

 




