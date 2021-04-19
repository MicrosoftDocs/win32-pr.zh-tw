---
description: 這個運算子會測試某個參考時間是否大於另一個參考時間。
ms.assetid: db281040-9bcf-41fc-95b4-5481ffc5061f
title: COARefTime (Ctlutil) 的運算子> 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator>
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7c796bd5194c5bdb2dcbe260b803274962f81347
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991023"
---
# <a name="coareftimeoperator-method"></a>COARefTime 運算子> 方法

這個運算子會測試某個參考時間是否大於另一個參考時間。

## <a name="syntax"></a>語法


```C++
BOOL operator>(
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

如果此物件嚴格大於 *rt*，則傳回 **TRUE** 。 否則，會傳回 **FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COARefTime 類別**](coareftime.md)
</dt> </dl>

 

 




