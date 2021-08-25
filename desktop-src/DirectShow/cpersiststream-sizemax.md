---
description: 抓取目前資料流程所需的最大位元組大小，不包含版本號碼。
ms.assetid: ca1a68e2-02b4-4eea-916a-e0418ae811ae
title: 'CPersistStream. SizeMax 方法 (Pstream .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.SizeMax
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b8f2c547e75303e4c54a49651f2118a90768bc0f42161ee3dae0de9bec2dcad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813298"
---
# <a name="cpersiststreamsizemax-method"></a>CPersistStream. SizeMax 方法

抓取目前資料流程所需的最大位元組大小，不包含版本號碼。

## <a name="syntax"></a>語法


```C++
virtual int SizeMax();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回資料所需的位元組數目，不包括版本號碼。

## <a name="remarks"></a>備註

預設版本傳回零;應該覆寫它，以提供一些其他適當的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Pstream (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPersistStream 類別**](cpersiststream.md)
</dt> </dl>

 

 




