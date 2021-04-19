---
description: SetPreroll 方法會指定此範例是否為可提前取樣。 不應顯示預先提供的範例。 這個方法會實 IMediaSample：： SetPreroll 方法。
ms.assetid: 2887e627-5999-407a-88d3-811c803c9a43
title: 'CMediaSample. SetPreroll 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 594f26ebb738a986c85a14b88f8896b122b58f47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977428"
---
# <a name="cmediasamplesetpreroll-method"></a>CMediaSample. SetPreroll 方法

`SetPreroll`方法會指定此範例是否為可提前取樣。 不應顯示預先提供的範例。 這個方法會實 [**IMediaSample：： SetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setpreroll) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT SetPreroll(
   BOOL bIsPreroll
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bIsPreroll* 
</dt> <dd>

布林值，指定這是否為可提前取樣。 若 **為 TRUE**，表示此為預先設置的範例。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

這個方法會更新 [**CMediaSample：： m \_ dwFlags**](cmediasample-m-dwflags.md) 成員變數，以指定預先執行的屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaSample 類別**](cmediasample.md)
</dt> </dl>

 

 




