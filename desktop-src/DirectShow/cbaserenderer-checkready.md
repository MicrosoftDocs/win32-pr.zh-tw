---
description: CheckReady 方法會查詢狀態轉換是否已完成。
ms.assetid: dfa669ed-a5ab-498e-9fc2-ff15d6ddbc13
title: 'CBaseRenderer. CheckReady 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CheckReady
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a1fac55eba92141ac8174b30ed2dcbc4685ba250b7bb21236432bb998b3b5e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043948"
---
# <a name="cbaserenderercheckready-method"></a>CBaseRenderer. CheckReady 方法

`CheckReady`方法會查詢狀態轉換是否已完成。

## <a name="syntax"></a>語法


```C++
BOOL CheckReady();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果狀態轉換完成，則傳回 **TRUE** ; 如果篩選仍在轉換成新狀態，則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> <dt>

[**CBaseRenderer：： NotReady**](cbaserenderer-notready.md)
</dt> <dt>

[**CBaseRenderer：： Ready**](cbaserenderer-ready.md)
</dt> </dl>

 

 




