---
description: 這個運算子會測試 CMediaType 物件是否相等。
ms.assetid: d50f3a72-c5e8-44a5-aa0e-b1c40a19fee3
title: 'CMediaType. CMediaType：： operator = = 方法 (Mtype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator==
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 93bc74338f994b967f313b7ed77529f9d90a8d01992b74cf4010f9aa51ab6a9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043647"
---
# <a name="cmediatypecmediatypeoperator-method"></a>CMediaType. CMediaType：： operator = = 方法

這個運算子會測試 [**CMediaType**](cmediatype.md) 物件是否相等。

## <a name="syntax"></a>語法


```C++
BOOL CMediaType::operator==(
  [ref] const CMediaType &rt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*rt* \[裁判\]
</dt> <dd>

要比較的 **CMediaType** 物件參考。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果 *rt* 等於這個物件，**則傳回 TRUE** 。 否則，會傳回 **FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Mtype (包含： .h) </dt> </dl>                                                                                     |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaType 類別**](cmediatype.md)
</dt> </dl>

 

 




