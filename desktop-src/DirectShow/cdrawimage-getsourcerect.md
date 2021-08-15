---
description: GetSourceRect 方法會抓取目前的來源矩形。
ms.assetid: e9ca091f-3fd7-4e42-90e9-b7831dd488a9
title: 'CDrawImage. GetSourceRect 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.GetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 81d7de629ec89fe31296a9efd10df3d4895f53a7dc67db58bfde77be8a75a82f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697882"
---
# <a name="cdrawimagegetsourcerect-method"></a>CDrawImage. GetSourceRect 方法

方法會抓取 `GetSourceRect` 目前的來源矩形。

## <a name="syntax"></a>語法


```C++
void GetSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSourceRect* 
</dt> <dd>

接收來源矩形的 **RECT** 結構指標。

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

 

 




