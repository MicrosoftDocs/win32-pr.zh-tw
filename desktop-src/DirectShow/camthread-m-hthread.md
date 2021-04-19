---
description: 執行緒的控制碼。
ms.assetid: 93d1182a-58f0-4570-8568-fe0fded762cb
title: 'CAMThread：： m_hThread 成員 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hThread
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e83dd225da0c3673f9c7f423e0bf56da7431b097
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984462"
---
# <a name="camthreadm_hthread-member"></a>CAMThread：： m \_ hThread 成員

執行緒的控制碼。

## <a name="syntax"></a>語法


```C++
HANDLE m_hThread;
```



## <a name="remarks"></a>備註

這個變數會初始化為 **Null**。 [**CAMThread：： Create**](camthread-create.md)方法會將這個變數設定為執行緒控制碼。 若要判斷線程是否存在，請呼叫 [**CAMThread：： ThreadExists**](camthread-threadexists.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CAMThread 類別**](camthread.md)
</dt> </dl>

 

 




