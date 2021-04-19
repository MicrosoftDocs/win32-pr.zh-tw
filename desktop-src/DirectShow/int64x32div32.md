---
description: Int64x32Div32 函式會將公式 ( (a \* b) + rnd) /c，其中 a 是64位值，b、c 和 rnd 則是32位值。
ms.assetid: 566ac194-5b15-43b7-aa7c-0c18c6f69691
title: 'Int64x32Div32 函式 (Wxutil) '
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
ms.openlocfilehash: de60ca08b262dbf97aa118bd115bd6dc58576a1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993230"
---
# <a name="int64x32div32-function"></a>Int64x32Div32 函式

`Int64x32Div32`函數會實作為 `((a*b)+rnd)/c` 64 位值的公式，而 *b*、 *c* 和 *rnd* 是32位值。

## <a name="syntax"></a>語法


```C++
LONGLONG WINAPI Int64x32Div32(
   LONGLONG a,
   LONG     b,
   LONG     c,
   LONG     rnd
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



| 傳回碼                                                                                       | Description                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**0x7FFFFFFFFFFFFFFF**</dt> </dl> | 發生溢位，因為結果太大 (正) 。<br/> |
| <dl> <dt>**0x8000000000000000**</dt> </dl> | 發生溢位，因為結果太大 (負) 。<br/> |



 

## <a name="remarks"></a>備註

分割區的舍入方向為零。 零除會視為溢位條件。

時間戳記和搜尋時間是64位的值，因此這個函式適用于在32位系統上執行轉換。 例如，在 MPEG 1 中，系統時鐘參考是 90-kHz，或每秒90000刻度。 將此轉換為參考時間的公式 (100-毫微秒單位) 為


```C++
(timestamp * 1000) / 9
```



可以計算為 `Int64x32Div32(timestamp, 1000, 9, 0)` 。 使用 *rnd* 參數作為舍入係數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[其他 Helper 函數](miscellaneous-helper-functions.md)
</dt> <dt>

[**llMulDiv**](llmuldiv.md)
</dt> </dl>

 

 




