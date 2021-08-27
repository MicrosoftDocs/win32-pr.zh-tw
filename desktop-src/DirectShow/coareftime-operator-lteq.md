---
description: 這個運算子會測試某個參考時間是否大於或等於另一個參考時間。
ms.assetid: 1182db5b-2d58-4abb-b9ec-f14c3de5a942
title: 'COARefTime. operator<= 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator<=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 448f36a9c746c22878d8bb0e48028dff211962cbf49827eab3c14f2b4af6b38c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087278"
---
# <a name="coareftimeoperator-method"></a>COARefTime. operator<= 方法

這個運算子會測試某個參考時間是否大於或等於另一個參考時間。

## <a name="syntax"></a>語法


```C++
BOOL operator<=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*rt* \[裁判\]
</dt> <dd>

要比較的 **COARefTime** 物件參考。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個物件大於或等於 *rt*，則傳回 **TRUE** 。 否則，會傳回 **FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COARefTime 類別**](coareftime.md)
</dt> </dl>

 

 




