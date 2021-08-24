---
description: CoInitializeHelper 方法會線上程的開頭呼叫 CoInitializeEx 函數。
ms.assetid: 1a981e1e-c059-4e51-81d8-33bcb39ee580
title: 'CAMThread. CoInitializeHelper 方法 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CoInitializeHelper
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 41a763a4b9151f22615aa0af3dae57af8281751209a016dc3135f3572e9d8ef3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768288"
---
# <a name="camthreadcoinitializehelper-method"></a>CAMThread. CoInitializeHelper 方法

`CoInitializeHelper`方法會線上程的開頭呼叫 CoInitializeEx 函數。

## <a name="syntax"></a>語法


```C++
static HRESULT CoInitializeHelper();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 以下是可能的值。



| 傳回碼                                                                             | 描述                                              |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | 無法使用 CoInitializeEx 函數。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 成功。<br/>                                      |
| <dl> <dt>**E \_ 失敗**</dt> </dl>  | 失敗。<br/>                                      |



 

## <a name="remarks"></a>備註

[**CAMThread：： InitialThreadProc**](camthread-initialthreadproc.md)方法會呼叫此 helper 方法，此方法會呼叫 CoInitializeEx 函數。 它會使用 COINIT \_ disable \_ OLE1DDE 旗標來停用動態資料交換 (DDE) 。 如需詳細資訊，請參閱 Platform SDK。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CAMThread 類別**](camthread.md)
</dt> </dl>

 

 




