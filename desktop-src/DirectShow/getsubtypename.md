---
description: GetSubtypeName 函式會取出影片子類型的人類可讀取名稱。
ms.assetid: 493b434e-2d36-4897-a5b2-7be0eb0a560f
title: 'GetSubtypeName 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSubtypeName
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f5cae835a3a7f1b5510d85ecf3f2ae9d15251a45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995016"
---
# <a name="getsubtypename-function"></a>GetSubtypeName 函式

函 `GetSubtypeName` 式會抓取影片子類型的人類可讀取名稱。

## <a name="syntax"></a>語法


```C++
TCHAR* GetSubtypeName(
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

傳回包含名稱的字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[影片和影像函式](video-and-image-functions.md)
</dt> </dl>

 

 




