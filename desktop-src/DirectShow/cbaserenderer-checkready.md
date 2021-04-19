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
ms.openlocfilehash: 28c0c8bcb6efb0e3cbd648c1e45d36e8b18d4b74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994130"
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

 

 




