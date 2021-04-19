---
description: EqualPins 函式會檢查兩個圖釘是否位於相同的物件上。
ms.assetid: b6a92cb6-f4a9-4a14-831c-3b123e4692c0
title: 'EqualPins 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EqualPins
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fdf499b494f41a0acc5cc446bc92deade61c045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994185"
---
# <a name="equalpins-function"></a>EqualPins 函式

EqualPins 函式會檢查兩個圖釘是否位於相同的物件上。

## <a name="syntax"></a>語法


```C++
BOOL EqualPins(
   IUnknown *pPin1,
   IUnknown *pPin2
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pPin1* 
</dt> <dd>

指向一個釘選的指標。

</dd> <dt>

*pPin2* 
</dt> <dd>

指向其他釘選的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果兩個圖釘都在相同的物件上，則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[其他 Helper 函數](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




