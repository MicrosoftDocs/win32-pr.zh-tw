---
description: LlMulDiv 函式會將公式 ( (a \* b) + rnd) /c，其中每個詞彙都是64位值。
ms.assetid: cd5073b9-27c7-42ee-8487-2d4ea29f77d4
title: 'llMulDiv 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Int64x32Div32
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: df58175955106906027a6d2d10c465b82ad6313cd493e3ef9ef3ba279cd0115f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952347"
---
# <a name="llmuldiv-function"></a>llMulDiv 函式

`llMulDiv`函數會執行公式， `((a*b)+rnd)/c` 其中每個詞彙都是64位值。

時間戳記和搜尋時間是64位的值，因此這個函式適用于在32位系統上執行轉換。 例如，每秒位元組數的公式為


```C++
(Number of Bytes * Reference Time) / 10,000,000
```



可以計算為 `llMulDiv(nBytes, rtTime, 10000000, 0)` 。 使用 *rnd* 參數作為舍入係數。

## <a name="syntax"></a>語法


```C++
LONGLONG WINAPI Int64x32Div32(
   LONGLONG a,
   LONGLONG b,
   LONGLONG c,
   LONGLONG rnd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*的* 
</dt> <dd>

被乘數.

</dd> <dt>

*b* 
</dt> <dd>

乘數。

</dd> <dt>

*c* 
</dt> <dd>

因數。

</dd> <dt>

*rnd* 
</dt> <dd>

進位係數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 `(a * b + rnd)/c` 計算或下列其中一個值。



| 傳回碼                                                                                       | 描述                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**0x7FFFFFFFFFFFFFFF**</dt> </dl> | 發生溢位，因為結果太大 (正) 。<br/> |
| <dl> <dt>**0x8000000000000000**</dt> </dl> | 發生溢位，因為結果太大 (負) 。<br/> |



 

## <a name="remarks"></a>備註

分割區的舍入方向為零。 零除會視為溢位條件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[其他 Helper 函數](miscellaneous-helper-functions.md)
</dt> <dt>

[**Int64x32Div32**](int64x32div32.md)
</dt> </dl>

 

 




