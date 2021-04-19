---
description: CheckTime 方法會判斷指定的時間是否為逾期。
ms.assetid: 522bc7ae-f998-4a7d-8bc3-caf09b4108a6
title: 'CCmdQueue. CheckTime 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.CheckTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 17fd67973e122830e53d93d1d8db17046f716507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983236"
---
# <a name="ccmdqueuechecktime-method"></a>CCmdQueue. CheckTime 方法

`CheckTime`方法會判斷指定的時間是否為逾期。

## <a name="syntax"></a>語法


```C++
BOOL CheckTime(
   CRefTime time,
   BOOL     bStream
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*time* 
</dt> <dd>

檢查的時間。

</dd> <dt>

*bStream* 
</dt> <dd>

如果 *time* 參數是資料流程時間值，則 **為 TRUE** ;如果 *時間* 是展示時間值，則 **為 FALSE** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果尚未通過指定的時間，則傳回 **TRUE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CCmdQueue 類別**](ccmdqueue.md)
</dt> </dl>

 

 




