---
description: GetDueCommand 方法會抓取指向下一個已到期命令的指標。
ms.assetid: f23434a6-ad2c-4b64-90b1-2f486a16e7e6
title: 'CCmdQueue. GetDueCommand 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetDueCommand
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a1297a3f0d514215270acf7e73b18cba46fca1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999094"
---
# <a name="ccmdqueuegetduecommand-method"></a>CCmdQueue. GetDueCommand 方法

`GetDueCommand`方法會抓取指向下一個命令的指標。

## <a name="syntax"></a>語法


```C++
virtual HRESULT GetDueCommand(
   CDeferredCommand **ppCmd,
   long             msTimeout
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppCmd* 
</dt> <dd>

延後命令指標的位址。

</dd> <dt>

*msTimeout* 
</dt> <dd>

執行超時之前要等候的時間量。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果發生超時，則傳回 E ABORT。 \_如果成功，則傳回 [確定]，否則會傳回錯誤。 傳回已使用 **IUnknown：： AddRef** 遞增的物件。

## <a name="remarks"></a>備註

此成員函式會封鎖，直到暫止的命令到期為止。 成員函式會封鎖 *msTimeout* 參數中指定的時間量（以毫秒為單位）。 資料流程時間命令只會在 [**CCmdQueue：： Run**](ccmdqueue-run.md) 和 [**CCmdQueue：： EndRun**](ccmdqueue-endrun.md) 成員函式之間到期。 此命令會一直排入佇列，直到執行或取消為止。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CCmdQueue 類別**](ccmdqueue.md)
</dt> </dl>

 

 




