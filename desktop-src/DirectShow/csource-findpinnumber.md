---
description: FindPinNumber 方法會抓取篩選上指定的 pin 數目。
ms.assetid: c9366fcc-7b13-4e43-883e-6003c32fadec
title: 'CSource. FindPinNumber 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.FindPinNumber
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6a71c65efd97c48eed58fb7d0b5aa8fcc2f178e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982076"
---
# <a name="csourcefindpinnumber-method"></a>CSource. FindPinNumber 方法

方法會抓取 `FindPinNumber` 篩選上指定的 pin 數目。

## <a name="syntax"></a>語法


```C++
int FindPinNumber(
   IPin *iPin
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*iPin* 
</dt> <dd>

釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 pin 碼，如果在此篩選器上找不到 pin，則傳回1。 第一個 pin 的編號為零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>來源 .h (包含) 的資料流程 </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSource 類別**](csource.md)
</dt> </dl>

 

 




