---
description: Run 方法會切換至執行模式，以便執行由資料流程時間延遲的命令。
ms.assetid: c529ae84-c9b7-46f1-a1e4-716fc9e9df13
title: 'CCmdQueue： Run 方法 (Winutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5da70c4ac0c5890e4483f7facdc4d1f5a3d5dd70906c53917bd83029dfaa6c6e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757138"
---
# <a name="ccmdqueuerun-method"></a>CCmdQueue 方法

`Run`方法會切換至執行模式，以便執行由資料流程時間延遲的命令。

## <a name="syntax"></a>語法


```C++
virtual HRESULT Run(
   REFERENCE_TIME tStreamTimeOffset
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*tStreamTimeOffset* 
</dt> <dd>

位移時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

在執行模式中，已知資料流程時間與呈現時間的對應。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CCmdQueue 類別**](ccmdqueue.md)
</dt> </dl>

 

 




