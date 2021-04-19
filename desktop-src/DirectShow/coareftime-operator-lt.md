---
description: 這個運算子會測試某個參考時間是否小於另一個。
ms.assetid: 709fb861-a836-4a20-8c93-c0e8ab79f377
title: COARefTime (Ctlutil) 的運算子< 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator<
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1c61403b959f8b5ee19e9ba0d9cd0ab4db54c124
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979452"
---
# <a name="coareftimeoperator-method"></a>COARefTime 運算子< 方法

這個運算子會測試某個參考時間是否小於另一個。

## <a name="syntax"></a>語法


```C++
BOOL operator<(
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

如果此物件嚴格小於 *rt*，則傳回 **TRUE** 。 否則，會傳回 **FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COARefTime 類別**](coareftime.md)
</dt> </dl>

 

 




