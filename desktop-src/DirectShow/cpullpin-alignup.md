---
description: AlignUp 方法會將值四捨五入到指定的對齊界限。請注意，已在 Windows 7 中移除。 .
ms.assetid: fa2a6567-3eb1-4aa9-b966-2e88b15c67b1
title: 'CPullPin. AlignUp 方法 (Pullpin .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.AlignUp
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4f33ae2b7434d90d909315edda4d49e07d8adab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987137"
---
# <a name="cpullpinalignup-method"></a>CPullPin. AlignUp 方法

**AlignUp** 方法會將值四捨五入到指定的對齊界限。

> [!Note]  
> 已在 Windows 7 中移除。

 

## <a name="syntax"></a>語法


```C++
LONGLONG AlignUp(
   LONGLONG ll,
   LONG     lAlign
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*將* 
</dt> <dd>

指定要對齊的數位。

</dd> <dt>

*lAlign* 
</dt> <dd>

指定對齊界限。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回對齊的結果。

## <a name="remarks"></a>備註

> [!Caution]  
> 如果 *ll* + (*lAlign* -1) 溢位，這個方法可能會造成數值溢位。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Pullpin。h</dt> </dl>                                                                                                       |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPullPin 類別**](cpullpin.md)
</dt> </dl>

 

 




