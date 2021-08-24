---
description: 抓取目前資料流程所需的最大位元組大小，包括版本號碼。
ms.assetid: 55ea4568-5ca4-4139-8def-bef20071835d
title: 'CPersistStream. GetSizeMax 方法 (Pstream .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetSizeMax
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 746fb01102642f2d3e6b254ac741c284143aaecfd401fc220bf7a9d97d93e64e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813368"
---
# <a name="cpersiststreamgetsizemax-method"></a>CPersistStream. GetSizeMax 方法

抓取目前資料流程所需的最大位元組大小，包括版本號碼。

## <a name="syntax"></a>語法


```C++
HRESULT GetSizeMax(
   ULARGE_INTEGER *pcbSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pcbSize* 
</dt> <dd>

儲存此資料流程所需的大小（以位元組為單位），包括版本號碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

此成員函式會實作為 **IPersistStream：： GetSizeMax** 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Pstream (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPersistStream 類別**](cpersiststream.md)
</dt> </dl>

 

 




