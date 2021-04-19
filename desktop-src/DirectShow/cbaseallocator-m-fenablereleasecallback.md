---
description: 指出是否已啟用發行回呼的旗標。 此旗標是在函式方法中設定。 如果值為 FALSE，則呼叫 CBaseAllocator：： SetNotify 方法會導致判斷提示 (在) 的 debug 組建中引發。
ms.assetid: cc9adc7c-ec44-41e7-875a-b3e553120804
title: 'CBaseAllocator：： m_fEnableReleaseCallback 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_fEnableReleaseCallback
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 626f1e8f4101eb48e79bc1cf679d1b91be9b2b31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995088"
---
# <a name="cbaseallocatorm_fenablereleasecallback-member"></a>CBaseAllocator：： m \_ fEnableReleaseCallback 成員

指出是否已啟用發行回呼的旗標。 此旗標是在函式方法中設定。 如果值為 FALSE，則呼叫 [**CBaseAllocator：： SetNotify**](cbaseallocator-setnotify.md)方法會導致 **判斷** 提示 (在) 的 debug 組建中引發。

## <a name="syntax"></a>Syntax


```C++
BOOL m_fEnableReleaseCallback;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseAllocator 類別**](cbaseallocator.md)
</dt> </dl>

 

 




