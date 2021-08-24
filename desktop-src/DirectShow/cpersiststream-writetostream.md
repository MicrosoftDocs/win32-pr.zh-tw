---
description: 將篩選的資料寫入至指定的資料流程。
ms.assetid: 1b405050-6cfd-4b69-b449-f00a6ecfac6a
title: 'CPersistStream. WriteToStream 方法 (Pstream .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.WriteToStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 139818d1434163255c62dd5cb109dbf505cea03b5876de14eb2aa4a0636f072f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813288"
---
# <a name="cpersiststreamwritetostream-method"></a>CPersistStream. WriteToStream 方法

將篩選的資料寫入至指定的資料流程。

## <a name="syntax"></a>語法


```C++
virtual HRESULT WriteToStream(
   IStream *pStream
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pStream* 
</dt> <dd>

指定篩選資料之目的地資料流程的 **IStream** 介面指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。 衍生類別應該會傳回有效的 **HRESULT** 值。

## <a name="remarks"></a>備註

預設版本不會寫入任何內容;您可以覆寫它來寫入您類別的特定資料。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Pstream (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPersistStream 類別**](cpersiststream.md)
</dt> </dl>

 

 




