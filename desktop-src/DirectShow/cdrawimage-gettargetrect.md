---
description: GetTargetRect 方法會抓取目前的目的地矩形。
ms.assetid: b6542b06-af36-4666-b6fa-d9fa3c6c7044
title: 'CDrawImage. GetTargetRect 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.GetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 547dd12117cec95ad1cb0159667a8dd72a95a6e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977682"
---
# <a name="cdrawimagegettargetrect-method"></a>CDrawImage. GetTargetRect 方法

方法會抓取 `GetTargetRect` 目前的目的地矩形。

## <a name="syntax"></a>語法


```C++
void GetTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pTargetRect* 
</dt> <dd>

接收目標矩形的 **RECT** 結構指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDrawImage 類別**](cdrawimage.md)
</dt> </dl>

 

 




