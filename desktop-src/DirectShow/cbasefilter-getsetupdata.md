---
description: GetSetupData 方法會捕獲篩選的註冊資料。
ms.assetid: 93582c75-4f40-492c-919c-c8a06dce7715
title: 'CBaseFilter. GetSetupData 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetSetupData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40223a22f4de4a078ce84f8ebe49bddd5ab13575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979461"
---
# <a name="cbasefiltergetsetupdata-method"></a>CBaseFilter. GetSetupData 方法

方法會抓取 `GetSetupData` 篩選的註冊資料。

> [!Note]  
> 這個方法已過時。 它是由 [**CBaseFilter：： Register**](cbasefilter-register.md) 和 [**CBaseFilter：：取消註冊**](cbasefilter-unregister.md) 方法所呼叫。

 

## <a name="syntax"></a>語法


```C++
virtual LPAMOVIESETUP_FILTER GetSetupData();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 [**AMOVIESETUP \_ 篩選**](amoviesetup-filter.md) 結構的指標，其中包含篩選準則的註冊資訊。

## <a name="remarks"></a>備註

基類會傳回 **Null**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseFilter 類別**](cbasefilter.md)
</dt> </dl>

 

 




