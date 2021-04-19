---
description: Set 方法會為事件發出信號。
ms.assetid: dfcb1601-aa65-47f5-ae3c-f13fcd7b1398
title: 'CAMEvent： Set 方法 (Wxutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9caeed17d42d121ae9263bf6c1fcd011ed573c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978452"
---
# <a name="cameventset-method"></a>CAMEvent 方法

方法會為 `Set` 事件發出信號。

## <a name="syntax"></a>語法


```C++
void Set();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

此行為取決於物件是否為自動重設事件或手動重設事件：

-   **自動重設**：如果有任何執行緒正在等候此事件，則會釋放一個執行緒，並重設該事件。 如果沒有任何執行緒正在等候此事件，事件會維持為信號。
-   **手動重設**：會釋放所有等候此事件的執行緒。 事件仍會收到信號。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CAMEvent 類別**](camevent.md)
</dt> </dl>

 

 




