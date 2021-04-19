---
description: JoinFilterGraph 方法會通知篩選其已加入或離開篩選圖形。 這個方法會實 IBaseFilter：： JoinFilterGraph 方法。
ms.assetid: ee02650c-aaf0-4a0e-914f-180230010709
title: 'CBaseFilter. JoinFilterGraph 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.JoinFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 45453c6423b8fa9f68e5d8dff86d13b130d65f6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993607"
---
# <a name="cbasefilterjoinfiltergraph-method"></a>CBaseFilter. JoinFilterGraph 方法

`JoinFilterGraph`方法會通知篩選其已加入或離開篩選圖形。 這個方法會實 [**IBaseFilter：： JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT JoinFilterGraph(
       IFilterGraph *pGraph,
  [in] LPCWSTR      pName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pGraph* 
</dt> <dd>

篩選圖形管理員 [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) 介面的指標，如果篩選離開圖形，則為 **Null** 。

</dd> <dt>

*pName* \[在\]
</dt> <dd>

包含篩選名稱的 Unicode 字串指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

這個方法會設定等於 *pGraph* 參數的 [**CBaseFilter：： m \_ pGraph**](cbasefilter-m-pgraph.md)成員變數。 它也會查詢 [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) 介面指標，並將它儲存在 [**CBaseFilter：： m \_ pSink**](cbasefilter-m-psink.md) 成員變數中。 但是，篩選不會在其中一個介面上保留參考計數。 這麼做會建立迴圈參考計數，因為篩選圖形管理員會保留篩選的參考計數。

方法會將 *pName* 指定的字串複製到 [**CBaseFilter：： m \_ pName**](cbasefilter-m-pname.md) 成員變數中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseFilter 類別**](cbasefilter.md)
</dt> </dl>

 

 




