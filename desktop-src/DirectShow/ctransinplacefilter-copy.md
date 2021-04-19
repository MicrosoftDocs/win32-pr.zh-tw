---
description: 複製方法會複製媒體範例。
ms.assetid: 3fbc6925-6e9c-4419-ab0d-0bbdbdf9bb8e
title: 'CTransInPlaceFilter 複製方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Copy
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3063427611cd3a5aae74fecf6be273c07fdb917c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978498"
---
# <a name="ctransinplacefiltercopy-method"></a>CTransInPlaceFilter 複製方法

`Copy`方法會複製媒體範例。

## <a name="syntax"></a>語法


```C++
IMediaSample* Copy(
   IMediaSample *pSource
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSource* 
</dt> <dd>

範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回新範例上 **IMediaSample** 介面的指標。

## <a name="remarks"></a>備註

這個方法會從下游配置器抓取空的緩衝區。 它會將 *pSource* 中的所有範例屬性複製到新的範例中，以及範例中的實際資料。 如果篩選準則使用兩個配置器，則會呼叫這個方法來跨緩衝區複製資料。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transip (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransInPlaceFilter 類別**](ctransinplacefilter.md)
</dt> </dl>

 

 




