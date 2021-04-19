---
description: IsEqualObject 函式會檢查兩個介面是否位於相同的物件上。
ms.assetid: 51325e05-5a7f-4a80-a12e-2e7dedc028e2
title: 'IsEqualObject 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsEqualObject
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e959d687d7d6b11dc6055daeda789e728d875d70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999160"
---
# <a name="isequalobject-function"></a>IsEqualObject 函式

`IsEqualObject`函數會檢查兩個介面是否位於相同的物件上。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI IsEqualObject(
   IUnknown *pFirst,
   IUnknown *pSecond
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFirst* 
</dt> <dd>

指向某個介面的指標。

</dd> <dt>

*pSecond* 
</dt> <dd>

指向其他介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果介面同時位於相同的物件上，則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[其他 Helper 函數](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




