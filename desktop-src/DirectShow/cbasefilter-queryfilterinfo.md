---
description: QueryFilterInfo 方法會捕獲篩選的相關資訊。 這個方法會實 IBaseFilter：： QueryFilterInfo 方法。
ms.assetid: 0c25aa9e-933c-4c45-a1cc-ffc9253dd561
title: 'CBaseFilter. QueryFilterInfo 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.QueryFilterInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31eb135a29a6e8e1c4f27c28d24b5cbf50eba3bb87b99ba9a1d3a5868c2fbc49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119341738"
---
# <a name="cbasefilterqueryfilterinfo-method"></a>CBaseFilter. QueryFilterInfo 方法

方法會抓取 `QueryFilterInfo` 篩選的相關資訊。 這個方法會實 [**IBaseFilter：： QueryFilterInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT QueryFilterInfo(
   FILTER_INFO *pInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pInfo* 
</dt> <dd>

[**篩選 \_ 資訊**](/windows/win32/api/strmif/ns-strmif-filter_info)結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK 或 E \_ 指標。

## <a name="remarks"></a>備註

這個方法會將篩選的名稱從 [**CBaseFilter：： m \_ pName**](cbasefilter-m-pname.md) 成員變數複製到篩選資訊結構的 **achName** 成員中 \_ 。 如果 **m \_ PName** 為 **Null**，則方法會將 **achName** 設定為 L ' \\ 0 '。

方法會將篩選資訊結構的 **pGraph** 成員設定 \_ 為等於 [**CBaseFilter：： m \_ pGraph**](cbasefilter-m-pgraph.md) 成員變數，並遞增參考計數。 呼叫端必須釋放介面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseFilter 類別**](cbasefilter.md)
</dt> </dl>

 

 




