---
description: SetProperties 方法會設定範例的屬性。 這個方法會實 IMediaSample2：： SetProperties 方法。
ms.assetid: 639aedf5-0c21-4578-b336-91859e40f3be
title: 'CMediaSample. SetProperties 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4bac378d41e0a9933f0903990e6368979c669c048102665a06b2ce59e4a45c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156530"
---
# <a name="cmediasamplesetproperties-method"></a>CMediaSample. SetProperties 方法

`SetProperties`方法會設定範例的屬性。 這個方法會實 [**IMediaSample2：： SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT SetProperties(
         DWORD cbProperties,
   const BYTE  *pbProperties
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*cbProperties* 
</dt> <dd>

要設定之屬性資料的長度（以位元組為單位）。

</dd> <dt>

*pbProperties* 
</dt> <dd>

*CbProperties* 大小的緩衝區指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                                   | 描述                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | Success<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 引數無效<br/>          |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足<br/>       |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | **Null** 指標引數<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaSample 類別**](cmediasample.md)
</dt> </dl>

 

 




