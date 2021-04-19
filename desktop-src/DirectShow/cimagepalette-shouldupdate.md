---
description: ShouldUpdate 方法會判斷是否需要建立新的調色板。
ms.assetid: 50886277-189b-4102-ade9-0366f64fdbcb
title: 'CImagePalette. ShouldUpdate 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.ShouldUpdate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f8cf27548487ad0338f0c4773c66df8f7d03c2f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990098"
---
# <a name="cimagepaletteshouldupdate-method"></a>CImagePalette. ShouldUpdate 方法

`ShouldUpdate`方法會判斷是否需要建立新的調色板。

## <a name="syntax"></a>語法


```C++
BOOL ShouldUpdate(
   const VIDEOINFOHEADER *pNewInfo,
   const VIDEOINFOHEADER *pOldInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pNewInfo* 
</dt> <dd>

[**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)結構的指標，其中包含新的色彩表。

</dd> <dt>

*pOldInfo* 
</dt> <dd>

**VIDEOINFOHEADER** 結構的指標，其中包含舊的色彩表。 此參數可以是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果需要更新調色板，則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

-   如果兩個 **VIDEOINFOHEADER** 結構都沒有包含色彩表，則此方法會傳回 **FALSE**。
-   如果只有一個結構包含色彩表，或如果 *pOldInfo* 為 **Null**，則此方法會傳回 **TRUE**。
-   如果這兩個結構都包含色彩表，而且色彩專案相符，則此方法會傳回 **FALSE**。
-   如果這兩個結構都包含色彩表，但色彩專案不相符，則此方法會傳回 **TRUE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CImagePalette 類別**](cimagepalette.md)
</dt> </dl>

 

 




