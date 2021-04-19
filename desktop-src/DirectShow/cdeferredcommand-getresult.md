---
description: GetResult 方法會抓取產生的引數清單（如果有的話）。
ms.assetid: a2a8b17c-3dcf-4f59-89c3-f42070d2a8eb
title: 'CDeferredCommand. GetResult 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetResult
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e8c1638dc33be6457dd682f37e2ddd49e73a111a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999401"
---
# <a name="cdeferredcommandgetresult-method"></a>CDeferredCommand. GetResult 方法

方法會抓取 `GetResult` 產生的引數清單（如果有的話）。

## <a name="syntax"></a>語法


```C++
VARIANT* GetResult();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **變數** 的指標，其中包含方法的引數清單（如果有的話）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDeferredCommand 類別**](cdeferredcommand.md)
</dt> </dl>

 

 




