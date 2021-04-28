---
description: CEnumPins。 CEnumPins 函式-函數方法。
ms.assetid: f696e433-b051-4de0-80e5-f9cd31fd0f23
title: 'CEnumPins. CEnumPins (Amfilter. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.CEnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: caa27dfe0190df15be1e41b7128c06249f1ae2b8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099226"
---
# <a name="cenumpinscenumpins-constructor"></a>CEnumPins. CEnumPins 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CEnumPins(
   CBaseFilter *pFilter,
   CEnumPins   *pEnumPins
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFilter* 
</dt> <dd>

要列舉釘選之篩選準則的指標。

</dd> <dt>

*pEnumPins* 
</dt> <dd>

要複製之列舉值的 [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) 介面指標，或 **Null**。

</dd> </dl>

## <a name="remarks"></a>備註

如果 *pEnumPins* 是 **Null**，這個方法會將列舉值初始化為列舉序列的開頭。 否則，它會複製 *pEnumPins* 所指定之列舉值的內部狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CEnumPins 類別**](cenumpins.md)
</dt> </dl>

 

 




