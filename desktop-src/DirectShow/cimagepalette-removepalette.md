---
description: RemovePalette 方法會刪除現有的邏輯元件，並在 CBaseWindow 物件上呼叫 CBaseWindow：： UnsetPalette。
ms.assetid: fab531b8-8630-43f8-bf08-cd8f24659bef
title: 'CImagePalette. RemovePalette 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.RemovePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c0410772203a22655968fba393c707bda790a5a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999114"
---
# <a name="cimagepaletteremovepalette-method"></a>CImagePalette. RemovePalette 方法

`RemovePalette`方法會刪除現有的邏輯元件，並在 **CBaseWindow** 物件上呼叫 [**CBaseWindow：： UnsetPalette**](cbasewindow-unsetpalette.md) 。

## <a name="syntax"></a>語法


```C++
HRESULT RemovePalette();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CImagePalette 類別**](cimagepalette.md)
</dt> </dl>

 

 




