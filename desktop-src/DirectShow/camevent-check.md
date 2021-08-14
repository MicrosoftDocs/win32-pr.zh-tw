---
description: 檢查方法會檢查是否已設定事件，而不會封鎖。
ms.assetid: b8e55798-fd8e-4442-bc35-08887d8a3129
title: 'CAMEvent： Check 方法 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Check
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a961d7df45ddac7ade5e39f91c1aed56609ce2d2eeb8e7423799c9a4903884e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955537"
---
# <a name="cameventcheck-method"></a>CAMEvent 檢查方法

`Check`方法會檢查是否已設定事件，而不會封鎖。

## <a name="syntax"></a>語法


```C++
BOOL Check();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="remarks"></a>備註

如果已設定事件，則傳回 **TRUE** ，否則傳回 **FALSE** 。 這個方法會呼叫 [**CAMEvent：： Wait**](camevent-wait.md) 方法，其時間為零。 如果物件是自動重設事件，這個方法會重設事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CAMEvent 類別**](camevent.md)
</dt> </dl>

 

 




