---
description: 使用此 pin 的串流執行緒數目。
ms.assetid: f8650a17-edab-4d69-91da-78107c3c60b9
title: 'CDynamicOutputPin：： m_dwNumOutstandingOutputPinUsers 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwNumOutstandingOutputPinUsers
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 29fc593065af4252f58ce4bb08dd41fac82926dc11490377f6a8af614794b22a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688708"
---
# <a name="cdynamicoutputpinm_dwnumoutstandingoutputpinusers-member"></a>CDynamicOutputPin：： m \_ dwNumOutstandingOutputPinUsers 成員

使用此 pin 的串流執行緒數目。

## <a name="syntax"></a>語法


```C++
DWORD m_dwNumOutstandingOutputPinUsers;
```



## <a name="remarks"></a>備註

[**CDynamicOutputPin：： StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md)方法會遞增此變數，而 [**CDynamicOutputPin：： StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md)方法會將它遞減。 當值大於零時，某些執行緒會使用此釘選來串流資料或變更連線類型。 在這種情況下，無法封鎖 pin。

存取此變數之前，請先保留 [**CDynamicOutputPin：： m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) 重要區段。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDynamicOutputPin 類別**](cdynamicoutputpin.md)
</dt> <dt>

[**CDynamicOutputPin::StreamingThreadUsingOutputPin**](cdynamicoutputpin-streamingthreadusingoutputpin.md)
</dt> </dl>

 

 




