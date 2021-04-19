---
description: 等候方法會封鎖，直到事件收到信號為止，或直到發生超時為止。
ms.assetid: bcc13723-a59b-4e8a-bfc8-eadb6facf116
title: 'CAMEvent. Wait 方法 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Wait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ab5bc2aabf77fb73739528e99cda7961ae87e9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980159"
---
# <a name="cameventwait-method"></a>CAMEvent. Wait 方法

`Wait`方法會封鎖，直到事件收到信號為止，或直到發生超時為止。

## <a name="syntax"></a>語法


```C++
BOOL Wait(
   DWORD dwTimeout = INFINITE
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwTimeout* 
</dt> <dd>

選擇性的超時值（以毫碼錶示）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果事件已發出信號，則傳回 **TRUE** 。 否則，會傳回 **FALSE**。

## <a name="remarks"></a>備註

如果是自動重設事件，當此方法傳回時，事件會重設為未收到信號狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CAMEvent 類別**](camevent.md)
</dt> </dl>

 

 




