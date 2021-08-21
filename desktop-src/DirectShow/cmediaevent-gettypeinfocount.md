---
description: CMediaEvent. GetTypeInfoCount 方法-抓取物件所提供的類型資訊介面數目。
ms.assetid: e16bc324-bb49-4df2-afeb-2c2cd1620693
title: 'CMediaEvent. GetTypeInfoCount 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6476e7949c9cad8e9ba13a562bf93fe7e3ffff39fe34cbe1101193bf9bc18289
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156996"
---
# <a name="cmediaeventgettypeinfocount-method"></a>CMediaEvent. GetTypeInfoCount 方法

抓取物件所提供的類型資訊介面數目。

## <a name="syntax"></a>語法


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pctinfo* 
</dt> <dd>

物件提供的類型資訊介面數目的指標。 如果物件提供型別資訊，這個數位就是 1;否則，此數目為0。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果 *pctinfo* 無效，則傳回 E 指標，否則傳回 S \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaEvent 類別**](cmediaevent.md)
</dt> </dl>

 

 




