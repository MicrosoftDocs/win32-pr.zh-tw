---
description: CompleteStateChange 方法會判斷轉換為暫停狀態是否已完成。
ms.assetid: 505a0b31-deaa-46be-91e6-f9bc8e47dd3a
title: 'CBaseRenderer. CompleteStateChange 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CompleteStateChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2465aeed3347f6ebc592dbe01bc3580a30983e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977771"
---
# <a name="cbaserenderercompletestatechange-method"></a>CBaseRenderer. CompleteStateChange 方法

`CompleteStateChange`方法會判斷轉換為暫停狀態是否已完成。

## <a name="syntax"></a>語法


```C++
virtual HRESULT CompleteStateChange(
   FILTER_STATE OldState
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*OldState* 
</dt> <dd>

轉換之前的狀態。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果轉換完成，則傳回 S OK。 否則，會傳回 \_ FALSE。

## <a name="remarks"></a>備註

[**CBaseRenderer：:P ause**](cbaserenderer-pause.md)方法會呼叫這個方法來更新狀態轉換狀態。 一般而言，在篩選器收到範例之前，將不會完成轉換至暫停的作業。 不過，在某些情況下，轉換會立即完成：例如，如果篩選器未連接，或已到達資料流程的結尾。 這個方法會檢查各種準則，然後呼叫 [**CBaseRenderer：： Ready**](cbaserenderer-ready.md) 方法或 [**CBaseRenderer：： NotReady**](cbaserenderer-notready.md) 方法來更新轉換狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




