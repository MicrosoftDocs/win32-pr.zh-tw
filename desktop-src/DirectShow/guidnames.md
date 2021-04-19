---
description: GuidNames 是 DirectShow 基類庫中的全域陣列，其中包含代表 Uuid 中定義之 Guid 的字串。 這個陣列適用于產生 debug 輸出。
ms.assetid: 6d72ad1e-588a-4a82-a1c1-e1e7b49df572
title: 'GuidNames (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GuidNames
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 359294d0cf3ab4e2074db5935cbbd604dcc1b250
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978713"
---
# <a name="guidnames"></a>GuidNames

`GuidNames` 是 DirectShow 基類庫中的全域陣列，其中包含代表 Uuid 中定義之 Guid 的字串。 這個陣列適用于產生 debug 輸出。

``` syntax
char* GuidNames[guid]
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="guid"></span><span id="GUID"></span>*Guid*
</dt> <dd>

指定標頭檔 Uuid 中定義的任何 GUID 值。

</dd> </dl>

## <a name="remarks"></a>備註

使用這個全域陣列，將 GUID 常數輸出為字串。 例如，下列程式碼會將「媒體型影片」字串列印 \_ 到主控台：


```C++
puts(GuidNames[MEDIATYPE_Video]);
```



如果 GUID 不相符，則會傳回「未知的 GUID 名稱」字串。 並非所有的 DirectShow Guid 都定義于 uuid. h 中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxdebug (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Debug Output 函數](debug-output-functions.md)
</dt> </dl>

 

 




