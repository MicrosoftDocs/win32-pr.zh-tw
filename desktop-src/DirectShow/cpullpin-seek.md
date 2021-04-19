---
description: Seek 方法會設定資料流程的開始和停止位置。
ms.assetid: d84476f5-688c-429d-a51b-7020a6316e35
title: 'CPullPin： Seek 方法 (Pullpin .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Seek
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6f1a82ec549b5ceb888acc194a7abc2cd3eace47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990748"
---
# <a name="cpullpinseek-method"></a>CPullPin. Seek 方法

`Seek`方法會設定資料流程的開始和停止位置。

## <a name="syntax"></a>語法


```C++
HRESULT Seek(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*tStart* 
</dt> <dd>

指定開始位置，以位元組乘以10000000。

</dd> <dt>

*tStop* 
</dt> <dd>

指定停止位置，以位元組乘以10000000。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果方法成功，則傳回 S OK，否則傳回錯誤碼。

## <a name="remarks"></a>備註

如果背景工作執行緒正在執行，方法會暫停執行緒、排清篩選圖形，然後繼續執行執行緒。 執行緒會從新的開始位置開始提取資料。 否則，每當啟動執行緒時，新的位置值就會生效。

位置是相對於原始來源的起點。 將所需的位元組位移乘以在基類庫中定義為10000000的常數單位。

當 pin 首次連接時，[停止] 和 [開始] 位置會預設為數據流的開頭和結尾。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Pullpin。h</dt> </dl>                                                                                                       |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPullPin 類別**](cpullpin.md)
</dt> </dl>

 

 




