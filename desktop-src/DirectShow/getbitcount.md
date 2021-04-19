---
description: GetBitCount 函式會傳回指定的影片子類型所使用的每個圖元位數。 此函數僅適用于未壓縮的 RGB 子類型。
ms.assetid: 876b91c8-50ba-4217-b79c-7f7ec1c22b83
title: 'GetBitCount 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fed9b24ebf2e95b2408de30a407904e6bd3c1c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992174"
---
# <a name="getbitcount-function"></a>GetBitCount 函式

此函式會傳回 `GetBitCount` 指定的影片子類型所使用的每個圖元位數。 此函數僅適用于未壓縮的 RGB 子類型。

## <a name="syntax"></a>語法


```C++
WORD GetBitCount(
   const GUID *pSubtype
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSubtype* 
</dt> <dd>

影片子類型 **GUID** 的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回這個子類型的每個圖元位數，如果無法辨識子類型，則值 **USHRT \_ MAX** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[影片和影像函式](video-and-image-functions.md)
</dt> </dl>

 

 




