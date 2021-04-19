---
description: GetProperties 方法會抓取範例的屬性。 這個方法會實 IMediaSample2：： GetProperties 方法。
ms.assetid: c2a6d611-9c17-41fb-bb6d-f5b17f1c9966
title: 'CMediaSample. GetProperties 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 06ee1022f298e2f5167d348777b33fc2f1703eef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989696"
---
# <a name="cmediasamplegetproperties-method"></a>CMediaSample. GetProperties 方法

`GetProperties`方法會捕獲範例的屬性。 這個方法會實 [**IMediaSample2：： GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT GetProperties(
   DWORD cbProperties,
   BYTE  *pbProperties
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*cbProperties* 
</dt> <dd>

要取出的屬性資料長度（以位元組為單位）。

</dd> <dt>

*pbProperties* 
</dt> <dd>

*CbProperties* 大小的緩衝區指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                               | Description                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>      | 成功。<br/>                   |
| <dl> <dt>**E \_ 指標**</dt> </dl> | **Null** 指標引數。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaSample 類別**](cmediasample.md)
</dt> </dl>

 

 




