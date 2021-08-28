---
description: Get 方法會在指定的位置抓取專案。
ms.assetid: cafa4083-96e6-4ed3-afbc-5828b7f1c5be
title: 'CGenericList： Get 方法 (Wxlist) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Get
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dae90872ea607571b215aafe3f9f35a645cd50d140dcbad0783369ce2189c881
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813768"
---
# <a name="cgenericlistget-method"></a>CGenericList. Get 方法

`Get`方法會在指定的位置抓取專案。

## <a name="syntax"></a>語法


```C++
OBJECT* Get(
   POSITION pos
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pos* 
</dt> <dd>

要取得之專案的位置指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回)  (範本型別 **物件** 之物件的指標。

## <a name="remarks"></a>備註

如果 *pos* 是 **null**，則方法會傳回 **null**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxlist (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CGenericList 類別**](cgenericlist.md)
</dt> </dl>

 

 




