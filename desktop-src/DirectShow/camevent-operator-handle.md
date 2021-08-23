---
description: 捕獲事件控制碼。 這個運算子不支援做為左值。
ms.assetid: 9000d6d1-bbca-44ac-8808-0b3b827086c5
title: 'CAMEvent 處理方法 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.operator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afc3bcc1044d3d14b7ebf77ce12027fb3b772185f62b917fce7b74fbb3fa7e87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689328"
---
# <a name="cameventoperator-handle-method"></a>CAMEvent 運算子控制碼方法

捕獲事件控制碼。 這個運算子不支援做為左值。

## <a name="syntax"></a>語法


```C++
 operator HANDLE() const;
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 [**CAMEvent：： m \_ hEvent**](camevent-m-hevent.md) 成員變數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CAMEvent 類別**](camevent.md)
</dt> </dl>

 

 




