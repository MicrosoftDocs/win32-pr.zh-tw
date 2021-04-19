---
description: QueryVendorInfo 方法會抓取包含廠商資訊的字串。 這個方法會實 IBaseFilter：： QueryVendorInfo 方法。
ms.assetid: 083c0556-d516-4daf-8621-e158ea78b5a3
title: 'CBaseFilter. QueryVendorInfo 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.QueryVendorInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1786477c042bb1d9ecc6340056a771141d0a3c74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994904"
---
# <a name="cbasefilterqueryvendorinfo-method"></a>CBaseFilter. QueryVendorInfo 方法

方法會抓取 `QueryVendorInfo` 包含廠商資訊的字串。 這個方法會實 [**IBaseFilter：： QueryVendorInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryvendorinfo) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT QueryVendorInfo(
   LPWSTR *pVendorInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVendorInfo* 
</dt> <dd>

變數的位址，此變數會接收包含廠商資訊之寬字元字串的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 E \_ >notimpl。

## <a name="remarks"></a>備註

若要提供篩選準則的廠商資訊，請覆寫這個方法。 如果您執行此方法，請使用 **CoTaskMemAlloc** 函數來配置字串的記憶體。 呼叫端負責呼叫 **CoTaskMemFree** 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseFilter 類別**](cbasefilter.md)
</dt> </dl>

 

 




