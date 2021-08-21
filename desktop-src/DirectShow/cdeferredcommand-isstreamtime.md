---
description: IsStreamTime 方法會指定是否要在資料流程時間或呈現時間執行命令。
ms.assetid: 4fb315a4-1bc6-49c8-a47f-0a8a46f3f790
title: 'CDeferredCommand. IsStreamTime 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.IsStreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 82c541220a2b89ecdd23e4676175f4c7b2aacd93aac008546349b38e7bc2455a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657201"
---
# <a name="cdeferredcommandisstreamtime-method"></a>CDeferredCommand. IsStreamTime 方法

`IsStreamTime`方法會指定是否要在資料流程時間或呈現時間執行命令。

## <a name="syntax"></a>語法


```C++
BOOL IsStreamTime();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果設定為數據流時間，則傳回 **TRUE** ;否則，會傳回 **FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDeferredCommand 類別**](cdeferredcommand.md)
</dt> </dl>

 

 




