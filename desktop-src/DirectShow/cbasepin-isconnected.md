---
description: IsConnected 方法會判斷釘選是否連接到另一個 pin。
ms.assetid: d8b9b43b-6f8d-4d75-9688-f0cee3794a78
title: 'CBasePin. IsConnected 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.IsConnected
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 95bfbe3613482d879bde4945d32e3df590c9bd5491b9f274442f3315771f9f96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955177"
---
# <a name="cbasepinisconnected-method"></a>CBasePin. IsConnected 方法

`IsConnected`方法會判斷 pin 是否已連接到另一個 pin。

## <a name="syntax"></a>語法


```C++
BOOL IsConnected();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果釘選連接，則傳回 **TRUE** 。 否則，會傳回 **FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




