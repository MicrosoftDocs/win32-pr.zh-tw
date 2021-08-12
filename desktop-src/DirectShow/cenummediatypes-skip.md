---
description: Skip 方法會略過指定數目的媒體類型。 這個方法會實 IEnumMediaTypes：： Skip 方法。
ms.assetid: a01fb084-b227-4ca6-b5ca-c57d56e8b1aa
title: 'CEnumMediaTypes. Skip 方法 (Amfilter. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Skip
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a9930472b5c8a2873ca0a7f3280565bd41ac6b0aac7e1e33303464d3a2c1ca3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118656443"
---
# <a name="cenummediatypesskip-method"></a>CEnumMediaTypes. Skip 方法

`Skip`方法會略過指定數目的媒體類型。 這個方法會實 [**IEnumMediaTypes：： Skip**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-skip) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT Skip(
   ULONG cMediaTypes
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*cMediaTypes* 
</dt> <dd>

要略過的媒體類型數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                                                | 描述                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>                    | 略過序列結尾的尾端。<br/>                                    |
| <dl> <dt>**S \_ 確定**</dt> </dl>                       | 成功。<br/>                                                                 |
| <dl> <dt>**VFW \_ E \_ 列舉 \_ 不 \_ \_ 同步**</dt> </dl> | Pin 的狀態已變更，且現在與列舉值不一致。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CEnumMediaTypes 類別**](cenummediatypes.md)
</dt> </dl>

 

 




