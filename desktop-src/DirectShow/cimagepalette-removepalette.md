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
ms.openlocfilehash: 0b87c8f028da17e6af305900f203c5cf1143132806ca1b2ce9b0edaddebd0eac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916007"
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

 

 




