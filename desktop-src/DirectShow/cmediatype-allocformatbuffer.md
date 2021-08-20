---
description: AllocFormatBuffer 方法會為格式區塊配置記憶體。
ms.assetid: 5ff716c7-f9cf-4b1c-9d3a-62ab955c1392
title: 'CMediaType. AllocFormatBuffer 方法 (Mtype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.AllocFormatBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2c53e739237f2d61a6c59c7fac96e1b97e6343fa6dd209bcf72700cefab7d599
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073982"
---
# <a name="cmediatypeallocformatbuffer-method"></a>CMediaType. AllocFormatBuffer 方法

方法會配置 `AllocFormatBuffer` 格式區塊的記憶體。

## <a name="syntax"></a>語法


```C++
BYTE* AllocFormatBuffer(
   ULONG length
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*length* (長度) 
</dt> <dd>

格式區塊所需的大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回新區塊的指標。 否則，會傳回 **Null**。

## <a name="remarks"></a>備註

如果方法成功配置新的格式區塊，就會釋出現有的格式區塊。 如果配置失敗，方法會保留現有的格式區塊。

方法會更新 **AM \_ 媒體 \_ 類型** 結構的 **cbFormat** 和 **pbFormat** 成員。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Mtype (包含： .h) </dt> </dl>                                                                                     |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaType 類別**](cmediatype.md)
</dt> </dl>

 

 




