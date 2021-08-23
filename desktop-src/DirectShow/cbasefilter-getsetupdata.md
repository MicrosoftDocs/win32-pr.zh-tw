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
ms.openlocfilehash: f86bc35688ab0ec1c19053a95cbfd2025cf45ad666ef419fdb8440c6a844cb61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640468"
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

 

 




