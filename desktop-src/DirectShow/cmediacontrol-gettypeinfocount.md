---
description: 抓取物件所提供的類型資訊介面數目。
ms.assetid: 29575325-8f97-4f39-8272-86a917d9144f
title: 'CMediaControl. GetTypeInfoCount 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f2454e503a045a02db20c0dc457b6367f6d3b427
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000960"
---
# <a name="cmediacontrolgettypeinfocount-method"></a>CMediaControl. GetTypeInfoCount 方法

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

[**CMediaControl 類別**](cmediacontrol.md)
</dt> </dl>

 

 




