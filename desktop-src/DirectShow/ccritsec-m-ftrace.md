---
description: 指定是否要追蹤此鎖定的布林值。
ms.assetid: 23417410-cfdc-426e-a662-7d6580b43a28
title: 'CCritSec：： m_fTrace 成員 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_fTrace
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 691e078bb3b502704aed585ba020d49b2bd99af1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987949"
---
# <a name="ccritsecm_ftrace-member"></a>CCritSec：： m \_ fTrace 成員

指定是否要追蹤此鎖定的布林值。

## <a name="syntax"></a>語法


```C++
BOOL m_fTrace;
```



## <a name="remarks"></a>備註

這個成員變數只會在基類的 debug 版本中定義。 如果值為 **TRUE**，會將鎖定狀態的追蹤寫入至 debug 記錄檔。 重要區段的 (偵錯工具記錄必須為使用 ) 中。如需詳細資訊，請參閱 [**DbgLockTrace**](dbglocktrace.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CCritSec 類別**](ccritsec.md)
</dt> </dl>

 

 




