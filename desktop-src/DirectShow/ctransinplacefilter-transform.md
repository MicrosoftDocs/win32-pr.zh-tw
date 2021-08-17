---
description: 轉換方法會就地轉換範例。
ms.assetid: 2268041b-70d4-48a9-9bb8-4ab921cce649
title: 'CTransInPlaceFilter 轉換方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Transform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 224052bc882792f57eedf9ea58842b953e5853012d3581ef14cad58467b614b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953397"
---
# <a name="ctransinplacefiltertransform-method"></a>CTransInPlaceFilter 轉換方法

`Transform`方法會就地轉換範例。

## <a name="syntax"></a>語法


```C++
virtual HRESULT Transform(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSample* 
</dt> <dd>

範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                             | 描述                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | 請勿傳遞此範例。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 成功。<br/>                    |



 

## <a name="remarks"></a>備註

衍生的類別必須執行此方法。 就地轉換範例資料。 如果篩選準則使用兩個配置器，它會將輸入範例中的資料複製到新的範例，並將該複本傳遞給這個方法。

如果篩選器不應該傳遞此範例 (例如，為了支援品質控制) ，此方法應該會傳回 \_ FALSE。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transip (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransInPlaceFilter 類別**](ctransinplacefilter.md)
</dt> </dl>

 

 




