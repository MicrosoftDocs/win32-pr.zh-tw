---
description: 變更目前資料流程的變更旗標。
ms.assetid: 65fa7fbe-4fa7-45a3-91a4-4a3547b035b9
title: 'CPersistStream. SetDirty 方法 (Pstream .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.SetDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31a00de873f33cedd1451ebebd0ec21f1dfaa83690923712d867ec4a8d34d502
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909298"
---
# <a name="cpersiststreamsetdirty-method"></a>CPersistStream. SetDirty 方法

變更目前資料流程的變更旗標。

## <a name="syntax"></a>語法


```C++
HRESULT SetDirty(
   BOOL fDirty
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*fDirty* 
</dt> <dd>

此資料流程的新中途旗標。 **TRUE** 表示資料尚未儲存。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Pstream (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPersistStream 類別**](cpersiststream.md)
</dt> </dl>

 

 




