---
description: TranslateAccelerator 方法會指示屬性頁處理按鍵。 這個方法會實 IPropertyPage：： TranslateAccelerator 方法。
ms.assetid: 2da214c9-35dc-470c-9b7f-2f4ef6bcd40a
title: 'CBasePropertyPage. TranslateAccelerator 方法 (Cprop .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.TranslateAccelerator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3116e85eec8fbf3a00bf434a1f88c8cac662ed0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986795"
---
# <a name="cbasepropertypagetranslateaccelerator-method"></a>CBasePropertyPage. TranslateAccelerator 方法

`TranslateAccelerator`方法會指示屬性頁處理按鍵。 這個方法會實 **IPropertyPage：： TranslateAccelerator** 方法。

## <a name="syntax"></a>語法


```C++
HRESULT TranslateAccelerator(
   LPMSG lpMsg
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpMsg* 
</dt> <dd>

訊息 **結構的** 指標，描述要處理的按鍵。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 E \_ >notimpl。

## <a name="remarks"></a>備註

如果您想要提供屬性頁的鍵盤快速鍵，請覆寫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Cprop (包含： .h) </dt> </dl>                                                                                     |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePropertyPage 類別**](cbasepropertypage.md)
</dt> </dl>

 

 




