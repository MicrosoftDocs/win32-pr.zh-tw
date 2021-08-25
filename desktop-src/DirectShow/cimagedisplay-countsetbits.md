---
description: CountSetBits 方法會傳回在指定位欄位中設定為1的位數目。
ms.assetid: fc5701b8-88ff-4c23-9d26-854bb65cc55c
title: 'CImageDisplay. CountSetBits 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CountSetBits
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d334111c18c2c94c79a8b49ed7c0601efabb2bd13922a68c292970d4d2c379bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824068"
---
# <a name="cimagedisplaycountsetbits-method"></a>CImageDisplay. CountSetBits 方法

方法會傳回在 `CountSetBits` 指定位欄位中設定為1的位數目。

## <a name="syntax"></a>語法


```C++
DWORD CountSetBits(
   const DWORD Field
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*欄位* 
</dt> <dd>

將位欄位指定為 **DWORD** 值。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回設定為1的位數目。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CImageDisplay 類別**](cimagedisplay.md)
</dt> </dl>

 

 




