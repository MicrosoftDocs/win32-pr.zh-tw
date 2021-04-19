---
description: GetCommandDueFor 方法會抓取在指定時間排程的延後命令。
ms.assetid: f8a2f9ae-f359-4429-aca5-021b6fe2aa93
title: 'CCmdQueue. GetCommandDueFor 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetCommandDueFor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 48a01436a68a5b98d08880c1516bbf4576d10be2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992385"
---
# <a name="ccmdqueuegetcommandduefor-method"></a>CCmdQueue. GetCommandDueFor 方法

`GetCommandDueFor`方法會抓取在指定時間排程的延後命令。

## <a name="syntax"></a>語法


```C++
virtual HRESULT GetCommandDueFor(
   REFERENCE_TIME   tStream,
   CDeferredCommand **ppCmd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*tStream* 
</dt> <dd>

排定命令的時間。

</dd> <dt>

*ppCmd* 
</dt> <dd>

要在 *tStream* 參數中指定的時間執行之延後命令指標的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_ \_ 如果沒有任何命令，則會傳回 VFW E \_ ; 否則會傳回 S \_ OK。

## <a name="remarks"></a>備註

此成員函式會接受資料流程時間，並傳回該時間排程的延遲命令。 執行命令佇列時，會計算實際的資料流程時間位移。 命令會保持佇列，直到執行或取消為止。 此成員函式不會封鎖。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CCmdQueue 類別**](ccmdqueue.md)
</dt> </dl>

 

 




