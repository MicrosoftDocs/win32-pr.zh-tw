---
description: 抓取此篩選準則的類別識別碼。
ms.assetid: f0559437-5d0d-4522-a3dc-947e3494b576
title: 'CPersistStream. GetClassID 方法 (Pstream .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e500b91453bd7c9d76f243939a98b0779f1873ed7b5f79128e639173710e62de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915558"
---
# <a name="cpersiststreamgetclassid-method"></a>CPersistStream. GetClassID 方法

抓取此篩選準則的類別識別碼。

## <a name="syntax"></a>語法


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pClsID* 
</dt> <dd>

CLSID 結構的指標。 將您的類別識別碼複製到這裡。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Pstream (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPersistStream 類別**](cpersiststream.md)
</dt> </dl>

 

 




