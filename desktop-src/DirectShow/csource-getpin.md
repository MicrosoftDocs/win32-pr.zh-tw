---
description: GetPin 方法會抓取 pin。 這個方法會實作為純虛擬 CBaseFilter：： GetPin 方法。
ms.assetid: 7f30a1ba-8e7b-4bde-9f4d-a85b3a2122e9
title: 'CSource. GetPin 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4c5b7548eca20f9ec6d9e03d0e708ead1b106f543ca8cac108700c64c9352ea3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087078"
---
# <a name="csourcegetpin-method"></a>CSource. GetPin 方法

方法會抓取 `GetPin` pin。 這個方法會實作為純虛擬 [**CBaseFilter：： GetPin**](cbasefilter-getpin.md) 方法。

## <a name="syntax"></a>語法


```C++
CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*n* 
</dt> <dd>

指定之 pin 的編號。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 [**CBasePin**](cbasepin.md) 物件的指標，該物件會執行釘選，如果索引超出範圍，則傳回 **Null** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>來源 .h (包含) 的資料流程 </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSource 類別**](csource.md)
</dt> </dl>

 

 




