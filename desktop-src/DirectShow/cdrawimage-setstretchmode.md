---
description: SetStretchMode 方法會計算影片影像是否必須伸展。
ms.assetid: ffdcaf9c-e157-4557-9193-8430c1c451bf
title: 'CDrawImage. SetStretchMode 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetStretchMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b3886910bce57aca728f64ffbe9d660c1073d1281864a7721faa7e757c7c7d81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526488"
---
# <a name="cdrawimagesetstretchmode-method"></a>CDrawImage. SetStretchMode 方法

`SetStretchMode`方法會計算影片影像是否必須伸展。

## <a name="syntax"></a>語法


```C++
void SetStretchMode();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

每當來源或目標矩形變更時， **CDrawImage** 類別就會自動呼叫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDrawImage 類別**](cdrawimage.md)
</dt> </dl>

 

 




