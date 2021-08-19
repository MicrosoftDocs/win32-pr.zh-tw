---
description: 將背景工作執行緒執行的要求排在佇列中。
ms.assetid: a854f962-143d-4776-bf98-119d003867df
title: 'CMsgThread. PutThreadMsg 方法 (Msgthrd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.PutThreadMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7eefa95c4fd6ab19c895b4d1d47dba3a19302023985a4631708c3cf7ccc10d06
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585638"
---
# <a name="cmsgthreadputthreadmsg-method"></a>CMsgThread. PutThreadMsg 方法

將背景工作執行緒執行的要求排在佇列中。

## <a name="syntax"></a>語法


```C++
void PutThreadMsg(
   UINT     uMsg,
   DWORD    dwMsgFlags,
   LPVOID   lpMsgParam,
   CAMEvent *pEvent = NULL
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*uMsg* 
</dt> <dd>

要求代碼。

</dd> <dt>

*dwMsgFlags* 
</dt> <dd>

選擇性旗標參數。

</dd> <dt>

*lpMsgParam* 
</dt> <dd>

包含額外參數或傳回值之資料區塊的選擇性指標。 必須是靜態或堆積配置，而不是自動。

</dd> <dt>

*pEvent* 
</dt> <dd>

事件物件的選擇性指標，會在完成時收到信號。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

此成員函式會將背景工作執行緒執行的要求排到佇列。 此成員函式的參數將會在 [**CMsg**](cmsg.md) 物件中排入佇列 (，) 並傳遞給背景工作執行緒的 [**CMsgThread：： ThreadMessageProc**](cmsgthread-threadmessageproc.md) 成員函式。 此成員函式會在將要求排入佇列之後立即傳回，而且不會等候執行緒完成要求。 衍生類別的 **CMsgThread：： ThreadMessageProc** 成員函式會定義四個參數。

這個成員函式會使用多執行緒安全清單，因此可以安全地從不同的執行緒呼叫這個成員函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Msgthrd (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMsgThread 類別**](cmsgthread.md)
</dt> </dl>

 

 




