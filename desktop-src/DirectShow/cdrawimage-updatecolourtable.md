---
description: UpdateColourTable 方法會以新的調色板更新色彩表。
ms.assetid: 61ad98c6-a526-4aac-ad68-d44fadc668de
title: 'CDrawImage. UpdateColourTable 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.UpdateColourTable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5a53413cd1aaf60c17031f126f0a158629f5c41f8ca94981d293f003afadda8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119384028"
---
# <a name="cdrawimageupdatecolourtable-method"></a>CDrawImage. UpdateColourTable 方法

`UpdateColourTable`方法會使用新的調色板來更新色彩表。

## <a name="syntax"></a>語法


```C++
void UpdateColourTable(
   HDC              hdc,
   BITMAPINFOHEADER *pbmi
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hdc* 
</dt> <dd>

包含映射的裝置內容。

</dd> <dt>

*pbmi* 
</dt> <dd>

[**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)結構的指標，其中包含新的調色板。

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

 

 




