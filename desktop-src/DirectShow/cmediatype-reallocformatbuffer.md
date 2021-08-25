---
description: ReallocFormatBuffer 方法會將格式區塊重新配置為新的大小。
ms.assetid: 49bec677-09cc-4e1a-994a-13e873e61713
title: 'CMediaType. ReallocFormatBuffer 方法 (Mtype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.ReallocFormatBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7bd4d7bd27c3698f1e30c690f755f445ffaffeff37c88f27d0a5c8ba58cd2d32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768168"
---
# <a name="cmediatypereallocformatbuffer-method"></a>CMediaType. ReallocFormatBuffer 方法

方法會將 `ReallocFormatBuffer` 格式區塊重新配置為新的大小。

## <a name="syntax"></a>語法


```C++
BYTE* ReallocFormatBuffer(
   ULONG length
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*length* (長度) 
</dt> <dd>

格式區塊所需的新大小（以位元組為單位）。 必須大於零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回新區塊的指標。 否則，會傳回舊格式區塊的指標，或傳回 **Null**。

## <a name="remarks"></a>備註

這個方法會配置新的格式區塊。 它會將現有的格式區塊盡可能複製到新的格式區塊。 如果新區塊小於現有區塊，則會截斷現有的格式區塊。 如果新的區塊更大，則不會定義其他空間的內容。 它們不會明確設定為零。

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

 

 




