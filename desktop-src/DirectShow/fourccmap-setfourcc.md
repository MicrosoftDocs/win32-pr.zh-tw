---
description: 設定 FOURCCMap 物件的 FOURCC 部分。
ms.assetid: cc821e39-e565-4255-a289-2c9507d43433
title: 'FOURCCMap：： SetFOURCC 方法 (Fourcc .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.SetFOURCC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 435eb209e39ffad29f041e2e117a45d735abffed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976144"
---
# <a name="fourccmapsetfourcc-method"></a>FOURCCMap：： SetFOURCC 方法

設定 [**FOURCCMap**](fourccmap.md)物件的 **FOURCC** 部分。

## <a name="syntax"></a>語法


```C++
void SetFOURCC(
   const GUID *pguid
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pguid* 
</dt> <dd>

傳回的全域唯一識別碼的指標， (**GUID**) **FOURCCMap** 物件的一部分。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Fourcc (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**FOURCCMap 類別**](fourccmap.md)
</dt> </dl>

 

 




