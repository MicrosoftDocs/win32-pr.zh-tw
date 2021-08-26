---
description: IncrementPaletteVersion 方法會遞增元件的版本。 如果媒體類型變更為新的調色盤格式，則呼叫這個方法。
ms.assetid: 1ce77f97-d225-45f5-a259-1dcca1272d15
title: 'CDrawImage. IncrementPaletteVersion 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.IncrementPaletteVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7884c4d552920a9e5650d2a092b7fffc43a1c67bf03916eab7bb72da3a87946a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076398"
---
# <a name="cdrawimageincrementpaletteversion-method"></a>CDrawImage. IncrementPaletteVersion 方法

`IncrementPaletteVersion`方法會遞增元件的版本。 如果媒體類型變更為新的調色盤格式，則呼叫這個方法。

## <a name="syntax"></a>語法


```C++
void IncrementPaletteVersion();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會遞增 **m \_ PaletteVersion** 成員變數的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDrawImage 類別**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::GetPaletteVersion**](cdrawimage-getpaletteversion.md)
</dt> <dt>

[**CDrawImage::ResetPaletteVersion**](cdrawimage-resetpaletteversion.md)
</dt> </dl>

 

 




