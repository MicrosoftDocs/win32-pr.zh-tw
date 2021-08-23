---
description: SetAbortSignal 方法會設定旗標，指出是否要停止轉譯和拒絕進一步的範例。
ms.assetid: 2dbf3b4d-e285-4d17-a77c-01a16c09d148
title: 'CBaseRenderer. SetAbortSignal 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetAbortSignal
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 819f279d20192ff82d9021e03780713f714682abf47aaf854b4568312572e8d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526530"
---
# <a name="cbaserenderersetabortsignal-method"></a>CBaseRenderer. SetAbortSignal 方法

`SetAbortSignal`方法會設定旗標，指出是否要停止轉譯和拒絕進一步的範例。

## <a name="syntax"></a>語法


```C++
void SetAbortSignal(
   BOOL bAbort
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bAbort* 
</dt> <dd>

指出是否要停止轉譯的布林值。 若 **為 TRUE**，則篩選不會再轉譯任何範例。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會設定 [**CBaseRenderer：： m \_ bAbort**](cbaserenderer-m-babort.md) 旗標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




